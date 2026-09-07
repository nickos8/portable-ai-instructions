# Portable AI Instructions

Version: 1.2.0  
Last updated: 2026-09-07

This private, reusable instruction kit keeps your preferred AI behavior independent of any single account. The files are written in Markdown so they work well in GitHub, text editors, and most AI platforms.

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

## Best way to use this kit

### In a new AI account

1. Open `QUICK_START_PROMPT.md`.
2. Copy it into the platform's custom-instruction or personalization field.
3. For a learning session, also attach `modules/TEACHING_AND_REVIEW.md` and `modules/LEARNING_DOCUMENTATION.md`.
4. For programming work, also attach `modules/CODING_AND_PROJECT_WORK.md`.
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

