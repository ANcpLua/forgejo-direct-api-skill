# Forgejo Direct API Skill

Forgejo-first Codex skill for working with Forgejo v15 repositories, Actions, runners, pull requests, reviews, statuses, packages, releases, webhooks, and live Swagger.

This is intentionally not a GitHub compatibility shim. The goal is to teach agents the direct Forgejo API surface so they do not hallucinate GitHub-only behavior.

## Files

- `SKILL.md` - skill entrypoint
- `references/forgejo-api-map.md` - Forgejo-native endpoint map by task
- `references/forgejo-v15-endpoints.md` - generated full v15 route inventory
- `references/forgejo-actions-runner.md` - Actions runner and workflow notes
- `references/forgejo-ai-review.md` - Forgejo-native AI review flow
- `scripts/fetch-forgejo-swagger.sh` - refresh generated endpoint inventory
- `scripts/verify-forgejo-skill.sh` - verify documented routes against live Swagger and safe API probes

## Verify

```bash
./scripts/verify-forgejo-skill.sh https://v15.next.forgejo.org ANcpLua qyl
```

With a private repo token:

```bash
FORGEJO_TOKEN=... ./scripts/verify-forgejo-skill.sh https://v15.next.forgejo.org ANcpLua qyl
```
