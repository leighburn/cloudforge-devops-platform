# Getting Started

This documentation package is designed to complement the existing CloudForge repository. Review the existing application, Terraform and workflow files before replacing anything.

## Local application

Use the repository's existing Docker/Compose configuration and `.env.example`. Never commit the real `.env` file.

Typical inspection commands:

```bash
docker compose config
docker compose up -d
docker compose ps
docker compose logs
```

## Terraform

Work from the appropriate Terraform directory/environment and validate before planning:

```bash
terraform fmt -check
terraform init
terraform validate
tflint
terraform plan
```

Review every plan before applying it. Destroy unused learning infrastructure when appropriate to avoid unnecessary AWS charges.

## GitHub Actions

Check the Actions tab after a push or pull request. A red job is evidence to investigate, not something to hide. Open the failed step, identify the failing layer and reproduce the relevant check locally where possible.
