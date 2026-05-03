# Claude Code Usage Policy

## Purpose

Claude Code and similar terminal-based coding assistants can reason over large codebases and may execute commands or modify files. They are useful for deep analysis, but their broad context window and tool access require careful scoping.

## Approved Uses

- Codebase navigation and explanation.
- Multi-file refactoring on feature branches.
- Test generation, documentation updates, and issue triage.
- Preparing migration plans for human review.

## Risk Areas

- Large context uploads may include confidential business logic or secrets accidentally embedded in files.
- Terminal access can run destructive commands.
- Long-running sessions can drift from the original approved task.
- Generated plans may sound authoritative even when assumptions are wrong.

## Controls

- Start every run with a precise task, allowed directories, prohibited actions, and expected deliverables.
- Keep production secrets outside the workspace.
- Use read-only mode for analysis when edits are not required.
- Require confirmation before shell commands that install packages, delete files, modify git history, touch infrastructure, or access networks.
- Save a run log for non-trivial sessions.

## Review Standard

- Human owner reviews all code diffs and command outputs.
- Security-sensitive recommendations need independent verification.
- The assistant must not be the only reviewer for generated tests or security fixes.
