<!-- Updated by mariuszo for COE demo -->

# 🏗️ Fabrikam Modular Homes - Business AI Demonstration Platform

> **🤖 GITHUB COPILOT: CRITICAL SERVER RULES** ⚠️  
> **ALWAYS use VS Code tasks for servers**: `run_task(id: "🌐 Start Both Servers")`  
> **NEVER use run_in_terminal for servers**: `dotnet run` commands break server management  
> **Use separate terminals for commands**: `run_in_terminal(command: "curl...", isBackground: false)`  
> **📖 Full Rules**: `COPILOT-SERVER-RULES.md` and `.copilot/instructions.md`

> **🚨 MONOREPO STRUCTURE**: This is a multi-project .NET solution. See `.github/MONOREPO-GUIDE.md` for complete development guidance.

> **🤖 GitHub Copilot Notice**: This project uses **automated CI/CD** with GitHub Actions. Every code change triggers testing and deployment. See `.github/copilot-cicd-context.md` for full pipeline details.

A comprehensive .NET-based business simulation platform designed for **Microsoft Copilot demonstrations**, **partner training**, and **AI business value showcases**. This project simulates Fabrikam, a fictional modular home builder, with realistic business operations and AI-powered tools.

## 🎯 Purpose

- **Accelerate Copilot adoption** with realistic SME&C business scenarios
- **Enable hands-on AI labs** demonstrating tangible business value
- **Support partner training** with ready-to-deploy environments
- **Showcase Model Context Protocol (MCP)** integration patterns

## 🚀 **Status: Production Ready!**

**✅ Live Deployment**: https://fabrikam-api-dev-y32g.azurewebsites.net  
**✅ Authentication Complete**: 100% success rate with Azure Key Vault RBAC  
**✅ Demo Ready**: 7 working demo users across all roles  
**✅ Fully Tested**: Automated testing with CI/CD integration

## 📚 **Quick Navigation**

| Resource | Purpose | Status |
|----------|---------|--------|
| **[🚀 Deploy to Azure](docs/deployment/DEPLOY-TO-AZURE.md)** | One-click Azure deployment | ✅ Production Ready |
| **[📚 Documentation Index](docs/DOCUMENTATION-INDEX.md)** | Complete documentation guide | ✅ Organized |
| **[🎉 Authentication Complete](docs/development/AUTHENTICATION-IMPLEMENTATION-COMPLETE.md)** | Implementation results | ✅ 100% Success |
| **[🧪 Testing Guide](test.ps1)** | Automated testing | ✅ Local + Production |

## 🎬 Demo Video

Watch the complete Fabrikam Project demonstration showcasing:

- Customer management and business analytics
- Product catalog and inventory tracking
- Order processing and timeline management
- MCP tool integration with AI assistants
- Real-time business dashboard functionality

**📹 [View Demo Video](docs/assets/fabrikamprojectdemo1.mp4)** _(11 minutes - comprehensive walkthrough)_

## ⚡ Quick Start

### **Local Development** (Monorepo Structure)

```powershell
# 🚀 Start both servers from workspace root
.\test.ps1 start

# 🧪 Test everything (convenient shortcuts available!)
.\test.ps1 -Quick               # Root shortcut

# 📊 Check status
.\test.ps1 status
```

**Testing Shortcuts**: For convenience, you can use the root-level shortcuts:
- `.\test.ps1` - PowerShell wrapper for the main testing script (**Recommended**)
- `.\test.bat` - Batch file wrapper for command prompt users

### **Option 1: Use Deployed Services** (Recommended)

- **API**: https://fabrikam-api-dev-y32g.azurewebsites.net
- **MCP**: wss://fabrikam-mcp-dev-y32g.azurewebsites.net  
- **Copilot Studio**: See [Setup Guide](docs/demos/Copilot-Studio-Agent-Setup-Guide.md)

### **Option 2: Local Development**

```powershell
# Run API locally
cd FabrikamApi/src
dotnet run

# Run MCP server locally
cd FabrikamMcp/src
dotnet run
```

## 🏗️ Architecture

![Fabrikam Architecture](docs/assets/FabrikamArchitecture.png)

Two integrated services providing complete business functionality:

### **FabrikamApi** - Business Operations API

- **Sales Analytics**: Order management and revenue tracking ($829K+ in sample data)
- **Product Catalog**: Modular homes with specifications and inventory tracking
- **Customer Management**: CRM with order history and support integration
- **Asset Management**: Images, blueprints, and marketing materials

### **FabrikamMcp** - AI Integration Server

- **Natural Language Interface**: Query business data conversationally
- **10 Consolidated Tools**: Optimized for Copilot Studio's 15-tool limit
- **Intelligent Defaults**: Works without parameters for robust AI interactions
- **Real-time Data**: Connects to live API for current business information

## � Authentication System

**Complete ASP.NET Core Identity implementation with Azure integration:**

- **JWT Token Management**: Secure authentication with access/refresh token lifecycle
- **Role-Based Access Control**: Admin, Sales, Customer service roles with appropriate permissions  
- **Azure Key Vault Integration**: RBAC-based secrets management with managed identity
- **Demo User System**: 7 pre-configured users for immediate testing and demonstrations
- **Production Deployment**: Fully tested in Azure App Service with 100% authentication success rate

**🔗 [View Authentication Details](AUTHENTICATION-IMPLEMENTATION-COMPLETE.md)**

## �📊 Business Data

Comprehensive sample data for realistic demonstrations:

- **8 Customers**: Business and individual buyers across regions
- **45 Products**: Modular homes, ADUs, materials with specifications
- **15 Orders**: $829,482.50 in sample revenue with regional breakdowns
- **20 Support Tickets**: Customer service cases with realistic workflows
- **Asset Library**: House images, blueprints, and marketing materials

## 🧪 Testing Your Setup

### **API Endpoints**

```powershell
# Health check
curl https://fabrikam-api-dev-y32g.azurewebsites.net/health

# Sales analytics
curl https://fabrikam-api-dev-y32g.azurewebsites.net/api/orders/analytics

# Product inventory
curl https://fabrikam-api-dev-y32g.azurewebsites.net/api/products/inventory
```

### **MCP Integration**

```powershell
# Server status
curl https://fabrikam-mcp-dev-y32g.azurewebsites.net/status

# List available tools
curl https://fabrikam-mcp-dev-y32g.azurewebsites.net/mcp
```

## 📖 Documentation

### **Essential Guides**

- [**Copilot Studio Setup**](docs/demos/Copilot-Studio-Agent-Setup-Guide.md) - Create your business AI assistant
- [**Asset Management**](docs/development/ASSET-MANAGEMENT-GUIDE.md) - Add images, blueprints, and files
- [**Authentication Implementation**](docs/development/AUTHENTICATION-IMPLEMENTATION-GUIDE.md) - Development workflow and methodology
- [**Deployment Guide**](docs/deployment/DEPLOYMENT-GUIDE.md) - Azure deployment instructions

## 📚 Documentation

Comprehensive documentation is organized in the [`docs/`](docs/) directory:

### 🎬 **Demos & Showcases**

- [**Demo Ready Summary**](docs/demos/DEMO-READY-SUMMARY.md) - Complete 3-minute demo guide
- [**Copilot Demo Prompts**](docs/demos/COPILOT-DEMO-PROMPTS.md) - Business intelligence scenarios
- [**Quick Demo Prompts**](docs/demos/QUICK-DEMO-PROMPTS.md) - Copy-paste ready prompts

### 🚀 **Deployment & Production**

- [**Deployment Guide**](docs/deployment/DEPLOYMENT-GUIDE.md) - Azure deployment instructions
- [**Release Guide**](docs/deployment/RELEASE-GUIDE.md) - Release process and versioning
- [**Production Testing**](docs/deployment/PRODUCTION-TESTING-GUIDE.md) - Production validation

### 🛠️ **Development**

- [**Development Workflow**](docs/development/DEVELOPMENT-WORKFLOW.md) - Daily development process
- [**Testing Strategy**](docs/development/TESTING-STRATEGY.md) - Comprehensive testing approach
- [**Commit Checklist**](docs/development/COMMIT-CHECKLIST.md) - Pre-commit validation
- [**Utility Scripts**](scripts/README.md) - Development and testing utilities

### 🏗️ **Architecture & Planning**

- [**Future Enhancements**](docs/architecture/TODO-FUTURE-ENHANCEMENTS.md) - Planned features and roadmap
- [**Visual Assets**](docs/assets/README.md) - Branding and Copilot Studio assets

> **📖 Full Navigation**: See [`docs/README.md`](docs/README.md) for complete documentation index

### **Implementation Status**

- ✅ **API Controllers**: All business endpoints implemented and tested
- ✅ **MCP Tools**: 10 consolidated tools optimized for Copilot Studio
- ✅ **Azure Deployment**: Both services deployed and accessible
- ✅ **Asset Structure**: Directory structure ready for house designs and blueprints
- 🔄 **Content Expansion**: Adding product images and architectural drawings

## 🎯 Business Scenarios

Perfect for demonstrating AI value in:

- **Sales Analytics**: "What are our sales numbers?" → Real revenue data with breakdowns
- **Inventory Management**: "What products need restocking?" → Live stock levels and alerts
- **Customer Service**: "Any urgent support tickets?" → Priority ticket management
- **Product Information**: "Show me our ADU options" → Complete product specifications

## 🤝 Contributing

This project is designed for demonstrations and training. To extend functionality:

1. **Fork the repository** for your own customizations
2. **Follow our [Development Workflow](docs/development/DEVELOPMENT-WORKFLOW.md)** for daily development
3. **Add your business scenarios** by extending the sample data
4. **Test with our comprehensive tools** - see [Testing Strategy](docs/development/TESTING-STRATEGY.md)
5. **Follow deployment best practices** - see [Deployment Guide](docs/deployment/DEPLOYMENT-GUIDE.md)

For detailed contributing guidelines, see [CONTRIBUTING.md](CONTRIBUTING.md).

---

_Fabrikam Modular Homes - Showcasing AI-powered business operations_
