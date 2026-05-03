# Team Rollout Guide

## Phase 1: Baseline

- Adopt the one-page checklist.
- Decide which AI tools are approved for company or client work.
- Publish the rule: no secrets, tokens, API keys, or customer data in prompts.
- Identify human approval gates for production, DNS, payments, customer data, mass outreach, and infrastructure.

## Phase 2: Project Risk Assessment

- Complete the project AI risk assessment for each repository.
- Classify data sensitivity and production impact.
- Identify allowed tools, forbidden paths, and required reviewers.
- Configure ignore/exclusion rules for secrets, logs, dumps, and private data.

## Phase 3: Sandbox and Logging

- Configure filesystem, network, shell, browser, MCP, GitHub token, CI/CD, database, and production boundaries.
- Require agent run logs for autonomous work.
- Keep commits small and auditable.

## Phase 4: PR Workflow

- Add the AI-assisted PR review template.
- Require reviewers for security, data, infra, dependency, and production changes.
- Require test evidence and rollback notes.

## Phase 5: Continuous Improvement

- Review incidents and near misses monthly.
- Update tool permissions as capabilities change.
- Reassess vendors and client requirements.
- Train new team members and contractors before granting repository access.

## Suggested Metrics

- Number of AI-assisted PRs reviewed.
- Number of agent runs with complete logs.
- Policy exceptions granted.
- Secret exposure or near-miss events.
- Mean time to revoke exposed credentials.
