# Cross-Assistant Collaboration Contract

Use across ChatGPT, Claude, Copilot, and other assistants. Capabilities differ: follow the available tools and disclose access limits instead of pretending actions occurred.

## Single source of truth

- `portable-ai-instructions/MASTER_INSTRUCTIONS.md` defines reusable teaching and safety standards.
- Each project's `AGENTS.md` defines project-specific obligations and links to relevant portable modules.
- `CLAUDE.md` and `.github/copilot-instructions.md` are brief pointers, not competing copies.
- Source code, working-tree state, and actual test results determine current implementation state. Documentation records observed checkpoints but may lag.

## Mandatory session entry

1. Read local project instructions and continuity documents.
2. Inspect actual branch, staged/unstaged/untracked files, latest commits, and relevant source/tests.
3. Check remote state when accessible. Distinguish remote from local and last verified checkpoints.
4. If state cannot be inspected, label it unknown; ask for safe outputs rather than guessing.
5. Identify one smallest safe next action.

## Stale-state and concurrent-edit safeguards

- A prior assistant's summary or previously read file is not proof of current state.
- Before writing, re-read target files when another assistant, editor, automation, or teammate could have edited them.
- Do not overwrite unexpected changes. Stop, compare, and ask for a safe reconciliation plan.
- For simultaneous agents, prefer separate branches, worktrees, or explicit file ownership; never silently share a mutable working tree.
- Never use an old file SHA to force an update over newer content.

## Handoff contract

Record: project and goal; current branch; working-tree changes; latest local commit; latest remote commit; last verified checkpoint; commands/tests and observed outcomes; blockers; decisions; exact next safe action. Mark unavailable facts as unknown.

## Changes and approval

- Explain intended edits, affected files, expected behavior, and verification before significant changes.
- Preserve unrelated work and secrets.
- Do not claim checks passed unless run.
- Show proposed GitHub writes and obtain explicit approval before remote mutation; verify the resulting state.
- Never auto-pull, reset, rebase, clean, or force-push to fix uncertainty.

## Assistant adapters

- `AGENTS.md` is the local contract and must be usable without network access to the portable repository.
- Assistant-specific adapters should direct the agent to `AGENTS.md` and avoid conflicting rules.
- If an assistant cannot load a referenced portable module, use the locally embedded safety and verification rules; disclose which extended instructions were not loaded.
