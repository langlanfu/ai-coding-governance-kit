# Solo Developer AI Policy Example

## Context

This policy is for a solo developer using AI assistants on personal or indie projects.

## Allowed

- Copilot or AI IDE completion for routine code.
- Terminal agents for scoped tasks on git branches.
- AI-generated tests and documentation.
- Local-only experiments with disposable data.

## Not Allowed Without a Manual Pause

- Production deployment.
- DNS, payment, email, or account changes.
- Database migration against production.
- Browser form submission or public posting.
- Any use of real customer data.

## Personal Rules

- Keep `.env` files out of AI context.
- Start each agent run with a clear scope and branch.
- Commit before broad refactors so rollback is easy.
- Review every diff before merge.
- Run tests before deploy.

## Incident Response

If a secret is exposed, revoke it immediately, rotate the affected credential, inspect logs, and document what changed in the project notes.
