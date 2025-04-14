# 🚀 Kubernetes Minikube Deployment

This project demonstrates how to build a Kubernetes cluster locally using **Minikube** and deploy a simple **NGINX application**.

## 🛠 Tools Used

- Minikube
- kubectl
- Docker
- EC2 Ubuntu Instance

## 📦 What’s Inside

- `deployment.yaml` - Kubernetes Deployment configuration for the NGINX app  
- `service.yaml` - NodePort Service to expose the app  
- Sample commands to interact with the cluster

## ⚙️ Steps to Run

### 1. Install Prerequisites

- Docker
- Minikube
- kubectl
- cri-dockerd (for none driver)
- container networking plugins

### 2. Start Minikube

```bash
minikube start --driver=none
Make sure Docker and required plugins are set up properly.
