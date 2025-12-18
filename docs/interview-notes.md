# ENTERPRISE DEVOPS — DAY 0 INTERVIEW NOTES
Rajesh Panda

---

## 1. Why do you use Linux for DevOps work?

**Answer:**
Linux is the de-facto production OS for most enterprise systems. Using Linux locally ensures that process management, filesystem behavior, networking, permissions, and debugging workflows closely match production environments. This reduces surprises during deployments and incidents.

---

## 2. How do you do DevOps work on a Windows laptop?

**Answer:**
I use Windows only as the host OS and run all DevOps work inside WSL2 with Ubuntu. This provides a real Linux kernel with near-native performance. Tools like Docker, Kubernetes CLI, Git, and Python run inside Ubuntu, closely mirroring production systems.

---

## 3. Why WSL2 instead of dual boot or virtual machines?

**Answer:**
WSL2 provides a real Linux kernel without the overhead of managing a full virtual machine. It offers better filesystem integration, faster startup, and seamless networking while still behaving like a production Linux environment.

---

## 4. How does Docker work on Windows with WSL2?

**Answer:**
Docker runs via Docker Desktop on the Windows side, and the Docker CLI is exposed inside WSL2. This allows me to use Docker commands natively in Linux while Docker Desktop manages the daemon, networking, and resources.

---

## 5. How do you verify Docker is working correctly?

**Answer:**
I check the Docker version and run a test container such as `hello-world` to confirm that the CLI can communicate with the daemon, pull images, create containers, and stream logs correctly.

---

## 6. Why do you use virtual environments for Python?

**Answer:**
Virtual environments isolate dependencies per project, prevent system-level conflicts, and ensure reproducibility. This is critical in DevOps where Python is used for automation, APIs, CI/CD tooling, and integrations.

---

## 7. What Python use cases do you have in DevOps?

**Answer:**
I use Python for infrastructure automation, writing CLI tools, building internal APIs with FastAPI, interacting with cloud and Kubernetes APIs, and integrating AI or monitoring systems.

---

## 8. Why did you structure your workspace into multiple directories?

**Answer:**
I separate concerns such as Linux scripts, shell automation, Python code, CI/CD pipelines, Kubernetes manifests, and documentation. This keeps the workspace maintainable, scalable, and easy to navigate in large projects.

---

## 9. Why did you configure Git default branch as `main`?

**Answer:**
`main` is the enterprise standard across most organizations now. Setting it globally avoids inconsistencies, aligns with CI/CD pipelines, and ensures repositories follow modern conventions.

---

## 10. Why do you initialize Git even for personal or setup projects?

**Answer:**
Version control ensures traceability, allows rollback, and enforces discipline. Even environment setup scripts can be valuable references during audits, interviews, or future automation.

---

## 11. How do you practice Kubernetes locally?

**Answer:**
I use `kind`, which runs Kubernetes clusters inside Docker containers. It is lightweight, fast, and closely mirrors real Kubernetes behavior, making it ideal for local testing and troubleshooting.

---

## 12. Why `kind` instead of Minikube?

**Answer:**
`kind` integrates directly with Docker, is simpler to automate, and behaves closer to managed Kubernetes clusters. It is also easier to use in CI pipelines.

---

## 13. How do you verify a Kubernetes cluster is healthy?

**Answer:**
I check node status using `kubectl get nodes`, verify system pods in the `kube-system` namespace, and ensure networking and DNS pods are running correctly.

---

## 14. Why do you use SSH keys instead of passwords?

**Answer:**
SSH keys are more secure, eliminate password-based attacks, and allow controlled access management. They are standard for Git, servers, and CI/CD systems.

---

## 15. Why do you keep timestamped shell history?

**Answer:**
Timestamped history helps with auditing, troubleshooting, and reconstructing actions during incidents. It also improves accountability and traceability.

---

## 16. What tools do you install first on a new Linux system?

**Answer:**
I install Git, curl, wget, vim, jq, htop, networking tools, and build essentials. These enable debugging, automation, API inspection, and system monitoring.

---

## 17. How do you approach debugging a slow Linux system?

**Answer:**
I start with system-level checks: load average, CPU, memory, disk usage, and IO wait. Then I identify top resource-consuming processes before looking at application-level issues.

---

## 18. How do you ensure your local setup mirrors production?

**Answer:**
By using Linux, Docker, Kubernetes, isolated Python environments, and structured repositories. I avoid OS-specific shortcuts and always test workflows end-to-end.

---

## 19. How does this Day 0 setup help in real projects?

**Answer:**
It removes environment-related friction, enables faster onboarding, improves reliability, and allows me to focus on solving real problems instead of tooling issues.

---

## 20. How would you explain your DevOps setup to a new team?

**Answer:**
I’d explain that it’s a Linux-first, containerized, Kubernetes-ready environment designed to replicate production behavior, ensure consistency, and support automation and rapid debugging.

---

## END OF DAY 0 INTERVIEW NOTES

