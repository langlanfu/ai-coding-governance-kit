# AI Coding Team Governance Kit

A practical, GitHub-ready governance kit for individuals and small teams using AI coding tools such as GitHub Copilot, Codex-style agents, Claude Code, Cursor, OpenCode/OpenCLI, browser automation, MCP tools, and custom automation agents.

This project provides policy templates, checklists, review forms, and incident response playbooks to help teams adopt AI-assisted development with clear boundaries, auditability, and human accountability.

> This kit is a governance template. It does not guarantee security, replace professional security review, provide legal advice, or certify compliance.

## Who This Is For

- Solo developers who use AI coding assistants for local development.
- Startups and small engineering teams adopting AI IDEs or coding agents.
- Agencies and outsourced teams working with client repositories.
- Teams evaluating MCP tools, browser automation, CI automation, or autonomous agents.
- Maintainers who want lightweight rules before opening repositories to AI-assisted contributions.

## Quick Start

1. Read [`CHECKLIST.md`](CHECKLIST.md) for the one-page baseline.
2. Pick the policy matching your tool:
   - [`docs/copilot-usage-policy.md`](docs/copilot-usage-policy.md)
   - [`docs/codex-usage-policy.md`](docs/codex-usage-policy.md)
   - [`docs/claude-code-usage-policy.md`](docs/claude-code-usage-policy.md)
   - [`docs/cursor-and-ai-ide-policy.md`](docs/cursor-and-ai-ide-policy.md)
3. Complete the risk assessment template in [`templates/`](templates/) for each project.
4. Configure sandbox restrictions using [`docs/ai-agent-sandbox-checklist.md`](docs/ai-agent-sandbox-checklist.md).
5. Add [`templates/pr-review-template.md`](templates/pr-review-template.md) to your pull request workflow.
6. Keep an [`templates/agent-run-log-template.md`](templates/agent-run-log-template.md) for autonomous or semi-autonomous runs.
7. Review production boundaries in [`docs/production-change-policy.md`](docs/production-change-policy.md).

## Directory Navigation

```text
docs/       Tool-specific policies, safety checklists, incident response, rollout guide
templates/  Fillable policy, risk assessment, PR review, sandbox audit, agent run log
examples/   Example policies for solo developers, startup teams, and agencies
```

## Core Principles

1. **No secrets in prompts.** Never paste API keys, tokens, passwords, private keys, customer credentials, or production secrets into AI tools.
2. **Least privilege by default.** Agents receive only the minimum file, network, shell, browser, MCP, and token permissions needed for the task.
3. **Human approval for irreversible actions.** Production deploys, DNS changes, payments, customer data operations, mass outreach, destructive database changes, and security-sensitive configuration changes require explicit human confirmation.
4. **Auditability.** Agent activity should be logged: prompt intent, tools used, files changed, commands run, approvals granted, and rollback plan.
5. **Reversibility.** Prefer branches, pull requests, feature flags, backups, migrations with rollback, and small commits.
6. **Review before trust.** AI output is untrusted until reviewed, tested, and approved by an accountable human.
7. **Data minimization.** Provide only the minimum context needed; redact sensitive data and use synthetic examples where possible.
8. **Tool-specific controls.** Copilot suggestions, terminal agents, AI IDEs, MCP tools, and browser automation have different risk profiles and require different boundaries.

## Recommended Usage Pattern

- Use AI for drafting, refactoring, tests, documentation, and exploratory analysis.
- Avoid using AI as the sole approver for authentication, authorization, cryptography, billing, privacy, legal, or production operations.
- Require PR review for AI-assisted changes touching security, data models, infrastructure, CI/CD, dependency management, or customer-facing behavior.
- Keep autonomous agents on non-production branches and scoped sandboxes unless a human explicitly grants more access.

## What This Kit Does Not Do

- It does not provide a legal compliance program.
- It does not certify that a repository or team is secure.
- It does not replace threat modeling, penetration testing, vendor review, or professional legal/security advice.
- It does not recommend sending private data to any AI provider without a completed privacy, security, and contractual review.

## Chinese Summary / 中文摘要

本项目是一个“AI 编程团队治理包”本地 MVP，面向使用 GitHub Copilot、Codex、Claude Code、Cursor、MCP、浏览器自动化和自动化 Agent 的个人、小团队和外包团队。它提供英文为主的治理规范、沙箱检查清单、安全审查模板、生产变更边界、事故响应流程和团队落地指南。

核心边界：不要把 secrets/token/API key 粘贴给 AI；生产部署、DNS、支付、客户数据、批量外联等必须人工确认；Agent 默认最小权限、可审计、可回滚。本项目只是治理模板，不是法律建议、安全认证或合规保证。

## License

MIT License. See [`LICENSE`](LICENSE).
