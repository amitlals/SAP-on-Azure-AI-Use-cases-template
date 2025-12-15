# Getting Started Guide

Welcome to the SAP on Azure AI Use Cases Template! This guide will help you get started with the templates and examples in this repository.

## 📋 Prerequisites

Before you begin, ensure you have:

### SAP Requirements
- Access to SAP BTP (Business Technology Platform) account
- SAP Build subscription (for low-code scenarios)
- SAP Joule for Developers (J4D) access - [Sign up here](https://developers.sap.com/joule)
- SAP Business Application Studio or ADT (ABAP Development Tools)

### Azure Requirements
- Active Azure subscription
- Azure AI Services access (Azure OpenAI, Cognitive Services)
- Azure Portal access
- Azure CLI installed (optional but recommended)

### Development Tools
- GitHub account with Copilot access
- Git installed locally
- Code editor (VS Code recommended with SAP extensions)
- Node.js (for Fiori development)
- Python 3.8+ (for AI/ML scenarios)

## 🚀 Quick Start

### 1. Clone or Use This Template

#### Option A: Use as Template
```bash
# Click "Use this template" button on GitHub
# Then clone your new repository
git clone https://github.com/YOUR-USERNAME/YOUR-REPO-NAME.git
cd YOUR-REPO-NAME
```

#### Option B: Clone Directly
```bash
git clone https://github.com/amitlals/SAP-on-Azure-AI-Use-cases-template.git
cd SAP-on-Azure-AI-Use-cases-template
```

### 2. Choose Your Use Case

Browse the available use cases in the [README](README.md):
1. Screenshot to Fiori App (UI Generation)
2. Dual Copilot Integration (J4D + GitHub Copilot)
3. Fiori App Development with Joule
4. SAP Build Low-Code Solutions
5. Azure SRE Agent Integration
6. SAP Joule AMA (Ask Me Anything)
7. SAP-RPT-1-OSS (Tabular LLM)
8. Foundry Local (On-device AI)

### 3. Set Up Your Environment

#### For SAP Development
```bash
# Install SAP Fiori tools
npm install -g @sap/generator-fiori

# Install SAP Cloud SDK
npm install @sap-cloud-sdk/core
```

#### For Azure AI Integration
```bash
# Install Azure CLI
# See: https://learn.microsoft.com/en-us/cli/azure/install-azure-cli

# Login to Azure
az login

# Set up Python environment (for AI scenarios)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install azure-ai-openai azure-cognitiveservices
```

## 🎯 Use Case Setup Guides

### Use Case 1: Screenshot to Fiori App
**Goal**: Transform UI screenshots into functional Fiori applications in under 5 minutes

**Setup Steps**:
1. Enable GitHub Copilot in your IDE
2. Access SAP Business Application Studio
3. Create new Fiori project
4. Use Copilot to generate components from screenshots
5. Deploy to SAP BTP

**Learn More**: Contact for detailed setup instructions

### Use Case 2: Power of Two Copilots (J4D + GHCP)
**Goal**: Combine SAP Joule for Developers and GitHub Copilot

**Setup Steps**:
1. Sign up for Joule for Developers
2. Enable GitHub Copilot
3. Configure both tools in your IDE
4. Use J4D for SAP-specific code generation
5. Use GHCP for general development tasks

**Learn More**: Contact for detailed setup instructions

### Use Case 3: SAP Build with Joule Copilot
**Goal**: Create low-code solutions using SAP Build and Joule

**Setup Steps**:
1. Access SAP Build via SAP BTP
2. Enable Joule Copilot
3. Create new low-code application
4. Use Joule for natural language app building
5. Deploy and test

**Learn More**: Contact for demo access

### Use Case 4: Azure SRE Agent Integration
**Goal**: Implement agentic DevOps for SAP workloads on Azure

**Setup Steps**:
1. Enable Azure SRE Agent (public preview)
2. Configure for SAP workload monitoring
3. Set up automated incident response
4. Integrate with SAP systems

**Learn More**: Contact for integration guide

## 🔧 Configuration

### Environment Variables
Create a `.env` file in your project root (never commit this file):

```bash
# Azure Configuration
AZURE_SUBSCRIPTION_ID=your-subscription-id
AZURE_OPENAI_ENDPOINT=your-endpoint
AZURE_OPENAI_API_KEY=your-api-key

# SAP Configuration
SAP_BTP_URL=your-btp-url
SAP_CLIENT_ID=your-client-id
SAP_CLIENT_SECRET=your-secret
```

### Best Practices
- Use Azure Key Vault for secrets in production
- Never commit credentials to version control
- Use managed identities where possible
- Follow the principle of least privilege

## 📚 Additional Resources

### SAP Resources
- [SAP Business Application Studio](https://help.sap.com/docs/SAP%20Business%20Application%20Studio)
- [SAP Joule Documentation](https://help.sap.com/docs/joule)
- [SAP Build](https://help.sap.com/docs/build)

### Azure Resources
- [Azure AI Services](https://learn.microsoft.com/en-us/azure/ai-services/)
- [Azure OpenAI](https://learn.microsoft.com/en-us/azure/ai-services/openai/)
- [SAP on Azure](https://learn.microsoft.com/en-us/azure/sap)

### GitHub Resources
- [GitHub Copilot Documentation](https://docs.github.com/en/copilot)
- [GitHub Actions for SAP](https://github.com/features/actions)

## 🆘 Need Help?

- **Issues**: [Open an issue](https://github.com/amitlals/SAP-on-Azure-AI-Use-cases-template/issues)
- **Discussions**: Start a discussion for questions
- **Contact**: Ask the repository owner for setup assistance

## 📖 Next Steps

1. Review the [README](README.md) for use case overviews
2. Check [CONTRIBUTING](CONTRIBUTING.md) to contribute
3. Read [SECURITY](SECURITY.md) for security guidelines
4. Explore the use case folders (coming soon)

---

**Ready to innovate with SAP + Azure AI?** Pick a use case and start building! 🚀
