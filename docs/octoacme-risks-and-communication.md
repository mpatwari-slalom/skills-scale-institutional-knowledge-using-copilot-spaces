# OctoAcme — Risk Management & Communication

## Purpose
Explain how to identify, manage, and communicate risks and dependencies.

## Risk Register
Maintain a simple table with:
- ID
- Description
- Impact (High/Med/Low)
- Likelihood (High/Med/Low)
- Owner
- Mitigation plan
- Status

## Risk Lifecycle
- Identify: during planning and ongoing execution
- Assess: estimate impact and likelihood
- Mitigate: reduced via actions, contingency plans
- Monitor: review at weekly syncs and update status

## Stakeholder Communication

### Stakeholder Mapping
Identify and map stakeholders by interest and influence:
- **High Interest, High Influence**: Sponsor, Product Lead, Key Business Units
  - Frequency: Weekly updates, milestone reviews
  - Owner: PM and PdM
  
- **High Interest, Low Influence**: End Users, Customer Success, Support
  - Frequency: Release announcements, training sessions
  - Owner: PdM with support from BA
  
- **Low Interest, High Influence**: Senior Leadership, Finance
  - Frequency: Milestone updates, quarterly reviews
  - Owner: PM and Sponsor
  
- **Low Interest, Low Influence**: Peripheral teams
  - Frequency: As-needed updates
  - Owner: PM

### Communication Channels
- **Project Status**: Weekly email or dashboard (PM)
- **Release Communications**: Release notes and announcements (Release Manager with PdM)
- **Design Updates**: Design reviews and Figma links (UX Designer)
- **Requirements Changes**: Change requests and impact analysis (BA with PM)
- **Quality Reports**: Test results and defect trends (QA Lead)

### Single Source of Truth
- Use a single source of truth (project README or release doc) for status
- All team members update their section weekly
- PM consolidates and publishes unified status report

## Communication Templates
Weekly Status Template:
- Progress this week:
- Next steps:
- Risks & blockers:
- Ask / decisions needed:

Incident Communication
- Triage summary
- Actions being taken
- Expected timeline
- Post-incident blameless retrospective scheduled

## Escalation Paths

### Standard Project Issues
1. **Team Level**: Identified and triaged by role leads (Tech Lead, QA Lead, etc.)
2. **PM Level**: PM coordinates resolution with functional leads
3. **Product/Delivery Lead Level**: Product Lead or Delivery Manager engages
4. **Sponsor Level**: Executive sponsor makes final decision

### By Issue Type
- **Technical/Architecture**: Developer → Tech Lead → Engineering Manager → CTO
- **Requirements/Scope**: BA → PdM → Product Lead → Sponsor
- **Quality/Testing**: QA Lead → PM → Product Lead
- **Release/Deployment**: Release Manager → PM → Delivery Lead
- **Design/UX**: UX Designer → Design Lead → Product Lead
- **Resource/Schedule**: PM → Delivery Manager → Sponsor

### Critical Incidents
- **Security incidents**: Immediate escalation to Security on-call, notify CISO, follow security incident runbook
- **Production outages**: Release Manager triggers incident response, notify on-call rotation
- **Data breaches**: Immediate escalation to Legal and Security teams

### Cross-team Dependencies
- Blocking dependencies escalated by PM to peer PM and respective delivery leads
- Regular cross-PM syncs for dependency management
