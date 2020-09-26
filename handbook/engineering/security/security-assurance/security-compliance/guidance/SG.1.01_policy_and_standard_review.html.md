---
layout: handbook-page-toc
title: "SG.1.01 - Policy and Standard Review Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# SG.1.01 - Policy and Standard Review

## Control Statement

GitLab's information security policies and standards are reviewed, updated if required, and approved by management, annually. Information security policies and standards are communicated to personnel through the GitLab Handbook.

## Context

The purpose of this control is to ensure GitLab's policies and procedures are kept up-to-date and relevant, changes are appropriately reviewed and approved, and GitLab team members have a way to track those changes.

Due to the nature of how GitLab operates and it's value of being iterative, continual updates are made to the related security policies and standards (as deemed necessary) that have been listed as in-scope for this control. Changes made to these procedures are always reviewed prior to being updated in GitLab's handbook. Evidence of changes can be identified via the related handbook page's markdown file in the www-gitlab-com project repo or by visiting the [Handbook Changelog](/handbook/CHANGELOG.html).

## Scope

All policies and standards having a direct impact to how GitLab carries out it's IT/Security practices are in-scope for this control. Policies and standards impacting the broader organization have been determined to be entity level policies which are considered as part of the Entity Level Controls (ELC) documented within the [Sarbanes-Oxley (SOX) Compliance](/handbook/internal-audit/sarbanes-oxley/) Handbook page. 

The specific policies and standards described in the [Policy Reference](#policy-reference) section below are subject to this control.

## Ownership

Control Owner:

* Security Compliance

Process Owner:

* Security

## Guidance

On an annual cadence, GitLab's Information Security Policies are reviewed and approved by the appropriate level of management. 

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Policy and Standard Review control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/875).

### Policy Reference
- [Engineering Department](/handbook/engineering/) Policies and Standards
  - [Development Department](/handbook/engineering/development/)
  - [Infrastructure Department](/handbook/engineering/infrastructure/)
    - [Backup Policies](/handbook/engineering/infrastructure/production/#backups) and [Backup Recovery Testing](https://gitlab.com/gitlab-com/gl-infra/gitlab-restore/postgres-gprd/blob/master/README.md)
    - [Change Management](/handbook/engineering/infrastructure/change-management/)
    - [Disaster Recovery](https://gitlab.com/gitlab-com/gl-infra/readiness/-/blob/master/library/disaster-recovery/index.md) and [Disaster Recovery - Databases](/handbook/engineering/infrastructure/database/disaster_recovery.html)
    - [Incident Management](/handbook/engineering/infrastructure/incident-management/)
    - [Production Architecture Page](/handbook/engineering/infrastructure/production/architecture/)
  - [Quality Department](/handbook/engineering/quality/)
  - [Security Department](/handbook/engineering/security/)
    - [Data Classification Policy](/handbook/engineering/security/data-classification-standard.html)
    - [Data Protection Impact Assessment (DPIA) Policy](/handbook/engineering/security/dpia-policy/)
    - [Incident Response Guide](/handbook/engineering/security/sec-incident-response.html)
    - [GitLab Password Policy Guidelines](/handbook/security/#gitlab-password-policy-guidelines)
    - [Risk Management](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html)
    - [Security Incident Communications Plan](/handbook/engineering/security/security-incident-communication-plan.html)
    - [Security Operations On-Call Guide](/handbook/engineering/security/secops-oncall.html#major-incident-response-workflow) for Major Incidents
    - [Third Party Vendor Security Review Procedures](/handbook/engineering/security/security-assurance/security-compliance/third-party-vendor-security-review.html)
    - [Vulnerability Management](/handbook/engineering/security/vulnerability_management/#vulnerability-management-overview)
  - [Support Team](/handbook/support/)
    - [Incident Management for Self-Managed Customers](/handbook/support/incident-management/)
  - [GitLab Security Practices](/handbook/security/)
    - [Business Continuity Plan](/handbook/business-ops/gitlab-business-continuity-plan.html)
    - [Data Team](/handbook/business-ops/data-team/) Policies and Standards
    - [Team Member Enablement Policies and Standards](/handbook/business-ops/team-member-enablement/onboarding-access-requests/) 
      - [Inventory Management](/handbook/business-ops/team-member-enablement/onboarding-access-requests/#fleet-intelligence--remote-lockwipe) <!-- Fleetsmith will be deprecated for DriveStrike. When this happens, this link needs to be updated. -->
    - [IT Help Team](/handbook/business-ops/team-member-enablement/self-help-troubleshooting/) Policies and Standards
- General Policies and Standards
  - [Offboarding Procedures](/handbook/people-group/offboarding/offboarding_guidelines/)

## Framework Mapping

* SOC2 CC
  * CC5.2
  * CC5.3
* PCI
   * SAQ-A
