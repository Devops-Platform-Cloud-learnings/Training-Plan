# DevOps · Cloud · Platform Engineering
## 3-Month Training Program — Detailed Plan

---

## Program Summary

| Item | Details |
|------|---------|
| **Duration** | 12 Weeks (3 Months) |
| **Target Audience** | Freshers / Students (CS, IT, ECE graduates) |
| **Daily Hours** | ~8 hours/day (theory + labs) |
| **Format** | Instructor-led + Hands-on labs + Projects |
| **Certification** | Certificate of Completion (on passing 70%+) |

---

## Phases Overview

| Phase | Duration | Focus |
|-------|----------|-------|
| Phase 1 | Month 1 (Weeks 1–4) | Foundations — Linux, Git, Python, Docker |
| Phase 2 | Month 2 (Weeks 5–9) | CI/CD, Cloud, Terraform, Kubernetes |
| Phase 3 | Month 3 (Weeks 10–12) | Platform Engineering, GitOps, Capstone |

---

## Phase 1 — Foundations (Month 1)

### Week 1: Linux & Bash Scripting

**Learning Objectives:**
- Navigate the Linux filesystem confidently
- Write Bash scripts to automate repetitive tasks
- Manage users, permissions, and processes

**Topics:**
- Linux architecture overview (kernel, shell, filesystem hierarchy)
- Essential commands: `ls`, `cd`, `grep`, `awk`, `sed`, `find`, `chmod`, `chown`
- File permissions (rwx), users and groups
- Shell scripting: variables, loops, conditionals, functions
- Cron jobs and task scheduling
- Process management: `ps`, `kill`, `top`, `systemctl`
- Package management: `apt`, `yum`

**Lab Exercises:**
1. Write a Bash script to automate system health checks (disk, CPU, memory)
2. Create a user management script with error handling
3. Schedule a log rotation script using cron

**Resources:** Linux Foundation materials, `man` pages, tldr.sh

---

### Week 2: Git & Python for DevOps

**Learning Objectives:**
- Use Git for version control in team environments
- Write Python scripts to automate infrastructure tasks

**Topics (Git):**
- Git internals: commits, branches, staging area
- Branching strategies: GitFlow, trunk-based development
- Merge vs. rebase
- Pull requests, code reviews, conflict resolution
- GitHub/GitLab workflows

**Topics (Python):**
- Python basics: data types, loops, functions, modules
- File I/O and JSON/YAML parsing
- subprocess module to run shell commands
- Requests library for HTTP/API calls
- boto3 basics (AWS SDK preview)

**Lab Exercises:**
1. Simulate a GitFlow workflow with feature branches and PRs
2. Write a Python script to parse a YAML config and provision mock resources
3. API automation script: call a REST API and save results to JSON

---

### Week 3: Networking & Security Basics

**Learning Objectives:**
- Understand how networks underpin cloud infrastructure
- Apply basic security concepts in DevOps contexts

**Topics:**
- OSI model, TCP/IP stack
- IP addressing, CIDR notation, subnets
- DNS resolution flow
- HTTP/HTTPS, TLS/SSL basics
- Firewalls, Security Groups, NACLs
- SSH key-based authentication
- VPN fundamentals
- Common ports and protocols

**Lab Exercises:**
1. Configure SSH key pairs and secure a VM
2. Trace a DNS lookup using `dig` and `nslookup`
3. Analyze network traffic with `tcpdump` / Wireshark basics

---

### Week 4: Docker & Containerisation

**Learning Objectives:**
- Understand containers vs virtual machines
- Build, ship, and run Docker containers
- Orchestrate multi-service apps with Docker Compose

**Topics:**
- Container concepts: namespaces, cgroups, images, layers
- Writing Dockerfiles (multi-stage builds, best practices)
- Docker CLI: build, run, exec, logs, inspect
- Docker image optimization
- Docker Hub / private registries
- Docker Compose: services, volumes, networks
- Container networking modes

**Lab Exercises:**
1. Dockerise a Node.js / Python Flask app
2. Multi-stage Docker build to minimize image size
3. Docker Compose for a 3-tier app (web + API + database)

**Phase 1 Mini Project:** Containerised Python web app with Bash automation scripts, version-controlled in Git with a proper branching strategy.

---

## Phase 2 — Core DevOps & Cloud (Month 2)

### Week 5–6: CI/CD Pipelines

**Learning Objectives:**
- Design and implement CI/CD pipelines end-to-end
- Use GitHub Actions for real-world pipelines

**Topics:**
- CI/CD principles: why, what, how
- Pipeline stages: source → build → test → artifact → deploy
- GitHub Actions: workflow YAML, jobs, steps, actions
- Reusable workflows, matrix builds, secrets
- Artifact management (Nexus, JFrog, ECR)
- Pipeline best practices: fail fast, parallel stages, rollback

**Lab Exercises:**
2. GitHub Actions workflow: lint → test → build → deploy to staging
3. Implement automated rollback on deployment failure

---

### Week 7–8: Cloud Platforms & Infrastructure as Code

**Learning Objectives:**
- Provision and manage cloud resources on AWS and Azure
- Write Terraform code to automate infrastructure

**Topics (Cloud):**
- AWS core services: EC2, S3, RDS, VPC, IAM, ELB, Auto Scaling, ECR, EKS
- Azure equivalents: VMs, Blob Storage, AKS, Azure DevOps, RBAC
- Cloud networking: VPC, subnets, route tables, NAT gateway
- IAM: roles, policies, least privilege principle
- Cost management basics

**Topics (IaC):**
- Terraform concepts: providers, resources, state, plan/apply/destroy
- HCL syntax, variables, outputs, locals
- Terraform modules (reusable components)
- Remote state with S3/Azure Blob
- Ansible: playbooks, roles, inventory, variables
- Ansible vs Terraform: when to use which

**Lab Exercises:**
1. Provision a full VPC with public/private subnets, EC2, RDS using Terraform
2. Write Ansible playbook to configure and harden an EC2 instance
3. Terraform module for a reusable EKS cluster

---

### Week 9: Kubernetes

**Learning Objectives:**
- Understand Kubernetes architecture and components
- Deploy, scale, and manage applications on K8s

**Topics:**
- K8s architecture: control plane (API Server, etcd, scheduler, controller manager), worker nodes (kubelet, kube-proxy)
- Core objects: Pod, ReplicaSet, Deployment, Service (ClusterIP, NodePort, LoadBalancer), Ingress
- ConfigMaps and Secrets
- Persistent Volumes and Persistent Volume Claims
- Namespaces and RBAC
- Horizontal Pod Autoscaler (HPA)
- Rolling updates and rollbacks
- Helm: charts, values, templates, repositories
- kubectl commands mastery

**Lab Exercises:**
1. Deploy a microservices app to a local K8s cluster (minikube/kind)
2. Configure HPA and test autoscaling under load
3. Package an app as a Helm chart and deploy to multiple environments

**Week 9 also covers:** Monitoring basics — Prometheus + Grafana setup, alerting rules, dashboards

**Phase 2 Mini Project:** Full CI/CD pipeline that builds a Docker image, pushes to ECR, provisions EKS with Terraform, and deploys via Helm chart.

---

## Phase 3 — Platform Engineering (Month 3)

### Week 10: Platform Engineering & IDPs

**Learning Objectives:**
- Understand the Internal Developer Platform (IDP) concept
- Build self-service capabilities for development teams

**Topics:**
- Platform Engineering vs. DevOps mindset
- What is an IDP? Golden paths, self-service, paved roads
- Backstage by Spotify: setup, plugins, service catalogue, scaffolding templates
- Platform APIs and developer experience (DevEx)
- Standardizing deployment workflows
- Template-driven onboarding for new services

**Lab Exercises:**
1. Set up a Backstage developer portal with service catalogue
2. Create a Backstage scaffolding template for a new microservice
3. Integrate Backstage with GitHub and Kubernetes

---

### Week 11: GitOps, Observability & Security

**Learning Objectives:**
- Implement GitOps workflows with ArgoCD
- Build a production observability stack
- Apply DevSecOps practices

**Topics (GitOps):**
- GitOps principles: Git as single source of truth
- ArgoCD: installation, app-of-apps pattern, sync policies, drift detection
- Flux CD overview
- Progressive delivery: canary, blue-green with ArgoCD Rollouts

**Topics (Observability):**
- The three pillars: Metrics, Logs, Traces
- Prometheus: scrape configs, PromQL, alerting rules
- Grafana: dashboards, alertmanager integration
- EFK stack: Elasticsearch + Fluentd + Kibana (or Loki)
- Jaeger / OpenTelemetry for distributed tracing

**Topics (DevSecOps):**
- Shift-left security: SAST (Semgrep, SonarQube) in pipelines
- Container image scanning: Trivy, Snyk
- Secrets management: HashiCorp Vault
- Policy as Code: OPA/Gatekeeper for K8s
- DAST basics

**Lab Exercises:**
1. ArgoCD app-of-apps deployment across dev/staging/prod
2. Full observability stack: instrument an app, visualize in Grafana
3. Integrate Trivy image scanning into a CI/CD pipeline

---

### Week 12: Capstone Project

**Project Goal:** Build and document a production-ready DevOps platform from scratch.

**Deliverables:**

1. **Infrastructure (Terraform)**
   - Cloud environment with VPC, subnets, security groups
   - Managed Kubernetes cluster (EKS or AKS)
   - Container registry, object storage

2. **Application (Containerised)**
   - Dockerised 3-tier application
   - Multi-stage optimized Docker builds

3. **CI/CD Pipeline (GitHub Actions)**
   - Lint → Test → Build → Push → Deploy stages
   - Environment-specific deployments (dev/staging/prod)

4. **Kubernetes Deployment (Helm)**
   - Helm chart with configurable values per environment
   - HPA, resource limits/requests

5. **GitOps (ArgoCD)**
   - ArgoCD app syncing from Git
   - Automated sync with manual prod approvals

6. **Observability**
   - Prometheus metrics + Grafana dashboards
   - Centralized logging

7. **Documentation**
   - Architecture diagram (draw.io / Miro)
   - Runbook for common operations
   - README with setup instructions

**Presentation:** 15-minute demo + Q&A to panel of trainers

---

## Assessment Framework

| Component | Weight | Description |
|-----------|--------|-------------|
| Weekly Quizzes | 15% | MCQ + short answer, end of each week |
| Lab Assignments | 25% | Graded lab tasks per module |
| Phase 1 Mini Project | 15% | Containerised app + automation |
| Phase 2 Mini Project | 15% | CI/CD + Cloud + K8s pipeline |
| Capstone Project | 30% | Full platform build + presentation |
| **Total** | **100%** | Passing score: **70%** |

---

## Daily Schedule

| Time | Activity |
|------|----------|
| 09:00 – 10:30 | Concept Session (theory + slides) |
| 10:30 – 10:45 | Break |
| 10:45 – 12:30 | Hands-On Lab (guided exercises) |
| 12:30 – 13:30 | Lunch |
| 13:30 – 15:00 | Tool Deep Dive / Demo |
| 15:00 – 15:15 | Break |
| 15:15 – 16:30 | Project Work (self-paced, mentor available) |
| 20:30 – 21:30 | Daily Standup (doubts, review, preview) |

---

## Tools & Technologies Covered

| Category | Tools |
|----------|-------|
| OS / Shell | Linux (Ubuntu), Bash, Zsh |
| Version Control | Git, GitHub, GitLab |
| Scripting | Python 3, Bash |
| Containers | Docker, Podman, Docker Compose |
| CI/CD | GitHub Actions, GitLab CI |
| Cloud | AWS (EC2, S3, EKS, VPC, IAM), Azure (AKS, VMs, DevOps) |
| IaC | Terraform, Ansible |
| Orchestration | Kubernetes, Helm, Kustomize |
| GitOps | ArgoCD, Flux |
| Observability | Prometheus, Grafana, EFK/Loki, Jaeger |
| Platform | Backstage, Port |
| Security | Vault, Trivy, Semgrep, OPA/Gatekeeper |
| Registries | Docker Hub, AWS ECR, Harbor |
| Editors | VS Code + DevOps extensions |

---

## Trainer Recommendations

- Keep batch size between 15–20 students for effective lab support
- Provide cloud sandbox accounts per student (AWS Free Tier or Azure for Students)
- Use local Kubernetes clusters (minikube, kind) for early practice, move to managed clusters in Phase 2
- Set up a shared GitHub organization for collaboration
- Weekly retrospectives help course-correct early
- Encourage students to document their learnings in a personal blog/wiki

---

## Post-Training Career Paths

- **Junior DevOps Engineer** → CI/CD, Docker, basic cloud
- **Cloud Engineer** → AWS/Azure deep-dive, certifications (AWS Solutions Architect, AZ-900/AZ-104)
- **SRE (Site Reliability Engineer)** → Observability, incident management, SLOs
- **Platform Engineer** → IDP, Backstage, developer experience
- **Recommended Certifications:** CKA (Kubernetes), AWS SAA, Terraform Associate, GitLab CI/CD Associate

---

*Training Plan v1.0 — 3-Month DevOps · Cloud · Platform Engineering Program*
