# OctoAcme — Release & Deployment Guide

## Purpose
Standardize how OctoAcme releases features to production to reduce risk and improve observability.

## Release Types
- Patch: hotfixes addressing critical production issues
- Minor: incremental features and improvements
- Major: significant functionality or breaking changes

## Pre-release requirements
- All acceptance criteria met and PRs merged
- Passing CI and security scans (Security Lead sign-off required)
- Release notes drafted
- Rollback / mitigation plan documented (DevOps Engineer approval)
- Smoke tests prepared
- Infrastructure and deployment readiness confirmed (DevOps Engineer)
- Security review completed for significant changes (Security Lead)

## Deployment Checklist
- [ ] Deployment window scheduled (if needed)
- [ ] Backup or snapshot (if applicable)
- [ ] Deploy to staging and run smoke tests
- [ ] DevOps Engineer confirms infrastructure readiness
- [ ] Security Lead approves for security-sensitive changes
- [ ] Deploy to production (automated pipeline preferred)
- [ ] Run post-deploy verifications
- [ ] Monitor key metrics and performance (with Data Analyst if applicable)
- [ ] Announce release to stakeholders and support

## Rollback & Incident Playbook
- If a deployment fails or causes a critical issue:
  - Trigger incident response and notify on-call
  - Engage DevOps Engineer for rollback execution
  - Notify Security Lead if security implications exist
  - Rollback to last known-good release if necessary
  - Triage root cause and capture action items
  - Include relevant specialists (DevOps, Security, Data Analyst) in post-incident review

## Release Notes Template
- Release name / number:
- Date:
- Summary:
- Notable changes:
- Migration steps (if any):
- Known issues:
