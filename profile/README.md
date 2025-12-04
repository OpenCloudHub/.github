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
  <h1>☸️ Cloud-Native MLOps Platform</h1>
  <p>
    <strong>Master's Thesis:</strong> A Scalable MLOps System for Multimodal Educational Analysis<br>
    <em>Goethe University Frankfurt / DIPF Leibniz Institute</em>
  </p>
  <div>
    <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes">
    <img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white" alt="ArgoCD">
    <img src="https://img.shields.io/badge/Ray-028CF0?style=for-the-badge&logo=ray&logoColor=white" alt="Ray">
    <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow">
  </div>
  <br>
  <div>
    <a href="#overview"><strong>📖 Overview</strong></a> •
    <a href="#architecture"><strong>🏗️ Architecture</strong></a> •
    <a href="#repositories"><strong>📂 Repositories</strong></a> •
    <a href="#demonstrations"><strong>🎬 Demos</strong></a>
  </div>
</div>

______________________________________________________________________

<h2 id="overview">📖 Overview</h2>

OpenCloudHub is an open-source, self-hostable MLOps platform developed as part of a master's thesis. It demonstrates how to build infrastructure for machine learning and AI workflows using cloud-native technologies—all deployable on institution-controlled infrastructure for data sovereignty.

**Key Characteristics:**

- 🔓 **Fully Open-Source** — No proprietary dependencies or vendor lock-in
- 🏠 **Self-Hostable** — Deploy on your own infrastructure for data privacy
- 🔄 **GitOps-First** — Git as single source of truth for all cluster state
- 🤖 **ML Framework Agnostic** — sklearn, PyTorch, Transformers, LLMs
- 📊 **End-to-End Traceability** — Data version → training run → deployed model

______________________________________________________________________

<h2 id="architecture">🏗️ Architecture</h2>

```
┌─────────────────────────────────────────────────────────────────────────┐
│                              Teams / Workloads                          │
│         Wine Classifier • Fashion MNIST • BERT • Qwen-VL • RAG App      │
├─────────────────────────────────────────────────────────────────────────┤
│                             Platform Services                           │
├─────────────────┬─────────────────┬─────────────────┬───────────────────┤
│     MLOps       │   Observability │     Storage     │    GitOps         │
│                 │                 │                 │                   │
│ • Argo Workflows│ • Prometheus    │ • MinIO (S3)    │ • ArgoCD          │
│ • MLflow        │ • Grafana       │ • CloudNativePG │ • Image Updater   │
│ • KubeRay       │ • Loki & Tempo  │ • pgvector      │ • ApplicationSets │
│ • DVC           │ • Alloy         │                 │                   │
├─────────────────┴─────────────────┴─────────────────┴───────────────────┤
│                          Infrastructure Layer                           │
│          Kubernetes • Istio (Ambient) • External Secrets • Vault        │
└─────────────────────────────────────────────────────────────────────────┘
```

**Design Principles:**

- **Layered Architecture** — Infrastructure, Platform, and Workload layers with clear boundaries
- **Integration Coherence** — Argo ecosystem for orchestration, Ray ecosystem for ML compute
- **Declarative Everything** — All configuration in Git, reconciled by ArgoCD

______________________________________________________________________

<h2 id="repositories">📂 Repositories</h2>

<details open>
<summary><strong>🛠️ Platform Infrastructure</strong></summary>

| Repository                                                                         | Description                                                                                 |
| ---------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [gitops](https://github.com/opencloudhub/gitops)                                   | ArgoCD configuration, app-of-apps pattern, all platform components, Argo Workflow templates |
| [.github](https://github.com/opencloudhub/.github)                                 | Shared GitHub Actions workflows and composite actions                                       |
| [data-registry](https://github.com/opencloudhub/data-registry)                     | DVC-versioned datasets, data pipelines, embeddings generation                               |
| [gh-actions-local-runner](https://github.com/opencloudhub/gh-actions-local-runner) | Self-hosted GitHub Actions runner for local development                                     |
| [k6s-testing](https://github.com/opencloudhub/k6s-testing)                         | Load testing with k6 operator, Grafana integration                                          |

</details>

<details open>
<summary><strong>🤖 ML Workload Demonstrations</strong></summary>

| Repository                                                                       | Framework                | Demonstrates                                            |
| -------------------------------------------------------------------------------- | ------------------------ | ------------------------------------------------------- |
| [ai-ml-sklearn](https://github.com/opencloudhub/ai-ml-sklearn)                   | scikit-learn             | Traditional ML, Ray joblib, full MLOps pipeline         |
| [ai-dl-lightning](https://github.com/opencloudhub/ai-dl-lightning)               | PyTorch Lightning        | Deep learning, Ray DDP distributed training             |
| [ai-dl-bert](https://github.com/opencloudhub/ai-dl-bert)                         | HuggingFace Transformers | DistilBERT, Ray Tune + ASHA hyperparameter optimization |
| [ai-dl-qwen](https://github.com/opencloudhub/ai-dl-qwen)                         | Qwen2.5-VL               | Vision-language fine-tuning, GPU training, QLoRA/LoRA   |
| [demo-app-genai-backend](https://github.com/opencloudhub/demo-app-genai-backend) | LangChain                | RAG application, prompt versioning, MLflow evaluation   |

</details>

<details>
<summary><strong>🧰 Development Tools</strong></summary>

| Repository                                                                 | Description                                                   |
| -------------------------------------------------------------------------- | ------------------------------------------------------------- |
| [local-compose-setup](https://github.com/opencloudhub/local-compose-setup) | Docker Compose stack for local development without Kubernetes |

</details>

______________________________________________________________________

<h2 id="demonstrations">🎬 Demonstrations</h2>

The platform validates 16 functional requirements through video demonstrations:

| Category           | What's Demonstrated                                                   |
| ------------------ | --------------------------------------------------------------------- |
| **Traditional ML** | Full pipeline: GH Action → Argo Workflow → MLflow → GitOps deployment |
| **Deep Learning**  | Distributed training with Ray DDP across multiple workers             |
| **Transformers**   | Hyperparameter optimization with Ray Tune + ASHA scheduler            |
| **GenAI**          | LLM serving with vLLM, RAG with prompt versioning and evaluation      |
| **Data Pipelines** | DVC versioning, parallel pipelines, embeddings with Ray Data          |
| **Observability**  | Grafana dashboards, distributed load testing with k6                  |

______________________________________________________________________

<h2 id="quick-start">🚀 Quick Start</h2>

```bash
# Clone GitOps repository
git clone https://github.com/opencloudhub/gitops.git
cd gitops

# Bootstrap local cluster (requires Docker, minikube or kind)
# Follow the setup instructions and then run
./local-development/start-dev.sh

# Access platform UIs after bootstrap completes
# - ArgoCD:        https://argocd.internal.opencloudhub.org
# - MLflow:        https://mlflow.internal.opencloudhub.org
# - Grafana:       https://grafana.internal.opencloudhub.org
# - Argo Workflows: https://argo-workflows.internal.opencloudhub.org
```

See [gitops/README.md](https://github.com/opencloudhub/gitops) for detailed setup instructions.

______________________________________________________________________

<h2 id="thesis">🎓 Thesis Context</h2>

**Research Questions:**

- **RQ1:** How can a scalable and traceable MLOps pipeline be designed to support both predictive and generative ML workloads? (This Org is the POC)
- **RQ2:** What roadmap is required to evolve from proof-of-concept to production-ready system?

**Purpose**:
This organisation serves as the conclusion of **RQ1**.

**Contributions of this org:**

1. Working MLOps platform with GitOps, experiment tracking, data versioning, and model serving
1. Framework-agnostic validation across sklearn, PyTorch, Transformers, and LLMs
1. GenAI workflow patterns including RAG and prompt versioning

______________________________________________________________________

<div align="center">
  <p><em>Open-source • Self-hostable • Privacy-preserving</em></p>
  <a href="https://github.com/opencloudhub/gitops">
    <img src="https://img.shields.io/badge/Start%20Here-GitOps%20Repo-blue?style=for-the-badge&logo=github" alt="Start Here">
  </a>
</div>
