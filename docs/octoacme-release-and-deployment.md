# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements — requires an assigned **Release Manager**
- Major: significant functionality or breaking changes — requires an assigned **Release Manager**

## Release Manager Responsibilities

For Minor and Major releases, a Release Manager must be explicitly assigned. The Release Manager:
- Owns the go/no-go decision before each deployment
- Verifies that all pre-release gates are satisfied (CI, QA sign-off, release notes, rollback plan)
- Coordinates the deployment window with **DevOps/On-call**
- Communicates release status to **Stakeholder Liaison** and **Support Representative**
- Maintains and, if needed, triggers the rollback plan
- Facilitates a post-release review for Major releases

See [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) for the full Release Manager persona description.

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans
- Release notes drafted (by **Release Manager**, reviewed by **Product Manager**)
- Rollback / mitigation plan documented and confirmed by **Release Manager**
- Smoke tests prepared and signed off by **QA Lead**

## Release Checklist

### Pre-Release
- [ ] Release Manager assigned (required for Minor and Major releases)
- [ ] All PRs targeting this release are merged and CI is green
- [ ] QA Lead has completed smoke tests on staging and provided written sign-off
- [ ] Release notes drafted and reviewed
- [ ] Rollback plan documented and reviewed by Release Manager and DevOps/On-call
- [ ] Deployment window scheduled and communicated to relevant teams
- [ ] Stakeholder Liaison notified of upcoming release

### Deployment
- [ ] Backup or snapshot taken (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] Release Manager issues go/no-go decision
- [ ] Deploy to production (automated pipeline preferred)
- [ ] DevOps/On-call monitors deployment and confirms no error-rate spike

### Post-Deploy Verification
- [ ] Run post-deploy verification tests (QA Lead + DevOps/On-call)
- [ ] Confirm key metrics are within expected range (error rate, latency, usage)
- [ ] Support Representative briefed on known issues and workarounds
- [ ] Stakeholder Liaison announces release to stakeholders

### Communication
- [ ] Release notes published
- [ ] Support Representative has release summary and known issues list
- [ ] Post-release retrospective scheduled (required for Major; recommended for Minor)

See [release-checklist.md](release-checklist.md) for the standalone reusable release checklist template.

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - **DevOps/On-call** triggers incident response and notifies **Release Manager**
  - **Release Manager** decides whether to rollback to last known-good release
  - **Project Manager** escalates to stakeholders if business impact is confirmed
  - **Stakeholder Liaison** communicates status to affected stakeholders
  - Triage root cause and capture action items in post-mortem

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
