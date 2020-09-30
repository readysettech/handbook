---
layout: handbook-page-toc
title: "Access Management Policy"
---

### On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Access Management 

Centralized access management is key to ensuring that the correct GitLab team-members have access to the correct data and systems and at the correct level. GitLab access controls are guided by the principle of least privilege and need-to-know. These controls apply to information and information processing systems at the application and operating system layers, including networks and network services.

The [access request project](https://gitlab.com/gitlab-com/team-member-epics/access-requests) is used to request and track the following access-related activities:

1. [New Access Requests](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request)
2. [Access Removal Requests](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Remove_Access_Request)
3. [Access Reviews](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Access_Review)
4. [New Service Account Requests](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=New_Service_Account_Request)

Usage guidelines for each of the access templates is outlined on the [Team Member enablement's handbook page](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/).

These templates should be used during the [onboarding process](/handbook/people-group/general-onboarding/) and throughout the employment tenure of a GitLabber. Access required as part of the team member's onboarding should be requested using the [New Access Requests](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request) or if applicable, one of the available [Role-based entitlements templates](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/tree/master/.gitlab/issue_templates/role_baseline_access_request_tasks).

### Access Control Policy and Procedures

* All new access or permissioning change requests require a [New Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request).

* Shared accounts may not be used for customers.gitlab.com, dev.gitlab.org, Shopify, Stripe, and Zuora in order to comply with PCI-DSS requirements. Currently, GitLab's financial controls prohibit the use of shared accounts within the following applications: NetSuite.

* Shared and group credentials are restricted. Any systems that require shared accounts or credentials and are not yet implemented or configured into Okta must have an Access Request approved and an exception to this policy for each user. Bulk access requests are not allowed for shared or group credentials.

* All access requests must be approved by the team member's manager with the exception of:

   - ARs for G-Suite email distribution lists for internal GitLab team members
   - ARs for Slack groups for internal GitLab team members
   - ARs using a role based template

  Please note that ARs for access to internal systems for "external to GitLab individuals" (eg. customers, prospects) require managerial approval. This includes access to G-Suite security groups also require managerial approval.

* Access requests are required when requesting a role above developer (i.e. maintainer, owner) on the following GitLab repositories and Groups:

- Repos:
   - www-gitlab-com
   - [GitLab CE and GitLab EE](https://gitlab.com/gitlab-org/gitlab) (aka single Rails repository)

- Groups:
   - gitlab.com and gitlab.org - top level group permissions

* Access requests should be submitted when requesting explicit access to private groups, sub-groups, and repositories in order to facilitate deprovisioning.

* Requests for access to Infrastructure assets (servers and databases) require a second layer of approval from Infrastructure Management.

* All access requests must be provisioned as approved. An AR that is approved without a role specified should not be provisioned until the role being requested is identified and re-approved.

* Administrative permissions should be considered operational in nature. This means that they are granted for the sole purpose of system management, configuration, and support. They should be recognized as privileged accounts and as such, activities must be logged and the logs protected and regularly reviewed.

* Time-based access may be provided if administrative action is required for a set period of time. This should be documented as part of the Access Request SLAs.

* All requests for new service accounts require a [New Service Account Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=New_Service_Account_Request)

* All requests for new service accounts must be approved by a member of Infrastructure Management.

* In regard to support during or prior to provisioning, please do not tag the Security Operations team in the AR issue; to ask Security for help with AR assignments, please use the #it_help channel.

* If admin-level access is being requested, the request must be approved by the team member's manager and Infrastructure Management if applicable.

### Access Control Process Exceptions

* An access request is not required for Google Drive folders or files.

* Managerial approval is not required when requesting access to:

  - ARs for G-Suite email distribution lists for internal GitLab team members
  - ARs for Slack groups for internal GitLab team members
  - ARs using role based templates

### Bulk Access Requests

* Bulk access requests are those that are for multiple GitLab team-members. Bulk requests can be submitted for the following three types of requests:

  - Email aliases/forwarding in GSuite.
  - The adding of team members to Slack groups.
  - All GitLab team-members listed on the Access Request have the same manager and the same level of access is being requested.

  Please note that the above use cases do not apply to ADMIN-level access, which needs to be submitted using the  **one** issue per GitLab team-member rule.


### Access Requests and Onboarding

During the onboarding process, the manager should determine which email and slack groups the new team member should be added to. Also determine if new team member will need access to the `dev` server, which is used by engineers to prepare fixes for security issues and also allows for access to version.gitlab.com and license.gitlab.com. If so, request the creation of a [new dev.GitLab.org account](https://dev.gitlab.org/admin/users/new) *with the same username the team member has on gitlab.com* and an invitation to the [gitlab group](https://dev.gitlab.org/groups/gitlab/group_members) as a Developer. Fill out one [access request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request) for both the groups and Dev account if needed.

### Principle of Least Privilege

GitLab operates its access management under the [principle of least privilege](https://csrc.nist.gov/glossary/term/least_privilege). Under least privilege, a team member should only be granted the minimum necessary access to perform their function. An access is considered necessary only when a GitLabber cannot perform a function without that access. If an action can be performed without the requested access, it's not considered necessary. Least privilege is important because it protects GitLab and its customers from unauthorized access and configuration changes and in the event of an account compromise by limiting access.

### Least Privilege Reviews for Access Requests

* A least privilege review should be performed by a system's administrator and the manager of the team member for whom access is being requested. System administrators should be provided security training that includes specific training on least privilege and its application.

* To perform a least privilege review, compare the rationale provided for the service(s) to which access is being requested with the level of access being requested.

  - Consider whether the access requested provides the team member access beyond what is required per the information provided in the `rationale` section of the access request.

* If the access requested provides the team member only the access they require to perform what's in the `rationale` section of the access request, the access request should be approved. In this case, simply proceed with approving the access request. An access request approval is considered confirmation the request has been reviewed for least privilege. Once your approval has been submitted, there's no more action for you to take for the least privilege review.

* If the access requested provides the team member **access beyond what is required** in the information provided in the `rationale` section of the access request, the request doesn't align with the principle of least privilege and the request should be temporarily rejected until the appropriate access can be defined. To reject an access request on the basis of least privilege, respond to the issue with the following information:

  - Which service(s) are being requested excessive permissions.
  - A specific example of why the requested access is excessive. For example, a team member is requesting Super Admin access on GSuite only for provision user accounts, but the Super Admin role provides access far beyond just user account provisioning.
  - An alternative level of access and brief explanation how the new level of access allows the team member to fulfill their role. For example, a User Admin role on GSuite allows the team member to provision user accounts while not also providing all the other access a Super Admin role would. If no alternative can be given, the access request should be approved in the interest of the team member's productivity.

* Should there be disagreement on an access request rejection on the basis of least privilege, an [exception request](/handbook/engineering/security/index.html#information-security-policy-exception-management-process) should be submitted. An exception request is important because it provides a clearly defined escalation process, promotes transparency, and allows us to appropriately track any deviations from policy.

### Deprovisioning

* In the case of a separation from the company, all access will be deprovisioned within 3 business days from the date on which the offboarding request is submitted unless otherwise specified.

* All attempts will be made for individual access removal requests to be processed within the SLA requested. If no SLA is noted, access will be deprovisioned within 3 business days of the submission of the issue.

* If access removal needs to occur immediately, please follow the [panic email procedures](/handbook/security/#panic-email), which will alert the Security Team on-call.

### Job Transfers

* An access review should be documented and performed as part of a [formal job transfer](/handbook/engineering/security/security-assurance/security-compliance/guidance/IAM.1.05_role_change_access_deprovisioning.html). The review should be perfomed by the new manager of the team member who is transferring to a new role.

* Upon notification of a reassignment or transfer, management reviews the GitLabber's access for appropriateness. Access that is no longer required is revoked and documented.

### Access Reviews

* [Access reviews](/handbook/engineering/security/security-assurance/security-compliance/access-reviews.html) will be formally documented using the [Access Reviews](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Access_Review) template.

  - The Security Operations team will periodically perform an access review of **GitLab infrastructure** accounts, to include a [least privilege review](/handbook/engineering/security/index.html#least-privilege-reviews-for-access-requests).
  - The Internal Audit team will periodically perform an access review of **financial application** accounts, to include a [least privilege review](/handbook/engineering/security/index.html#least-privilege-reviews-for-access-requests), as part of routine audits. A comprehensive access audit may be performed based on an annual risk assessment.
  - Quarterly access reviews and access recertifications are performed for all applications that are determined by Internal Audit to be [SOX-in-scope](/handbook/internal-audit/sarbanes-oxley/).
  - For source code security, access reviews for `gitlab.org` owners and maintainers will be performed quarterly by the Security Compliance team and verified by Infrastructure for appropriate permissions.

* As part of an access review, existing access may be modified or revoked. New access (not modification of existing access) requires the submission of a [New Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request).


* An [access review](/handbook/engineering/security/security-assurance/security-compliance/access-reviews.html) includes two parts:
  - review current access and access level appropriateness, i.e. Does team member need access and are the system entitlements that they have appropriate?
  - recertification of appropriateness of access and entitlements, i.e. Approve continued access to system at the same level

* Please note that access reviews should include a [least privilege review](/handbook/engineering/security/#least-privilege-reviews-for-access-requests). This is considered as part of the review of appropriateness of system entitlements, aka access level.

* Review and recertification is generally performed by team member's manager or someone above them in their reporting hierarchy. For example, review can be performed by a Director and include their direct reports' direct reports.

* If reviewer is not the manager of team member, reviewer should be the system owner or the data owner, or an individual with sufficient understanding of the system(s), the system entitlements, and the ability to assess the appropriateness of the access granted.

* Reviewers must never recertify their own access; this must be reviewed and recertified by an alternate system administrator, system owner, or the primary reviewer's manager (or someone above them in their reporting hierarchy).

* An access review should be documented and performed as part of a formal job transfer. This should be initiated by the team member transferring and their new manager.

Please refer to the [Access reviews](/handbook/engineering/security/security-assurance/security-compliance/access-reviews.html) page for additional information.


### Access Control Procedure Activities

GitLab's access controls include the following control activities:
1. user registration and de-registration
2. user access provisioning
3. removal of adjustment of user access rights
4. management of privileged access rights
5. management and use of secret authentication information
6. review and recertification of user access rights
7. secure log-on procedures
8. management of passwords and tokens
9. access to privileged utility programs
10. access to program source code

### Account Naming Conventions

- GitLab.com Administrator Account Naming Convention:
 - Use user's GitLab G-Suite email `+admin@gitlab.com` as the email address: **username+ADMIN@gitlab.com**
 - GitLab.com admin account name should the user's normal account with `-admin` appended: **username-admin**
 - The admin account "Full name" should include text to indicate it is an admin account: **First Last (Admin)**

- Temporary Contractor Account Naming Convention: **username-CTR@gitlab.com**

### Automated Group Membership Reports for Managers

If you would like to check whether or not a team-member is a member of a Slack or a G-Suite group, you can view the following automated group membership reports:

[G-Suite Group Membership Reports](https://gitlab.com/gitlab-com/security-tools/report-gsuite-group-members)

[Slack Group Membership Reports](https://gitlab.com/gitlab-com/security-tools/report-slack-group-members)

### Unique Account Identifiers

Every service and application must use unique identifiers for user accounts and prevent the re-use of those identifiers.

For example, if a user account is identified with a username, there can only be one account with that username. Accounts may eventually be deleted and that username (or other unique identifier) intentionally released for re-use, but that new account may not have the same permissions or access as the first account that was deleted. This doesn't preclude the use of shared accounts (except where it is strictly forbidden, like in-scope PCI systems) and applies to both individual and shared accounts. If a shared account is used, that account must have a unique identifier in the same way an individual, non-shared account does.

This is required to allow the actions of any given account to be associated back with that particular account. If two accounts share an identifier, if a malicious action were taken, we'd have no way of identifying which of the two accounts performed that malicious action. It's also important to preserve the confidentiality of information; if access or permission are given to an account, they should only be given to the specific account for which they were intended.