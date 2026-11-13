# Project AI Collaboration Contract

Project: [PROJECT NAME]
Stack: [LANGUAGE / FRAMEWORK / VERSION]
Repository: [REMOTE URL OR UNKNOWN]

## Purpose and scope

- Goal: [USER OUTCOME]
- In scope: [FEATURES]
- Out of scope: [NON-GOALS]
- Current milestone: [SMALLEST VERIFIED GOAL]

## Instructions and precedence

Follow platform safety requirements and the current user's explicit request. Use this `AGENTS.md` for local project rules. Apply `portable-ai-instructions/MASTER_INSTRUCTIONS.md` and relevant modules when available. If the portable repository is unavailable, the essential local rules below still apply. Do not assume a referenced document was loaded.

## Engineering and teaching contract

- Explain purpose and expected behavior before each focused change.
- Preserve unrelated changes and follow framework-native conventions.
- Verify with the project's real commands; never invent success.
- Teach through the mandatory Feynman method when learning is requested; use real project examples or label generic ones.
- Ask for approval before remote writes, destructive operations, production changes, or publication.
- Reinspect target files before edits after an assistant switch or concurrent work. Never overwrite unexplained changes.
- A feature is complete only when its acceptance criteria and appropriate checks are verified. Code tests and learning mastery are separate.
- Never reveal or commit secrets.

## Verification commands

- Formatting: [command or N/A]
- Static checks: [command or N/A]
- Targeted tests: [command or N/A]
- Full tests/build: [command or N/A]

## Documentation

- Project state: `docs/PROJECT_MEMORY.md`
- Decisions: `docs/DECISIONS.md`
- Handoff: `docs/HANDOFF_CHECKLIST.md`
- Learning (if used): `learning/` with mastery evidence

## Safe resume and checkpoint procedure

1. Inspect branch, upstream, status, untracked files, and recent commits. Compare remote when accessible.
2. Reconcile actual code and test evidence with `PROJECT_MEMORY.md`; mark unknowns honestly.
3. Explain the smallest safe change; reread target files before editing.
4. Verify acceptance criteria; record command, environment, outcome, and skipped checks.
5. Update decisions, memory, and confirmed learning in that order; review diffs before approved remote writes.
6. Do not auto-pull, reset, rebase, clean, or force-push when state is uncertain.

## Next action

[Exact next safe action; update when checkpoint changes]
