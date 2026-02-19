# AGENTS.md

Guidance for coding agents working in this repository.

## Goals
- Keep this repository lightweight and practical for developer workflow utilities.
- Favor simple scripts and documentation over heavy frameworks.
- Keep every change easy to review and safe to run locally.

## Working conventions
- Make focused changes with clear commit messages.
- Prefer small, composable utilities and plain-text docs.
- Document every new utility in `README.md` with usage examples.
- Avoid unrelated refactors in the same branch.

## Branching and commits
- Create a dedicated branch per task using a `feat/`, `fix/`, `chore/`, or `docs/` prefix.
- Keep commits atomic and descriptive.
- Rebase or merge from the latest default branch before opening a PR when possible.

## Validation
- Run available checks before committing.
- If no automated checks exist, validate by running the updated utility directly and record what was executed.
- Include command outputs (or a concise summary) in the PR description.

## Pull requests
- Use concise PR titles with a prefix such as `feat:`, `fix:`, `chore:`, or `docs:`.
- PR descriptions should include:
  - What changed
  - Why it changed
  - How it was validated
  - Any follow-up tasks or known limitations
