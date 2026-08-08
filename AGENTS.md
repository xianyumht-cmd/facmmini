# AGENTS.md — Mandatory AI Repository Rules

> **ChatGPT / Codex / other coding agents: read this before any repository action.** These are standing user instructions; do not wait for the user to repeat them.

- Canonical branch: `main`.
- One task = one short-lived branch from the latest canonical branch.
- Check for an existing active branch/PR before creating another branch for the same task.
- Never create auxiliary `v2`, `v3`, `final`, `current`, `backup`, `test`, `build`, `deploy`, `handoff`, `note`, or packaging branches.
- Use Issues/task-state docs for unfinished work, Actions artifacts for builds, and tags for immutable releases/history.
- Preserve unique history with a verified `archive/*` tag before branch deletion.
- After PR merge: verify `main`, update task state, delete the temporary branch.
- Do not force push, `git reset --hard`, history-rewrite rebase, `git clean`, `git stash`, or destructively move refs unless the user explicitly authorizes a narrowly scoped recovery.
- If branch/origin/worktree/history is unexpected or divergent, stop and report exact state instead of rewriting history.
- Never commit secrets, credentials, local environment files, or sensitive diagnostics.
- At task start, read all applicable `AGENTS.md`, identify branch/origin/worktree state, inspect referenced Issue/PR, and discover project-specific build/deploy docs.
- Destructive Git operations, branch/tag deletion, deployment, or service restart require explicit user intent and fresh safety checks.
- Keep persistent remote branches minimal; temporary branches exist only while their task is active.
