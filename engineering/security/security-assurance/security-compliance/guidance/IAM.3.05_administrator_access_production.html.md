---
layout: handbook-page-toc
title: "IAM.3.05 - Administrator access to Production"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.3.05 - Administrator access to Production

## Control Statement
Administrator access to the production system is granted based on job roles and responsibilities and limited to authorized personnel.

## Context
Administrator Access is defined as a level of access above that of a normal user. Use of Administrator Access should be consistent with an individual’s role or job responsibilities at GitLab. When a team member's role or job responsibilities change, their Administrator Access should be appropriately updated or removed. In situations where it is unclear whether a particular action is appropriate, and within the scope of current job responsibilities, the situation should be discussed with management. The spirit of this control is to ensure there's a process in place so that all additions and updates to the production environment, are appropriately reviewed and approved before being merged.


## Scope
This control applies to any system or process where source code can be modified.

## Ownership
Control owner:
 * Engineering
 * Infrastructure

Process owner:
 * Infrastructure Team
 * All engineering teams
 * IT-Ops

## Guidance
* Establish and administer privileged user accounts in accordance with role-based access scheme that organizes information system and network privileges into roles
* Track and monitor privileged role assignments.
* Priveleged access to production is granted only after review and approval by manager
* Implement separation of duties through assigned information system access authorizations


### Possible evidence an auditor would request
* Handbook links and other relevant documentation and links
* Policy and Process documents proving that Administrator access to the production system is granted based on job roles and responsibilities and limited to authorized personnel.
* Example - Merge requests or templates showing authorized access and appropriate approval.

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Source Code Security control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/1731).

### Policy Reference
* [Production Architecture](/handbook/engineering/infrastructure/production/architecture/)
* [Infrastructure Production](/handbook/engineering/infrastructure/production/)
* [Engineering Production Architecture](/handbook/engineering/infrastructure/production/architecture/ci-architecture.html)
* [Gemnasium Service Production Architecture](/handbook/engineering/dev-backend/production-architecture/gemnasium-service.html)
* The CI/CD pipeline for GitLab.com is documented in the [handbook](/handbook/engineering/infrastructure/design/cicd-pipeline/)
* The Change Management process is documented, in detail, in the [handbook](/handbook/engineering/infrastructure/change-management/)
* Additional information about the engineering workflow can be found in the [handbook](/handbook/engineering/workflow/)
* The security release process is documented in the [handbook](/handbook/engineering/infrastructure/blueprint/release/security/)
* [GitLab Enterprise Edition Docs - Permissions](https://docs.gitlab.com/ee/user/permissions.html)
* [GitLab Enterprise Edition Docs - Merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html)


## Framework Mapping
*  SOC2 CC
  * CC6.1
  * CC8.1
