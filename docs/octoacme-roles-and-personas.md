# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises.

---

## Developers

### Role Summary
Developers design, build, test, and deliver software components. They collaborate with product and project leads to implement features that meet acceptance criteria and quality standards.

### Responsibilities
- Implement features and fixes to meet acceptance criteria
- Write and maintain tests and documentation
- Participate in design and code reviews
- Assist in estimating and planning work
- Help identify technical risks and propose mitigations

### Goals
- Deliver reliable, maintainable code
- Reduce cycle time from idea to production
- Maintain high test coverage and observability

### Typical Communication
- Daily standups and sprint planning
- PR descriptions and code review comments
- Technical design docs when needed

---

## Product Managers

### Role Summary
Product Managers define what should be built to deliver customer and business value. They own the product vision, prioritize the backlog, and measure outcomes.

### Responsibilities
- Define problem statements and success metrics
- Prioritize the roadmap and backlog
- Collaborate with stakeholders and engineering on trade-offs
- Validate solutions through user research and metrics

### Goals
- Maximize customer value and impact
- Make clear, data-driven prioritization decisions
- Ensure product-market fit and usability

### Typical Communication
- Weekly alignment with PM and engineering leads
- Roadmap updates and stakeholder briefings
- Acceptance criteria and feature specs

---

## Project Managers

### Role Summary
Project Managers coordinate delivery activities, manage schedules, risks, and communications. They enable the team to deliver on commitments efficiently.

### Responsibilities
- Create and maintain project plans and timelines
- Manage risks, dependencies, and resource constraints
- Facilitate meetings (kickoff, planning, retrospectives)
- Ensure consistent project documentation and status reporting
- Coordinate cross-team and stakeholder communication

### Goals
- Deliver projects on time and within scope
- Minimize unplanned work and escalations
- Maintain transparency and alignment across stakeholders

### Typical Communication
- Weekly status updates and stakeholder reports
- Risk registers and decision logs
- Coordination via project boards and meeting facilitation

---

---

## Release Manager

### Role Summary
The Release Manager owns the end-to-end coordination of software releases. They ensure that deployment activities are planned, validated, communicated, and reversible.

### Responsibilities
- Own the release schedule and coordinate release windows with stakeholders
- Verify that all pre-release gates (CI, QA sign-off, release notes, rollback plan) are satisfied before deployment
- Lead or delegate go/no-go decisions for each release
- Coordinate with DevOps/On-call to execute and monitor deployments
- Communicate release status to stakeholders before and after deployment
- Maintain the rollback plan and trigger rollback if required
- Facilitate post-release retrospectives for Major and Minor releases

### Goals
- Ship releases predictably with minimal disruption to users
- Ensure every release has a documented rollback path
- Reduce release-related incidents through thorough pre-release validation

### Typical Communication / Interactions
- Works with **Project Manager** to align the release schedule with the project timeline
- Works with **QA Lead** to confirm test sign-off before each release
- Works with **DevOps/On-call** to schedule deployment windows and monitor rollout
- Works with **Product Manager** to validate that release scope matches intended delivery
- Notifies **Stakeholder Liaison** and **Support Representative** of upcoming and completed releases

---

## QA Lead

### Role Summary
The QA Lead defines quality standards, owns the test strategy, and ensures that acceptance criteria are verified before features move to production.

### Responsibilities
- Define and maintain the test strategy (unit, integration, end-to-end, manual)
- Review and approve acceptance criteria with the Product Manager
- Coordinate testing activities across Developers and QA team members
- Provide formal test sign-off before merging to the release branch
- Track defects, regressions, and their resolution
- Contribute to post-release quality retrospectives

### Goals
- Prevent defects from reaching production
- Ensure consistent and repeatable test coverage
- Shorten feedback loops between development and quality validation

### Typical Communication / Interactions
- Works with **Developers** to review pull requests and confirm test coverage
- Works with **Product Manager** to align acceptance criteria with user expectations
- Provides sign-off to **Release Manager** before each deployment
- Escalates unresolved defects or quality risks to **Project Manager**
- Collaborates with **UX Designer** to validate usability and accessibility concerns

---

## UX Designer

### Role Summary
The UX Designer researches user needs, creates interaction designs and prototypes, and ensures that delivered features provide an intuitive and accessible user experience.

### Responsibilities
- Conduct user research and synthesize insights into design requirements
- Create wireframes, prototypes, and high-fidelity designs
- Collaborate with Product Manager to translate user needs into acceptance criteria
- Provide design specifications and assets to Developers
- Participate in sprint reviews and demos to validate that implementation matches design intent
- Document design decisions and rationale

### Goals
- Deliver user experiences that meet accessibility and usability standards
- Reduce rework by clarifying design intent before development begins
- Ensure shipped features match validated prototypes

### Typical Communication / Interactions
- Partners with **Product Manager** on defining user stories and acceptance criteria
- Hands off design specs and assets to **Developers** at the start of implementation
- Participates in **QA Lead** reviews to validate UI acceptance criteria
- Presents designs at demos and collects feedback from **Stakeholder Liaison**
- Flags usability risks to **Project Manager** when scope changes affect UX

---

## Support Representative

### Role Summary
The Support Representative is the primary contact for end-user questions and post-release issues. They feed customer insights back to the product and project teams.

### Responsibilities
- Handle incoming user questions, bug reports, and feedback post-release
- Triage and document issues, distinguishing between usage questions and defects
- Escalate confirmed defects or regressions to Project Manager and Product Manager
- Track post-release issue volume and severity to inform future prioritization
- Communicate workarounds and known issues to affected users

### Goals
- Minimize user impact from post-release issues
- Provide timely and accurate responses to user queries
- Feed customer insights back into the product backlog

### Typical Communication / Interactions
- Escalates critical defects and regressions to **Project Manager** and **Product Manager**
- Coordinates with **Release Manager** to understand known issues and rollback status
- Files post-release bug reports in the project backlog for **Developers** to address
- Receives release communication from **Stakeholder Liaison** before public announcements

---

## DevOps / On-call (Operations Engineer)

### Role Summary
The Operations Engineer maintains CI/CD pipelines, monitors production systems, and is the first technical responder for incidents. They ensure the deployment infrastructure is reliable and observable.

### Responsibilities
- Build and maintain CI/CD pipelines and deployment automation
- Monitor production health dashboards and alerts
- Execute deployment runbooks in coordination with Release Manager
- Respond to on-call incidents and perform rollbacks when necessary
- Document infrastructure changes and runbook updates
- Participate in post-incident reviews and capture action items

### Goals
- Maximize deployment reliability and reduce mean time to recovery (MTTR)
- Ensure production environments are observable and auditable
- Automate repetitive operational tasks to reduce human error

### Typical Communication / Interactions
- Coordinates deployment execution with **Release Manager**
- Provides pipeline status and infrastructure readiness to **QA Lead** and **Release Manager**
- Escalates production incidents to **Project Manager** and on-call stakeholders
- Collaborates with **Developers** on build optimization and test infrastructure
- Informs **Support Representative** of known production issues and mitigations

---

## Stakeholder Liaison

### Role Summary
The Stakeholder Liaison bridges the project team and external stakeholders (executives, customers, partners). They ensure stakeholders receive timely, clear updates and that stakeholder feedback is communicated back to the team.

### Responsibilities
- Coordinate stakeholder communication plans for major milestones and releases
- Prepare and distribute release announcements and status updates
- Gather and consolidate stakeholder feedback for Product Manager and Project Manager
- Schedule and facilitate stakeholder reviews and demos
- Track stakeholder sign-offs required before releases

### Goals
- Maintain stakeholder confidence and alignment with project goals
- Ensure no surprise escalations by proactively sharing status
- Streamline the feedback loop between stakeholders and the delivery team

### Typical Communication / Interactions
- Works closely with **Project Manager** and **Product Manager** to align on messaging
- Distributes release communications prepared by **Release Manager** and **Support Representative**
- Facilitates stakeholder demos with input from **UX Designer**
- Reports stakeholder concerns or blockers back to **Project Manager**

---

## Interactions and Handoffs

Cross-role workflows that span multiple personas require clear handoff points to avoid gaps.

| Workflow | Key Roles | Handoff Point |
|---|---|---|
| Feature release | PM → QA Lead → Release Manager → DevOps | QA Lead provides written sign-off; Release Manager issues go/no-go; DevOps executes deployment |
| UX to development | UX Designer → Developers → QA Lead | UX Designer delivers specs; Developers implement; QA Lead validates against acceptance criteria |
| Post-release support | Release Manager → Support Representative → PM/PdM | Release Manager notifies Support of known issues; Support files bugs; PM/PdM prioritizes fixes |
| Incident response | DevOps → Release Manager → PM → Stakeholder Liaison | DevOps triggers incident; Release Manager decides on rollback; PM escalates if needed; Liaison updates stakeholders |
| Stakeholder feedback | Stakeholder Liaison → Product Manager → Developers | Liaison collects feedback; PM translates to backlog items; Developers implement |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Cross-reference [role-responsibility-matrix.md](role-responsibility-matrix.md) to see how each persona maps to project activities.

