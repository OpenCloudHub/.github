# Organization Labels & Issue Types - Quick Reference

This organization uses a structured labeling system across all repositories to categorize and track work. Labels follow a `category:value` syntax (e.g., `status:blocked`, `team:ai`, `priority:high`) and are automatically applied through issue templates or manually added as needed.

## Issue Types
| Type | Purpose |
|------|---------|
| **Epic** | Large work packages spanning weeks/months |
| **Feature** | New functionality or significant components |
| **Task** | Specific implementation work |
| **Bug** | Something broken that needs fixing |
| **Research** | Investigation or analysis needed |
| **Documentation** | Create/update docs and guides |

## Teams & Responsibilities
| Team | Focus Area |
|------|------------|
| **Platform** | Infrastructure, GitOps, core services |
| **AI** | ML models, training, experiments |
| **App** | Frontend, backend, demo applications |
| **Thesis** | Research, documentation, academic work |

## System Components
| Component | Coverage |
|-----------|----------|
| **infra** | Terraform, Kubernetes, cluster setup |
| **gitops** | ArgoCD, ApplicationSets, Helm |
| **cicd** | GitHub Actions, pipelines |
| **ai-platform** | MLflow, training, serving |
| **ai-models** | BERT, Qwen, model development |
| **security** | Keycloak, auth, certificates |
| **observability** | Prometheus, Grafana, monitoring |
| **storage** | MinIO, PostgreSQL, data |
| **demo-app** | User-facing applications |
| **general** | Cross-cutting or uncategorized |

## Priority Levels
| Priority | When to Use |
|----------|-------------|
| **Critical** | Blocking progress, system down |
| **High** | Important for milestone |
| **Medium** | Standard priority |
| **Low** | Nice to have, can defer |

## Work Status
| Status | Meaning |
|--------|---------|
| **Blocked** | Waiting on dependency |
| **In Review** | PR submitted, awaiting feedback |
| **Needs Info** | Requires clarification |

## Size Estimates
| Size | Effort |
|------|--------|
| **XS** | < 2 hours |
| **S** | 2-8 hours (half to full day) |
| **M** | 1-3 days (typical task) |
| **L** | 3-7 days (substantial feature) |
| **XL** | 1+ weeks (consider breaking down) |

## Default Labels
- **good first issue** - Easy entry point for newcomers
- **help wanted** - Community contributions welcome  
- **question** - Need clarification or information

---
*Every issue should have: 1 type + 1 team + 1+ components + 1 priority + 1 size*