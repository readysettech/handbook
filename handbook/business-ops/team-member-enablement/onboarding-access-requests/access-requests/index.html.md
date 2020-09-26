---
layout: handbook-page-toc
title: "Access Requests (AR)"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Access Requests (ARs)

Access Requests are owned by the IT team, while onboarding, offboarding and internal transition requests are owned by the People Experience Team.

If you have any access requests related questions, please reach out to #it_help or the tool provisioner in Slack.

## Access requests related pages

<div class="flex-row" markdown="0">
  <div>
    <a href="/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/frequently-asked-questions" class="btn btn-purple" style="width:170px;margin:5px;">Frequently asked questions</a>
    <a href="/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/baseline-entitlements" class="btn btn-purple" style="width:170px;margin:5px;">Baseline Entitlements</a>
  </div>
</div>

## Need help?

- Please @ mention `@gitlab-com/business-ops/team-member-enablement` in the issue, with no particular SLA.
- If your request is urgent, @ mention `it-help`in the #it_help channel in slack with a note on why it is urgent.

## How do I choose which template to use?

#### [Single Person Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request)

_Do you have one person who needs access to a single system or one person who needs access to multiple systems?_

{::options parse_block_html="true" /}

<div class="panel panel-success">

**Instructions:**
{: .panel-heading}

<div class="panel-body">

1. Title issue "Full Name, Role, System(s)" using your information.
1. Fill out the `Person Details` section.
1. Add the public ssh key if the requestee needs ssh access.
1. **Remove or add lines** for the systems you need access to so only the ones you want are left in the issue. **Do not check them off.**
    - _Request the least amount of access you need as per the [least privilege review](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege) and explain why you need access in the rationale section and name the role you are requesting. Be specific._
1. If you are the manager of this person, add the labels `AR-Approval::Manager Approved` and `ReadyForProvisioning` to the issue; if you are the one asking for access, then you have to assign to _your_ manager for approval and they must add the labels `AR-Approval::Manager Approved` and `ready for provisioning`.
1. After approval, then YOU MUST **assign the issue to the system provisioner** [listed in the tech stack.](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit#gid=0)
1. Close the issue when it's complete.

</div>
</div>

---

#### [Bulk Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Bulk_Access_Request)

_Do you have a bunch of people with the same manager or part of the same department or division to add to the same system/vault/group?_

> Note: Admin access cannot be granted by bulk, please open single person requests.
> There is one exception to this rule: bulk requests that include admin-level permissions can be used when it is for the correction or realignment of baseline role entitlements.
> In cases where a team's baseline entitlements must be realigned or corrected, a bulk access request can be sumitted if realigned entitlements include admin-level permissions.

When access is being requested for multiple people who report to different managers but are part of the same department or division, approval can be obtained by the manager at the highest level; that is, the Director, Vice President, or Executive of the department or division.

<div class="panel panel-success">

**Instructions:**
{: .panel-heading}

<div class="panel-body">

1. Title issue: Bulk Access, Name of system/group/vault/etc.
1. Add all the email addresses or aliases depending on the tool separated by commas.
1. If you are the manager of these people, add the labels `AR-Approval::Manager Approved` and `ready for provisioning` to the issue; if you are included in this request for access, then you have to assign to _your_ manager for approval and they must add the labels `AR-Approval::Manager Approved` and `ready for provisioning`.
1. After approval, then YOU MUST **assign the issue to the system provisioner** [listed in the tech stack.](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit#gid=0)
1. Close the issue when it's complete.

</div>
</div>

---

#### [Shared Account Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Shared_account_access_request)

All shared accounts must be managed via Okta.
If 1password must be used (okta not technically possible), this needs to be outlined in the Access Request.

Prior to submitting this Issue Request, please review our [Access Control Policy and Procedures](/handbook/engineering/security/#access-control-policy-and-procedures) to ensure that your request is in line with GitLab's policies and procedures.
If after review you feel that a shared account is still needed, complete the form below.
**Note that systems with PCI data is not allowed shared accounts.**

Please note that shared account request(s) will need to be reviewed and approved by IT Ops and the listed Tech Stack Owner.
An [Exception Request](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/new?issuable_template=Exception%20Request) will need to be logged for each user you are requesting to be added.
Note that with an Exception Requet the maximum exception length is 90 days.
After the Exception Length, you will be required to submit another Exception Request for review and approval.
**If the exception request is not logged, reviewed, and approved for an extension, note that the Shared Account will be disabled.**
Please refer to our [Information Security Policy Exception](/handbook/engineering/security/#information-security-policy-exception-management-process) handbook page for more information.

<div class="panel panel-success">

**Instructions:**
{: .panel-heading}

<div class="panel-body">

1. Title issue "Shared Account Request, Role, System(s)" using your information.
1. Fill out the `User Details` section and **remove or add lines** as needed.
1. **Add lines** for the system(s) you need access to so only the ones you want are left in the issue.
    **Do not check them off.**
    - _Request the least amount of access you need as per the [least privilege review](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege) and explain why you need access in the rationale section and name the role you are requesting.
        Be specific._
1. If you are the manager of this person, add the labels `AR-Approval::Manager Approved` and `ready for provisioning` to the issue; if you are the one asking for access, then you have to assign to _your_ manager for approval and they must add the labels `AR-Approval::Manager Approved` and `ready for provisioning`.
1. After approval, then YOU MUST **assign the issue to the system provisioner** [listed in the tech stack.](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit#gid=0)
1. Close the issue when it's complete.

</div>
</div>

---

#### [Access Change Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Access_Change_Request)

Access Change Requests are logged when a team member no longer requires access to a currently provisioned system or no longer requires the same level of access (downgraded access from admin to user etc).
Refer to [`For People Ops Analysts: Processing Promotions & Compensation Changes`](/handbook/people-group/promotions-transfers/#for-people-ops-analysts-processing-promotions--compensation-changes) section of the GitLab handbook for additional information.

It is important to note that while Okta has provisioning/deprovisioning automation in place, this is not a complete/accurate reflection of access provisioning and deprovisioning.
Okta has been configured to assign integrated/implemented applications based on a user's role/group.
This makes applications accessible via Okta but users may still have the ability to access the systems directly.
Refer to [Okta Application Stack](/handbook/business-ops/okta/okta-appstack/) for a list of applications set up in Okta.

What this means is:

1. A GitLab Team member gets transferred to a different role.
1. The team member's profile in BambooHR is changed.
1. This profile change automatically triggers a change in his Okta profile accordingly.
1. This, in turn, results in the team member getting assigned to new applications based on his new department and role.
1. Simultaneously all old applications that are not relevant to his new role get revoked/unassigned.
1. Additionally, the Okta administrator gets an Email from Okta, that there has been a change to a User profile - (Email Subject line: 1 existing user updated). Okta automation already happens in the background, this email is informational only.

While this application automation will take place in Okta, "true" system provisioning and deprovisioning will still need to be manually completed within the impacted systems via an Access Change Request.

---

#### [Slack, Google Groups, 1Password Vaults or Groups Access Requests](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=slack_googlegroup_1Passwordgroupvault)

<div class="panel panel-success">
**Instructions:**
{: .panel-heading}
<div class="panel-body">

1. **Title** issue "Full Name - System - Role" (ex: Laura Croft Google Group: adventurer)
1. **Remove or add rows** for the access you need.
1. Assign to your manager to get approval by label **if** this request is for (they must apply labels `AR-Approval::Manager Approved` and `ReadyForProvisioning`:
    - access to a 1Password vault or group
    - admin access
    - access to a slack group for a non-internal person
    - Please note if a non-internal person has been removed from a slack channel and is requesting access again they will need a new access request and manager approval
1. **Close** the issue when it's complete.

</div>
</div>

---

## Single/Bulk Access Requests Instructions

##### Instructions and Guidance for Managers

1. Issues should only be approved after carefully considering whether the requestor needs the permissions outlined.
    Every review should include a [least privilege review](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege)
1. Add your approval by adding the label `AR-Approval::Manager Approved` and `ready for provisioning`.
1. If you do not approve, add a comment and close the issue.
1. If you are unsure whether the requestor needs the permissions outlined to fulfill their duties, mention `@gitlab-com/gl-security/security-assurance/sec-compliance` in a comment for assistance

##### Instructions and Guidance for Provisioners

1. Carefully review the rationale provided by the requestor to determine whether the access level is necessary or if a lower access level would be sufficient. Review the [Least Privilege](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege) write-up for guidance.
1. If manager approval is required for the request, verify the requester's manager has added the ~AR-Approval::Manager Approved label.
1. If the request involves access to critical Infrastructure systems, @ mention `Infrastructure-Managers` and ask them to approve by adding the ~InfrastructureApproved label.
1. If all necessary approvals have been granted, proceed with provisioning.
1. Edit the last column in the table to `yes` or `no` once you issue credentials/access or not, so it's clear you responded to the request.
1. If administrative access is being granted, mention `@gitlab-com/gl-security/secops` in a comment and add the label `admin-access` to this request so Security Operations knows who has admin access.
1. If requesting admin access, the system admin should additionally add the labels `SystemOwnerApproved` and `AdminLevelAccess` labels.

##### Instructions and Guidance for IT

1. Review the Shared Account Access Request and ensure that there is an [Exception Request](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Exception%20Request) for each user that is being added to the shared account.
1. Review the Exception Request and document in the Access Request issue the Exception Length.
1. Ensure that the Exception Request has been reviewed and approved by Security prior to adding your approval or setting up the shared account.
1. If the shared account will be managed in Okta - Set a review/reminder date in Okta to review shared account access dependent on exception timeline and close issue.
    1. When notification is received from Okta regarding timeline length nearing expiration, log a new Shared Account Access Request and assign to the Shared Account Owner to complete.
1. If the shared account will be managed in 1Password - Add a Due date dependent on exception timeline and leave issue open.
    1. When notification is received from `GitLab.com` regarding timeline length nearing expiration, close existing issue and log a new Shared Account Access Request and assign to the Shared Account Owner to complete.

## Working on Access Requests

##### Department Access Request Boards

- If you need additional labels or have suggestions for improving the process until we can fully automate, please [open an issue](https://gitlab.com/gitlab-com/business-ops/team-member-enablement/issue-tracker/-/issues/new).
- ARs are auto-assigned and auto-labeled when possible by department. In some cases, there are multiple provisioners per tool. If a template cannot be auto-assigned, Business Operations will provide a board where the provisioners can review their department's issues by label (ie `dept::to do`. It is up to the department to manage the workflow on who works the issues to completion.
- **Moving an issue from one column to another will remove the first label (per the column header) and add the second label. Please use caution when moving issues between columns.**
- Departments can check their outstanding access request issues by viewing their board below.

<div class="panel panel-success">
**AR boards: to-do:**
{: .panel-heading}
<div class="panel-body">

1. [Data](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1319045)
1. [Finance](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1319048)
1. [Infra](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1262513)
1. [IT](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1262521)
1. [Legal](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1319051)
1. [PeopleOPs](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1318841)
1. [Prod+Eng](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1319057)
1. [Sales](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1262518)
1. [Security](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1319052)
1. [Support](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/boards/1319053)

</div>
</div>
