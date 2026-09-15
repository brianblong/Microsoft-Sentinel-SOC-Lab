# Security Policy

## Scope

This repository contains defensive security research and authorized lab simulations. It must not be used against systems without explicit permission.

## Reporting a repository security issue

Do not open a public issue containing a credential, exploitable secret, personal data, or a vulnerability that could place a real environment at risk. Remove exposed credentials immediately, rotate them at their source, and then sanitize the repository history before publication.

## Sensitive data policy

The following must never be committed:

- Passwords, tokens, API keys, certificates, or private keys
- Logic App callback URLs or webhooks
- Terraform state or unredacted deployment outputs
- Raw production or personal logs
- Real tenant, subscription, user, host, domain, or public IP identifiers
- Ground-truth data that would compromise an active blind investigation

Use placeholders in documentation and sanitized synthetic data in examples.

## Simulation safety

Every executable scenario must define authorized targets, prerequisites, expected effects, stop conditions, cleanup steps, and validation checks. See the repository [rules of engagement](docs/security/rules-of-engagement.md).

