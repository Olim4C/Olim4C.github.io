# Hi there! I'm Camilo | Cloud, DevOps & Platform Engineer 🚀

I am passionate about designing rock-solid, secure, and highly scalable cloud runways. My primary focus goes beyond simply connecting cloud services—I aim to make architectural decisions rooted in the core trade-offs between Security, High Availability, Automation, and FinOps.

Currently, I specialize in enterprise-grade, mission-critical infrastructure and cloud-native ecosystems governed by mature GitOps practices.

---

## 🛠️ Core Technology Stack

| Compute & Orchestration | Infrastructure as Code | CI/CD & GitOps | Networking & Security |
| :--- | :--- | :--- | :--- |
| **Kubernetes (GKE)** | **Terraform** (v5.x+) | **GitHub Actions** | **Zero Trust Architecture** |
| **Docker** | **Terragrunt** (DRY Architecture) | **ArgoCD** (App of Apps) | **Private GKE** (No Public IPs) |
| **Google Cloud (GCP)** | Remote & Versioned Modules | **Jenkins Pipelines** | Cross-Project IAM Binding |

---

## 🚀 Recent Engineering & Featured Projects

### 🏛️ Multi-Project & "Air-Gapped" Corporate Landing Zone (GCP & GitOps)
Designed and implemented a Google Cloud Landing Zone from scratch using a *Hub-and-Spoke* topology to effectively isolate environments and secure the software supply chain.
* **Total Isolation (Zero Trust):** Configured a centralized, dedicated project (`oli-share-environment`) to exclusively host a private **Google Artifact Registry (GAR)**.
* **Internet-Immune Workloads:** Redesigned the cloud infrastructure to eliminate public outbound dependencies (Cloud NAT) for container images. This forces the private GKE cluster to pull base images (such as ArgoCD or Istio) internally via Google's backbone network, significantly mitigating suprosal attacks and lowering data egress costs.
* **Granular Permissions:** Developed custom Service Accounts (`gke-nodes-sa`) with dynamic, batch IAM bindings using Terraform `for_each` loops to securely bridge resources across GCP project boundaries.

### ⚙️ Evolutionary Infrastructure Pipelines (Jenkins ➡️ GitHub Actions)
Automated the full lifecycle of infrastructure management (Plan ➡️ Apply ➡️ Destroy), mapping cloud workflows directly to Git branch lifecycles.
* **Orchestrator Migration:** Translated complex legacy logic from Jenkins Declarative Pipelines into modern, native **GitHub Actions** workflows.
* **Security Guardrails:** Embedded bash-driven logical barriers that strictly prevent accidental modifications or destructive impacts on critical environments (such as Production or Share projects) unless the operator is explicitly on the `main` branch.
* **Team Visibility (SRE Culture):** Captured Terraform outputs using standard Linux utilities (`tee`) and text diffs to automatically inject interactive, collapsible change summaries directly into the GitHub `STEP_SUMMARY` page for peer reviews.

### 🧪 IaC Modularization & Best Practices
* Maintained decoupled Terraform state states stored in isolated remote GCS buckets to significantly reduce the *Blast Radius* during updates.
* Enforced strict immutability rules through dependency lockfiles (`.terraform.lock.hcl`) and semantic version control using Git tags on standalone repositories for Network, IAM, and Compute modules.

---

## 🎯 Current Focus & Next Challenges
* **Efficient Data Architectures:** Deploying self-managed, cost-optimized Big Data clusters using Google Dataproc (leveraging Master-only configurations with zero fixed workers for non-production environments to curb idle spend).
* **Service Mesh:** Implementing advanced internal traffic routing, automated mTLS, and progressive delivery strategies (*Canary/Blue-Green deployments*) using **Istio**.
* **Personal Ventures:** Architecting a cloud-native, microservices-based medical and dental SaaS solution deployed completely through GitOps.

---

## 📈 GitHub Stats

<p align="left">
  <img src="https://github-readme-stats.vercel.app/api?username=Olim4C&show_icons=true&theme=tokyonight&include_all_commits=true&count_private=true" alt="Camilo's GitHub Stats" height="180px"/>
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Olim4C&layout=compact&theme=tokyonight&hide=html,css" alt="Camilo's Top Languages" height="180px"/>
</p>

---

## 🤝 Connect With Me
Are you looking to discuss decoupled cloud architectures, FinOps, Kubernetes scaling, or end-to-end automation? Let's talk!

* **LinkedIn:** [linkedin.com/in/camiloponcecatalan](https://www.linkedin.com/in/camiloponcecatalan/)
* **GitHub:** [github.com/Olim4C](https://github.com/Olim4C)
