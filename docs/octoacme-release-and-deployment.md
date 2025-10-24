# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release Requirements

### Quality Sign-offs (coordinated by Release Manager)
- **QA Lead**: All acceptance criteria met, test pass rate acceptable
- **Tech Lead**: All PRs merged, CI passing, no critical technical debt
- **Security**: Security scans passing, no critical vulnerabilities
- **Product Manager**: Release content matches planned features
- **UX Designer**: UI/UX implementation matches design specs (for user-facing changes)

### Documentation and Planning
- Release notes drafted (Release Manager with PdM)
- Rollback / mitigation plan documented (Release Manager with Tech Lead)
- Smoke tests prepared and validated (QA Lead)
- Deployment runbook reviewed (Release Manager)
- Stakeholder communication prepared (PM)

## Deployment Checklist (owned by Release Manager)
- [ ] **Pre-deployment**
  - [ ] Deployment window scheduled and communicated
  - [ ] All pre-release sign-offs obtained (QA, Tech, Security, Product)
  - [ ] Backup or snapshot created (if applicable)
  - [ ] On-call rotation confirmed and incident response ready
  - [ ] Rollback plan reviewed and validated

- [ ] **Staging Deployment**
  - [ ] Deploy to staging environment
  - [ ] QA Lead runs smoke tests in staging
  - [ ] Verify monitoring and alerting in staging
  - [ ] Stakeholder demo in staging (if needed)

- [ ] **Production Deployment**
  - [ ] Go/No-Go decision checkpoint with PM, PdM, Tech Lead, QA Lead
  - [ ] Deploy to production (automated pipeline preferred)
  - [ ] Run post-deploy verifications and smoke tests
  - [ ] Monitor key metrics for 30 minutes post-deployment
  - [ ] Verify no critical errors or performance degradation

- [ ] **Post-deployment**
  - [ ] Announce release to stakeholders and support (PM)
  - [ ] Update status page or release tracker
  - [ ] Schedule release retrospective within 1 week
  - [ ] Archive deployment artifacts and logs

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
