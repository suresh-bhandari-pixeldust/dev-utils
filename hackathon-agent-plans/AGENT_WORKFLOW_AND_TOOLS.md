# Agent Workflow and Tools

## Delivery model
Use a multi-agent pipeline with human approval checkpoints at architecture, security, and release stages.

## Agent roles and tools
### 1) Planner / PM Agent
- Tools: Notion/Linear/Jira API, prompt templates
- Output: PRD, stories, acceptance criteria, definition of done

### 2) Architect Agent
- Tools: Mermaid, OpenAPI generator, ADR templates
- Output: system diagram, API contracts, DB schema decisions

### 3) Implementation Agents (FE/BE)
- Tools: coding agent + repo CI
- Output: feature branches, tests, docs, migration scripts

### 4) QA Agent
- Tools: Playwright, Pytest/Jest, contract tests
- Output: automated test suite + regression report

### 5) DevOps Agent
- Tools: GitHub Actions, Docker, Terraform (optional in hackathon)
- Output: CI/CD pipeline, environment configs, deploy previews

### 6) Security Agent
- Tools: Semgrep, dependency audit, secret scanning
- Output: risk report and remediation PRs

### 7) Release Agent
- Tools: changelog generator, release checklist
- Output: release notes, rollback plan, go-live checklist

## Branching model
- `docs/*` for planning/docs
- `feat/*` for features
- `fix/*` for bug fixes
- short-lived branches + PR-based merge only

## Required quality gates
- Lint + format checks
- Unit tests for core business logic
- One e2e critical path test
- No high-severity vulnerabilities
- All environment variables documented

## Hackathon command checklist
- `npm run lint` or equivalent
- `npm test` / `pytest`
- `npx playwright test` (critical flow only)
- `docker compose up` (if local stack used)
