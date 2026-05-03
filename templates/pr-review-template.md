# AI-Assisted Pull Request Review Template

## Summary

What changed and why?

## AI Assistance Disclosure

- AI tools used:
- What the AI generated or modified:
- What the human author verified:
- Agent run log link, if applicable:

## Risk Areas

Check all that apply:

- [ ] Authentication or authorization
- [ ] Secrets or configuration
- [ ] Customer data or privacy
- [ ] Database migration or destructive operation
- [ ] CI/CD or deployment
- [ ] Infrastructure or cloud permissions
- [ ] Dependencies or supply chain
- [ ] Payment, billing, DNS, email, or account management
- [ ] Browser automation or external communication
- [ ] None of the above

## Review Checklist

- [ ] No secrets, tokens, API keys, private keys, or customer data are included.
- [ ] AI-generated code was manually reviewed.
- [ ] Tests were added or updated and were not weakened.
- [ ] Security-sensitive behavior has regression coverage.
- [ ] New dependencies are justified and reviewed.
- [ ] Production impact is documented.
- [ ] Rollback plan exists for risky changes.

## Test Evidence

Commands run and results:

```text

```

## Human Approval

Required approvers:

- Code owner:
- Security/data owner if applicable:
- Production owner if applicable:
