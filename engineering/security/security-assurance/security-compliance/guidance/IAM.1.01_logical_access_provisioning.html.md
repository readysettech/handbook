---
layout: handbook-page-toc
title: "IAM.1.01 - Logical Access Provisioning Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.1.01 - Logical Access Provisioning

## Control Statement
Logical access provisioning requires approval from appropriate personnel.

## Context
The purpose of this control is to ensure there is a process in place to review and authorize new user account requests. Ensuring only people who require access to a system or service receive access helps improve GitLab's overall security posture by limiting the number of accounts with access and reducing the overall likelihood of an account being compromised.

## Scope
This control applies to any system or service where user accounts can be provisioned.

## Ownership
Control ownership:
* IT Operations

Process ownership:
* IT Operations
* Managers
* Systems Owners

## Guidance
Provisioning should be based on predetermined roles with business justification and management approval. The process owner should use role-based authentication whenever possible to make this control easier and to segregate out this function from that of other system functions.

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Logical Access Provisioning control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/805).

## Policy Reference
- [Access Control Policy](/handbook/engineering/security/Access-Management-Policy.html)
- [Access Request Process](/handbook/engineering/security/Access-Management-Policy.html#access-requests-and-onboarding)
- [Principle of least privilege access](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege)
- [IT Ops instructions and FAQs for Access Requests](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/)	
- [Okta Baseline Entitlements-Okta Application stack](/handbook/business-ops/okta/okta-appstack/)
- [Single Person Access Requests](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/#single-person-access-request) 	
- [Access Request Template](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=New_Access_Request)
- [Template used for Access Reviews](https://gitlab.com/gitlab-com/team-member-epics/access-requests/issues/new?issuable_template=Access_Review)

## Framework Mapping
* SOC2 CC
  * CC6.1 