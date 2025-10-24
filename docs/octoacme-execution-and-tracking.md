# OctoAcme — Execution & Tracking

## Purpose
Guidance for managing day-to-day execution and tracking progress toward project milestones.

## Team Rhythm
- Daily standups (15 min) — focus on progress, blockers, dependencies
- Weekly delivery sync — show progress, updates, and flagged risks
- Demo/Review at the end of each sprint or milestone

## Workflows
- Use the project board (e.g., GitHub Projects) with columns: Backlog, Ready, In Progress, In Review, QA, Done
- Pull Request workflow:
  - Small PRs (<= 400 lines when possible)
  - Include issue link and acceptance criteria in PR description
  - Run automated tests and linting in CI before requesting review
  - Require at least one approval before merging (or team-defined policy)

## Quality & Testing
- Unit tests for new logic
- Integration tests where applicable
- End-to-end smoke tests for critical flows before release
- Security scanning in CI
- Manual QA for feature acceptance when needed

## Reporting & Metrics
- Track velocity and burndown
- Monitor success metrics identified in the Project One-pager
- Use dashboards for key signals (errors, latency, usage)

## Blocker Escalation

### Escalation Ownership by Type
- **Technical blockers**: Tech Lead → Engineering Manager
- **Requirements clarity**: BA or PdM → Product Lead
- **Resource constraints**: PM → Delivery Lead or Sponsor
- **Quality/Testing issues**: QA Lead → PM → Product Lead
- **Design ambiguity**: UX Designer → Design Lead or PdM
- **Dependency on external team**: PM coordinates with other PM

### Escalation Path by Severity
- **Level 1** (Minor delay, <1 day impact): Team-level triage in daily standup
  - Owner: Tech Lead or relevant role lead
  - Resolution time: Same day
  
- **Level 2** (Moderate impact, 1-3 day delay): PM escalates to functional leads
  - Owner: PM coordinates with Product Lead, Tech Lead, or dependent teams
  - Resolution time: Within 24 hours
  - Communication: Escalation email with impact assessment
  
- **Level 3** (Critical, >3 day delay or release risk): Sponsor-level escalation
  - Owner: PM escalates to Sponsor and Stakeholder Committee
  - Resolution time: Immediate triage meeting
  - Communication: Formal escalation with options and recommendations

## Cross-team Collaboration and Handoffs

Effective collaboration requires clear handoff processes and communication:

### Design to Development Handoff
1. **UX Designer** creates design specs with annotations in Figma/design tool
2. **Design review** with Developers and PdM to clarify interactions and edge cases
3. **UX Designer** marks designs as "Ready for Development"
4. **Developers** ask clarifying questions before implementation starts
5. **UX Designer** reviews implementation against design specs before QA sign-off

### Requirements to Development Handoff
1. **BA** documents requirements with acceptance criteria
2. **BA and PdM** refine and prioritize in backlog
3. **BA** presents requirements to Tech Lead and Developers in refinement session
4. **Developers** ask questions and provide technical feasibility feedback
5. **BA** remains available during development for clarifications

### Development to QA Handoff
1. **Developer** completes feature and runs local tests
2. **Developer** creates PR with clear description and test instructions
3. **Code review** completed and approved by peer developers
4. **Developer** deploys to test environment and marks story as "Ready for QA"
5. **QA Lead** assigns testing and validates against acceptance criteria
6. **QA** reports defects; **Developer** fixes and resubmits

### QA to Release Handoff
1. **QA Lead** provides release readiness report with test results
2. **QA Lead** prepares smoke test suite for production verification
3. **Release Manager** reviews quality sign-off and coordinates go-live
4. **QA Lead** executes smoke tests post-deployment
5. **QA Lead** confirms production validation complete

## Execution Checklist
- [ ] All team members onboarded to project tools and workflows
- [ ] Branching and PR conventions documented in repo
- [ ] CI configured for tests and lint by Tech Lead
- [ ] QA Lead has reviewed test coverage and automation strategy
- [ ] Regular demos scheduled with stakeholders
- [ ] Daily standups scheduled with core team
- [ ] Weekly PM/PdM sync scheduled
- [ ] Risk register updated weekly by PM
- [ ] Design handoffs scheduled between UX Designer and Developers
- [ ] Code review assignments and rotation established
- [ ] Monitoring and alerting configured for production services
- [ ] Handoff processes documented and understood by all team members
