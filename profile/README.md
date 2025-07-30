# 🚀 OpenCloudHub — MLOps Platform Organization Hub

Welcome to **OpenCloudHub**, the central repository for our Kubernetes-based MLOps platform project — initially developed as a master's thesis and designed to grow into a scalable, secure solution for AI teams.  

This repository serves as your starting point and coordination hub for all things OpenCloudHub.

---

## 🎯 Project Overview

OpenCloudHub is a Proof-of-Concept (PoC) platform that demonstrates the full machine learning lifecycle — from training and validation to deployment and monitoring — running initially on local Kubernetes (kind).  

We support:  
- **Predictive Models:** classical ML workflows using libraries like scikit-learn  
- **Generative AI:** fine-tuning and serving large language models such as BERT and Qwen  

The platform’s architecture is designed for extensibility toward production-grade environments used by university teams and future startups needing custom and private AI model integration as well as opensource infrastructure supporting their applications.

---

## 🏗️ Architectural Highlights

- **Infrastructure as Code (IaC):** Terraform + Terragrunt for flexible environment management  
- **GitOps Deployments:** Argo CD with ApplicationSets, Helm, and Kustomize  
- **CI/CD Pipelines:** GitHub Actions driving build, test, and deploy workflows  
- **ML Pipelines:** Argo Workflows for reproducible and scalable model training  
- **Model Serving:** KServe for high-performance inference endpoints  
- **Experiment Tracking:** MLflow managing experiment metadata and model registry  
- **Observability:** Prometheus, Grafana, Loki, Tempo, and Opencost for full-stack monitoring  
- **Authentication & Secrets:** Keycloak and HashiCorp Vault  
- **Storage:** MinIO for object storage and CloudNativePG for PostgreSQL management  
- **Team Isolation:** Dedicated Kubernetes namespaces per team/project for security and resource control  

---

## 👥 Team & Repository Structure

| Team             | Repositories                                      | Description                                  |
|------------------|-------------------------------------------------|----------------------------------------------|
| **Admin**        | `.github`, `docs`                                | Org-wide GitHub settings, issue & PR templates, and centralized documentation website |
| **Platform Team**| `github-management`, `infra-modules`, `infra-live`, `gitops` | Core infrastructure, Terraform modules, and GitOps deployment tooling |
| **AI Team**      | `ai-ml-demo`, `ai-bert-demo`, `ai-qwen-demo`    | Model development and experimentation for predictive and generative AI |
| **Demo App Team**| `demo-app-frontend`, `demo-app-backend`          | Applications showcasing platform integration and usage scenarios |
| **Thesis Team**  | `thesis` (admin-only)                            | Master’s thesis work and research artifacts |

---

## ☸️ Kubernetes Cluster Architecture

We leverage modern cloud-native tools for scalable, secure, and observable operations:  

- Argo CD (GitOps continuous deployment)  
- Istio (ambient mode) service mesh  
- Kubernetes Gateway API (ingress management)  
- cert-manager (automated TLS certificates)  
- External Secrets synchronization  
- Observability stack: Prometheus, Grafana, Loki, Tempo, Grafana Alloy  
- Keycloak (authentication)  
- CloudNativePG (PostgreSQL operator)  
- MinIO (object storage)  
- HashiCorp Vault (secrets and encryption management)  

---

## 📖 Getting Started & Next Steps

This repository is **not** intended to replace detailed documentation. For comprehensive guides, architecture diagrams, and developer onboarding, please visit our [Documentation Website](#) (replace with actual URL).

Explore individual repositories under each team for code, pipelines, and infrastructure configurations.

---

## 📬 Questions or Collaboration?

Feel free to reach out via internal communication channels or open an issue in the relevant repo.

---

Thank you for your interest in OpenCloudHub — powering the next generation of secure and scalable cloudnative AI platforms! 🌐🤖

