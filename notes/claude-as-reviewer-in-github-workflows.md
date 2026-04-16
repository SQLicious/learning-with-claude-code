# 2026-04-15

> **Essence:** I set up Claude Code GitHub review for my Query Forge repo so Claude can assist inside PR and issue workflows, while I still keep control of my daily manual commits and pushes from VS Code.

## What I learned
1. Claude in GitHub is usually set up through a GitHub Action inside `.github/workflows`, not through automatic syncing from VS Code.
2. Claude’s GitHub integration needs both a workflow file and an auth secret, such as `ANTHROPIC_API_KEY` or `CLAUDE_CODE_OAUTH_TOKEN`.
3. When `claude` shows up as a contributor on a repo, it usually means Claude is participating through GitHub-side automation like PR reviews, issue responses, or code changes.

## What I applied
- Set up Claude Code GitHub review in the workflows for my Query Forge folder.
- Clarified the difference between Claude helping locally in VS Code and Claude acting inside GitHub workflows.
- Kept my intended workflow manual for end-of-day commits and pushes.

## What was confusing
- I initially mixed up Claude as a local coding assistant with Claude as a GitHub workflow automation tool.
- It was not obvious at first what it meant when `claude` appeared as a contributor on someone else’s repo.

## Next thing to try
- Test `@claude` in a PR or issue to confirm the workflow triggers correctly.
- Review my `.github/workflows` file again so I understand the triggers, permissions, and auth setup clearly.
- Build a simple end-of-day git habit for Query Forge: `git add .`, `git commit -m "end of day"`, and `git push`.
