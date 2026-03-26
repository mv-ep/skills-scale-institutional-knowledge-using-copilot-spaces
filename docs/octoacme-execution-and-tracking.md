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

| Level | Trigger | Responsible Role | Action |
|-------|---------|-----------------|--------|
| 1 | Blocker raised in standup | Developer or QA Lead | Team triage; owner identified within 24 hours |
| 2 | Blocker unresolved after 24 h, or cross-team dependency | Project Manager | Escalates to Product Lead and dependent team leads; documents in risk register |
| 3 | Business-impacting or customer-facing issue | PM + Stakeholder Liaison | Sponsor-level escalation; Stakeholder Liaison prepares business-impact summary |

## Execution Checklist

### Pre-Sprint / Kickoff
- [ ] Acceptance criteria reviewed and marked testable by **QA Lead** before sprint planning
- [ ] **UX Designer** designs reviewed and assets handed off to Developers
- [ ] Branching and PR conventions confirmed in repo

### During Development
- [ ] PRs are small (≤ 400 lines when possible), linked to issues, and include acceptance criteria
- [ ] CI (tests + lint + security scan) is green before requesting review
- [ ] **QA Lead** reviews PR description for testability; adds or updates test plan
- [ ] At least one peer approval before merge (or team-defined policy)

### QA Acceptance Gate
- [ ] Feature deployed to staging environment by **Operations Engineer**
- [ ] **QA Lead** executes test plan; defects filed and triaged
- [ ] **UX Designer** completes UX acceptance review in staging
- [ ] **QA Lead** issues written sign-off (or lists outstanding blocking defects)
- [ ] No PRs merged to release branch without QA sign-off

### Pre-Deployment Gate
- [ ] **Release Manager** confirms all approved PRs are merged to release branch
- [ ] **Release Manager** confirms rollback plan is documented and tested
- [ ] **Operations Engineer** verifies infrastructure readiness (capacity, secrets, monitoring)
- [ ] **Support Representative** confirms knowledge base and support docs are updated

### Post-Deployment
- [ ] **Operations Engineer** and **Release Manager** run post-deploy smoke tests
- [ ] **Release Manager** distributes final release notes
- [ ] **Stakeholder Liaison** sends release announcement
- [ ] Risk register updated; sprint retrospective scheduled

## Execution Role Responsibilities

| Step | Primary Responsible Role |
|------|--------------------------|
| Write release notes | Product Manager (PdM) with input from Developers |
| Create QA test plan | QA Lead |
| Perform smoke tests (staging) | QA Lead + Operations Engineer |
| Issue QA sign-off | QA Lead |
| Merge PRs to release branch | Release Manager (after QA sign-off) |
| Confirm rollback plan | Release Manager |
| Execute production deployment | Operations Engineer (Release Manager coordinates) |
| Run post-deploy verification | Operations Engineer + Release Manager |
| Notify stakeholders of release | Stakeholder Liaison |
| Update support documentation | Support Representative |
| Track blockers and risks | Project Manager |
| Conduct UX acceptance review | UX Designer |
