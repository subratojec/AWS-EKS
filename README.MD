# 🎮 2048 Game Deployment on AWS EKS with Fargate & ALB Ingress

A hands-on DevOps project demonstrating real-world Kubernetes deployment using **Amazon EKS**, **Fargate**, **Helm**, and the **AWS ALB Ingress Controller**. The goal is to deploy a containerized 2048 game application with fully managed infrastructure — no EC2 nodes, minimal manual setup, and production-grade networking.

---

## 📌 What This Project Covers

Through this project, I’ve successfully implemented and learned the following DevOps concepts and tools:

### ✅ EKS Cluster Creation Using `eksctl`
- Provisioned an EKS cluster with **Fargate** for serverless pod execution.
- Used `eksctl` for declarative and quick setup of cluster resources (VPC, subnets, etc.).

### ✅ Kubernetes Workload Management
- Defined and deployed:
  - A **Namespace** for isolating the app.
  - A **Deployment** with 5 replicas pulling from a public ECR image.
  - A **NodePort Service** to expose the deployment internally.
  - An **Ingress** resource with ALB annotations to route traffic externally.

### ✅ AWS Fargate for Serverless Kubernetes
- Avoided the complexity of node group management.
- Let AWS Fargate automatically assign compute resources for each pod.

### ✅ ALB Ingress Controller Integration
- Installed the **AWS ALB Ingress Controller** using **Helm**.
- Configured **IAM OIDC Provider** and attached a custom **IAM policy** to the controller’s service account.
- Used Ingress annotations to create a **public-facing ALB** that routes to the 2048 app.

### ✅ Helm for Kubernetes Add-ons
- Leveraged **Helm** to install and manage the ALB Controller cleanly and efficiently.

### ✅ IAM & Security Configuration
- Created IAM roles and attached policies using AWS CLI.
- Understood how OIDC allows EKS to securely use AWS IAM roles inside pods.

---

## 🛠️ Tools & Technologies Used

| Tool/Service | Purpose |
|--------------|---------|
| `kubectl` | Manage Kubernetes workloads |
| `eksctl` | Provision EKS clusters |
| `helm` | Install and manage K8s add-ons |
| `awscli` | Manage AWS services (IAM, EKS, VPC) |
| AWS EKS | Managed Kubernetes cluster |
| AWS Fargate | Serverless container compute engine |
| AWS ALB Controller | Ingress controller to expose apps externally |

---

![2048(1)](https://github.com/user-attachments/assets/cad7f525-8c83-4496-b0a6-b53019f80c7a)

