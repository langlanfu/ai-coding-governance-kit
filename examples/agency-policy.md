# Agency AI Policy Example

## Context

This example is for agencies and outsourcing teams working across client repositories.

## Client Consent

- Confirm whether AI tools are permitted for each client and repository.
- Respect client-specific data handling, vendor, and confidentiality requirements.
- Do not upload proprietary client data to AI systems unless the client has approved the tool and use case.

## Approved Uses

- Drafting documentation and tests from non-sensitive code.
- Local refactoring on feature branches.
- Issue triage using approved project metadata.
- Generating implementation plans for client review.

## Restricted Uses

- No client secrets, tokens, private keys, production logs, customer exports, or credentials in prompts.
- No autonomous production deploys.
- No browser automation against client accounts without written task approval.
- No mass outreach, scraping, payments, DNS, or account changes without client confirmation.

## Review and Audit

- Keep agent run logs for billable AI-assisted work.
- Disclose AI-assisted contributions when required by contract.
- Use client-approved repositories, accounts, and tokens only.
- Remove local client data at project close according to contract.

## Incident Handling

Notify the agency lead and client contact if AI use may have exposed secrets, customer data, or unauthorized changes. Rotate credentials and preserve logs for investigation.
