# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- **Patch**: hotfixes addressing critical production issues — no Release Manager assignment required, but Release Manager should be notified
- **Minor**: incremental features and improvements — **Release Manager must be assigned**
- **Major**: significant functionality or breaking changes — **Release Manager must be assigned**

## Release Manager Responsibilities
A Release Manager must be assigned for all Minor and Major releases. The Release Manager:
- Owns the release schedule and communicates the deployment window to Project Manager, QA Lead, DevOps/On-call, and Stakeholder Liaison
- Confirms all pre-release gates are met before issuing a go/no-go decision
- Ensures a rollback or mitigation plan is documented before deployment begins
- Coordinates post-deploy verification with QA Lead and DevOps/On-call
- Publishes release notes and notifies Support Representative when the release is live

See the [Roles and Personas](./octoacme-roles-and-personas.md) document for the full Release Manager role definition.

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- QA Lead sign-off obtained
- Release notes drafted and reviewed by Product Manager
- Rollback / mitigation plan documented
- Smoke tests prepared
- Release Manager assigned (Minor/Major only) and go/no-go decision recorded

## Deployment Checklist
For a reusable, copy-paste release checklist, see [release-checklist.md](./release-checklist.md).

- [ ] Release Manager assigned and release scope confirmed
- [ ] Deployment window scheduled and communicated (if needed)
- [ ] Backup or snapshot taken (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] QA Lead confirms staging sign-off
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Announce release to Stakeholder Liaison and Support Representative

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify DevOps/On-call
  - Rollback to last known-good release if necessary
  - Project Manager escalates to Stakeholder Liaison if business-impacting
  - Triage root cause and capture action items in a post-mortem

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
