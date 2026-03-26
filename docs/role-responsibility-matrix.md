# OctoAcme — Role Responsibility Matrix (RACI)

## Purpose

This matrix maps key project activities to team roles using the **RACI** model, so every team member knows exactly what is expected of them for each activity.

## How to Use This Matrix

| Code | Meaning |
|------|---------|
| **R** | **Responsible** — Does the work; executes the activity |
| **A** | **Accountable** — Owns the outcome; approves the result (only one per activity) |
| **C** | **Consulted** — Provides input or expertise before/during the activity |
| **I** | **Informed** — Kept up to date on progress and outcome |

**Rules of thumb:**
- Every activity must have exactly one **A** (accountable owner).
- There can be multiple **R** roles if work is shared.
- Minimize the number of **C** roles to keep decision-making efficient.
- **I** roles receive a summary or notification, not a detailed update.

---

## RACI Matrix

| Activity | PM (Project Mgr) | PdM (Product Mgr) | Developers | QA Lead | Release Manager | DevOps / On-call | UX Designer | Support Rep | Stakeholder Liaison |
|---|---|---|---|---|---|---|---|---|---|
| **Project initiation** | A | C | I | I | I | I | C | I | C |
| **Backlog prioritization** | C | **A** | C | C | I | I | C | C | I |
| **Sprint planning** | **A** | C | R | C | I | I | C | I | I |
| **Development** | I | I | **A/R** | C | I | C | C | I | I |
| **UX acceptance review** | I | C | C | C | I | I | **A/R** | I | I |
| **QA sign-off** | I | I | C | **A/R** | C | I | C | I | I |
| **Release coordination** | C | C | C | C | **A/R** | R | I | C | R |
| **Production deployment** | I | I | I | C | A | **R** | I | I | I |
| **Incident response** | I | I | C | I | C | **A/R** | I | R | R |
| **Post-mortem / retrospective** | **A** | C | R | R | C | R | C | C | I |
| **Stakeholder communication** | C | C | I | I | C | I | I | C | **A/R** |
| **Post-release support handoff** | I | I | I | C | R | C | I | **A/R** | C |

---

## Example: Sprint Planning Activity

> Use this example as a guide when reading the matrix.

**Activity:** Sprint Planning

| Role | Code | What this means in practice |
|------|------|-----------------------------|
| Project Manager | **A** | Facilitates the sprint planning meeting; owns the final sprint commitment |
| Product Manager | C | Reviews and clarifies backlog items before planning; confirms priorities |
| Developers | R | Estimates and selects items from the backlog to commit to in the sprint |
| QA Lead | C | Reviews acceptance criteria for testability; flags items needing QA prep |
| UX Designer | C | Confirms designs are ready for items scheduled in the sprint |
| Others | I | Notified of sprint scope and timeline after planning is complete |

---

## Guidance for Teams

1. **Review this matrix at project kickoff** to ensure every team member understands their role for each activity.
2. **Update the matrix when roles or activities change** — add a row for new activities or a column for new roles as the team evolves.
3. **Use it to resolve accountability disputes** — if two people think they own the same outcome, clarify using this matrix.
4. **Reference the [Roles and Personas doc](octoacme-roles-and-personas.md)** for full role descriptions, responsibilities, and interaction patterns.
5. **Reference the [Release Checklist](release-checklist.md)** for step-level ownership during the Release Coordination and Production Deployment activities.
