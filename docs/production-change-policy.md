# Production Change Policy

AI tools may assist with planning and drafting production changes, but they must not independently approve or execute high-impact production operations.

## Human Confirmation Required

A named human owner must explicitly confirm before:

- Production deployment or rollback.
- DNS, domain, SSL/TLS, email, or identity provider changes.
- Payment, billing, pricing, refund, or subscription changes.
- Customer data export, deletion, migration, or bulk modification.
- Database schema changes in production.
- Cloud IAM, firewall, network, secret manager, or infrastructure changes.
- CI/CD workflow changes that affect deployment or secrets.
- Batch outreach, posting, messaging, or browser actions on third-party platforms.

## Required Change Record

- Change owner.
- Business reason.
- AI tools used and generated artifacts.
- Systems affected.
- Risk level and customer impact.
- Test evidence.
- Rollback plan.
- Approval record.
- Monitoring plan after release.

## Deployment Guardrails

- Use feature flags for risky changes.
- Prefer staged rollout over big-bang release.
- Keep database migrations backward compatible where possible.
- Verify backups before destructive changes.
- Monitor logs, metrics, and alerts after release.

## Emergency Exception

Emergency production actions may be accelerated only when delaying creates greater harm. The human owner must still record what happened, why AI assistance was used, what was verified, and what follow-up review is required.
