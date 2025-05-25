# Microservices App CI/CD Pipeline

## Overview

This repo contains a sample microservices app with CI/CD pipeline setup using:

- GitHub (source code)
- Cloud Build (build & deploy)
- Artifact Registry (Docker images)
- GKE (Kubernetes deployment)
- GitOps style environment namespaces (dev shown here)

---

## How it works

- On push to `main` branch, Cloud Build trigger runs:
  - Builds Docker image
  - Pushes image to Artifact Registry
  - Deploys image to GKE in the `dev` namespace using Kubernetes manifests

---

## Setup instructions

1. Connect this GitHub repo to Cloud Build triggers in GCP Console.
2. Create Artifact Registry Docker repo: `microservices-repo`.
3. Create GKE cluster and configure `kubectl` credentials.
4. Push changes to `main` to trigger CI/CD pipeline.

---

## Kubernetes

Manifests are under `k8s/dev/`. Adjust for `stage` and `prod` as needed.

---
