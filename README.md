# 🛠️ The SRE Playbook

> "Engineering for reliability through automation, observability, and deep-stack troubleshooting."

This repository serves as a central engineering log. It documents technical deep-dives, automated solutions, and architectural patterns encountered while managing high-scale enterprise infrastructure.

---

## 👤 Profile
- **Role:** Site Reliability Engineer (SRE)
- **Location:** Pune, India
- **Mission:** Systematizing the elimination of toil and ensuring 99.99% uptime.
- **Connect:** [LinkedIn](https://www.linkedin.com/in/pranjallll)

---

## 🏗️ Active Modules

### 🧂 [SaltStack](./SaltStack)
*Orchestration & Configuration Management.* Focusing on idempotent state management, secret handling via Pillars, and complex Orchestration runners.

### 🐧 [Linux Administration](./Linux)
*Systems Engineering & Hardening.* Focusing on performance tuning, shell scripting, `systemd` management, and kernel optimization.

### 📈 [Dynatrace](./Dynatrace)
*Observability & AIOps.* Focusing on full-stack monitoring, API-driven automation, and SLO/SLI alerting logic.

### 🌐 [Networking](./Networking)
*Connectivity & Protocols.* Focusing on firewall/NSG debugging, DNS management (A, SRV, CNAME), and OSI Layer analysis.

### 🤖 [Automation](./Automation)
*Eliminating Toil.* Focusing on Python and PowerShell utilities for Infrastructure-as-Code (IaC) and API integrations.

---

## 📂 Repository Structure

```text
/
├── 🧂 SaltStack/          # SLS States, Pillars, and Orchestration logic
├── 🐧 Linux/              # Shell scripts, Kernel tuning, and OS hardening
├── 📈 Dynatrace/          # API scripts, Dashboarding, and Alerting logic
├── 🌐 Networking/         # Connectivity troubleshooting, DNS, and Firewalls
├── 🤖 Automation/         # Python/PowerShell utilities and IaC templates
├── ☁️ Infrastructure/     # Cloud-specific configurations (Azure/AWS)
├── 🛡️ Security/           # Identity management, Patching, and Compliance
└── 📝 Incident-Reports/   # Post-mortems and RCA Case Studies