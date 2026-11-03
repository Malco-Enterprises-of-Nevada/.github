# .github

Org-wide reusable workflows for Malco-Enterprises-of-Nevada.

- `.github/workflows/claude-review.yml` — Claude code review on every pull request. Each repo
  calls it from its own `.github/workflows/claude-review.yml`. It comments only; approvals come
  from Copilot and humans via the org rulesets. It needs one org Actions secret:
  `ANTHROPIC_API_KEY` (Claude Console) or `CLAUDE_CODE_OAUTH_TOKEN` (`claude setup-token`,
  Pro/Max), created with repository access **All repositories** (malco-entra-auth is public; a
  private-only secret never reaches it). Until one exists the job logs a notice and skips.
  This repo is public because a public repo can only call reusable workflows from public repos;
  keep secrets out of it.
