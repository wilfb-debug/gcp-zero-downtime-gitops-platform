# gcp-zero-downtime-gitops-platform
# Zero-Downtime GitOps Platform on Kubernetes

## Overview
This project demonstrates a production-grade GitOps deployment platform using Argo CD and Kubernetes.  
All application changes are delivered declaratively via Git, enabling safe, auditable, and zero-downtime deployments across multiple environments.

## Architecture
### GitOps Control Flow
![GitOps Architecture](diagrams/gitops-architecture.png)

### Multi-Environment Deployment
![Kustomize Environments](diagrams/kustomize-environments.png)

### Zero-Downtime Rollouts
![Zero Downtime](diagrams/zero-downtime-rollout.png)

## Key Concepts Demonstrated
- GitOps with Argo CD (single source of truth)
- Environment separation using Kustomize overlays
- Zero-downtime rolling deployments
- Declarative Kubernetes management
- No direct kubectl access in production

## Repository Structure

## Deployment Flow
1. Developer pushes changes to GitHub
2. Argo CD continuously reconciles cluster state
3. Kubernetes performs rolling updates with no downtime
4. Service ensures traffic is always served

## Environments
- **dev** – rapid iteration and validation
- **staging** – production-like validation before release

## Technologies Used
- Kubernetes
- Argo CD
- Kustomize
- GitHub
- Docker

## Future Improvements
- Deploy platform to Google Kubernetes Engine (GKE)
- Provision infrastructure using Terraform
- Add monitoring and alerting (Prometheus & Grafana)

## GitOps Deployment Proof

### ArgoCD Applications (Dev & Staging)
![ArgoCD Dev](screenshots/argocd/argocd-hello-service-dev.png)
![ArgoCD Staging](screenshots/argocd/argocd-hello-service-staging.png)

### GKE Autopilot Workloads
![GKE Workloads](screenshots/gke/gke-workloads-overview.png)

### hello-service (dev)
![Dev Deployment](screenshots/gke/gke-hello-service-dev-details.png)


## Proof (GitOps in action)

### ArgoCD
![ArgoCD Dev](screenshots/argocd/argocd-dev.png)
![ArgoCD Staging](screenshots/argocd/argocd-staging.png)

### App output
![Dev UI](screenshots/app/dev.png)
![Staging UI](screenshots/app/staging.png)
