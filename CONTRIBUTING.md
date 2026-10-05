# Contributing

This repository is one of the Oneways engineering repositories. The same conventions apply across all of them.

## Branches

- Work happens on short-lived branches cut from `main`: `type/short-description` (for example `fix/booking-timezone`, `feat/quote-pdf`, `docs/runbook-rollback`).
- `main` is protected: changes land through a pull request with at least one review. Never push directly to `main`.

## Commits

- Conventional Commits: `type(scope): summary` with `type` one of `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `ci`, `perf`, `build`.
- `scope` names the package, service or area touched (for example `rfq-svc`, `map`, `terraform/iam`).
- One logical change per commit; the summary is imperative and under 72 characters.

## Pull requests

- Describe what changed and why, how it was verified, and anything a reviewer must know to run it.
- Keep PRs small enough to review in one sitting; split unrelated changes.
- All checks listed in the README's "Run, test, build" table must pass locally before requesting review.
- The merge method is fixed per repository and shown on the PR page; do not change repository settings to merge.

## Documentation

- The README describes the software as it is, not the history of how it got there. If a change alters setup, configuration, commands or deployment, update the README and `.env.example` in the same PR.
- Decisions with lasting consequences go in `docs/adr/` (one file per decision, `ADR-NNNN-title.md`). Operational procedures go in `docs/runbooks/`.

## Secrets and personal data

- Never commit secrets, tokens, account numbers or customer data. Configuration is read from environment variables and Secret Manager; `.env` files are ignored by git.
- Do not reference personal machines, home directories or personal accounts in code, scripts or docs.

## Releases and deployment

How a change reaches users is described in the README's "Deploy" section and in `docs/runbooks/`.
