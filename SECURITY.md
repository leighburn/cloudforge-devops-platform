# Security Policy

Do not open a public issue containing credentials, private keys, tokens or other secrets.

CloudForge is a portfolio/learning platform. Security issues in the repository should be reported privately to the repository owner where possible.

## Secret handling

Never commit AWS access keys, SSH private keys, GitHub tokens, database passwords or populated `.env` files. If a secret is accidentally committed, revoke/rotate it immediately and remove it from the repository history where appropriate.
