# Role Responsibility Matrix

> **How to use:** This RACI-style matrix maps common project activities to roles. Copy this template into your project docs and customize for your team. For each cell, assign one of:
> - **R** — Responsible: does the work
> - **A** — Accountable: owns the outcome and makes decisions
> - **C** — Consulted: provides input before/during the activity
> - **I** — Informed: notified of progress or outcomes

---

## RACI Key

| Code | Meaning |
|---|---|
| R | Responsible — performs the task |
| A | Accountable — owns the outcome; approves deliverables |
| C | Consulted — provides input; two-way communication |
| I | Informed — kept up to date; one-way communication |

> **Rule:** Each activity should have exactly one **A** (accountable). Multiple **R**s are acceptable. Avoid assigning too many **C**s to keep decisions fast.

---

## Matrix

| Activity | Project Manager (PM) | Product Manager (PdM) | Developers | QA Lead | Release Manager | DevOps / On-call | UX Designer | Support Representative | Stakeholder Liaison |
|---|---|---|---|---|---|---|---|---|---|
| Project initiation | A | C | I | I | I | I | C | I | I |
| Backlog prioritization | C | A | C | C | I | I | C | C | I |
| Sprint planning | A | C | R | C | C | I | C | I | I |
| Feature development | I | C | A/R | C | I | C | C | I | I |
| UX design & review | C | C | C | C | I | I | A/R | I | I |
| QA sign-off | C | C | C | A/R | C | I | C | I | I |
| Release coordination | C | C | C | C | A/R | R | I | C | C |
| Deployment execution | I | I | C | C | A | R | I | I | I |
| Post-deploy verification | I | I | C | R | A | R | I | I | I |
| Incident response | C | I | C | C | C | A/R | I | C | I |
| Stakeholder communication | C | C | I | I | C | I | I | C | A/R |
| Post-mortem / retrospective | A | C | R | R | R | R | C | C | I |

---

## Guidance Notes

1. **Project initiation** — PM drives kickoff, charter, and initial scope. PdM and UX Designer are consulted to align on vision.
2. **Backlog prioritization** — PdM is accountable for what gets built. PM, QA Lead, and Support Representative provide input based on delivery constraints and customer feedback.
3. **Sprint planning** — PM owns logistics; Developers, QA Lead, and Release Manager are consulted on capacity and release implications.
4. **Feature development** — Developers are accountable for implementation. DevOps/On-call is consulted for infrastructure or pipeline changes.
5. **UX design & review** — UX Designer is accountable; Developers and QA Lead are consulted to ensure feasibility and testability.
6. **QA sign-off** — QA Lead is accountable for sign-off before a feature or release moves forward.
7. **Release coordination** — Release Manager is accountable for the end-to-end release. DevOps/On-call is responsible for executing deployment steps.
8. **Deployment execution** — DevOps/On-call is responsible; Release Manager is accountable for the go/no-go decision.
9. **Post-deploy verification** — Release Manager is accountable; QA Lead and DevOps/On-call are both responsible.
10. **Incident response** — DevOps/On-call is accountable for immediate technical response. PM escalates if business impact is confirmed.
11. **Stakeholder communication** — Stakeholder Liaison is accountable; PM and Release Manager provide content and timing guidance.
12. **Post-mortem / retrospective** — PM facilitates and is accountable; all delivery roles are responsible for contributing.

---

## Example: Customized for Project "Acme-Alpha"

| Activity | PM (Alex) | PdM (Sam) | Dev Lead (Jordan) | QA Lead (Casey) | Release Manager (Riley) |
|---|---|---|---|---|---|
| Sprint planning | A | C | R | C | C |
| Feature development | I | C | A/R | C | I |
| QA sign-off | C | C | C | A/R | C |
| Release coordination | C | C | C | C | A/R |

---

## Related Documents

- [octoacme-roles-and-personas.md](octoacme-roles-and-personas.md) — Full persona descriptions including responsibilities, goals, and cross-role interactions
- [release-checklist.md](release-checklist.md) — Reusable release checklist template
- [octoacme-execution-and-tracking.md](octoacme-execution-and-tracking.md) — Execution role responsibilities and escalation ownership
