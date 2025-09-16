# GitHub Runner Build Information 🏗️

[![Build Status](https://github.com/framinosona/GitHub_Runner_Information/actions/workflows/build-info.yml/badge.svg)](https://github.com/framinosona/GitHub_Runner_Information/actions/workflows/build-info.yml)
[![GitHub Pages](https://img.shields.io/badge/docs-GitHub%20Pages-blue)](https://framinosona.github.io/GitHub_Runner_Information)

> Comprehensive build information collection from GitHub-hosted runners across multiple platforms

## 🌐 Live Documentation

**[View the interactive documentation site →](https://framinosona.github.io/GitHub_Runner_Information)**

The site provides detailed build information for all GitHub-hosted runners with:

- 🖥️ **Collapsible OS sections** for easy navigation
- 📋 **Interactive JSON viewers** with syntax highlighting
- 🔍 **Searchable content** powered by DocFX
- 📱 **Mobile-friendly interface**

## 📊 What's Collected

This project automatically gathers comprehensive build environment information from GitHub Actions runners including:

### 🎯 Platform Coverage

- **Ubuntu**: 22.04, 24.04
- **Windows Server**: 2022, 2025
- **macOS**: 13, 14, 15

### 📋 Information Collected

- **🔧 .NET MAUI Workloads**: Installation status and compatibility across platforms
- **⚙️ .NET SDK Information**: Complete runtime and SDK details
- **🌍 GitHub Context**: Repository, workflow, and environment metadata (tokens redacted)
- **🖥️ Runner Details**: Hardware specifications and OS information
- **📦 Environment Variables**: Build environment configuration
- **🎛️ Matrix Configuration**: Build strategy and platform settings

## 🚀 How It Works

1. **🔄 Automated Collection**: GitHub Actions workflow runs on every push
2. **🏗️ Multi-Platform Build**: Collects data from all supported runner types
3. **🔒 Security**: Automatically redacts sensitive tokens and secrets
4. **📖 Documentation**: Generates interactive site with DocFX
5. **🌐 Deployment**: Publishes to GitHub Pages automatically

## 🛠️ Technical Details

### Workflow Architecture

```text
collect-build-info → generate-site → deploy-site
```

- **Collection Job**: Runs on matrix of all OS types, installs MAUI workloads, collects environment data
- **Generation Job**: Downloads artifacts, builds DocFX documentation site
- **Deployment Job**: Publishes to GitHub Pages with proper permissions

### Key Features

- ✅ **Resilient Workload Installation**: Individual MAUI workload steps with failure tolerance
- 🔐 **Security-First**: Token redaction using regex patterns
- 📁 **Artifact Management**: Structured data collection and transfer
- 🎨 **Interactive UI**: Collapsible sections and embedded content viewers

## 📁 Repository Structure

```text
GitHub_Runner_Information/
├── .github/workflows/
│   └── build-info.yml      # Main collection workflow
├── docs/
│   └── intro.md           # Documentation homepage content
├── README.md              # This file
└── LICENSE.md            # MIT License
```

## 🤝 Contributing

Contributions are welcome! Areas for improvement:

- 🔧 Additional workload types (Blazor, WASM, etc.)
- 📊 Performance benchmarking
- 🎨 UI/UX enhancements
- 📈 Historical data tracking
- 🔍 Advanced filtering and search

## 📜 License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## 🎯 Use Cases

This project is particularly useful for:

- **🔬 DevOps Research**: Understanding GitHub runner capabilities
- **🏗️ Build Planning**: Choosing the right runner for your project
- **🛠️ Tool Compatibility**: Checking MAUI/.NET support across platforms
- **📊 Environment Analysis**: Comparing runner specifications
- **🎓 Educational**: Learning about CI/CD environments

---

**[📖 Explore the Documentation](https://framinosona.github.io/GitHub_Runner_Information)** | **[🚀 View Workflow Runs](https://github.com/framinosona/GitHub_Runner_Information/actions)**

> Automatically updated with each workflow run
