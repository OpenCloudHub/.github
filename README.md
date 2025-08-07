<a id="readme-top"></a>

<!-- PROJECT LOGO & TITLE -->

<div align="center">
  <a href="https://github.com/opencloudhub">
  <picture>
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/opencloudhub/.github/main/assets/brand/assets/logos/primary-logo-light.svg">
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/opencloudhub/.github/main/assets/brand/assets/logos/primary-logo-dark.svg">
    <!-- Fallback -->
    <img alt="OpenCloudHub Logo" src="https://raw.githubusercontent.com/opencloudhub/.github/main/assets/brand/assets/logos/primary-logo-dark.svg" style="max-width:700px; max-height:175px;">
  </picture>
  </a>

<h1 align="center">GitHub Standards & Templates</h1>

<p align="center">
    Central repository for managing OpenCloudHub's GitHub metadata, workflows, contribution standards, branding, and reusable templates.<br />
    <a href="https://github.com/opencloudhub"><strong>Explore the organization »</strong></a>
  </p>

<p align="center">
    <a href="https://github.com/opencloudhub/.github/graphs/contributors">
      <img src="https://img.shields.io/github/contributors/opencloudhub/.github.svg?style=for-the-badge" alt="Contributors">
    </a>
    <a href="https://github.com/opencloudhub/.github/network/members">
      <img src="https://img.shields.io/github/forks/opencloudhub/.github.svg?style=for-the-badge" alt="Forks">
    </a>
    <a href="https://github.com/opencloudhub/.github/stargazers">
      <img src="https://img.shields.io/github/stars/opencloudhub/.github.svg?style=for-the-badge" alt="Stars">
    </a>
    <a href="https://github.com/opencloudhub/.github/issues">
      <img src="https://img.shields.io/github/issues/opencloudhub/.github.svg?style=for-the-badge" alt="Issues">
    </a>
    <a href="https://github.com/opencloudhub/.github/blob/main/LICENSE">
      <img src="https://img.shields.io/github/license/opencloudhub/.github.svg?style=for-the-badge" alt="License">
    </a>
  </p>
</div>

______________________________________________________________________

<details>
  <summary>📑 Table of Contents</summary>
  <ol>
    <li><a href="#features">Features</a></li>
    <li><a href="#branding">Branding</a></li>
    <li><a href="#emplates">Templates</a></li>
    <li><a href="#ared-configurations">Shared Configurations</a></li>
    <li><a href="#rkflows--automation">Workflows & Automation</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#object-structure">Project Structure</a></li>
    <li><a href="#ontributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

______________________________________________________________________

<h2 id="features">✨ Features</h2>

This repository serves as the centralized location for **organization-level GitHub configuration and standards** across all `OpenCloudHub` repositories. It contains:

- Branding and logo assets
- Markdown and metadata templates
- CI workflow definitions
- Pre-commit and linting configurations
- GitHub profile page (`profile/README.md`)
- Labeling, dependabot, and security policies

All other repositories within the organization can reference or copy these resources to ensure **standardization and compliance**.

______________________________________________________________________

<h2 id="branding">🎨 Branding</h2>

The `/brand` folder contains assets and styling guidelines for use in documentation, websites, or repository READMEs:

- Logos (SVG, PNG)
- Style guide (`style-guide.md`)
- CSS variables for consistent theming

Use the **light-background** logo variants for public documentation to ensure maximum compatibility across light/dark themes.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="templates">🧰 Templates</h2>

Available templates under `/templates` and `.github`:

- **README_TEMPLATE.md**: General-purpose, pre-structured project README template
- **Issue templates**: Bug reports and feature requests (YAML-configured)
- **Pull request template**
- **CONTRIBUTING.md**, **CODE_OF_CONDUCT.md**, **SECURITY.md**: Community and contribution policies

These templates enable fast, standardized setup for any new repository under the organization.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="shared-configurations">⚙️ Shared Configurations</h2>

Reusable configurations and tools for repository maintainers and contributors:

- `config/pre-commit-config.yaml`: Centralized pre-commit hook setup
- `.github/labeler.yml`: Automatic labeling of pull requests based on file paths
- `dependabot.yml`: Common dependency update configuration

Pre-commit config can be symlinked or copied into individual repos. The code quality workflow will enforce this configuration via CI.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="workflows-automation">🤖 Workflows & Automation</h2>

Reusable workflows are stored under `.github/workflows` and can be shared via `workflow_call`. Examples include:

- Python testing & linting
- Docker build & push
- Node.js/Next.js CI
- Pre-commit hook enforcement
- Markdown linting and README validation

These workflows can be imported into any repository in the organization for consistent CI/CD practices.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="getting-started">🚀 Getting Started</h2>

To make use of this repository’s content in your own repo:

1. Reference templates manually or via automation
1. Use `uses: opencloudhub/.github/.github/workflows/<workflow>.yaml@main` in your Actions
1. Copy branding assets or style guide as needed
1. Clone or curl raw pre-commit config:
   ```sh
   curl -O https://raw.githubusercontent.com/opencloudhub/.github/main/config/pre-commit-config.yaml
   ```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- PROJECT STRUCTURE -->

<h2 id="project-structure">📁 Project Structure</h2>

```
.github/
├── brand/
│   ├── assets/                 # Logos and visual assets
│   ├── style-guide.md          # Branding rules
│   └── templates/              # CSS variables, UI references
├── config/
│   └── pre-commit-config.yaml  # Shared pre-commit hooks
├── profile/
│   └── README.md               # Org profile page
├── templates/
│   └── README_TEMPLATE.md      # Project README boilerplate
├── .github/
│   ├── ISSUE_TEMPLATE/         # Issue templates (YAML)
│   ├── workflows/              # Shared GitHub Actions workflows
│   ├── PULL_REQUEST_TEMPLATE.md
│   ├── labeler.yml             # Auto-labeling config
│   ├── CODE_OF_CONDUCT.md
│   ├── CONTRIBUTING.md
│   └── SECURITY.md
├── LICENSE
└── README.md                   # This file
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTRIBUTING -->

<h2 id="contributing">👥 Contributing</h2>

Contributions are welcome! This template is designed to make contribution as smooth as possible with templates and guidelines.

Please see our [Contributing Guidelines](../.github/CONTRIBUTING.md) and [Code of Conduct](../.github/CODE_OF_CONDUCT.md) for more details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- LICENSE -->

<h2 id="license">📄 License</h2>

Distributed under the Apache 2.0 License. See [LICENSE](/LICENSE) for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- CONTACT -->

<h2 id="contact">📬 Contact</h2>

Organization Link: [https://github.com/OpenCloudHub](https://github.com/OpenCloudHub)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ACKNOWLEDGEMENTS -->

<h2 id="acknowledgements">🙏 Acknowledgements</h2>
Share links or references to useful resources:

- [Best-README-Template](https://github.com/othneildrew/Best-README-Template) - The foundation for this README design

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- MARKDOWN LINKS & IMAGES -->
