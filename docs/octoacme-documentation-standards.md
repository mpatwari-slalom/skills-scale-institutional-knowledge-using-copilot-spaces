# OctoAcme — Documentation Standards

## Purpose
Establish consistent documentation practices across all OctoAcme projects to improve knowledge sharing, onboarding, and long-term maintainability.

---

## Core Principles

1. **Write for your future self**: Assume you won't remember the context in 6 months
2. **Make it discoverable**: Use clear titles, organize logically, and link related docs
3. **Keep it current**: Update docs when processes or decisions change
4. **Write for newcomers**: Don't assume deep domain knowledge
5. **Be concise but complete**: Include enough detail to be actionable

---

## Documentation Ownership

### By Document Type
- **Project Charter/One-pager**: Product Manager (with PM input)
- **Technical Architecture**: Tech Lead
- **API Documentation**: Developers (owners of respective APIs)
- **User Stories & Requirements**: Business Analyst (with PdM)
- **Test Plans & QA Strategy**: QA Lead
- **Release Notes**: Release Manager (with PdM input)
- **Design Specifications**: UX Designer
- **Process Documentation**: Project Manager
- **Retrospective Notes**: PM (facilitator captures outcomes)

### Maintenance Responsibilities
- Document owner reviews and updates quarterly or when significant changes occur
- PM maintains index of all project documentation
- All team members can suggest edits via PR or comments

---

## Required Documentation by Project Phase

### Initiation Phase
- [ ] Project One-pager (problem, goals, metrics, stakeholders)
- [ ] Stakeholder map and communication plan
- [ ] High-level timeline and milestones
- [ ] Initial risk list

### Planning Phase
- [ ] Detailed requirements or user stories with acceptance criteria
- [ ] Technical architecture or design doc (for complex projects)
- [ ] UX designs and user flows (for user-facing features)
- [ ] Test strategy and QA plan
- [ ] Release plan and deployment approach
- [ ] Risk register with mitigations

### Execution Phase
- [ ] Updated project status (weekly)
- [ ] Technical design decisions (ADRs - Architecture Decision Records)
- [ ] API documentation or integration guides
- [ ] Runbooks for operational procedures
- [ ] Updated risk register

### Release Phase
- [ ] Release notes with notable changes and migration steps
- [ ] Deployment checklist completed
- [ ] Post-deployment validation results
- [ ] Known issues and workarounds

### Retrospective Phase
- [ ] Retrospective notes (what went well, what to improve, action items)
- [ ] Lessons learned summary
- [ ] Metrics review (actual vs. planned)

---

## Documentation Templates

### Architecture Decision Record (ADR)
```markdown
# ADR-[NUMBER]: [Title]

**Status**: [Proposed | Accepted | Deprecated | Superseded]
**Date**: YYYY-MM-DD
**Deciders**: [Names or roles]

## Context
What is the issue we're trying to solve?

## Decision
What did we decide to do?

## Consequences
What are the positive and negative outcomes of this decision?

## Alternatives Considered
What other options did we evaluate and why were they not chosen?
```

### User Story Template
```markdown
## [Story Title]

**As a** [persona/role]
**I want** [goal/desire]
**So that** [benefit/value]

### Acceptance Criteria
- [ ] Criterion 1
- [ ] Criterion 2
- [ ] Criterion 3

### Definition of Done
- [ ] Code implemented and reviewed
- [ ] Unit tests written and passing
- [ ] Integration tests passing
- [ ] Documentation updated
- [ ] QA validated
- [ ] UX reviewed (if user-facing)

### Additional Context
- Designs: [Link to Figma]
- Related stories: [Links]
- Dependencies: [Description]
```

### Technical Design Document Template
```markdown
# [Feature/Component Name] - Technical Design

## Overview
Brief description of what is being built and why.

## Goals and Non-Goals
**Goals:**
- Goal 1
- Goal 2

**Non-Goals:**
- What is explicitly out of scope

## Architecture
High-level architecture diagram and description.

## Detailed Design
### Component 1
Description of implementation approach.

### Component 2
Description of implementation approach.

## API/Interface Design
Describe APIs, data models, or interfaces.

## Data Model Changes
Database schema changes if applicable.

## Testing Strategy
How will this be tested? (unit, integration, e2e)

## Deployment Approach
How will this be rolled out? Migrations needed?

## Monitoring and Alerting
What metrics and alerts will be added?

## Security Considerations
Security review, authentication, authorization, data protection.

## Alternatives Considered
What other approaches were evaluated?

## Open Questions
Unresolved questions that need input.

## Timeline
Rough estimate of effort and key milestones.
```

### Runbook Template
```markdown
# [Process/Service Name] Runbook

## Purpose
What does this process/service do?

## Owner
Who is responsible for this? (Team or role)

## Prerequisites
What access or knowledge is needed to execute this?

## Normal Operation
How to verify it's working correctly.

## Common Issues and Resolution
### Issue 1: [Description]
**Symptoms**: How to identify this issue
**Resolution**: Step-by-step fix

### Issue 2: [Description]
**Symptoms**: How to identify this issue
**Resolution**: Step-by-step fix

## Escalation
When and how to escalate if standard resolution doesn't work.

## Monitoring and Alerts
Where to check dashboards and alert definitions.
```

---

## File Naming Conventions

### Documentation Files
- Use lowercase with hyphens: `octoacme-project-planning.md`
- Include project prefix for project-specific docs: `octoacme-*`
- Use descriptive names: `api-authentication-guide.md` not `auth.md`

### Location
- **Project-level docs**: `/docs/` directory in repository
- **Code-level docs**: `README.md` in respective code directories
- **API docs**: Generated from code comments, published to `/docs/api/`
- **Architecture docs**: `/docs/architecture/` or ADRs in `/docs/adr/`

---

## Writing Style Guidelines

### Clarity
- Use active voice: "Deploy the service" not "The service should be deployed"
- Be specific: "Run `npm install`" not "Install dependencies"
- Avoid jargon or explain it when first used
- Use examples and code snippets where helpful

### Structure
- Start with a clear purpose statement
- Use headings to organize content (H2 for major sections, H3 for subsections)
- Use bullet points for lists and steps
- Include a table of contents for docs longer than 3 pages

### Formatting
- Use code blocks with language specification: ```python
- Use tables for structured data
- Use callouts for important notes:
  - 💡 **Tip**: Helpful suggestion
  - ⚠️ **Warning**: Important caution
  - 📝 **Note**: Additional context

### Links
- Always use descriptive link text: "See the [API Guide](link)" not "Click [here](link)"
- Link to related documentation
- Keep links up to date; broken links reduce trust in documentation

---

## Documentation Review Process

### When to Review
- During PR review (if documentation is part of the change)
- Quarterly documentation audit led by PM
- When onboarding feedback indicates confusion
- When processes change

### Review Criteria
- [ ] Is it accurate and up-to-date?
- [ ] Is it clear and easy to follow?
- [ ] Is it complete (answers likely questions)?
- [ ] Are there broken links?
- [ ] Does it follow formatting standards?
- [ ] Is the owner/last updated date current?

### Approval
- Minor edits: Any team member can PR updates
- Major changes: Review by document owner and PM

---

## Tools and Storage

### Primary Tools
- **Markdown files** in Git repositories (version controlled, easy to review)
- **GitHub Wiki** for less formal, frequently updated content
- **Confluence or similar** for cross-project documentation (if applicable)
- **Design tools** (Figma, etc.) for design documentation

### Backups and Versioning
- All docs in Git are automatically versioned
- Tag releases with documentation snapshots
- Archive old versions in `/docs/archive/` if significant rewrites occur

---

## Measuring Documentation Quality

### Key Metrics
- Onboarding time: How long to get new team member productive?
- Number of repeated questions: Are team members asking the same things?
- Broken links: Run periodic link checks
- Documentation age: Flag docs not updated in 6+ months for review

### Feedback Mechanisms
- Onboarding surveys: Ask new team members about doc quality
- Docs backlog: Create issues for missing or unclear documentation
- Retrospective action items: Flag documentation issues in retros

---

## Continuous Improvement

Documentation is a living practice. Regularly:
- Ask "Is this documented?" when answering questions
- Create docs for repeated questions or processes
- Celebrate good documentation in team meetings
- Make documentation part of Definition of Done

---

## Questions or Suggestions?

If you have feedback on these standards or need clarification, contact the Project Manager or suggest changes via PR.
