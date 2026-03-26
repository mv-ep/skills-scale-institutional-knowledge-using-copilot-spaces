# OctoAcme Personas

This document defines typical roles and responsibilities used in OctoAcme project docs and exercises. See also the [Role Responsibility Matrix](./role-responsibility-matrix.md) for a RACI-style overview of who is responsible for each activity.

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

### Interactions with Other Roles
- Receive acceptance criteria and priorities from **Product Manager** and **Project Manager**
- Collaborate with **UX Designer** on UI/UX requirements and demo expectations
- Coordinate with **QA Lead** on test plans and sign-off before merging to release branch
- Notify **Release Manager** when features are ready for release branch inclusion

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

### Interactions with Other Roles
- Partner with **UX Designer** on user flows, prototypes, and acceptance criteria
- Align with **Project Manager** on scope, timeline, and risk decisions
- Receive escalated user feedback from **Support Representative**
- Coordinate post-release communication with **Stakeholder Liaison**

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

### Interactions with Other Roles
- Escalate blockers from **Developers** or **QA Lead** to **Product Manager** or sponsors
- Coordinate release scheduling with **Release Manager**
- Work with **Stakeholder Liaison** to communicate status and decisions externally
- Receive incident and post-release issue reports from **Support Representative**

---

## Release Manager

### Role Summary
The Release Manager owns the end-to-end release coordination process. They ensure each release is planned, validated, communicated, and deployed safely with a documented rollback plan. A Release Manager must be assigned for all Minor and Major releases. See [Release & Deployment Guide](./octoacme-release-and-deployment.md) and the [Release Checklist](./release-checklist.md).

### Responsibilities
- Own the release schedule and deployment windows
- Ensure all pre-release gates are met (CI passing, QA sign-off, release notes drafted)
- Confirm a rollback or mitigation plan is documented before deployment
- Coordinate deployment with **DevOps/On-call** and notify **Support Representative** post-release
- Publish release notes and communicate go/no-go decisions

### Goals
- Reduce release-related incidents through disciplined process
- Provide a consistent, repeatable release experience
- Maintain clear audit trails for every release

### Typical Communication
- Release calendar and go/no-go decisions shared with PM, QA Lead, and DevOps
- Post-release summaries sent to Stakeholder Liaison and Support Representative

### Interactions with Other Roles
- Works with **Project Manager** and **Product Manager** to align release timing with roadmap commitments
- Coordinates with **QA Lead** to confirm test sign-off before promoting to release branch
- Partners with **DevOps/On-call** to schedule deployment windows and confirm monitoring is active
- Notifies **Stakeholder Liaison** and **Support Representative** once a release is live

---

## QA Lead

### Role Summary
The QA Lead defines quality standards, coordinates testing activities, and verifies that acceptance criteria are met before features are promoted to production.

### Responsibilities
- Define and maintain the test plan for each sprint/release
- Coordinate manual and automated testing efforts
- Sign off on features before they merge to the release branch
- Log and triage defects; escalate critical issues to PM and Project Manager
- Ensure regression coverage is updated after each release

### Goals
- Prevent defects from reaching production
- Maintain a high-quality, well-documented test suite
- Enable fast and confident releases through clear sign-off gates

### Typical Communication
- Test plans and results shared in PR descriptions and sprint reviews
- Defect reports and escalation notices to Project Manager and Product Manager

### Interactions with Other Roles
- Collaborates with **Developers** to review and approve test plans for PRs
- Provides formal sign-off to **Release Manager** before release branch promotion
- Escalates critical defects to **Project Manager** and **Product Manager**
- Coordinates exploratory and acceptance testing with **UX Designer** for UI features

---

## UX Designer

### Role Summary
The UX Designer creates user flows, wireframes, and prototypes that ensure features are intuitive and aligned with user needs. They translate requirements into designs that Developers can implement and stakeholders can evaluate.

### Responsibilities
- Produce wireframes, mockups, and interactive prototypes
- Define user flows and interaction patterns
- Collaborate with Product Manager on acceptance criteria
- Participate in demos and usability reviews to validate implementations
- Maintain a design system or component library (if applicable)

### Goals
- Ensure features are user-centric and meet usability standards
- Reduce rework by aligning design and engineering early
- Provide clear visual and interaction specifications

### Typical Communication
- Design files shared in sprint planning and review sessions
- Feedback provided in PR reviews for UI changes

### Interactions with Other Roles
- Partners with **Product Manager** to translate requirements into user-facing designs
- Works directly with **Developers** to clarify UI specifications and review implementations
- Coordinates with **QA Lead** on acceptance testing criteria for UI features
- Presents design rationale to **Stakeholder Liaison** when required

---

## Support Representative

### Role Summary
The Support Representative is the primary point of contact for end-user questions, issues, and feedback post-release. They capture customer insights and route them to the appropriate team for resolution or future prioritization.

### Responsibilities
- Respond to user-reported issues and questions
- Triage and escalate critical issues to the Project Manager and Product Manager
- File post-release GitHub Issues for bugs or UX concerns discovered in production
- Communicate release timelines and known issues to end users
- Provide customer feedback summaries in retrospectives

### Goals
- Minimize user impact from release issues
- Ensure user feedback is captured and considered in future planning
- Serve as a bridge between end users and the development team

### Typical Communication
- Issue reports and escalation notices filed in GitHub or project tracker
- Regular feedback summaries shared with Product Manager and Project Manager

### Interactions with Other Roles
- Escalates critical production issues to **Project Manager** (Level 2+) and **Product Manager**
- Receives release announcements and known-issues documentation from **Release Manager**
- Feeds user feedback into backlog refinement sessions with **Product Manager**
- Coordinates handoff notes before and after each release with **Release Manager**

---

## DevOps / On-call (Operations Engineer)

### Role Summary
The DevOps/On-call Engineer maintains the build, deployment, and monitoring infrastructure. They ensure the system is observable, reliable, and that incidents are detected and resolved quickly.

### Responsibilities
- Maintain CI/CD pipelines and deployment automation
- Configure and monitor alerting, logging, and observability tooling
- Respond to on-call pages and lead incident triage
- Execute and verify production deployments in coordination with Release Manager
- Document runbooks and rollback procedures

### Goals
- Maximize system reliability and deployment frequency
- Reduce mean time to detection (MTTD) and resolution (MTTR) for incidents
- Automate toil and improve deployment confidence

### Typical Communication
- Deployment status updates shared with Release Manager and Project Manager
- Incident reports and post-mortems documented and shared with the full team

### Interactions with Other Roles
- Partners with **Release Manager** to schedule and execute deployment windows
- Escalates production incidents to **Project Manager** and on-call rotation
- Provides monitoring and rollback status to **Release Manager** during deployments
- Contributes infrastructure requirements to planning sessions with **Developers** and **Project Manager**

---

## Stakeholder Liaison

### Role Summary
The Stakeholder Liaison acts as the communication bridge between the project team and external stakeholders (executives, customers, partners, or other business units). They ensure stakeholders are informed, aligned, and that their feedback is routed appropriately.

### Responsibilities
- Represent stakeholder interests in project discussions
- Distribute status updates, release announcements, and roadmap summaries
- Gather stakeholder feedback and communicate it to the Product Manager
- Facilitate executive reviews and approvals when required
- Ensure compliance with any external reporting or communication requirements

### Goals
- Maintain stakeholder confidence and alignment throughout the project
- Reduce communication overhead on the core delivery team
- Ensure feedback loops are short and actionable

### Typical Communication
- Regular written updates sent to stakeholders via email or shared portals
- Attendance at key demos and review sessions

### Interactions with Other Roles
- Receives release notes and status updates from **Release Manager** and **Project Manager**
- Routes stakeholder feedback to **Product Manager** for backlog consideration
- Coordinates escalation paths with **Project Manager** for business-impacting issues
- Supports **Support Representative** with external communication during incidents

---

## Interactions and Handoffs

The following describes common cross-role workflows:

| Workflow | Roles Involved | Key Handoff |
|---|---|---|
| Release planning | Project Manager → Release Manager → QA Lead → DevOps | PM confirms scope; Release Manager schedules window; QA Lead signs off; DevOps deploys |
| Feature acceptance | Developer → QA Lead → Product Manager | Developer marks PR ready; QA Lead verifies tests; Product Manager validates acceptance criteria |
| Post-release issue | Support Representative → Project Manager / Product Manager | Support files issue; PM triages priority; PdM decides backlog placement |
| Incident response | DevOps/On-call → Project Manager → Stakeholder Liaison | On-call triggers incident; PM escalates if business-impacting; Stakeholder Liaison communicates externally |
| Design handoff | UX Designer → Developers → QA Lead | UX shares designs in sprint planning; Developers implement; QA Lead validates against UX specs |
| Stakeholder communication | Release Manager → Stakeholder Liaison → Stakeholders | Release Manager finalizes notes; Stakeholder Liaison distributes to external audiences |

---

## How these personas are used in the exercise
- Use these persona definitions to frame scenarios and sample interactions in the Skills Exercise.
- Each persona can be used as a persona prompt for Copilot Spaces to shape role-specific guidance.
- Refer to the [Role Responsibility Matrix](./role-responsibility-matrix.md) to quickly understand accountability for each activity.

