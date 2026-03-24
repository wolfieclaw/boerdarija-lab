# Security

This repo contains experiments, content, and tooling. It should **not** contain plaintext secrets.

## Rules

- Never commit API keys, tokens, passwords, private keys, or `.env` files.
- Treat audio-generation helpers and utility scripts as high-risk for accidental leaks.
- Run the local secret scan before pushing important changes.
- If a secret is ever exposed, rotate it first, then scrub the repo/history.

## Secret scan

Run:

```bash
./scripts/scan-secrets.sh
```

To install local git hooks that run the scan automatically:

```bash
./scripts/install-git-hooks.sh
```

## Ignored local files

Common local-only secret paths are ignored via `.gitignore`, including:
- `.env`
- `*.env`
- `*token*`
- `*api_key*`
- local credentials/secrets folders

That is only a safety net, not a guarantee.

## If a leak happens

1. Rotate/revoke the secret immediately.
2. Remove it from the working tree.
3. Rewrite git history if it was committed.
4. Force-push the cleaned history if needed.
5. Re-scan the repo.

## Notes for this repo

This repo has historically included local helper scripts for generating audio. Those files are exactly the sort of place where secrets can accidentally end up. Assume they are dangerous until proven otherwise.
