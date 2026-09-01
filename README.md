# Hi, I'm Haani 👋

DevOps Engineer based in Scotland, focused on AWS, Kubernetes, infrastructure as code, and CI/CD automation.

I build production-grade infrastructure from scratch, then debug it until I understand every piece. Below are my two main projects.

---

### 🚀 Production-Grade AWS Deployment Pipeline
Docker-containerised application deployed to **AWS ECS Fargate** behind an Application Load Balancer.

- Infrastructure provisioned as code with **Terraform** (VPC across 3 AZs, ALB, ECS, ACM), S3 remote backend with DynamoDB state locking
- CI/CD automated through **GitHub Actions** using **OIDC** — no long-lived AWS credentials
- IAM scoped from `AdministratorAccess` down to ~90 explicit, resource-locked actions using CloudTrail analysis
- HTTPS via ACM, custom domain delegated from Cloudflare to Route 53
- Multi-stage Docker build reducing image size from 234MB → 88MB
- Idempotent Bash setup script parameterising the whole stack from 4 inputs, redeployable to any AWS account

[View repo →](https://github.com/akhihaani/production-grade-aws-deployment)

---

### ☸️ Memos Notes App on AWS EKS
Containerised notes app deployed on **Amazon EKS** with full GitOps delivery.

- **GitOps with ArgoCD** — image tag commits trigger auto-sync and self-healing deployments
- Infrastructure organised with **Terraform + Terragrunt** (DRY modules, native S3 state locking)
- Security-gated CI pipeline: **Checkov** (infra scanning) + **Trivy** (container scanning), fails build on CRITICAL/HIGH findings
- Automated TLS and DNS via **cert-manager** + **ExternalDNS**, scoped through IRSA
- Monitoring with **kube-prometheus-stack** (Prometheus + Grafana), custom dashboards
- Keyless CI via GitHub OIDC with a hand-written least-privilege IAM policy

[View repo →](https://github.com/akhihaani/production-grade-eks-helm-deployment)

---

### 🛠️ Core Stack
![AWS](https://img.shields.io/badge/AWS-%23FF9900.svg?style=for-the-badge&logo=amazon-aws&logoColor=white)
![Terraform](https://img.shields.io/badge/Terraform-%235835CC.svg?style=for-the-badge&logo=terraform&logoColor=white)
![Kubernetes](https://img.shields.io/badge/Kubernetes-%23326CE5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-%232496ED.svg?style=for-the-badge&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-%232088FF.svg?style=for-the-badge&logo=github-actions&logoColor=white)
![ArgoCD](https://img.shields.io/badge/ArgoCD-%23EF7B4D.svg?style=for-the-badge&logo=argo&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-%234EAA25.svg?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Prometheus](https://img.shields.io/badge/Prometheus-%23E6522C.svg?style=for-the-badge&logo=prometheus&logoColor=white)
![Grafana](https://img.shields.io/badge/Grafana-%23F46800.svg?style=for-the-badge&logo=grafana&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-%23FCC624.svg?style=for-the-badge&logo=linux&logoColor=black)

### 📫 Let's Connect
[LinkedIn](https://www.linkedin.com/in/abu-niyyah/) · akhihaani@gmail.com
