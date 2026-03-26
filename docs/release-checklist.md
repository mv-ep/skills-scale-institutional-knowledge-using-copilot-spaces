# Release Checklist Template

> **How to use:** Copy this file (or the checklist sections below) into a release-specific document (e.g., `releases/v1.2.0-checklist.md`). Fill in the release details at the top, then work through each section in order. Update owners as needed for your team's structure.

---

## Release Details

| Field | Value |
|---|---|
| Release name / version | |
| Release type | Patch / Minor / Major |
| Target release date | |
| Release Manager | |
| QA Lead | |
| DevOps/On-call | |
| Stakeholder Liaison | |

---

## 1. Pre-Release Checks

### Scope & Readiness
- [ ] Release scope confirmed and communicated to team (**Release Manager**)
- [ ] All PRs targeting this release are merged (**Developers**)
- [ ] CI pipeline is green (tests, lint, security scans) (**DevOps/On-call**)
- [ ] No P0/P1 open defects against this release scope (**QA Lead**)
- [ ] Feature flags configured correctly for this release (**Developers**)

### QA Sign-Off
- [ ] Test plan reviewed and approved (**QA Lead**)
- [ ] Smoke tests executed on staging environment (**QA Lead**)
- [ ] Acceptance criteria verified for all included stories (**QA Lead**)
- [ ] Accessibility and usability review completed if UX changes are included (**UX Designer**)
- [ ] **QA Lead written sign-off recorded:** _Date/Link:_ ________________

### Documentation & Communication
- [ ] Release notes drafted (**Release Manager**) and reviewed (**Product Manager**)
- [ ] Migration steps documented for any breaking changes (**Developers**)
- [ ] Rollback plan documented and reviewed by **Release Manager** and **DevOps/On-call**
- [ ] Deployment window scheduled and confirmed (**Release Manager** + **DevOps/On-call**)
- [ ] **Stakeholder Liaison** notified of release schedule
- [ ] **Support Representative** briefed on known issues and upcoming changes

### Go / No-Go Decision
- [ ] **Release Manager** confirms all pre-release gates are satisfied
- [ ] Go/No-Go decision recorded: **Go ☐ / No-Go ☐** — Date: _____________ — By: _________________

---

## 2. Deployment Steps

- [ ] Backup or snapshot of production data/state taken (if applicable) (**DevOps/On-call**)
- [ ] Deploy to staging environment (**DevOps/On-call**)
- [ ] Staging smoke tests pass (**QA Lead**)
- [ ] Deploy to production using automated pipeline (**DevOps/On-call**)
- [ ] Monitor deployment logs and error rates in real time (**DevOps/On-call**)
- [ ] Confirm deployment completes without rollback triggers (**Release Manager**)

---

## 3. Rollback / Mitigation

> Complete this section **before** deployment and keep it accessible during the release window.

- **Rollback trigger criteria:** _(e.g., error rate > X%, critical workflow broken)_
- **Rollback procedure:** _(link to runbook or describe steps)_
- **Rollback owner:** (**DevOps/On-call** executes; **Release Manager** approves)
- **Estimated rollback time:** ____________
- **Communication owner during rollback:** **Stakeholder Liaison**

### Rollback Execution Checklist (if triggered)
- [ ] **Release Manager** issues rollback decision
- [ ] **DevOps/On-call** executes rollback to last known-good release
- [ ] **Release Manager** confirms rollback success
- [ ] **Project Manager** assesses business impact and escalates if needed
- [ ] **Stakeholder Liaison** notifies affected stakeholders of rollback and ETA for fix
- [ ] Incident ticket created for root cause analysis (**Project Manager**)

---

## 4. Post-Deploy Verification

- [ ] Run post-deploy verification test suite (**QA Lead** + **DevOps/On-call**)
- [ ] Confirm key metrics are within expected range:
  - [ ] Error rate: ________ (baseline: ________)
  - [ ] P95 latency: ________ (baseline: ________)
  - [ ] Key user flows functional (manual check if needed)
- [ ] Confirm no unexpected alerts firing (**DevOps/On-call**)
- [ ] **QA Lead** records post-deploy verification result: _Pass ☐ / Fail ☐_

---

## 5. Communication & Support Handoff

- [ ] Release notes published to the appropriate channel (**Release Manager**)
- [ ] **Stakeholder Liaison** sends release announcement to stakeholders
- [ ] **Support Representative** receives final release summary including:
  - Known issues and workarounds
  - Links to release notes
  - Escalation path for critical defects
- [ ] Support team enabled and monitoring post-release issue volume (**Support Representative**)
- [ ] Post-release retrospective scheduled (**Project Manager**):
  - Required for Major releases
  - Recommended for Minor releases

---

## Notes & Action Items

| Item | Owner | Due Date | Status |
|---|---|---|---|
| | | | |
| | | | |
