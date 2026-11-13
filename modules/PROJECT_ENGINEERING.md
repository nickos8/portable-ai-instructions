# Universal Project Engineering Standard

Applies to software projects of any language or framework. Keep universal behavior here; place stack-specific commands, paths, and constraints in each project's `AGENTS.md` and `docs/`.

## Principles

- Understand the problem and success criteria before selecting tools.
- Prefer the smallest maintainable architecture that meets actual requirements. Avoid speculative abstractions and unnecessary dependencies.
- Standardize *responsibilities*, not identical directory layouts. Use the framework's conventions for source, tests, build, and deployment.
- Distinguish planned, implemented, locally verified, remotely verified, and deployed states.
- Never treat documentation, a GitHub view, or an AI assertion as proof of the current local working tree.

## Project initiation

1. Define purpose, users, scope, non-goals, constraints, and definition of done.
2. Select stack with explicit reasons, tradeoffs, and environment requirements.
3. Define data flow, major components, interfaces, and testing strategy appropriate to project size.
4. Propose the framework-native layout plus minimal continuity documentation.
5. Establish `.gitignore`, safe configuration examples, README, and baseline verification commands.
6. Ask for approval before creating remote repositories, pushing, publishing, deleting, or changing external resources.
7. Capture initial decisions in `docs/DECISIONS.md` and next task in `docs/PROJECT_MEMORY.md`.

## Documentation tiers

- **Experiment:** README, source/tests, and short learning/session notes as needed. Do not create empty bureaucracy.
- **Standard project:** `AGENTS.md`, README, `docs/PROJECT_MEMORY.md`, `docs/DECISIONS.md`, `docs/HANDOFF_CHECKLIST.md`, source/tests; `learning/` if learning is a goal.
- **Larger/team project:** add `docs/ARCHITECTURE.md`, contribution/deployment instructions, CI, and operational documentation when justified.
- `CLAUDE.md` and `.github/copilot-instructions.md` should be short adapters pointing to `AGENTS.md`, not divergent copies of rules.

## Starting or resuming work

1. Read `AGENTS.md` and the referenced project documents.
2. Inspect branch, status including untracked files, recent commits, relevant code and tests. Compare local state with remote only when accessible.
3. Identify uncommitted work, last *verified* checkpoint, missing verification, and current task.
4. If local access is unavailable, say so and request only the necessary safe command output. Never claim a GitHub clone reveals local changes.
5. When sources disagree, stop mutations, preserve data, inspect differences, and propose a recoverable resolution.

## Implementation cycle

1. Explain one coherent change and expected behavior.
2. Inspect existing implementation and dependencies.
3. Make a focused change, preserving unrelated work.
4. Run formatter/static analysis, targeted tests, and relevant build checks; expand verification based on risk.
5. Inspect diffs, including generated files and secrets; record exact checks and outcomes.
6. Update decisions only when an architectural choice changes; update memory with observed state and next action.
7. Record learning as mastery only after user teach-back or demonstrated independent application.
8. Before commit/push, show intended staged files and obtain approval for remote actions. Check branch divergence before pushing.

## Definition of done and evidence gates

A task is **planned** when its acceptance criteria exist, **implemented** when code is written, **verified** only when appropriate checks demonstrate the required behavior, and **complete** only when acceptance criteria are met, no blocking failures remain, and the checkpoint accurately records the evidence. Deployment is a separate state.

- Before implementation, define observable acceptance criteria and the smallest useful tests, including error and edge cases where relevant.
- For each check, record the command or manual scenario, environment, result, and date. Record **not run** and the reason when unavailable. A formatter, successful build, or green unit test alone does not prove end-to-end behavior.
- When verification is blocked, label the work **implemented, unverified**, not complete. Do not silently waive a required check.
- Code correctness and user learning are separate gates: passing tests does not establish mastery; teach-back or independent application is evidence of understanding.

## Git inspection and synchronization safety

- Before synchronizing or publishing, inspect current branch, upstream, tracked modifications, staged changes, untracked files, and local/remote divergence. Use `git status --short --untracked-files=all`, `git branch -vv`, `git log --oneline -10`, and `git fetch` when safe and available; inspect relevant diffs.
- `git fetch` updates remote-tracking information but does not merge local files. Do not infer a clean tree from a remote GitHub view.
- Never automatically `pull`, `reset`, `rebase`, `clean`, or force-push to resolve uncertainty. Explain alternatives and obtain explicit approval for risky or destructive operations.
- Reinspect status and relevant file contents immediately before writing if another assistant, editor, automation, or collaborator may have changed the repository since the last read.

## Verification and risk

- Never fabricate tool outputs or say 'passed' for checks not run. Record 'not run' with reason.
- Prefer isolated test data. Ask before production data changes, migrations against live services, external publication, or irreversible operations.
- Check authorization, input validation, secrets, error handling, accessibility, and appropriate edge cases.
- A feature is 'done' only when acceptance criteria and relevant checks pass, or clearly state remaining exceptions.

## Checkpoint documentation order

After a verified change: (1) collect actual implementation/test evidence; (2) update `DECISIONS.md` if architecture changed; (3) update `PROJECT_MEMORY.md` with state, evidence, and one exact next action; (4) update learning records **only** for demonstrated understanding; (5) inspect code/documentation diffs and sensitive files; (6) stage exact files and commit/push only with the applicable approval. Never claim a remote checkpoint exists before verifying the push.

## Checkpoint and handoff

Keep distinct: current local working tree; latest local commit; latest remote commit; last verified commit; last verification command/results; next safe step. See `templates/PROJECT_MEMORY_TEMPLATE.md` and `templates/HANDOFF_CHECKLIST_TEMPLATE.md`.
