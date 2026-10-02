# AGENTS.md

## Orca Homebase

This repository is the source of truth for Orca Homebase.

### Rules

- Work on `main` unless a task explicitly requests another branch.
- Inspect the repository before making architectural assumptions.
- Build real, functional software. No fake integrations, fake data states, simulated backend behavior, or dead buttons.
- Preserve working functionality when extending the project.
- Keep the application lightweight, fast, mobile-first, and maintainable.
- Avoid unnecessary dependencies and infrastructure.
- Keep secrets and API keys out of source control. Use environment variables and document required variables in `.env.example`.
- Do not change domains, DNS, publishing ownership, external service ownership, or account settings unless explicitly requested.
- Do not delete user work without verifying what it is and why it is safe to remove.
- If an integration is unavailable, isolate it behind a clean interface instead of pretending it works.
- Prefer small, verifiable changes over speculative rewrites.

### Codex delivery workflow

1. Inspect the repository and git status.
2. Read this file before implementation.
3. Identify the existing stack and smallest architecture needed.
4. Implement the requested work.
5. Run available tests, type checks, linting, and builds.
6. Fix failures before reporting completion.
7. Review the final diff for accidental changes, secrets, generated junk, and broken files.
8. Commit the completed work with a clear message.
9. Push to the configured GitHub remote when the Codex environment has push access.
10. Report the commit SHA, branch, verification results, and any blocker.

### GitHub remote

`https://github.com/mmsplarmaaloeallal-sys/orcahomebase.git`

If Codex cannot authenticate or push, report the exact access blocker. Do not claim a push succeeded when it did not.

### Product direction

Orca Homebase is intended to become a real personal AI workspace with a useful shell, modular agents, utilities, unified conversation, tools/plugins, projects/tasks, and dynamic UI reflecting actual state.

Prioritize:
- fast startup and responsive interaction
- mobile usability
- clear information hierarchy
- real state and real actions
- modular agent/tool boundaries
- secure server-side credentials
- graceful failures and useful error states
- simple deployment and strong ownership

Do not add domains, monetization, or unrelated features unless explicitly requested.
