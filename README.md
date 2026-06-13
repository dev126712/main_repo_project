# Alexandre St-Fort — Cloud | DevOps | AI | Platform Engineering

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Alexandre%20St--Fort-0A66C2?logo=linkedin)](https://ca.linkedin.com/in/alexandre-st-fort-7b32681b8)

![Banner](https://github.com/dev126712/dockerized-three-tier-app/blob/64105d4d0de1f6b2286aa6f47ae82d9ba965c086/licensed-image.jpeg)

Portfolio showcasing production-grade projects across **cloud infrastructure**, **Kubernetes/GitOps**, **AIOps**, and **platform engineering**. Private repos are available on request — just reach out on LinkedIn.

---

## Skills at a Glance

| Domain | Tools |
|---|---|
| **Cloud** | AWS · GCP (GKE) |
| **IaC** | Terraform · Helm · Kustomize |
| **Containers & Orchestration** | Docker · Kubernetes · ArgoCD |
| **CI/CD & DevSecOps** | GitHub Actions · Jenkins · Trivy · Semgrep |
| **AI / AIOps** | LangGraph · FastAPI · Groq · Claude · Ollama · Isolation Forest |
| **Observability** | Prometheus · Grafana · Loki · VictoriaMetrics · Alertmanager |
| **Platform Engineering** | Backstage IDP · HashiCorp Vault · Secrets management |
| **Languages** | Python · HCL · TypeScript · Go · Bash · JavaScript |

---

## Flagship Projects (private — available on request)

### [KubeAIOps](https://github.com/dev126712/k8s-aiops) 🔒
**Production-grade AIOps platform for Kubernetes**

A self-hosted control plane that connects to a live Kubernetes cluster, analyses it with a LangGraph reasoning graph, and automates remediations through GitOps PRs — all from a single dashboard.

| Capability | Detail |
|---|---|
| **AI analysis** | 3-node LangGraph graph: triage → deep_analyze → validate |
| **LLM providers** | Claude · GPT-4o · Ollama · Azure OpenAI · AWS Bedrock (switchable at runtime) |
| **GitOps automation** | Opens GitHub/GitLab PRs for scaling, image updates, HPA patches — auto-merges Tier 1 |
| **ArgoCD integration** | Sync status, drift detection, manual sync from the dashboard |
| **Prometheus enrichment** | 7-day CPU/memory history + recurring spike detection → predictive pre-scaling |
| **Secrets auditing** | Anomaly detection on secret access patterns |
| **Persistence** | PostgreSQL checkpointing — agent state survives pod restarts |

```
START → [triage] → [deep_analyze] → [validate] → AIAnalysisResponse
```

**Stack:** FastAPI · LangGraph · Python · Kubernetes · ArgoCD · Prometheus · PostgreSQL · Docker · nginx

[![My Skills](https://skillicons.dev/icons?i=kubernetes,py,docker,postgres,prometheus,grafana)](https://skillicons.dev)

---

### [RecruitFlow](https://github.com/dev126712/RecruitFlow) 🔒
**AI-powered job application pipeline**

Fetches a LinkedIn job posting via Playwright, runs OSINT research with Tavily, maps candidate strengths against the role, and generates a tailored resume — streamed live to the browser via SSE.

```
LinkedIn URL → [Career Profile Detection] → [OSINT Research]
            → [Alignment Analysis] → [Resume Tailoring] → PDF
```

| Feature | Detail |
|---|---|
| **AI pipeline** | 4-node LangGraph graph with Groq (qwen3-32b, parsed reasoning) |
| **Job fetching** | Playwright headless Chromium with automatic Tavily fallback |
| **Auth** | JWT via HttpOnly cookie · bcrypt · 7-day sessions |
| **PDF export** | 3 resume templates (ATS-safe, Technical, Compact) via ReportLab |
| **Run history** | All pipeline runs persisted to PostgreSQL |

**Stack:** FastAPI · LangGraph · Groq · Playwright · Tavily · PostgreSQL · SQLAlchemy · Docker

[![My Skills](https://skillicons.dev/icons?i=py,fastapi,docker,postgres)](https://skillicons.dev)

---

## Cloud & Kubernetes Projects

### [Microservices Platform on GKE](https://github.com/dev126712/microservice-end-to-end)
GitOps-driven microservices architecture on Google Kubernetes Engine using a three-repo pattern (app code · Helm values · Terraform infra).

| Layer | Tool |
|---|---|
| Cloud & IaC | GCP · GKE · [Terraform](https://github.com/dev126712/micro-service-infra-management) |
| GitOps | ArgoCD · [Helm charts](https://github.com/dev126712/microservice-charts-deployment) |
| CI/CD & Security | GitHub Actions · Trivy (runtime + CI) · Semgrep SAST |
| Ingress | GKE Gateway API (HTTPRoute + ReferenceGrant) |
| Observability | VictoriaMetrics · Grafana · Fluent-bit · VMLogs |
| Secrets | HashiCorp Vault |
| Apps | Flask · Go · Node.js · Redis · PostgreSQL |

[![My Skills](https://skillicons.dev/icons?i=gcp,kubernetes,terraform,githubactions,helm,grafana,redis,postgres,flask,go,nodejs)](https://skillicons.dev)

---

### Three-Tier Application Suite

A fully end-to-end three-tier system split across three repos — app, deployment manifests, and cloud infrastructure.

| Repo | Purpose | Stack |
|---|---|---|
| [dockerized-three-tier-app](https://github.com/dev126712/dockerized-three-tier-app) | CRUD app + CI/CD + DevSecOps pipeline | Express · MongoDB · Docker · Nginx · GitHub Actions |
| [three-tier-architecture-deployment](https://github.com/dev126712/three-tier-architecture-deployment) | Kubernetes manifests, GitOps, multi-env observability | K8s · ArgoCD · Helm · Grafana · VictoriaMetrics · Node Exporter |
| [three-tier-architecture](https://github.com/dev126712/three-tier-architecture) | AWS infrastructure as code | Terraform · AWS |

[![My Skills](https://skillicons.dev/icons?i=kubernetes,docker,terraform,aws,githubactions,grafana,mongodb,express,nginx)](https://skillicons.dev)

---

### Express API Platform

A React/Express/MongoDB full-stack app with end-to-end DevSecOps — from local Docker Compose through Kustomize-based multi-environment GitOps on GKE.

| Repo | Purpose |
|---|---|
| [express-api](https://github.com/dev126712/express-api) | App code · Docker Compose · Prometheus monitoring · Slack alerts · DevSecOps CI |
| [express-api-CD](https://github.com/dev126712/express-api-CD) | Kubernetes manifests with Kustomize overlays (dev / stage / prod) · ArgoCD |
| [express-api-Infrastructure](https://github.com/dev126712/express-api-Infrastructure) | GKE cluster provisioned with Terraform |

[![My Skills](https://skillicons.dev/icons?i=react,express,mongodb,docker,kubernetes,githubactions,prometheus,terraform,gcp)](https://skillicons.dev)

---

## AIOps & AI Projects

![AIOps](https://github.com/dev126712/main_repo_project/blob/16c32485040a15e124205272764a21feaacaff4a/aiops.jpg)

### [AIOps Log Converter 2.0](https://github.com/dev126712/aiops-log-converter2.0)
Production-ready log intelligence pipeline with a full observability stack, ML anomaly detection, and LLM-generated explanations.

- **Ingest:** Loki + Promtail (Docker log collector → structured log store)
- **Detect:** Isolation Forest (scikit-learn) — unsupervised anomaly scoring
- **Explain:** Groq (Llama 3.3 70B) locally, Ollama on a K8s GPU node — provider-agnostic router
- **Store:** MongoDB (anomaly records) · Redis (deduplication cache, LRU eviction)
- **Observe:** Prometheus metrics on every pipeline run · Grafana dashboards pre-provisioned
- **Architecture:** Adapter pattern — cache, storage, and alert backends are swappable without touching pipeline logic

[![My Skills](https://skillicons.dev/icons?i=py,docker,prometheus,grafana,mongodb,redis)](https://skillicons.dev)

---

### [AIOps Log Converter](https://github.com/dev126712/aiops-log-converter)
Original AIOps pipeline — Isolation Forest anomaly detection with Gemini 1.5 Flash explanations, Slack alerting, and a GitHub Actions CI/CD workflow.

[![My Skills](https://skillicons.dev/icons?i=py,docker,githubactions)](https://skillicons.dev)

---

## Platform Engineering

### [Backstage IDP](https://github.com/dev126712/Backstage)
Self-hosted Backstage Internal Developer Portal configured with a software catalog, API registry, software templates, and TechDocs.

- **Software catalog:** Components, APIs, systems, and ownership mapped in YAML
- **API registry:** OpenAPI definitions surfaced in the catalog
- **Software templates:** Scaffolding template for a serverless three-tier app on GCP (with base skeleton and Backstage component registration)
- **TechDocs:** Documentation-as-code integrated into the catalog

[![My Skills](https://skillicons.dev/icons?i=ts,kubernetes,docker)](https://skillicons.dev)

---

## Infrastructure & IaC

### [Terraform Modules](https://github.com/dev126712/terraform-modules)
Reusable, opinionated Terraform modules for GCP and AWS. Designed for composability across the other projects in this portfolio.

[![My Skills](https://skillicons.dev/icons?i=terraform,aws,gcp)](https://skillicons.dev)

---

### [CI/CD Infrastructure](https://github.com/dev126712/cicd)
Terraform-provisioned Jenkins CI/CD stack on AWS — EC2, S3 artifact store, Docker Compose runner, and shell-scripted pipeline helpers.

![CI/CD Diagram](https://github.com/dev126712/cicd/blob/2d79805398c75877537e3484ff48f43334716e04/cicd.png)

[![My Skills](https://skillicons.dev/icons?i=terraform,aws,jenkins,docker,bash)](https://skillicons.dev)

---

*Private repos (KubeAIOps, RecruitFlow) are available for review upon request — reach out on [LinkedIn](https://ca.linkedin.com/in/alexandre-st-fort-7b32681b8).*
