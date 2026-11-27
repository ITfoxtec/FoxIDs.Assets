# FoxIDs.Assets
This repository contains deployment assets for FoxIDs (Kubernetes, Docker, Azure) and module-specific assets.

The Kubernetes, Docker Compose and Azure examples use FoxIDs and FoxIDs Control 2.34.5. Use your customer ID and pull secret from [FoxIDs releases](https://www.foxids.com/releases) to pull both images. For Docker Compose, run `docker login www.foxids.com --username <customer-id>` and enter the pull secret at the prompt.

The Kubernetes and Docker examples use MongoDB 9.0.8 for new databases. Before reusing an existing volume from an earlier example, check the running MongoDB version and feature compatibility version, take a backup and follow the [MongoDB upgrade procedure](https://www.mongodb.com/docs/manual/release-notes/9.0-upgrade-standalone/).

The full Azure template provisions Standard Azure Cache for Redis 6.0. In Azure public cloud, this requires a tenant that already had Azure Cache for Redis before 1 April 2026. The small Azure template uses in-memory caching. [Microsoft retirement and eligibility dates](https://learn.microsoft.com/en-us/azure/azure-cache-for-redis/cache-whats-new#july-2026).

## Contents
- `Docker/` - Docker Compose files for images and development plus image documentation.
- `Kubernetes/` - Kubernetes manifests for FoxIDs, Gateway API listeners and routes, per-host TLS certificates, cert-manager issuers, and backing services (MongoDB, PostgreSQL, Redis) including configmaps, secrets, deployments, and PV/PVC examples.
- `Azure/` - ARM templates for provisioning FoxIDs resources (`azuredeploy.json`, `azuredeploy-small.json`).
- `modules/` - Module assets. Currently includes `modules/nemlogin` with certificates, metadata, and integration test reports.
