# 🛠️ The SRE Playbook

> "Engineering for reliability through automation, observability, and deep-stack troubleshooting."

This repository serves as a central engineering log. It documents technical deep-dives, automated solutions, and architectural patterns encountered while executing a 31-week FAANG-track SRE/DevOps curriculum — from Linux fundamentals through Kubernetes, Terraform, observability, DevSecOps, GitOps, and a full capstone build.

---

## 👤 Profile
- **Role:** Site Reliability Engineer (SRE)
- **Location:** Pune, India
- **Mission:** Systematizing the elimination of toil and ensuring 99.99% uptime.
- **Connect:** [LinkedIn](https://www.linkedin.com/in/pranjallll)

---

## ⚙️ Core Engineering Principles

- **Automate the toil, not the judgment.** Bash and Python automation (`Automation/`) eliminates repetitive operational load so engineering time goes toward decisions systems can't make on their own.
- **Least privilege, everywhere.** From scoped `sudoers` entries and `chmod 770` up through IAM policy JSON and Vault-issued short-lived database credentials, every access grant is scoped to the minimum required and expires by default.
- **Idempotency is non-negotiable.** Ansible playbooks, Terraform plans, and Kubernetes reconciliation loops must converge to the same end state no matter how many times they run.
- **Reliability is a measured target, not a feeling.** SLIs/SLOs and multi-window burn-rate alerting replace gut-feel uptime claims with error budgets and paged, actionable thresholds.
- **Postmortems are blameless and written down.** `Incident-Reports/` exists because every production failure is a documented, shareable lesson — not a hallway conversation.
- **Prove resilience, don't assume it.** Chaos engineering and circuit-breaker patterns validate that failure modes degrade gracefully instead of cascading.

---

## 🏗️ Active Modules

### 🧂 [SaltStack](./SaltStack)
*Orchestration & Configuration Management.* Idempotent state management, secret handling via Pillars, and complex Orchestration runners.

### 🐧 [Linux](./Linux)
*Systems Engineering & Hardening.* CLI/FHS navigation, permissions & package management, process internals, `/proc`, storage, and `systemd`.

### 📈 [Dynatrace](./Dynatrace)
*Observability & AIOps.* Full-stack monitoring, API-driven automation, and SLO/SLI alerting logic.

### 🌐 [Networking](./Networking)
*Connectivity & Protocols.* OSI Layer analysis, subnetting, PKI/TLS certificate chains, and DNS resolution.

### 🛡️ [Security](./Security)
*Identity, Secrets & Compliance.* DevSecOps practices and dynamic secret management with HashiCorp Vault.

### 🤖 [Automation](./Automation)
*Eliminating Toil.* Bash/Python scripting fundamentals (`basics/`), AWS SDK tooling (`boto3/`), systems automation & Ansible (`systems/`), and automated test suites (`tests/`).

### ☁️ [Infrastructure](./Infrastructure)
*Cloud-Specific Configurations.* AWS VPC networking, EC2/compute & IAM, storage & serverless, and Terraform IaC.

### 🐳 [Containers](./Containers)
*Container Runtime Fundamentals.* Linux namespaces, cgroups, image builds, Docker networking, and Compose multi-service stacks — the runtime layer beneath Kubernetes.

### ☸️ [Kubernetes](./Kubernetes)
*Container Orchestration.* Raw manifests, Helm charts, ArgoCD GitOps delivery, and Istio service mesh.

### 🔭 [Observability](./Observability)
*Full-Stack Visibility.* Prometheus metrics, Grafana dashboards, Loki logs, OpenTelemetry tracing, and eBPF kernel-level diagnostics.

### 🔁 [CI-CD](./CI-CD)
*Delivery Pipelines.* GitHub Actions workflows and Jenkins multi-node pipeline configurations, including image scanning and signing.

### 🧩 [System-Design](./System-Design)
*Non-Abstract Large System Design (NALSD).* Capacity planning, reliability patterns, multi-region disaster recovery, and FAANG-style interview drills.

### 🏗️ [Capstone](./Capstone)
*End-to-End Synthesis Project.* Terraform + EKS provisioning, GitOps delivery, full-stack observability, and Chaos Mesh fault injection — every prior module integrated into one system.

### 📝 [Incident-Reports](./Incident-Reports)
*Post-mortems and RCA Case Studies.* USE/RED diagnostic frameworks and blameless postmortem write-ups.

---

## 📂 Repository Structure

```text
/
├── 🧂 SaltStack/          # SLS States, Pillars, and Orchestration logic
├── 🐧 Linux/              # CLI navigation, permissions, /proc, systemd, kernel hardening
├── 📈 Dynatrace/          # API scripts, Dashboarding, and Alerting logic
├── 🌐 Networking/         # OSI analysis, subnetting, PKI/TLS, DNS
├── 🛡️ Security/           # DevSecOps, Vault dynamic secrets, compliance
├── 🤖 Automation/         # Python/Bash utilities and IaC helpers
│   ├── basics/            # Shell scripting, grep/sed/awk, defensive Bash
│   ├── boto3/             # AWS SDK automation scripts
│   ├── systems/           # Python infra automation, Ansible
│   └── tests/             # unittest/pytest suites for automation code
├── ☁️ Infrastructure/     # Cloud-specific configurations (AWS)
│   ├── VPC/                # Subnets, route tables, NAT/IGW, security groups
│   ├── Compute/             # EC2, AMIs, Auto Scaling, Load Balancers, IAM
│   ├── Storage/            # S3, EBS, EFS, Lambda, API Gateway
│   └── Terraform/          # State management, modules, provisioning
├── 🐳 Containers/         # Docker runtime fundamentals
│   ├── docker/              # Namespaces, cgroups, image builds
│   └── compose/             # Multi-container orchestration & networking
├── ☸️ Kubernetes/         # Container orchestration
│   ├── manifests/           # Core workloads, storage, ingress, RBAC, autoscaling
│   ├── helm/                 # Helm charts
│   ├── argocd/               # GitOps Application CRDs & sync policies
│   └── istio/                # Service mesh, mTLS, traffic splitting
├── 🔭 Observability/      # Full-stack monitoring & diagnostics
│   ├── prometheus/          # Metrics, PromQL, SLO burn-rate alerting
│   ├── grafana/               # Dashboards
│   ├── loki/                  # Log aggregation
│   ├── otel/                  # Distributed tracing
│   └── ebpf/                  # Kernel-level visibility, bpftrace, flame graphs
├── 🔁 CI-CD/              # Delivery pipelines
│   ├── github-actions/      # Workflows, Trivy scanning, Cosign image signing
│   └── jenkins/               # Multi-node pipeline configs
├── 🧩 System-Design/      # NALSD capacity planning & reliability patterns
├── 🏗️ Capstone/           # End-to-end integration project (Weeks 28–29)
└── 📝 Incident-Reports/   # Post-mortems and RCA Case Studies
```
