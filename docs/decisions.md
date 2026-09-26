# Engineering Decisions

## Infrastructure as code

Terraform is used so infrastructure changes can be reviewed, repeated and version-controlled rather than relying on undocumented console configuration.

## Containers

Docker creates a consistent application runtime between local development and cloud deployment. Docker Compose provides a practical way to run the Ghost/MySQL application stack while the orchestration layer is still evolving.

## GitHub Actions

Keeping automation close to the repository makes checks visible on pull requests and connects source changes to validation, image builds and deployment work.

## GHCR

Publishing versioned container images makes a build traceable and separates image creation from the target runtime.

## Incremental orchestration

Kubernetes/EKS and ECS are not added merely to increase the tool count. The project first develops reliable infrastructure, delivery, security and observability foundations.
