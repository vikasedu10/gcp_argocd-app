# 🚀 Hello-World Helm Chart

This repository contains a simple **Helm chart** used to deploy a sample "Hello World" web application on a **Google Kubernetes Engine (GKE)** cluster.  
It is also integrated with **Argo CD** for GitOps-based continuous delivery.

---

## 🧱 Repository Structure
   ```.
├── Chart.yaml # Helm chart metadata
├── values.yaml # Default configuration values
├── templates/
│ ├── deployment.yaml # Kubernetes Deployment
│ ├── service.yaml # Service exposing the app
│ ├── configmap.yaml # Example ConfigMap
│ ├── secret.yaml # Example Secret
│ └── _helpers.tpl # Helm helper templates
└── README.md # This file
```
---

## ⚙️ Prerequisites

- A running **GKE cluster** (created via Terraform)
- **kubectl** configured to access the cluster
- **Helm v3+**
- **Argo CD** installed in the cluster
- (Optional) **nginx-ingress** controller for external access

---

## 🚢 Deploying with Helm (Manually)

1. **Add and update repositories** (if needed):

   ```bash
   helm repo add stable https://charts.helm.sh/stable
   helm repo update
