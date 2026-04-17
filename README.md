# 🚀 Frontend Service — Cloud-Native E-Commerce App

---

## 🧠 Project Overview

This repository contains the **frontend** of my production-style MERN e-commerce application.  
It is designed to be containerized with Docker, pushed to **AWS ECR** through **Azure DevOps Pipelines**, and deployed to **Amazon EKS** using a **GitOps workflow with ArgoCD and Helm**.

- Application source code is stored in GitHub
- CI is handled by **Azure DevOps Pipelines**
- Docker images are pushed to **AWS Elastic Container Registry (ECR)**
- Deployment configuration is stored in a separate **GitOps repository**
- **ArgoCD** watches the GitOps repo and deploys changes to **Amazon EKS**

---

## 🏗️ Architecture Flow

```text
Frontend Code (GitHub)
        ↓
Azure DevOps Pipeline
        ↓
Validate → Build Docker Image
        ↓
Push Image to AWS ECR
        ↓
Update Helm Values (GitOps Repo)
        ↓
ArgoCD detects change
        ↓
Deploy to AWS EKS 🚀
