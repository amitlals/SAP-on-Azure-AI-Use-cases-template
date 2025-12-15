# Repository Structure

This document provides an overview of the SAP on Azure AI Use Cases Template repository structure.

## 📁 Root Level Files

### Core Documentation
- **README.md** - Main repository overview with use case showcases
- **GETTING_STARTED.md** - Comprehensive setup guide and prerequisites
- **CONTRIBUTING.md** - Guidelines for contributing to the repository
- **CODE_OF_CONDUCT.md** - Community guidelines and standards
- **SECURITY.md** - Security policies and vulnerability reporting
- **LICENSE** - MIT License terms
- **.gitignore** - Git ignore patterns for common artifacts

### This Document
- **REPOSITORY_STRUCTURE.md** - You are here! Navigation guide

## 📂 Directory Structure

```
SAP-on-Azure-AI-Use-cases-template/
├── .github/                          # GitHub-specific files
│   ├── ISSUE_TEMPLATE/              # Issue templates
│   │   ├── bug_report.md           # Bug report template
│   │   ├── feature_request.md      # Feature request template
│   │   └── use_case_submission.md  # New use case submission
│   └── PULL_REQUEST_TEMPLATE/       # PR templates
│       └── pull_request_template.md
│
├── docs/                             # Documentation hub
│   └── README.md                    # Documentation overview and navigation
│
├── templates/                        # Code templates and snippets
│   └── README.md                    # Template catalog and usage
│
└── use-cases/                        # Use case implementations
    ├── README.md                    # Use cases overview
    ├── 01-screenshot-to-fiori/      # Use Case 1
    │   └── README.md
    ├── 02-dual-copilot/             # Use Case 2
    │   └── README.md
    ├── 03-fiori-with-joule/         # Use Case 3
    │   └── README.md
    ├── 04-sap-build-lowcode/        # Use Case 4
    │   └── README.md
    ├── 05-azure-sre-agent/          # Use Case 5
    │   └── README.md
    ├── 06-joule-ama/                # Use Case 6
    │   └── README.md
    ├── 07-sap-rpt-oss/              # Use Case 7
    │   └── README.md
    └── 08-foundry-local/            # Use Case 8
        └── README.md
```

## 🎯 Quick Navigation

### For New Users
1. Start with [README.md](README.md) for an overview
2. Read [GETTING_STARTED.md](GETTING_STARTED.md) for setup
3. Browse [use-cases/](use-cases/) to find your scenario
4. Follow the detailed README in your chosen use case folder

### For Contributors
1. Review [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines
2. Check [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md) for standards
3. Read [SECURITY.md](SECURITY.md) for security practices
4. Use [.github/ISSUE_TEMPLATE/](.github/ISSUE_TEMPLATE/) for reporting

### For Developers
1. Explore [use-cases/](use-cases/) for implementations
2. Check [templates/](templates/) for reusable code
3. Review [docs/](docs/) for technical documentation
4. Reference individual use case READMEs for details

## 📚 Documentation Files Explained

### Root Level Documentation

#### README.md
- **Purpose**: Main entry point and repository overview
- **Contains**: 
  - Project description
  - 8 featured use cases with videos/screenshots
  - Quick navigation links
  - Resource links
  - Getting started information

#### GETTING_STARTED.md
- **Purpose**: Comprehensive onboarding guide
- **Contains**:
  - Prerequisites for SAP, Azure, and development tools
  - Quick start instructions
  - Environment setup guides
  - Use case setup overviews
  - Configuration examples
  - Troubleshooting tips

#### CONTRIBUTING.md
- **Purpose**: Guide for contributors
- **Contains**:
  - How to contribute
  - Code quality guidelines
  - Commit message conventions
  - Pull request process
  - Community standards

#### CODE_OF_CONDUCT.md
- **Purpose**: Community guidelines
- **Contains**:
  - Behavioral standards
  - Expected conduct
  - Reporting procedures
  - Enforcement policies

#### SECURITY.md
- **Purpose**: Security policies
- **Contains**:
  - Security guidelines
  - Vulnerability reporting
  - Best practices
  - Disclaimer and warnings

### Use Cases Documentation

Each use case folder (`use-cases/01-*/` through `use-cases/08-*/`) contains:

- **README.md** with:
  - Objective and overview
  - Prerequisites
  - Setup instructions
  - Example workflows
  - Best practices
  - Troubleshooting
  - Resource links

#### Use Case 1: Screenshot to Fiori App
- Transform screenshots to Fiori apps in under 5 minutes
- Technologies: SAP Fiori, GitHub Copilot, UI5
- Difficulty: Intermediate

#### Use Case 2: Power of Two Copilots
- Combine J4D and GitHub Copilot
- Technologies: J4D, GitHub Copilot, SAP BAS
- Difficulty: Beginner-Intermediate

#### Use Case 3: Fiori with Joule
- Build Fiori apps with Joule assistance
- Technologies: SAP Fiori, Joule, SAPUI5
- Difficulty: Intermediate

#### Use Case 4: SAP Build Low-Code
- Create low-code solutions with Joule Copilot
- Technologies: SAP Build, Low-Code
- Difficulty: Beginner

#### Use Case 5: Azure SRE Agent
- Agentic DevOps for SAP on Azure
- Technologies: Azure SRE Agent, DevOps
- Difficulty: Advanced

#### Use Case 6: Joule AMA
- Ask Me Anything with SAP Joule
- Technologies: SAP Joule, NLP
- Difficulty: Beginner

#### Use Case 7: SAP-RPT-OSS
- Tabular LLM for data analysis
- Technologies: ML, Python, Tabular LLM
- Difficulty: Advanced

#### Use Case 8: Foundry Local
- On-device AI with complete privacy
- Technologies: On-Device AI, Privacy-First
- Difficulty: Intermediate

### GitHub Templates

#### Issue Templates (.github/ISSUE_TEMPLATE/)
- **bug_report.md**: Report bugs and issues
- **feature_request.md**: Suggest new features
- **use_case_submission.md**: Submit new use cases

#### Pull Request Template
- **pull_request_template.md**: Standard PR format with checklists

## 🔍 Finding What You Need

### By Experience Level
- **Beginners**: Start with Use Cases 4, 6
- **Intermediate**: Try Use Cases 1, 2, 3, 8
- **Advanced**: Challenge yourself with Use Cases 5, 7

### By Technology Focus
- **SAP Fiori/UI5**: Use Cases 1, 2, 3
- **Low-Code**: Use Case 4
- **DevOps**: Use Case 5
- **AI/ML**: Use Cases 6, 7, 8

### By Time Available
- **Quick (< 15 min)**: Use Cases 1, 6
- **Medium (15-30 min)**: Use Cases 2, 3, 4, 8
- **Extended (> 30 min)**: Use Cases 5, 7

## 🎨 Documentation Conventions

### Markdown Structure
- Headers use `#` for hierarchy
- Code blocks use triple backticks with language
- Links are relative within repository
- Emojis used for visual navigation

### File Naming
- UPPERCASE.md for root-level docs
- lowercase-with-hyphens for folders
- README.md in each directory

### Link Structure
- Root files: `[Text](FILE.md)`
- Use cases: `[Text](use-cases/##-name/)`
- External: Full URLs with descriptive text

## 🤝 Contributing to Documentation

When adding or updating documentation:
1. Follow existing structure and conventions
2. Update this file if adding new directories
3. Ensure all links work correctly
4. Use clear, concise language
5. Include code examples where helpful
6. Test all instructions before committing

## 📝 Maintenance Notes

### Regular Updates Needed
- Keep resource links current
- Update version numbers
- Refresh screenshots/videos
- Validate external links
- Review prerequisites

### Quarterly Review Items
- Check for outdated information
- Update technology versions
- Refresh best practices
- Verify all use cases work
- Update success metrics

## 📞 Questions?

If you have questions about the repository structure:
- Open an issue using the appropriate template
- Check the [docs/README.md](docs/README.md)
- Contact repository maintainers

---

**Last Updated**: December 2025
**Maintained By**: Repository Contributors
