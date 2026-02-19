# Selected Build Plan: AgencyOS CRM + Lead Manager

## Why this project
It solves a direct business problem for service organizations: lead leakage and poor sales-to-delivery handoff.

## Hackathon scope (48-72 hours)
### Demo goals
- Capture lead from web form/email
- Auto-score lead quality
- Move leads through pipeline stages
- Generate proposal draft from template + lead context
- Trigger handoff checklist when deal is marked won

### Non-goals for hackathon
- Complex billing and accounting sync
- Enterprise SSO
- Full analytics warehouse

## Architecture (fast but production-aware)
- Frontend: Next.js
- Backend API: FastAPI
- DB: PostgreSQL
- Queue: Redis + worker
- Auth: Clerk/Auth0 (quick setup)
- Deploy: Vercel (frontend) + Render/Fly (backend)

## Agent-first work breakdown
1. **PM Agent**: user stories + acceptance criteria
2. **Architect Agent**: API contracts + schema + flow diagrams
3. **Backend Agent**: lead, deal, activity, proposal endpoints
4. **Frontend Agent**: pipeline board, lead form, proposal page
5. **QA Agent**: smoke tests and e2e happy path
6. **DevOps Agent**: CI + deploy preview + secrets template
7. **Security Agent**: RBAC rules and dependency scan pass
8. **Demo Agent**: sample data, scripted demo path, fallback screenshots

## Timeline
### Day 0 (prep)
- Confirm scope and success metric: “lead response flow under 2 minutes”
- Prepare API keys and sandbox accounts

### Day 1
- Scaffold repo, models, and API
- Build lead intake and pipeline list
- Ship first deployed preview

### Day 2
- Add proposal generation and follow-up automation
- Add activity timeline and stage transitions
- Add smoke tests + error monitoring

### Day 3 (if 72-hour format)
- Polish UI
- Add dashboard metrics (new leads, stage conversion)
- Rehearse demo and prepare roadmap slide

## Demo script (5-7 minutes)
1. Submit a lead
2. Watch auto-scoring + stage assignment
3. Open lead and generate proposal draft
4. Mark deal as won
5. Show handoff checklist created automatically
6. Show dashboard and audit trail

## Productionization after hackathon (2-4 weeks)
- Add audit logs and tenant isolation
- Add role-based permissions
- Add retries and dead-letter queue for automation failures
- Add integration adapters (email/calendar/Slack)
- Add observability dashboards and SLO alerts
