# OctoAcme — Role Responsibility Matrix

This matrix provides a RACI-style overview of who is **R**esponsible, **A**ccountable, **C**onsulted, or **I**nformed for key activities across the OctoAcme project lifecycle.

For full role definitions see [Roles and Personas](./octoacme-roles-and-personas.md).

---

## How to Use This Matrix

| Code | Meaning |
|------|---------|
| **R** | **Responsible** — does the work |
| **A** | **Accountable** — owns the outcome; approves or signs off |
| **C** | **Consulted** — provides input before or during; two-way communication |
| **I** | **Informed** — notified of outcomes; one-way communication |

**Rules of thumb:**
- Each activity should have exactly **one A** (accountable owner).
- There can be multiple R, C, and I entries.
- Minimise unnecessary C/I entries to reduce noise.
- Update this matrix whenever roles or major activities change.

---

## RACI Matrix

| Activity | PM (Project Mgr) | PdM (Product Mgr) | Developers | QA Lead | Release Manager | DevOps / On-call | UX Designer | Support Rep | Stakeholder Liaison |
|---|---|---|---|---|---|---|---|---|---|
| Project initiation | A | C | I | I | I | I | C | I | I |
| Backlog prioritization | C | A | C | C | I | I | C | C | I |
| Sprint planning | A | C | C | C | I | I | C | I | I |
| Development | I | C | R/A | C | I | C | C | — | — |
| QA sign-off | C | C | R | A | C | — | C | — | — |
| Release coordination | C | I | C | C | A | R | — | I | I |
| Deployment | I | I | C | C | A | R | — | — | — |
| Post-deploy verification | I | I | R | R/A | C | C | — | — | — |
| Stakeholder communication | C | C | — | — | R | — | — | C | A |
| Incident response | C | I | C | C | C | R/A | — | I | C |
| Post-mortem / retrospective | A | C | R | C | C | C | C | C | I |
| User feedback collection | I | A | — | — | — | — | C | R | C |

> **Legend:** `—` = not involved in this activity. `R/A` = one person holds both roles (common in small teams).

---

## Example: Release Coordination

The table below shows a worked example for the **Release coordination** activity:

| Role | RACI | What They Do |
|---|---|---|
| Release Manager | **A** | Owns the release schedule, issues go/no-go, publishes release notes |
| DevOps/On-call | **R** | Executes the deployment and monitors infrastructure |
| QA Lead | **C** | Provides test sign-off before promotion to release branch |
| Project Manager | **C** | Confirms scope alignment and timeline |
| Support Representative | **I** | Notified once release is live; begins monitoring user feedback |
| Stakeholder Liaison | **I** | Receives release notes for external distribution |

---

## Updating the Matrix

1. Propose changes via a PR to this file.
2. Tag the Project Manager and Product Manager as reviewers.
3. Announce updates to the team in the weekly delivery sync.
