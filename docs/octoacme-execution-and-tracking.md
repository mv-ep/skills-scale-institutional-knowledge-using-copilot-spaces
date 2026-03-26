# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation

| Level | Trigger | Owner | Action |
|---|---|---|---|
| Level 1 | Blocker affects one team member or a single story | **Developer / PR Owner** | Raise in daily standup; team triages same day |
| Level 2 | Blocker affects sprint goal or a cross-team dependency | **Project Manager** | PM escalates to Product Lead and dependent team leads within 24 hours |
| Level 3 | Blocker has business or customer impact beyond the team | **Product Manager + Stakeholder Liaison** | Sponsor-level escalation; Stakeholder Liaison notifies affected parties |

## Execution Role Responsibilities

| Workflow Step | Primary Owner | Supporting Roles |
|---|---|---|
| Write release notes | **Release Manager** | Product Manager reviews for accuracy |
| Perform smoke tests | **QA Lead** | Developers support environment setup |
| Merge to release branch | **PR Owner (Developer)** | QA Lead provides written sign-off first |
| Schedule deployment window | **Release Manager** | DevOps/On-call confirms environment readiness |
| Execute deployment | **DevOps/On-call** | Release Manager monitors go/no-go |
| Post-deploy verification | **QA Lead + DevOps/On-call** | Release Manager reviews results |
| Notify stakeholders of release | **Stakeholder Liaison** | Release Manager provides release summary |
| Triage post-release defects | **Support Representative** | Files issues; PM/PdM prioritizes |

## Execution Checklist

### Development Phase
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint
- [ ] PR owner links issue and lists acceptance criteria in PR description
- [ ] **PR owner** coordinates with **QA Lead** to confirm test plan before review request
- [ ] **QA Lead** verifies test coverage and provides written sign-off before merge to release branch
- [ ] Code review approved by at least one team member per policy

### Pre-Release Gate
- [ ] **Release Manager** assigned for Minor and Major releases
- [ ] **Release Manager** confirms rollback plan is documented before deployment
- [ ] **QA Lead** completes smoke test run on staging and records results
- [ ] Release notes drafted by **Release Manager** and reviewed by **Product Manager**
- [ ] **Stakeholder Liaison** notified of release schedule

### Execution & Monitoring
- [ ] Regular demos scheduled
- [ ] **DevOps/On-call** confirms deployment pipeline is green before release window
- [ ] Risk register updated weekly by **Project Manager**
- [ ] Post-deploy verification completed by **QA Lead** and **DevOps/On-call**
- [ ] **Support Representative** briefed on known issues and workarounds before release announcement

See [release-checklist.md](release-checklist.md) for the full reusable release checklist template.
