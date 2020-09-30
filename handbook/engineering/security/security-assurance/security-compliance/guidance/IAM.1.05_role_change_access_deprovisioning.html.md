---
layout: handbook-page-toc
title: "IAM.1.05 - Transfers: Access De-provisioning Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.1.05 - Transfers: Access De-Provisioning

## Control Statement
Upon notification of a reassignment or transfer, management reviews the GitLab team member's access for appropriateness. Access that is no longer required is revoked and documented, and any shared authentication credentials to which the team member had access are rotated.

## Context
The purpose of this control is to ensure there is a process in place to remove access to user accounts that is no longer necessary in the event of a role change.  This control helps ensure that only authorized and active accounts can be accessed and used to prevent any unauthorized use or access of GitLab customer, GitLab teammember, and partner data. PeopleOperations would be responsible for advising of role change and new hiring manager of reviewing and de-provisioning any access that was no longer required. 

## Scope
This control applies to any system or service where user accounts can be provisioned.

## Ownership
* Control Owner:
    * PeopleOperations
    * Hiring Managers
* Process owner:
    * IT Operations

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Role Change: Access De-Provisioning control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/809).


### Policy Reference

- [Access Reviews](/handbook/engineering/security/#access-reviews)
- [Access Control Policy and Procedures](/handbook/engineering/security/#access-control-policy-and-procedures)
- [Job Transfers](/handbook/engineering/security/#job-transfers)
- [Access Change Request](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/#access-change-request)
- [Access Removal Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/tree/master)

## Framework Mapping
* ISO
  * A.7.3.1
  * A.9.2.1
  * A.9.2.2
  * A.9.2.3
  * A.9.4.1
  * A.9.2.6
  * A.18.1.3
* SOC2 CC
  * CC6.2
  * CC6.3
  * CC6.6
  * CC6.7
* PCI
  * 8.1.2
  * 8.1.3
  * 8.1.4