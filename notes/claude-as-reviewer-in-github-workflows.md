# 2026-04-15

> **Essence:** Today I set up Claude Code review for my Query Forge repo and learned that the reviewer workflow has to be defined at the repo level unless I create a reusable workflow pattern at the account level and call it from each repo.

## What I learned
1. Claude Code review is not just turned on once for my whole GitHub account. I have to add the reviewer workflow inside each repo where I want it to work.
2. I can make this easier by creating a reusable workflow at the account level and then inheriting or calling that workflow from each repo.
3. The Anthropic API key lives in Query Forge GitHub repo settings under Secrets, and I need to think more about how to manage that safely if I keep creating more repos.

## What I applied
- Added the Claude Code reviewer workflow to my Query Forge repo.
- Saved the Anthropic key in the repo’s GitHub Secrets settings.
- Started understanding the difference between repo-level setup and reusable workflow setup.

## What was confusing
- I first assumed Claude Code review could be enabled once at the GitHub account level for every repo automatically.
- I am still not clear on the best way to manage secrets securely across multiple repos.

## Next thing to try
- Test a reusable workflow setup so I do not have to rewrite the same reviewer workflow in every repo.
- Research the safest way to manage Anthropic secrets across multiple repos.
- Trigger `@claude` in Query Forge and confirm the reviewer flow works end to end.
- Review my `.github/workflows` file again so I understand the triggers, permissions, and auth setup clearly.
- Build a simple end-of-day git habit for Query Forge: `git add .`, `git commit -m "end of day"`, and `git push`.
