# 🚀 Frontend Service — Cloud-Native E-Commerce App

<p align="center">
  <img src="https://media.giphy.com/media/kH1DBkPNyZPOk0BxrM/giphy.gif" width="600" alt="CI/CD Pipeline">
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Frontend-React-blue?style=for-the-badge&logo=react">
  <img src="https://img.shields.io/badge/Docker-Containerized-blue?style=for-the-badge&logo=docker">
  <img src="https://img.shields.io/badge/Azure%20Pipelines-CI/CD-blue?style=for-the-badge&logo=azuredevops">
  <img src="https://img.shields.io/badge/AWS-ECR-orange?style=for-the-badge&logo=amazonaws">
  <img src="https://img.shields.io/badge/Kubernetes-EKS-blue?style=for-the-badge&logo=kubernetes">
  <img src="https://img.shields.io/badge/ArgoCD-GitOps-red?style=for-the-badge&logo=argo">
</p>

---

## 🧠 Project Overview

This repository contains the **frontend** of my production-style MERN e-commerce application.  
It is designed to be containerized with Docker, pushed to **AWS ECR** through **Azure DevOps Pipelines**, and deployed to **Amazon EKS** using a **GitOps workflow with ArgoCD and Helm**.

🔹 application source code is stored in GitHub
🔹 CI is handled by **Azure DevOps Pipelines**
🔹 Docker images are pushed to **AWS Elastic Container Registry (ECR)**
🔹 deployment configuration is stored in a separate **GitOps repository**
🔹 **ArgoCD** watches the GitOps repo and deploys changes to **Amazon EKS**

---

## 🏗️ Architecture Flow

<p align="center">
  <img src="https://media.giphy.com/media/coxQHKASG60HrHtvkt/giphy.gif" width="500">
</p>

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
