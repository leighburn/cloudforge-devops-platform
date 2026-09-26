# Troubleshooting

CloudForge uses a layer-by-layer troubleshooting approach.

## Deployment failure

1. Identify the exact failed GitHub Actions step.
2. Read the step output rather than changing several components at once.
3. Confirm required GitHub secrets exist without printing secret values.
4. Check network reachability and AWS security-group rules.
5. Verify the SSH public key is present in the target user's `authorized_keys`.
6. Verify permissions on `.ssh` and `authorized_keys`.
7. Test again and compare the result with the previous failure.

## Terraform CI failure

Run the same checks locally where possible:

```bash
terraform fmt -check
terraform init -backend=false
terraform validate
tflint
```

If CI fails before Terraform runs, inspect the workflow YAML and indentation first.

## Container failure

Check container state, logs, health status, port mappings, environment variables and persistent volumes before rebuilding infrastructure.
