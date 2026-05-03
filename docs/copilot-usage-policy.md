# GitHub Copilot Usage Policy

## Purpose

GitHub Copilot is primarily an inline code completion and chat assistant. Its main risk is that sensitive code context, proprietary snippets, or insecure suggestions may be accepted too quickly because the workflow feels like normal typing.

## Approved Uses

- Boilerplate, test scaffolding, documentation drafts, and small refactors.
- Explaining unfamiliar code when no secrets or customer data are included.
- Generating examples using synthetic data.
- Suggesting unit tests for reviewed code paths.

## Restricted Uses

Copilot output must not be accepted without human review when it touches:

- Authentication, authorization, session handling, or cryptography.
- Payment, billing, invoicing, or customer account operations.
- Database migrations, destructive queries, or production configuration.
- Security controls, audit logging, dependency pinning, or CI/CD secrets.

## Data Handling Rules

- Do not paste API keys, tokens, passwords, private keys, customer secrets, or production credentials into Copilot Chat.
- Do not ask Copilot to process raw customer records, regulated data, or confidential client documents unless approved by the organization.
- Redact logs before use. Replace real identifiers with synthetic examples.

## Review Requirements

- Treat suggestions as untrusted code.
- Run tests and linters before merging.
- Verify license-sensitive or unusual code manually.
- Require PR review for security-sensitive or production-affecting changes.

## Team Controls

- Document whether repository content may be used with Copilot based on company and client agreements.
- Prefer organization-managed settings over personal settings for business repositories.
- Keep Copilot use visible in PR notes for high-risk changes.
