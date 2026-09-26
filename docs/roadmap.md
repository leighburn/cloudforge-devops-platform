# Roadmap

![Roadmap](../diagrams/roadmap.svg)

## Foundation — implemented

Local container work, AWS EC2 deployment, Terraform networking/infrastructure and the initial CI/CD path.

## Delivery & security — implemented / evolving

Terraform CI, TFLint, Trivy, Docker build/publish, GHCR versioning and environment configuration.

## Platform hardening — next

- GitHub environment protection and production approval
- HTTPS and DNS
- CloudWatch metrics, logs and alarms
- application health checks
- stronger secret management
- reusable Terraform modules
- documented recovery/rollback path

## Orchestration — planned

Evaluate ECS and Kubernetes/EKS based on the problem being solved. Implement one path end-to-end before describing it as part of the current architecture.
