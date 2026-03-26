# Release Checklist Template

> **Usage:** Copy this file or copy-paste the sections below into a release-specific document (e.g., `docs/releases/v1.2.0-checklist.md`). Fill in the blanks and check off each item as it is completed. Update the **Owner** column with the name or GitHub handle responsible.

---

## Release Metadata

| Field | Value |
|-------|-------|
| Release name / version | |
| Target release date | |
| Release Manager | |
| QA Lead | |
| Operations Engineer | |
| Stakeholder Liaison | |

---

## Pre-Release

- [ ] All feature PRs are merged to the release branch
  - **Owner:** Release Manager
- [ ] CI pipeline (build, tests, security scan) is green on release branch
  - **Owner:** Operations Engineer
- [ ] QA Lead has issued written sign-off
  - **Owner:** QA Lead
- [ ] UX acceptance review completed; any deferred issues documented with issue links
  - **Owner:** UX Designer
- [ ] Release notes drafted and reviewed
  - **Owner:** PdM + Release Manager
- [ ] Rollback plan documented (target version, steps, decision criteria)
  - **Owner:** Release Manager + Operations Engineer
- [ ] Deployment window confirmed and communicated to stakeholders
  - **Owner:** Stakeholder Liaison
- [ ] Support Representative briefed; user-facing documentation updated
  - **Owner:** Support Representative
- [ ] Infrastructure readiness confirmed (capacity, configuration, feature flags, secrets)
  - **Owner:** Operations Engineer

---

## Deployment Steps

- [ ] Create a release tag in version control (e.g., `v1.2.0`)
  - **Owner:** Release Manager
- [ ] Take a backup or snapshot of the database / persistent data (if applicable)
  - **Owner:** Operations Engineer
- [ ] Deploy release branch to **staging** environment
  - **Owner:** Operations Engineer
- [ ] Run smoke tests in staging
  - **Owner:** QA Lead + Operations Engineer
- [ ] **Release Manager** approves promotion to production
- [ ] Deploy to **production** environment (automated pipeline preferred)
  - **Owner:** Operations Engineer
- [ ] Monitor deployment logs and error rates in real time
  - **Owner:** Operations Engineer

---

## Rollback / Mitigation

If a critical issue is detected during or after deployment:

- [ ] **Operations Engineer** alerts **Release Manager** immediately
- [ ] **Release Manager** makes go/no-go decision on rollback
- [ ] If rollback is initiated:
  - [ ] Operations Engineer executes rollback to last known-good version
  - [ ] Release Manager notifies stakeholders via Stakeholder Liaison
  - [ ] Support Representative prepares user-facing status communication
- [ ] Incident documented in the risk register
- [ ] Post-mortem scheduled within 48 hours of resolution

---

## Post-Deploy Verification

- [ ] Run automated post-deploy smoke tests
  - **Owner:** Operations Engineer + QA Lead
- [ ] Verify key metrics are within expected range (error rate, latency, throughput)
  - **Owner:** Operations Engineer
- [ ] Check feature flags are set to intended state for production
  - **Owner:** Operations Engineer
- [ ] Validate any database migrations completed successfully
  - **Owner:** Operations Engineer
- [ ] **Release Manager** declares the release successful

---

## Communication & Support Handoff

- [ ] Final release notes distributed to stakeholders
  - **Owner:** Release Manager
- [ ] Release announcement sent (internal + external as appropriate)
  - **Owner:** Stakeholder Liaison
- [ ] Support documentation published / knowledge base updated
  - **Owner:** Support Representative
- [ ] Support Representative confirms readiness to handle incoming queries
- [ ] Release retrospective or post-deploy review scheduled
  - **Owner:** Project Manager

---

## Sign-off

| Role | Name | Date | Signed off |
|------|------|------|------------|
| Release Manager | | | ☐ |
| QA Lead | | | ☐ |
| Operations Engineer | | | ☐ |
| Product Manager (PdM) | | | ☐ |
