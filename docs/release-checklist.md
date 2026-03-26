# OctoAcme — Reusable Release Checklist

Use this checklist for every Minor or Major release. Copy the relevant sections into your release issue or PR. Reference: [Release & Deployment Guide](./octoacme-release-and-deployment.md).

**Release:** `<!-- release name / version -->`
**Release Manager:** `<!-- @handle -->`
**Target Date:** `<!-- YYYY-MM-DD -->`

---

## Pre-Release

### Scope & Readiness
- [ ] Release scope confirmed with Product Manager and Project Manager
- [ ] All in-scope PRs merged to release branch
- [ ] CI passing (tests, lint, security scan) on release branch

### Quality Sign-off
- [ ] QA Lead has reviewed and signed off on all in-scope features
- [ ] Regression tests updated and passing
- [ ] Exploratory / acceptance testing completed for new UI features (UX Designer / QA Lead)

### Release Preparation
- [ ] Release notes drafted and reviewed by Product Manager
- [ ] Migration or configuration steps documented (if applicable)
- [ ] Rollback plan documented and reviewed by Release Manager and DevOps/On-call
- [ ] Deployment window confirmed with DevOps/On-call and Project Manager
- [ ] Support Representative briefed on known issues and support expectations
- [ ] Stakeholder Liaison notified of upcoming release

---

## Deployment

### Staging
- [ ] Deployed to staging environment
- [ ] Smoke tests executed on staging (QA Lead / Developers)
- [ ] Release Manager confirms go/no-go decision for production deployment

### Production
- [ ] Backup or snapshot taken (if applicable)
- [ ] Deployed to production via automated pipeline (preferred)
- [ ] Deployment logs reviewed by DevOps/On-call — no critical errors observed

---

## Post-Deploy Verification

- [ ] Smoke tests executed on production (QA Lead / Developers)
- [ ] Key metrics and alerts reviewed by DevOps/On-call (error rate, latency, usage)
- [ ] Rollback trigger criteria confirmed as not met — release declared stable
- [ ] Any issues found are logged as GitHub Issues and triaged by QA Lead and Project Manager

---

## Rollback / Mitigation

> Complete this section only if a post-deploy issue is detected.

- [ ] Incident triggered and DevOps/On-call notified
- [ ] Decision made: rollback vs. hotfix (Release Manager + Project Manager)
- [ ] If rollback: previous known-good release redeployed by DevOps/On-call
- [ ] If hotfix: hotfix PR created, reviewed, and deployed following Patch release process
- [ ] Project Manager escalates to Stakeholder Liaison if business-impacting
- [ ] Root cause and action items captured for post-mortem

---

## Communication & Support Handoff

- [ ] Release announcement sent by Release Manager to Stakeholder Liaison
- [ ] Stakeholder Liaison distributes release notes to external stakeholders
- [ ] Support Representative updated with release notes and known issues
- [ ] Internal teams notified (e.g., Slack announcement or email)
- [ ] Release tagged in version control and linked from project board

---

> **Tip:** Archive completed checklists in the release PR or a dedicated release issue so the team has a full audit trail.
