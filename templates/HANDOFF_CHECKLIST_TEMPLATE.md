# AI and Developer Handoff Checklist

## On session start

- [ ] Read `AGENTS.md`, `docs/PROJECT_MEMORY.md`, `docs/DECISIONS.md`, and this checklist.
- [ ] Inspect branch, upstream, status including staged/untracked files, recent commits, and relevant source/tests.
- [ ] Compare local state with remote if available; identify divergence.
- [ ] Identify last verified checkpoint, current uncommitted work, blockers, and next safe action.
- [ ] Do not pull, reset, delete, migrate, or overwrite when state is uncertain.

## During a focused change

- [ ] State intended outcome and smallest safe change.
- [ ] Inspect relevant files; preserve unrelated work.
- [ ] Reinspect target files after an assistant switch or concurrent edits. Implement, format, run targeted checks, and relevant full checks.
- [ ] Record acceptance criteria and exact command/manual test, environment, result, and date; include skipped checks and reasons.
- [ ] Review diffs and secret exposure before staging.

## Before commit or remote write

- [ ] Show intended files and staged diff/stat; recheck for concurrent edits.
- [ ] Confirm no credentials, `.env`, generated caches, or unrelated changes.
- [ ] Obtain required approval for remote actions.
- [ ] Verify branch divergence and successful write.

## Before pause or assistant switch

- [ ] After evidence and decisions, update `PROJECT_MEMORY.md` with observed working-tree status, commits, verification, blockers, and next command.
- [ ] Update `DECISIONS.md` for architecture choices.
- [ ] Record only confirmed learning in `learning/`.
- [ ] Mark unknown values as unknown; never claim GitHub contains local uncommitted changes.

## Emergency mismatch

Stop mutations. Preserve files. Compare working tree, local commits, remote commits, and documentation. Never automatically pull, reset, rebase, clean, or force-push. Propose a reversible reconciliation before acting.
