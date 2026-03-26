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
The Release Manager owns the end-to-end release process for Minor and Major releases. They coordinate readiness across engineering, QA, and support, and ensure each release meets deployment and rollback standards before it reaches production.

### Responsibilities
- Own and execute the release checklist for each Minor and Major release
- Schedule deployment windows and communicate timelines to all stakeholders
- Confirm that rollback plans are documented and tested before deployment
- Gate production deployment on QA sign-off
- Author or review release notes
- Lead post-deploy verification and coordinate incident response if issues arise

### Goals
- Ensure predictable, low-risk production deployments
- Reduce time-to-recovery for failed releases
- Maintain clear audit trails for every release

### Typical Communication/Interactions
- **With PM:** Aligns on deployment windows and scope; escalates blockers that affect the release date
- **With PdM:** Reviews release notes for accuracy and customer impact
- **With Developers:** Confirms all PRs are merged to release branch and CI is green
- **With QA Lead:** Receives formal QA sign-off before cutting the release; coordinates smoke test execution
- **With Stakeholders:** Sends pre-release announcement and post-deploy confirmation

---

## QA Lead

### Role Summary
The QA Lead defines quality standards, coordinates testing activities, and ensures acceptance criteria are met before any release gate. They are the final authority on QA sign-off.

### Responsibilities
- Write and maintain the QA test plan for each sprint and release
- Coordinate and execute functional, regression, and smoke testing
- Review PR descriptions to verify acceptance criteria are testable
- Provide formal QA sign-off (or rejection) before merging to release branch
- Track and triage defects; determine severity and blocking status
- Identify gaps in test coverage and recommend improvements

### Goals
- Prevent regressions from reaching production
- Shorten feedback loops between development and quality validation
- Ensure every release meets defined acceptance criteria

### Typical Communication/Interactions
- **With PM:** Reports QA status at daily standup; flags blockers requiring schedule changes
- **With PdM:** Validates acceptance criteria are clear and testable before sprint planning
- **With Developers:** Reviews PRs for testability; provides defect reports and retest confirmations
- **With Release Manager:** Issues formal QA sign-off; participates in post-deploy smoke tests
- **With Stakeholders:** Provides quality summary in release notes when requested

---

## UX Designer

### Role Summary
The UX Designer creates user flows, wireframes, and high-fidelity prototypes to ensure features are user-centric and meet usability standards before development begins.

### Responsibilities
- Conduct user research and synthesize findings into design requirements
- Produce wireframes, prototypes, and design specifications
- Collaborate with PdM on feature requirements and acceptance criteria
- Participate in design reviews with Developers and provide redlines/assets
- Conduct UX acceptance reviews on implemented features before QA sign-off
- Maintain a design system or component library to ensure consistency

### Goals
- Reduce usability issues found in QA or post-release
- Ensure features solve real user problems before coding begins
- Maintain a consistent and accessible product experience

### Typical Communication/Interactions
- **With PM:** Communicates design timeline and flags dependencies that could affect sprint planning
- **With PdM:** Collaborates on user stories and success metrics; validates designs against user research
- **With Developers:** Provides design specs and assets; answers implementation questions during development
- **With QA Lead:** Participates in UX acceptance review to confirm visual and interaction fidelity
- **With Stakeholders:** Presents design concepts and prototypes for feedback and approval

---

## Support Representative

### Role Summary
The Support Representative is the first point of contact for end-user questions and issues. They channel customer insights back to the product team and ensure users are informed around releases.

### Responsibilities
- Handle incoming support requests and triage issues against known bugs or feature gaps
- Escalate unresolved or critical issues to the QA Lead or PM
- Provide the product team with aggregated customer feedback and pain points
- Review release notes and update internal/external knowledge bases before each release
- Notify users of scheduled maintenance windows and release communications

### Goals
- Minimize user-facing impact of bugs and deployments
- Close the feedback loop between users and the development team
- Reduce repeat support contacts through documentation and proactive communication

### Typical Communication/Interactions
- **With PM:** Weekly summary of top support issues; flags trends that may indicate scope or quality gaps
- **With PdM:** Provides voice-of-customer input for backlog prioritization
- **With Developers:** Reports reproducible bugs with steps-to-reproduce; confirms fixes via regression
- **With QA Lead:** Shares real-world failure scenarios to expand test coverage
- **With Release Manager:** Receives pre-release briefing; confirms support documentation is ready before deploy

---

## DevOps / On-call (Operations Engineer)

### Role Summary
The Operations Engineer maintains CI/CD pipelines, infrastructure, and monitoring. They are the primary responder for production incidents and own the operational readiness of the release environment.

### Responsibilities
- Design, maintain, and improve CI/CD pipelines and deployment automation
- Monitor production systems and respond to alerts
- Own the on-call rotation and incident response runbooks
- Validate infrastructure readiness before each release (capacity, configuration, secrets)
- Execute or oversee production deployments alongside the Release Manager
- Lead rollback execution and post-incident reviews

### Goals
- Maximize deployment reliability and minimize mean time to recovery (MTTR)
- Reduce manual deployment steps through automation
- Ensure observability (logging, metrics, alerts) covers all critical paths

### Typical Communication/Interactions
- **With PM:** Reports infrastructure risks or capacity constraints that affect delivery timelines
- **With PdM:** Not typically a direct interaction; escalated through PM for strategic decisions
- **With Developers:** Reviews infrastructure-impacting PRs; provides deployment environment guidance
- **With QA Lead:** Sets up and maintains staging environments for QA testing
- **With Release Manager:** Co-executes production deployments; confirms rollback readiness; leads incident bridge calls

---

## Stakeholder Liaison

### Role Summary
The Stakeholder Liaison manages communication between the project team and external or executive stakeholders. They translate technical status into business language and ensure stakeholders can make informed decisions.

### Responsibilities
- Maintain an up-to-date stakeholder map and communication plan
- Prepare and deliver status reports, milestone updates, and executive briefings
- Gather and document stakeholder feedback; route it to the appropriate team member
- Manage approval workflows for milestone sign-offs or budget changes
- Coordinate cross-team dependencies and surface conflicts to the PM

### Goals
- Keep stakeholders informed without burdening the delivery team with ad-hoc requests
- Ensure stakeholder decisions and approvals happen on schedule
- Reduce miscommunication between technical teams and business leadership

### Typical Communication/Interactions
- **With PM:** Daily or as-needed; translates team status into stakeholder-ready language; flags pending approvals
- **With PdM:** Shares stakeholder feedback that may influence roadmap priorities
- **With Developers:** Minimal direct contact; coordinates demo or review participation when needed
- **With QA Lead:** Requests quality summaries for executive reports
- **With Release Manager:** Coordinates release announcement timing with business calendar

---

## Interactions and Handoffs

The following describes key workflows and handoff points between personas across the project lifecycle.

### Release Planning
1. **PdM** finalizes scope and acceptance criteria for the release.
2. **PM** schedules the release window in coordination with the **Release Manager** and **Operations Engineer**.
3. **Stakeholder Liaison** sends a pre-release communication to stakeholders.

### Development → QA
1. **Developer** opens a PR with acceptance criteria and links the issue.
2. **QA Lead** reviews the PR for testability and creates or updates the test plan.
3. **Developer** addresses review feedback; CI must be green.
4. **QA Lead** executes tests against the feature branch or staging environment and issues a formal sign-off or files defects.

### QA → Release Branch
1. **QA Lead** provides written sign-off confirming acceptance criteria are met.
2. **Release Manager** merges approved PRs to the release branch only after QA sign-off.
3. **UX Designer** conducts a UX acceptance review in staging before the release branch is locked.

### Release → Support
1. **Release Manager** confirms the deployment succeeded and runs post-deploy verification with **Operations Engineer**.
2. **Release Manager** distributes final release notes authored or reviewed by **PdM**.
3. **Support Representative** updates knowledge base articles and user-facing documentation.
4. **Stakeholder Liaison** sends the post-release announcement.

### Incident Escalation
1. **Operations Engineer** detects an alert and begins triage.
2. If user-facing: **Support Representative** is notified to prepare customer communications.
3. If the incident requires a rollback: **Release Manager** authorizes the rollback; **Operations Engineer** executes it.
4. **PM** and **Stakeholder Liaison** are notified for business-impact decisions.
5. Post-incident: **Operations Engineer** leads the post-mortem; **PM** ensures action items are tracked.

### UX Acceptance
1. **UX Designer** schedules a review session in staging after development is complete.
2. Feedback is documented as issues and triaged by **PdM** and **QA Lead** for inclusion or deferral.
3. **QA Lead** does not issue final sign-off until UX acceptance is complete or deferred issues are documented.

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.

