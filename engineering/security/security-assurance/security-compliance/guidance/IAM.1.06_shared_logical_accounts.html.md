---
layout: handbook-page-toc
title: "IAM.1.06 - Shared Logical Accounts Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.1.06 - Shared Logical Accounts

## Control Statement
GitLab restricts the use of shared and group authentication credentials. Shared and group accounts are reviewed quarterly to reassess whether use of shared credentials are appropriate.

## Context
Adding restrictions to the use of shared accounts help protect against malicious activity and stolen accounts. Shared accounts are more likely to be compromised because the account credentials are shared with multiple people and it's often not feasible to use multi-factor authentication. While shared accounts sometimes must be used, this control aims to limit account sharing to only those cases where it's necessary and no good alternatives exist, and to add safeguards to when they are used.

## Scope
This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership
* Control ownership: `IT Operations`
* Process ownership: `IT-Operations` 

## Guidance
* Okta `should be used` to manage authentication of shared accounts whenever possible, since Okta has individual user activity logs; these logs help provide a compensating control to mitigate the risk associated with shared account access. 
* When Okta is not able to be used, a `policy exception` is required to track this shared access. A process for the lifecycle of the access and a mechanism to alert the appropriate teams when authentication credentials must be reset (e.g., email alerts, an issue, calendar event, etc) should be established.

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Shared Logical Accounts control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/810).

### Policy Reference
* [Handbook section `Security Process and Procedures for Team Members` - Accounts and Passwords](/handbook/security/#security-process-and-procedures-for-team-members)
* [Handbook section `1Password for Teams`](/handbook/security/#1password-for-teams)
* [Handbook>Engineering>Security>`Access Management Process`](/handbook/engineering/security/#access-management-process)
* [Recorded meeting on the status of 1Password to Okta migration with Rob Mitchell](https://www.youtube.com/watch?v=UMU-V224Mws&feature=youtu.be)
* [Proposal: Set-up SAML for SOX-in-scope Applications to Support Compliance with 6 Information Security Controls](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/152)
* [People Ops Vault Shared Passwords](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/13)


## Framework Mapping
* SOC2 CC
  * CC6.1
