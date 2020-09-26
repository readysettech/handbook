---
layout: handbook-page-toc
title: "IAM.1.09 - Access Modification"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.1.09 - Access Modification

## Control Statement
Access modifications due to a change in role or responsibility are documented and tracked in a change request issue.


## Context
The purpose of this control is to ensure there is a process in place to modify access to user accounts in the event of a role change. This control helps ensure that only authorized and active accounts can be accessed and used to prevent any unauthorized use or access of GitLab customer, GitLab team member, and partner data. The manager would be responsible for advising of role change and accordingly, reviewing and de-provisioning any access that is no longer required. 


## Scope
This control applies to any system or service where user accounts can be provisioned.


## Ownership
* Control Owner:
    * PeopleOperations
    * Managers
* Process owner:
    * IT Operations
    * System Owners

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Role Change: Access Modification Control Issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1703).


### Policy Reference
- [Access Reviews](/handbook/engineering/security/#access-reviews)
- [Access Control Policy and Procedures](/handbook/engineering/security/#access-control-policy-and-procedures)
- [Job Transfers](/handbook/engineering/security/#job-transfers)
- [Access Change Request](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/#access-change-request)
- [Access Removal Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/tree/master)


## Framework Mapping
*  SOC2 CC
    *  CC6.2 - Prior to issuing system credentials and granting system access, the entity registers and authorizes new internal and external users whose access is administered by the entity. For those users whose access is administered by the entity, user system credentials are removed when user access is no longer authorized.

*  PCI
   * 7.1.4 - Limit access to system components and cardholder data to only those individuals whose job requires such access.
   * 8.1.2 - Control addition, deletion, and modification of user IDs, credentials, and other identifier objects.
   
