# GitOps Workflow using ArgoCD and Kubernetes

## Project Overview

Implemented a GitOps-based deployment workflow using ArgoCD and Kubernetes, where application deployment configurations are maintained in GitHub and automatically synchronized with a Kubernetes cluster.

The project demonstrates how Git acts as the single source of truth for Kubernetes application state.

---

## Architecture
Developer
    |
    |
Git Commit & Push
    |
    |
GitHub Repository
    |
    |
ArgoCD
    |
    |
Kubernetes Cluster (Minikube)
    |
    |
Nginx Application


---

## Tools Used

- Kubernetes
- Minikube
- ArgoCD
- Docker
- GitHub
- kubectl

---

## Implementation Steps

### 1. Kubernetes Cluster Setup

Created a local Kubernetes cluster using Minikube.

### 2. ArgoCD Installation

Installed ArgoCD inside Kubernetes and configured access through the ArgoCD dashboard.

### 3. Application Deployment Manifests

Created Kubernetes declarative manifests:
k8s/
 ├── deployment.yaml
 └── service.yaml

 
The deployment runs an Nginx application with configurable replicas.

### 4. GitOps Configuration

Connected ArgoCD with the GitHub repository and configured automatic synchronization.

### 5. Automated Deployment Updates

Updated Kubernetes configuration through Git commits.

Example:

Changed replica count: 3 to 5


After pushing changes to GitHub, ArgoCD automatically synchronized the desired state with Kubernetes.

---

## GitOps Workflow

1. Developer modifies Kubernetes manifests.
2. Changes are committed and pushed to GitHub.
3. ArgoCD detects repository changes.
4. ArgoCD synchronizes Kubernetes resources.
5. Application state is automatically updated.

---

## Outcome

Successfully implemented a GitOps pipeline using ArgoCD and Kubernetes with automated deployment synchronization from GitHub.
