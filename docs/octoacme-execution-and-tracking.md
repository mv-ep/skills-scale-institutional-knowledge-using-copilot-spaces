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
- **Level 1 — Team triage**: Developer or QA Lead raises blocker in daily standup; team attempts same-day resolution
- **Level 2 — PM escalation**: Project Manager escalates to Product Manager and dependent teams within 24 hours if unresolved; Release Manager notified if the blocker affects a release window
- **Level 3 — Sponsor escalation**: Project Manager escalates to Sponsor or executive stakeholder via Stakeholder Liaison for business-impacting issues unresolved after 48 hours

## Execution Role Responsibilities

| Step | Primary Responsible Role |
|---|---|
| Write and update release notes | Release Manager (drafts); Product Manager (reviews content) |
| Perform smoke tests | QA Lead (coordinates); Developers (execute) |
| Notify stakeholders of release | Release Manager (triggers); Stakeholder Liaison (distributes) |
| Update project board and status | Project Manager |
| Coordinate test plan for PRs | QA Lead (owns plan); PR Author (provides test evidence) |
| Verify CI/CD pipeline health | DevOps/On-call |
| Confirm rollback plan before deploy | Release Manager |
| File post-release issues | Support Representative |

## Execution Checklist

### Pre-sprint / Pre-milestone
- [ ] Acceptance criteria defined and reviewed by Product Manager and UX Designer
- [ ] Test plan prepared by QA Lead and shared with Developers
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests, lint, and security scanning
- [ ] Regular demos scheduled with Stakeholder Liaison or Product Manager

### During sprint / Development
- [ ] PRs linked to issues with acceptance criteria included
- [ ] PR author coordinates with QA Lead on test evidence before requesting review
- [ ] Code review approval obtained from at least one peer
- [ ] CI checks pass (tests, lint, security scan) before merge

### Pre-release acceptance gate
- [ ] QA Lead verifies test sign-off and marks feature ready for release branch
- [ ] Product Manager validates acceptance criteria are met
- [ ] Release Manager confirms rollback plan is documented (see [Release Checklist](./release-checklist.md))
- [ ] Release notes drafted and reviewed

### Post-release
- [ ] Smoke tests executed by QA Lead / Developers post-deploy
- [ ] Release Manager sends release announcement to Stakeholder Liaison and Support Representative
- [ ] Support Representative monitors for user-reported issues and files any new bugs
- [ ] Risk register updated by Project Manager
- [ ] Retrospective action items captured
