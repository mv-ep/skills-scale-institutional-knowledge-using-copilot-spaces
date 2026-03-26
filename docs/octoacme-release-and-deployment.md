# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types

- **Patch:** hotfixes addressing critical production issues — no Release Manager required, but Operations Engineer must confirm rollback readiness.
- **Minor:** incremental features and improvements — **Release Manager required**.
- **Major:** significant functionality or breaking changes — **Release Manager required**; Stakeholder Liaison must coordinate external communications.

## Release Manager Responsibilities (Minor and Major Releases)

- Own and drive the release checklist from pre-release through post-deploy verification.
- Schedule the deployment window and communicate it to all stakeholders via the Stakeholder Liaison.
- Gate production deployment on written QA sign-off from the QA Lead.
- Confirm a documented rollback plan exists and has been reviewed by the Operations Engineer before deployment.
- Author or review release notes in collaboration with the Product Manager.
- Lead the post-deploy verification call and authorize rollback if needed.
- Ensure the Support Representative is briefed before the release goes live.

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted
- Rollback / mitigation plan documented
- Smoke tests prepared

## Deployment Checklist

> **Tip:** For a copy-paste-ready checklist, see [docs/release-checklist.md](release-checklist.md).

### Pre-Release
- [ ] All acceptance criteria met and PRs merged to release branch (**Release Manager** confirms)
- [ ] CI and security scans passing on release branch (**Operations Engineer** confirms)
- [ ] QA Lead has issued written sign-off
- [ ] UX acceptance review completed or deferred issues documented
- [ ] Release notes drafted and reviewed (**PdM** + **Release Manager**)
- [ ] Rollback / mitigation plan documented and reviewed (**Release Manager** + **Operations Engineer**)
- [ ] Deployment window scheduled and communicated (**Release Manager** via **Stakeholder Liaison**)
- [ ] Support Representative briefed; knowledge base updated

### Deploy
- [ ] Backup or snapshot taken (if applicable) — **Operations Engineer**
- [ ] Deploy to staging and run smoke tests — **Operations Engineer** + **QA Lead**
- [ ] **Release Manager** approves promotion to production
- [ ] Deploy to production (automated pipeline preferred) — **Operations Engineer**

### Post-Deploy Verification
- [ ] Run post-deploy smoke tests — **Operations Engineer** + **Release Manager**
- [ ] Confirm key metrics (error rate, latency, usage) within expected range — **Operations Engineer**
- [ ] **Release Manager** declares release successful or initiates rollback

### Communication
- [ ] **Release Manager** distributes final release notes
- [ ] **Stakeholder Liaison** sends release announcement to stakeholders
- [ ] **Support Representative** confirms support documentation is live

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
