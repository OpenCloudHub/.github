<div align="center">
  <a href="https://github.com/opencloudhub">
    <img src="https://raw.githubusercontent.com/opencloudhub/.github/main/references/brand/assets/logos/primary-logo-light-background.svg" alt="OpenCloudHub Logo" width="100%" style="max-width:400px;" height="200">
  </a>
  <h1>🚀 Modern Cloud-Native Platform Engineering</h1>
  <p>
    <strong>Master's Thesis Project:</strong> Exploring cloud-native MLOps infrastructure patterns<br>
    <em>From local development to production-ready platform architecture</em>
  </p>
  <div>
    <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white" alt="Kubernetes">
    <img src="https://img.shields.io/badge/ArgoCD-EF7B4D?style=for-the-badge&logo=argo&logoColor=white" alt="ArgoCD">
    <img src="https://img.shields.io/badge/MLflow-0194E2?style=for-the-badge&logo=mlflow&logoColor=white" alt="MLflow">
    <img src="https://img.shields.io/badge/Status-In%20Development-yellow?style=for-the-badge" alt="Status">
  </div>
  <br>
  <div>
    <a href="#overview"><strong>📖 Overview</strong></a> •
    <a href="#current-status"><strong>📊 Status</strong></a> •
    <a href="#architecture"><strong>🏗️ Architecture</strong></a> •
    <a href="#get-involved"><strong>🚀 Get Started</strong></a>
  </div>
</div>

<h2 id="overview">📖 What is OpenCloudHub?</h2>
OpenCloudHub is a research-driven MLOps platform being developed as part of a master's thesis. The project explores how to build modern, cloud-native infrastructure for machine learning workflows—starting with a local proof-of-concept and evolving toward production-ready patterns.

**Research Focus:**
- 🔬 How do modern cloud-native technologies integrate into cohesive platforms?
- ☸️ What does comprehensive Kubernetes platform engineering look like in practice?
- 🤖 How do MLOps workflows drive platform requirements and design decisions?
- 🔐 How can we implement security, observability, and multi-tenancy from day one?
- 📚 How do we bridge the gap between local academic research and industry practices?

**ML Workloads We're Building For:**
- 🤖 **Classical ML:** Predictive models using scikit-learn
- 🧠 **Generative AI:** Fine-tuning BERT, Qwen, and other transformer models and llms
- 🔄 **End-to-End Pipelines:** From data ingestion to model serving

---

<h2 id="current-status">📊 Current Development Status</h2>

<table>
<tr>
<td width="33%">

**🏗️ Infrastructure Foundation**
- ✅ Kind cluster setup
- ✅ Terraform/Terragrunt IaC
- ✅ GitHub organization automation
- 🚧 Istio service mesh integration

</td>
<td width="33%">

**🤖 MLOps Core**
- ✅ MLflow experiment tracking
- 🚧 Argo Workflows for training
- 🚧 KServe model serving
- 📋 Multi-tenant ML pipelines

</td>
<td width="33%">

**🔐 Platform Services**
- 🚧 Keycloak authentication
- 🚧 Prometheus/Grafana observability
- 📋 Vault secrets management
- 📋 Multi-environment deployment

</td>
</tr>
</table>

**Legend:** ✅ Implemented • 🚧 In Progress • 📋 Planned

---

<h2 id="architecture">🏗️ Architecture Overview</h2>

```
┌─────────────────────────────────────────────────────────────────────────┐
│                          GitOps & Infrastructure                        │
│  GitHub Actions • Argo CD • Terraform • Terragrunt • Helm/Kustomize   │
├─────────────────┬─────────────────┬─────────────────┬─────────────────┤
│   ML Platform   │  Observability  │   Security      │   Storage       │
│                 │                 │                 │                 │
│ • Argo Workflows│ • Prometheus    │ • Keycloak      │ • MinIO         │
│ • KServe        │ • Grafana       │ • Vault         │ • PostgreSQL    │
│ • MLflow        │ • Loki & Tempo  │ • cert-manager  │ • Persistent    │
│                 │ • OpenCost      │ • Istio mTLS    │   Volumes       │
└─────────────────┴─────────────────┴─────────────────┴─────────────────┘
                    Kubernetes (kind → cloud-ready)
```

**Design Principles We're Exploring:**
- **Research-Driven:** Documenting architectural decisions and trade-offs
- **Cloud-Native Patterns:** Modern Kubernetes ecosystem integration
- **GitOps-First:** Declarative infrastructure and application management
- **Learning-Oriented:** Comprehensive documentation of the journey

---

<h2 id="repositories">📂 Project Structure</h2>


<details open>
  <summary><strong>🛠️ Platform Team</strong></summary>
  <ul>
    <li><a href="https://github.com/opencloudhub/.github">.github</a> – Shared org templates and workflows</li>
    <li><a href="https://github.com/opencloudhub/github-management">github-management</a> – Org automation with Terraform</li>
    <li><a href="https://github.com/opencloudhub/docs">docs</a> – Comprehensive documentation website</li>
    <li><a href="https://github.com/opencloudhub/infra-modules">infra-modules</a> – Reusable Terraform modules</li>
    <li><a href="https://github.com/opencloudhub/infra-live">infra-live</a> – Live infrastructure with Terragrunt</li>
    <li><a href="https://github.com/opencloudhub/gitops">gitops</a> – Argo CD apps and configs</li>
    <li><a href="https://github.com/opencloudhub/gh-actions-local-runner">gh-actions-local-runner</a> – Local runner utility for GH Actions</li>
  </ul>
</details>

<details>
  <summary><strong>🧠 AI Team</strong></summary>
  <ul>
    <li><a href="https://github.com/opencloudhub/ai-ml-demo">ai-ml-demo</a> – Classical ML pipeline examples</li>
    <li><a href="https://github.com/opencloudhub/ai-bert-demo">ai-bert-demo</a> – BERT fine-tuning workflows</li>
    <li><a href="https://github.com/opencloudhub/ai-qwen-demo">ai-qwen-demo</a> – Qwen model experimentation</li>
  </ul>
</details>

<details>
  <summary><strong>🌐 Application Team</strong></summary>
  <ul>
    <li><a href="https://github.com/opencloudhub/demo-app-frontend">demo-app-frontend</a> – React dashboard for model interactions</li>
    <li><a href="https://github.com/opencloudhub/demo-app-backend">demo-app-backend</a> – FastAPI backend with model integration</li>
    <li><a href="https://github.com/opencloudhub/landing-page">landing-page</a> – Org landing page</li>
  </ul>
</details>




---

<h2 id="get-involved">🚀 Getting Started</h2>

### 📚 For Researchers & Students
- **[📖 Full Documentation](https://opencloudhub.github.io/docs)** - Detailed setup guides and architectural decisions
- **[🎯 Local Development](https://opencloudhub.github.io/docs/getting-started/local-setup)** - Deploy the platform on your machine
- **[📋 Project Roadmap](https://github.com/orgs/opencloudhub/projects/1)** - See what's coming next

### 🔍 For Platform Engineers
- **Explore Implementation Details:** Browse the repositories above to see real-world GitOps and IaC patterns
- **Learn Integration Patterns:** See how modern cloud-native tools work together
- **Contribute Ideas:** Join discussions about platform engineering approaches

<!-- # TODO: add some videos here -->
### 💡 Demos
```bash
# Clone and deploy locally (requires Docker & kind)
git clone https://github.com/opencloudhub/infra-live.git
cd infra-live/local && ./deploy.sh

# Access MLflow UI
kubectl port-forward -n mlflow svc/mlflow-server 5000:5000
```

---

## 🎓 Academic Context & Future Vision

**Current Thesis Phase:** Building and documenting a comprehensive MLOps platform proof-of-concept

**Research Contributions:**
- Integration patterns for cloud-native MLOps toolchains
- Platform engineering approaches for AI/ML teams
- Documentation of architectural decisions and trade-offs

**Future Applications:**
- Foundation for university research projects requiring custom ML models and application integration
- Template for organizations transitioning from local development to production systems
- Personal showcase and learning resource for the cloud-native community
- Potential baseline for SaaS offerings or consulting engagements

---

<div align="center">
  <h3>🌟 Follow the Journey</h3>
  <p><em>Building in public • Learning together • Sharing knowledge</em></p>
  
  <div>
    <a href="https://opencloudhub.github.io/docs">
      <img src="https://img.shields.io/badge/Read%20the%20Docs-2596BE?style=for-the-badge&logo=read-the-docs&logoColor=white" alt="Documentation">
    </a>
    <a href="https://github.com/orgs/opencloudhub/discussions">
      <img src="https://img.shields.io/badge/Join%20Discussion-181717?style=for-the-badge&logo=github&logoColor=white" alt="Discussions">
    </a>
    <a href="https://github.com/orgs/opencloudhub/projects/1">
      <img src="https://img.shields.io/badge/View%20Roadmap-0052CC?style=for-the-badge&logo=jira&logoColor=white" alt="Roadmap">
    </a>
  </div>
</div>