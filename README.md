# Portable AI Instructions

Version: 2.0.0  
Last updated: 2026-11-13

This private, portable instruction kit defines how AI assistants teach, plan, engineer, verify, document, and hand off work across projects. Universal standards live here; each project maintains its own code, stack-specific rules, verified memory, and learning evidence.

## Recommended storage

Use a **private GitHub repository** as the main copy. Keep a second offline copy on your own device or personal cloud drive.

Do not store passwords, API keys, recovery codes, government ID numbers, private database URLs, or `.env` contents in this repository. Git history can preserve deleted information.

## Files

- `MASTER_INSTRUCTIONS.md`: complete source of truth
- `QUICK_START_PROMPT.md`: shorter version for custom-instruction fields
- `modules/`: focused instructions you can attach only when relevant
- `modules/LEARNING_DOCUMENTATION.md`: rules for recording confirmed learning
- `templates/PROJECT_CONTEXT_TEMPLATE.md`: reusable context for a project
- `templates/SESSION_HANDOFF_TEMPLATE.md`: saves progress before changing accounts or chats
- `templates/LEARNING_ENTRY_TEMPLATE.md`: reusable format for topic notes
- `learning/`: personal learning index, topic notes, session notes, and mastery tracker
- `SECURITY_CHECKLIST.md`: privacy rules for the repository
- `CHANGELOG.md`: record of instruction changes
- `modules/PROJECT_ENGINEERING.md`: reusable project lifecycle, architecture boundaries, verification, and Git safety
- `modules/ADHD_STUDY_PLANNING.md`: short focus cycles, recall, breaks, spaced review, and schedule output requirements
- `modules/AI_COLLABORATION.md`: cross-assistant instruction hierarchy, session entry, state checks, and handoffs
- `templates/AGENTS_TEMPLATE.md`: project-local AI contract
- `templates/PROJECT_MEMORY_TEMPLATE.md`: verified working-tree and checkpoint record
- `templates/DECISIONS_TEMPLATE.md`: architecture decision record
- `templates/HANDOFF_CHECKLIST_TEMPLATE.md`: safe resume, checkpoint, and pause procedure
- `templates/ARCHITECTURE_TEMPLATE.md`: optional design and data-flow document

## Best way to use this kit

### In a new AI account

1. Open `QUICK_START_PROMPT.md`.
2. Copy it into the platform's custom-instruction or personalization field.
3. For a learning session, also attach `modules/TEACHING_AND_REVIEW.md` and `modules/LEARNING_DOCUMENTATION.md`.
4. For programming work, also attach `modules/CODING_AND_PROJECT_WORK.md`, `modules/PROJECT_ENGINEERING.md`, and `modules/AI_COLLABORATION.md`. For study plans, load `modules/ADHD_STUDY_PLANNING.md`.
5. For job searching or resume work, also attach `modules/CAREER_SUPPORT.md`.
6. If the platform has no custom-instruction feature, paste the relevant file at the beginning of a new chat.
7. At the end of a meaningful learning session, update the relevant files under `learning/` only after your understanding has been checked.

### For an important ongoing project

1. Copy `templates/PROJECT_CONTEXT_TEMPLATE.md`.
2. Rename it for the project.
3. Fill in only the information the AI actually needs.
4. Update it when the project's state changes.
5. Before leaving a chat or account, fill in `templates/SESSION_HANDOFF_TEMPLATE.md`.

## Create the private GitHub repository

### Easy method using the GitHub website

1. Sign in to your own GitHub account.
2. Select **New repository**.
3. Name it `portable-ai-instructions`.
4. Select **Private**.
5. Do not enable GitHub Pages.
6. Upload the extracted files from this kit.
7. Commit with a message such as `Add portable AI instructions v1.0.0`.

### Optional Git method

```bash
git init
git add .
git commit -m "Add portable AI instructions v1.0.0"
git branch -M main
git remote add origin YOUR_PRIVATE_REPOSITORY_URL
git push -u origin main
```

## New software project workflow

1. Define scope, success criteria, constraints, and a framework-native architecture.
2. Select the documentation tier in `modules/PROJECT_ENGINEERING.md`.
3. Copy and adapt `templates/AGENTS_TEMPLATE.md`, `PROJECT_MEMORY_TEMPLATE.md`, `DECISIONS_TEMPLATE.md`, and `HANDOFF_CHECKLIST_TEMPLATE.md` into the project.
4. Add `ARCHITECTURE_TEMPLATE.md` only when complexity justifies it; use the existing `learning/` conventions for guided learning.
5. Keep `CLAUDE.md` and `.github/copilot-instructions.md` as short pointers to `AGENTS.md`.
6. On every return, inspect actual code and Git state before trusting project memory.
7. Review proposed remote writes and authorize them before publication.

## How to update safely

1. Change one section at a time.
2. Update `CHANGELOG.md` with what changed and why.
3. Increase the version number for meaningful changes.
4. Commit the update.
5. Test the new instructions in a fresh chat.
6. Revert the commit if the new version performs worse.

## Instruction priority

When instructions conflict, use this order:

1. Safety, law, privacy, and platform rules
2. The current user's explicit request
3. Project-specific context
4. `MASTER_INSTRUCTIONS.md`
5. Optional modules and style preferences

This order prevents a style preference from overriding correctness or safety.

