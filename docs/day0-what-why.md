# DAY 0 — ENTERPRISE DEVOPS SETUP  
## What We Did, Why We Did It, How to Explain It

---

## 1. Installed WSL2 with Ubuntu on Windows

### What we did
- Enabled WSL2 on Windows 11
- Installed Ubuntu as the Linux distribution
- Created a dedicated Linux user

### Why we did it
- Production systems run on Linux
- DevOps tools behave differently on Windows vs Linux
- WSL2 provides a real Linux kernel with near-native performance
- Avoids dual-boot or heavy virtual machines

### Interview explanation
> “I use Windows as the host OS, but all DevOps work runs inside WSL2 Ubuntu to closely mirror production Linux environments.”

---

## 2. Hardened the Base Ubuntu System

### What we did
- Updated package index and system packages
- Installed essential utilities: git, curl, wget, vim, jq, htop, net-tools, build-essential

### Why we did it
- Ensures security patches are applied
- Provides tooling required for debugging, automation, and scripting
- Prevents future dependency issues

### Interview explanation
> “First thing I do on any new environment is update the OS and install a minimal but sufficient toolchain for debugging and automation.”

---

## 3. Created a Structured DevOps Workspace

### What we did
- Created a dedicated workspace directory
- Segregated areas for Linux, shell, Python, CI/CD, Kubernetes, docs, and virtual environments

### Why we did it
- Separation of concerns
- Improves maintainability and readability
- Scales well as projects grow

### Interview explanation
> “I keep a structured workspace so scripts, manifests, pipelines, and documentation don’t get mixed.”

---

## 4. Set Up Python Using Virtual Environments

### What we did
- Installed Python virtual environment support
- Created a dedicated virtual environment for DevOps work
- Installed core Python packages: FastAPI, requests, PyYAML, click, rich

### Why we did it
- Prevents system-level dependency pollution
- Allows reproducible and isolated environments
- Python is heavily used in DevOps automation and integrations

### Interview explanation
> “I always use virtual environments to isolate dependencies and keep Python environments reproducible.”

---

## 5. Configured Git with Enterprise Standards

### What we did
- Configured global Git username and email
- Set default branch name to `main`

### Why we did it
- Ensures consistency across repositories
- Aligns with modern enterprise Git standards
- Avoids CI/CD and branching inconsistencies

### Interview explanation
> “I standardize Git configuration upfront to align with enterprise branching conventions.”

---

## 6. Installed Docker Using Docker Desktop with WSL2 Integration

### What we did
- Installed Docker Desktop on Windows
- Enabled WSL2 integration for Ubuntu
- Verified Docker CLI inside Ubuntu
- Ran a test container successfully

### Why we did it
- This is the officially supported way to run Docker on Windows
- Docker runs efficiently while exposing Linux-native CLI
- Avoids nested virtualization issues

### Interview explanation
> “On Windows, I use Docker Desktop with WSL2 integration so Docker behaves like a native Linux setup.”

---

## 7. Installed Kubernetes Tooling (kubectl and kind)

### What we did
- Installed kubectl for cluster interaction
- Installed kind for running local Kubernetes clusters
- Created and verified a local Kubernetes cluster

### Why we did it
- Enables realistic Kubernetes testing and debugging
- kind closely mirrors managed Kubernetes clusters
- Lightweight and CI/CD friendly

### Interview explanation
> “I use kind for local Kubernetes testing because it’s lightweight and behaves close to managed clusters.”

---

## 8. Enabled SSH-Based Authentication

### What we did
- Generated SSH key pair
- Prepared for GitHub and server access

### Why we did it
- SSH keys are more secure than passwords
- Industry standard for Git and server access
- Enables automation without credential exposure

### Interview explanation
> “I use SSH keys for secure Git and infrastructure access.”

---

## 9. Enabled Timestamped Shell History

### What we did
- Enabled timestamping in shell command history

### Why we did it
- Improves traceability
- Helps reconstruct actions during incidents
- Useful for auditing and debugging

### Interview explanation
> “I keep timestamped shell history for audit and incident analysis.”

---

## 10. Initialized Git Repository on Day 0

### What we did
- Initialized Git repository for the DevOps workspace
- Committed environment setup

### Why we did it
- Ensures traceability from day one
- Encourages disciplined version control
- Setup scripts are reusable references

### Interview explanation
> “I version even my environment setup so it’s repeatable and auditable.”

---

## 11. Verified End-to-End Environment Health

### What we did
- Verified Docker, Kubernetes, Python, and Git configurations

### Why we did it
- Confirms the environment is production-capable
- Removes environment-related blockers during development

### Interview explanation
> “I always validate the environment end-to-end before starting any serious work.”

---

## FINAL OUTCOME OF DAY 0

- Enterprise-grade Linux DevOps workstation
- Docker + Kubernetes ready
- Python isolated and reproducible
- Git-disciplined workflow
- Interview-ready explanations

---

## END OF DAY 0 — WHAT & WHY

