# FoxIDs.Assets
This repository contains deployment assets for FoxIDs (Kubernetes, Docker, Azure) and module-specific assets.

## Contents
- `Docker/` - Docker Compose files for images and development plus image documentation.
- `Kubernetes/` - Kubernetes manifests for FoxIDs, ingress, cert-manager issuer, and backing services (MongoDB, PostgreSQL, Redis) including configmaps, secrets, deployments, and PV/PVC examples.
- `Azure/` - ARM templates for provisioning FoxIDs resources (`azuredeploy.json`, `azuredeploy-small.json`).
- `modules/` - Module assets. Currently includes `modules/nemlogin` with certificates, metadata, and integration test reports.
