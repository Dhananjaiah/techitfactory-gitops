# Contributing (Trunk-Based Development)

## Branching
- Default branch: `main`
- Work in short-lived branches:
  - `feature/<topic>`
  - `fix/<topic>`
  - `chore/<topic>`

## Pull Requests
- Every change goes through a PR (no direct pushes to `main`)
- Keep PRs small (ideally <300 lines)
- PR must include:
  - clear description
  - test/verification notes
  - rollback plan

## Merging
- Use **Squash and merge**
- Delete branch after merge

## Release & Promotion
- Dev auto-deploy happens from merges to `main`
- Prod promotion happens ONLY through Git tag/release gate (later sprint)
