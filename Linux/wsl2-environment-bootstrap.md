# WSL2 Environment Bootstrap & Toolchain Verification

This document logs the core toolchain setup and verification for the WSL2 (Ubuntu 22.04 LTS) environment, including tool installation methods, verified output versions, and operational contexts for Site Reliability Engineering (SRE).

---

##  Toolchain Checklist

### 1. `curl`
* **Install Method:** Standard Package Manager (`sudo apt install -y curl`)
* **Verified Version:** `curl 8.5.0 (x86_64-pc-linux-gnu)`
* **Why it exists in an SRE's kit:** `curl` is an indispensable command-line tool for transferring data with URL syntax and probing network endpoints. SREs rely heavily on `curl` to test REST APIs, verify HTTP response status codes and headers, execute health-check scripts, and troubleshoot network connectivity issues across distributed microservice architectures.

### 2. `git`
* **Install Method:** Standard Package Manager (`sudo apt install -y git`)
* **Verified Version:** `git version 2.43.0`
* **Why it exists in an SRE's kit:** `git` is the foundation of version control and GitOps workflows. SREs use `git` to version-control Infrastructure as Code (IaC) repositories, manage application configurations, write operational runbooks, and audit changes across production environments to ensure system stability and trace outage causes.

### 3. `openssl`
* **Install Method:** Standard Package Manager (`sudo apt install -y openssl`)
* **Verified Version:** `OpenSSL 3.0.13 30 Jan 2024`
* **Why it exists in an SRE's kit:** `openssl` provides robust cryptography and TLS/SSL certificate management tools. In SRE practice, it is crucial for inspecting and verifying SSL/TLS certificates, testing secure TLS handshakes, generating cryptographic key pairs, and diagnosing connection security failures across services.

### 4. `jq`
* **Install Method:** Standard Package Manager (`sudo apt install -y jq`)
* **Verified Version:** `jq-1.7`
* **Why it exists in an SRE's kit:** `jq` is a flexible command-line JSON processor. Because modern cloud APIs, Kubernetes outputs, and structured application logs heavily rely on JSON, `jq` allows SREs to rapidly query, slice, filter, and transform raw JSON streams during active incident response and automated monitoring pipelines.

### 5. `terraform`
* **Install Method:** Official HashiCorp APT Repository
* **Verified Version:** `Terraform v1.5.3 on linux_amd64`
* **Why it exists in an SRE's kit:** `terraform` is the standard Infrastructure as Code (IaC) tool used to declaratively provision and manage multi-cloud infrastructure. SREs utilize Terraform to maintain deterministic, repeatable environments, eliminate manual human configuration errors, manage cloud resources safely, and prevent drift across staging and production clusters.

### 6. `kubectl`
* **Install Method:** Native Binary Download / Kubernetes APT Repository
* **Verified Version:** `Client Version: v1.36.3 (Kustomize Version: v5.8.1)`
* **Why it exists in an SRE's kit:** `kubectl` is the primary command-line tool for interacting directly with the Kubernetes API server. SREs use it continuously to deploy applications, inspect cluster workload status, stream container logs, execute shell sessions into running pods, and troubleshoot containerized application failures.

### 7. `minikube`
* **Install Method:** Direct Binary Installation
* **Verified Version:** `minikube version: v1.38.1`
* **Why it exists in an SRE's kit:** `minikube` provisions a local, single-node Kubernetes cluster directly inside a virtual machine or container on your workstation. SREs use `minikube` as a safe local sandbox to validate deployment manifests, test Helm charts, simulate failure scenarios, and prototype operational tooling before deploying changes to shared staging or production clusters.

### 8. `helm`
* **Install Method:** Official Helm Script / Package Manager
* **Verified Version:** `version.BuildInfo{Version:"v3.21.3"}`
* **Why it exists in an SRE's kit:** `helm` is the package manager for Kubernetes that simplifies the deployment and management of complex Kubernetes applications using reusable templates called charts. SREs rely on Helm to manage application release lifecycles, automate rollbacks during bad deployments, and maintain standardized configuration values across diverse environments.
