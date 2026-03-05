# devops-gitops-demo

Demo project presenting a simple DevOps workflow using:

* GitHub Actions (CI/CD)
* Docker
* GitHub Container Registry (GHCR)
* Kubernetes
* Terraform (Infrastructure as Code)

---

## Architecture

```
Developer
   │
   ▼
GitHub Repository
   │
   ▼
GitHub Actions CI/CD
   │
   ▼
Docker Image (GHCR)
   │
   ▼
Kubernetes Cluster
   │
   ▼
Cloud Infrastructure (Terraform)
```

---

## Project Components

### Application

Simple containerized application located in:

```
app/
```

Built using Docker.

---

### CI/CD Pipeline

Defined in:

```
.github/workflows/ci.yaml
```

Pipeline steps:

1. Trigger on push to `main`
2. Build Docker image
3. Push image to GitHub Container Registry
4. Make image available for Kubernetes deployment

---

### Container Image

Docker image is built using:

```
Dockerfile
```

Published to:

```
ghcr.io/pumbstyler/devops-gitops-demo:latest
```

---

### Kubernetes Deployment

Kubernetes manifests located in:

```
k8s/
```

Includes:

* Deployment
* Service

---

### Infrastructure as Code

Cloud infrastructure is provisioned using:

```
infra/terraform/
```

Terraform demonstrates how infrastructure can be versioned and reproducible.

---

## DevOps Workflow

```
Developer → GitHub → CI Pipeline → Docker Build → Container Registry → Kubernetes Deployment → Terraform Infrastructure
```

---

## Purpose

This repository demonstrates a simplified DevOps lifecycle including:

* Continuous Integration
* Containerization
* Artifact publishing
* Infrastructure provisioning
* Kubernetes deployment
