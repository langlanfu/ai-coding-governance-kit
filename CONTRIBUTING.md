# Contributing

Thank you for improving the AI Coding Team Governance Kit.

## Contribution Types

- Tool-specific policy improvements.
- New governance templates.
- Better checklists and examples.
- Incident response lessons learned.
- Clarifications for small teams, agencies, and maintainers.

## Standards

- Keep content practical, specific, and vendor-neutral where possible.
- Do not claim that this kit guarantees safety, compliance, or legal adequacy.
- Avoid submitting secrets, private customer examples, proprietary client text, or confidential incident details.
- Prefer clear checklists and actionable language.
- Include human approval gates for production, DNS, payments, customer data, CI/CD secrets, and external communications.

## Pull Request Checklist

- [ ] Markdown is readable and non-empty.
- [ ] No real secrets, tokens, private keys, or customer data are included.
- [ ] New policy content includes boundaries, review expectations, and rollback/audit considerations.
- [ ] Examples use synthetic data.
- [ ] Disclaimer language is preserved where relevant.

## Local Review

Before submitting, search for obvious secret patterns and review the diff manually. This project is documentation-only; tests may consist of markdown linting and link checks when configured.
