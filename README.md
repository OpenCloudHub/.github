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
    Central repository for managing OpenCloudHub's GitHub metadata, reusable workflows, contribution standards, branding, and templates.<br />
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
    <li><a href="#about">About</a></li>
    <li><a href="#thesis-context">Thesis Context</a></li>
    <li><a href="#features">Features</a></li>
    <li><a href="#architecture">Architecture</a></li>
    <li><a href="#getting-started">Getting Started</a></li>
    <li><a href="#project-structure">Project Structure</a></li>
    <li><a href="#contributing">Contributing</a></li>
    <li><a href="#license">License</a></li>
    <li><a href="#contact">Contact</a></li>
  </ol>
</details>

______________________________________________________________________

<h2 id="about">🎯 About</h2>

This repository serves as the **centralized GitHub configuration hub** for the OpenCloudHub organization. It provides organization-wide standards, reusable CI/CD workflows, and templates that ensure consistency across all repositories in the platform.

**What problem does this solve?**

In a multi-repository MLOps platform, maintaining consistent CI/CD pipelines, code quality standards, and documentation templates across dozens of repos becomes a maintenance burden. This repository solves that by:

- Providing **reusable GitHub Actions workflows** that any repo can import
- Defining **custom composite actions** for common MLOps tasks (DVC versioning, Docker tag resolution, kubectl setup)
- Centralizing **issue templates, PR templates, and contribution guidelines**
- Hosting **branding assets** for consistent visual identity

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="thesis-context">🎓 Thesis Context</h2>

This repository is part of a **Master's thesis project** exploring cloud-native MLOps platform engineering. The research investigates how to build modern, production-ready infrastructure for machine learning workflows.

**Role of This Repository:**

- Demonstrates **GitOps principles** for organization-wide configuration
- Shows **workflow reusability patterns** across a multi-repo architecture
- Implements **MLOps-specific CI/CD patterns** (DVC integration, model deployment triggers)

For the full platform architecture, see the [organization profile](https://github.com/opencloudhub).

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="features">✨ Features</h2>

### Reusable Workflows

- **`shared-ci-code-quality.yaml`** — Pre-commit hooks with hadolint, shellcheck, typos, and biome
- **`shared-ci-test-python.yaml`** — Python testing with pytest, coverage thresholds, and uv package manager
- **`shared-ci-docker-build-push.yaml`** — Multi-stage Docker builds with registry caching and semantic tagging
- **`shared-mlops-pipeline.yaml`** — Full ML lifecycle orchestration via Argo Workflows

### Custom Composite Actions

- **`resolve-docker-tag`** — Finds the SHA-tagged image matching 'latest' for reproducible deployments
- **`resolve-dvc-version`** — Validates and resolves DVC data versions from the data registry
- **`setup-kubectl`** — Configures kubectl with cluster access for pipeline submissions

### Templates & Standards

- **Issue templates** — Bug, Feature, Epic, Task, Research, Documentation (YAML-configured)
- **PR template** — Structured checklist with change types and review requirements
- **Community files** — CONTRIBUTING.md, CODE_OF_CONDUCT.md, SECURITY.md
- **README template** — Standardized project documentation structure

### Branding & Assets

- **Logo suite** — Light/dark variants for all contexts
- **Style guide** — Color palette, typography, spacing system
- **CSS variables** — Ready-to-use design tokens

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="architecture">🏗️ Architecture</h2>

```
┌─────────────────────────────────────────────────────────────────────────────┐
│                        OpenCloudHub Organization                            │
├─────────────────────────────────────────────────────────────────────────────┤
│                                                                             │
│   ┌─────────────────┐    imports     ┌─────────────────────────────────┐    │
│   │  AI Team Repos  │ ─────────────▶│                                 │    │
│   │  - ai-ml-repo   │                │   .github Repository (this)     │    │
│   │  - ai-dl-repo   │                │                                 │    │
│   │  - ai-genai-repo│                │   ┌─────────────────────────┐   │    │
│   └─────────────────┘                │   │   Reusable Workflows    │   │    │
│                                      │   │   ├─ ci.yaml            │   │    │
│   ┌─────────────────┐    imports     │   │   ├─ code-quality.yaml  │   │    │
│   │  Platform Repos │ ─────────────▶│   │   ├─ docker-build.yaml  │   │    │
│   │  - infra-live   │                │   │   ├─ python-test.yaml   │   │    │
│   │  - gitops       │                │   │   └─ mlops-pipeline.yaml│   │    │
│   │  - docs         │                │   └─────────────────────────┘   │    │
│   └─────────────────┘                │                                 │    │
│                                      │   ┌─────────────────────────┐   │    │
│   ┌─────────────────┐    imports     │   │   Composite Actions     │   │    │
│   │  App Team Repos │ ─────────────▶│   │   ├─ resolve-docker-tag │   │    │
│   │  - frontend     │                │   │   ├─ resolve-dvc-version│   │    │
│   │  - backend      │                │   │   └─ setup-kubectl      │   │    │
│   └─────────────────┘                │   └─────────────────────────┘   │    │
│                                      │                                 │    │
│                                      └─────────────────────────────────┘    │
└─────────────────────────────────────────────────────────────────────────────┘
```

### Workflow Flow (MLOps Pipeline Example)

```
Dispatches Workflow ( Could be set up to trigger automatically or on schedule/external trigger)
        │
        ▼
┌───────────────────────┐
│ train.yaml triggers   │ ◀── Defined in consuming repo
└─────────┬─────────────┘
          │ uses
          ▼
┌───────────────────────────────────────────────────────────────┐
│                  shared-mlops-pipeline.yaml                   │
│                                                               │
│  ┌─────────────┐   ┌─────────────┐   ┌─────────────────────┐  │
│  │resolve-dvc- │   │resolve-     │   │setup-kubectl        │  │
│  │version      │   │docker-tag   │   │                     │  │
│  │             │   │             │   │                     │  │
│  │ Validates   │   │ Finds       │   │ Configures cluster  │  │
│  │ data version│   │ image SHA   │   │ access              │  │
│  └──────┬──────┘   └──────┬──────┘   └──────────┬──────────┘  │
│         │                 │                      │            │
│         └────────────────┬┴──────────────────────┘            │
│                          ▼                                    │
│            ┌─────────────────────────┐                        │
│            │ Submit Argo Workflow    │                        │
│            │ to Kubernetes cluster   │                        │
│            └─────────────────────────┘                        │
└───────────────────────────────────────────────────────────────┘
                           │
                           ▼
              ┌─────────────────────────┐
              │   Argo Workflows (K8s)  │
              │   Train → Eval → Deploy │
              └─────────────────────────┘
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="getting-started">🚀 Getting Started</h2>

### Using Reusable Workflows

In your repository's `.github/workflows/ci.yaml`:

```yaml
name: CI
on: [push, pull_request]

jobs:
  code-quality:
    uses: opencloudhub/.github/.github/workflows/shared-ci-code-quality.yaml@main

  test:
    uses: opencloudhub/.github/.github/workflows/shared-ci-test-python.yaml@main
    with:
      python-version: "3.12"
      coverage-threshold: "85"

  build:
    uses: opencloudhub/.github/.github/workflows/shared-ci-docker-build-push.yaml@main
    with:
      repo-name: my-service
    secrets:
      DOCKER_USERNAME: ${{ secrets.DOCKER_USERNAME }}
      DOCKER_TOKEN: ${{ secrets.DOCKER_TOKEN }}
```

### Using Custom Actions

```yaml
steps:
  - name: Resolve data version
    uses: OpenCloudHub/.github/.github/actions/resolve-dvc-version@main
    with:
      dataset: wine-quality
      version: latest
      dvc-repo: ${{ vars.DVC_REPO_URL }}

  - name: Resolve image tag
    uses: OpenCloudHub/.github/.github/actions/resolve-docker-tag@main
    with:
      repo: opencloudhub/wine-classifier
      prefix: main
      tag: latest
```

### Using Templates

1. Copy `assets/templates/README_TEMPLATE.md` to your new repo
1. Use issue templates automatically (inherited from this repo)
1. Reference branding assets via raw GitHub URLs

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="project-structure">📁 Project Structure</h2>

```
.github/
├── README.md                        # This file
│
├── .github/                         # GitHub-specific configurations
│   ├── workflows/                   # Reusable CI/CD workflows
│   │   ├── ci.yaml                  # Main entry point for this repo
│   │   ├── shared-ci-code-quality.yaml    # Pre-commit & linting
│   │   ├── shared-ci-test-python.yaml     # Python testing
│   │   ├── shared-ci-docker-build-push.yaml # Container builds
│   │   └── shared-mlops-pipeline.yaml     # ML lifecycle orchestration
│   │
│   ├── actions/                     # Custom composite actions
│   │   ├── resolve-docker-tag/      # Docker tag resolution
│   │   ├── resolve-dvc-version/     # DVC data version resolution
│   │   └── setup-kubectl/           # Kubernetes CLI setup
│   │
│   ├── ISSUE_TEMPLATE/              # Issue templates (YAML forms)
│   │   ├── bug.yaml                 # Bug report template
│   │   ├── feature.yaml             # Feature request template
│   │   ├── epic.yaml                # Epic/initiative template
│   │   ├── task.yaml                # Task template
│   │   ├── research.yaml            # Research/investigation template
│   │   └── documentation.yaml       # Documentation task template
│   │
│   ├── PULL_REQUEST_TEMPLATE.md     # PR template with checklists
│   ├── CONTRIBUTING.md              # Contribution guidelines
│   ├── CODE_OF_CONDUCT.md           # Community standards
│   ├── SECURITY.md                  # Security policy
│   ├── dependabot.yaml              # Dependency update config
│   └── labeler.yaml                 # Auto-labeling rules
│
├── assets/
│   ├── brand/                       # Branding assets
│   │   ├── assets/logos/            # Logo files (SVG)
│   │   ├── style-guide.md           # Design system documentation
│   │   └── templates/css-variables.css # Design tokens
│   │
│   └── templates/
│       └── README_TEMPLATE.md       # Standardized README template
│
└── profile/
    └── README.md                    # Organization profile page
```

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="contributing">👥 Contributing</h2>

Contributions are welcome after my thesis ends! When modifying shared workflows or actions, please ensure backward compatibility with existing consumers.

**Before submitting:**

- Test workflow changes in a fork first
- Update documentation headers in YAML files
- Follow the existing code style and emoji conventions

Please see our [Contributing Guidelines](.github/CONTRIBUTING.md) and [Code of Conduct](.github/CODE_OF_CONDUCT.md) for more details.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="license">📄 License</h2>

Distributed under the Apache 2.0 License. See [LICENSE](/LICENSE) for more information.

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<h2 id="contact">📬 Contact</h2>

Organization Link: [https://github.com/OpenCloudHub](https://github.com/OpenCloudHub)

<p align="right">(<a href="#readme-top">back to top</a>)</p>

______________________________________________________________________

<div align="center">
  <h3>🌟 Part of the OpenCloudHub Platform</h3>
  <p><em>Building a production-ready MLOps platform • Master's Thesis Project</em></p>

<div>
    <a href="https://opencloudhub.github.io/docs">
      <img src="https://img.shields.io/badge/Read%20the%20Docs-2596BE?style=for-the-badge&logo=read-the-docs&logoColor=white" alt="Documentation">
    </a>
    <a href="https://github.com/orgs/opencloudhub/discussions">
      <img src="https://img.shields.io/badge/Join%20Discussion-181717?style=for-the-badge&logo=github&logoColor=white" alt="Discussions">
    </a>
    <a href="https://github.com/orgs/opencloudhub/projects/4">
      <img src="https://img.shields.io/badge/View%20Roadmap-0052CC?style=for-the-badge&logo=jira&logoColor=white" alt="Roadmap">
    </a>
  </div>
</div>

<!-- MARKDOWN LINKS & IMAGES -->
