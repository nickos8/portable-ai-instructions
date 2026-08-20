# Security Checklist

Review this before committing changes to GitHub.

## Safe to store in a private instruction repository

- Learning preferences
- Formatting preferences
- Teaching method
- General career goals
- Public portfolio links
- Reusable templates
- Non-sensitive project summaries

## Do not store

- Passwords or password hints
- One-time codes or recovery codes
- API keys, access tokens, private keys, or signing secrets
- `.env` contents
- Database passwords or full private connection strings
- Card or bank information
- Full government ID numbers
- Private medical records
- Someone else's personal information
- Confidential employer, client, or school data

## Important Git warning

Deleting a secret in a later commit may not remove it from Git history. If a secret is accidentally committed:

1. Revoke or rotate the secret immediately.
2. Treat it as compromised.
3. Clean the repository history using an appropriate history-rewrite tool.
4. Force-push only after understanding the effect on collaborators.
5. Check forks, clones, releases, issues, and automated logs where it may remain.

## Borrowed-account checklist

- Download your files before ending the session.
- Do not save your GitHub password in the browser.
- Do not connect a personal account unless you can disconnect it afterward.
- Sign out from any personal services you opened.
- Remove downloaded personal files from the borrowed device if it is not yours.
- Check the browser's saved passwords, downloads, and active sessions.
- Change important passwords if you think another person may have seen them.

