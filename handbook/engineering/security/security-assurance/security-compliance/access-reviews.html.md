---
layout: handbook-page-toc
title: "Access Reviews"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}


## Purpose

**User access review process is an important control activity required for internal and external IT audits, helping to minimize threats, and provide assurance of who has access to what. This page will help provide context and guidance of access reviews for GitLab.**

####  Benefits to the organization:

* Reducing risk
* Identifies dormant and/or disabled accounts
* Ensures only required team members have access to a system
* Validates users who have changed roles have not retained access no longer relevant
* Terminated team members no longer can access company systems

### Access Review Responsibility Matrix

|  Type | Frequency | In-Scope Systems | Out-of-Scope |
| :---: | :---: | :---: | :---: |
|  Terminated User | Quarterly | Security Compliance | System Owner |
|  Least Privilege | Annually | Security Compliance | System Owner |
|  Entitlement | Annually | Security Compliance | System Owner |

### Types of Security Compliance Access Reviews

**Terminated Users**

* On a quarterly basis, collect the current access listings of systems and correlate against a list of active employees derived from data originating in BambooHR (GitLab's source of truth for employment status). If any users are found to have active system access that are not current GitLab employees, open access removal issues to kick off the access de-provisioning process.

**System Owner**

* Access for their system will be reviewed based on the job roles and departments, a system owner should have detailed knowledge of which roles/deparments should have access to their system.  These reviews will occur on an annual basis.  If a job role is deemed to be not applicable to have access to a system, a secondary review will go the team member(s) manager to determine if access is required.

**Team Member Manager**

* Access will be reviewed by a team member's manager for each system they have access for continued validation.  These reviews will occur on an annual basis or when a system owner identifies out-of-scope access and a secondary review is required.

Please Note: *By utilizing both system owner and team member manager access reviews we can maintain the least privilege model through checks and balances.*

## Audit Requirements

#### Timing of Quarterly Access Reviews

* The quarterly access review cycle starts after the close of each fiscal quarter and is performed as a "look back", i.e. the review of the appropriateness of the access and the access permissions is performed retroactively for the previous quarter.

* Quarterly access reviews will be staggered across the quarter's three months timespan and be completed by the end of the month they are assigned. In other words, the quarterly access review cycle should take no longer than 28-31 days, depending upon the number of days in the month.

* By completing the access review within a month's timeframe, we ensure the access data has not become stale and will pass audit review.


#### Access Review Notification Reminders

Security Compliance managed access reviews required for audit evidence have a deadline of 10 business days from the creation of the access review issue.  Automated reminders will be used based on number of days out from the due date:

|  Days until Due Date | Notification | Who is Notified |
| :---: | :---: | :---: |
|  5 | Comment within access review issue | Reviewer |
|  3 | Slack ping | Reviewer |
|  2 | Comment within access review issue & <br/>Slack ping the Reviewer | Reviewer, Reviewer's Manager, and Security Compliance Manager |
|  0 | Escalated to VP of Security | VP of Security |

{-If an access review is not completed within 10 days, identified access will be removed.-}

#### In-Scope Systems Required for Compliance

`The following table lists the systems that the security compliance team will perform access reviews for directly. The systems are directly related to security audit and regulatory requirements as well as the supporting critical systems.`

|  **System** | **Function** | **Department** | **Frequency** | **Quarter Month** | **Requirement(s)** |
| --- | --- | --- | --- | --- | --- |
|  ADP | Payroll (US) | Finance | Quarterly | 1 | SOX |
|  Avalara | Taxation | Finance | Quarterly | 2 | SOX |
|  BambooHR | HR Portal | People | Quarterly | 3 | SOX |
|  Bastion host | Jump server | Infrastructure | Quarterly | 1 | SOC2 |
|  Blackline | Reconciliation tool for AP | Finance | Quarterly | 2 | SOX |
|  Carta | Stock option administration, capitalization table and equity management application | Finance | Quarterly | 3 | SOX |
|  Chef server | Configuration management | Infrastructure | Quarterly | 1 | PCI |
|  customers.gitlab.com | Subscriptions | Fulfillment | Quarterly | 2 | PCI & SOX |
|  dev.gitlab.org | Developer Platform |  | Quarterly | 3 | PCI |
|  Expensify | Expenses | Finance | Quarterly | 1 | SOX |
|  Fivetran | Data loader primarily for Netsuite data | Data Team | Quarterly | 2 | SOX |
|  gitlab.com | GitLab service | Infrastructure | Quarterly | 3 | PCI, SOC2, SOX |
|  gitlab.com database | GitLab database | Infrastructure | Quarterly | 1 | SOC2 |
|  gitlab.com database console | GitLab database console | Infrastructure | Quarterly | 2 | SOC2 |
|  gitlab.com implement/deploy | GitLab implement/deploy | Infrastructure | Quarterly | 3 | SOC2 |
|  gitlab.com source code | GitLab service source code | Infrastructure | Quarterly | 1 | SOC2 |
|  Google Cloud Platform | Main Production Cloud Environment | Infrastructure | Quarterly | 2 | PCI & SOC2 |
|  Greenhouse | Recruitment | People | Quarterly | 3 | SOX |
|  GSuite | Email, calendar, drive, groups | IT Operations | Quarterly | 1 | PCI |
|  license.gitlab.com | Generate licenses |  | Quarterly | 2 | SOX |
|  NetSuite | Finances: chart of accounts, journal entries, variance analysis, period close | Finance | Quarterly | 3 | SOX |
|  Okta | Authentication | IT Operations | Quarterly | 1 | SOX |
|  SalesForce | Sales CRM | Sales | Quarterly | 2 | SOX |
|  Snowflake | Data Warehouse | Data Team | Quarterly | 3 | SOX |
|  Stitch |  |  | Quarterly | 1 | SOX |
|  Stripe | Subscription Payment Processer | Finance | Quarterly | 2 | PCI & SOX |
|  Tipalti | AP Automation | Finance | Quarterly | 3 | SOX |
|  TripActions | Corporate Travel | Finance | Quarterly | 1 | SOX |
|  Workiva | Financial Reporting Software | Finance | Quarterly | 2 | SOX |
|  Zuora | Sales order invoicing & processing | Finance | Quarterly | 3 | PCI & SOX |

#### Out-of-scope Systems

The systems listed in the previous section will have access reviewed by the Security Compliance team.  All other systems, containing data ranging from green to red data classifications, require system owners to review access on a quarterly basis to identify and de-provision terminated users. A least privilege and entitlement review of all systems will be performed annually.

The [Access Review](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=) template available in the Access Requests project provides the outline to complete these access reviews, including how to confirm [least privilege](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege).

In the event access is identified to no longer be required, open an [Access Removal](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=) issue for each account that no longer requires access and related it to the system access review issue.

If you have any questions or require assistance with completing an access review, please [contact the GitLab Security Compliance team](/handbook/engineering/security/security-assurance/security-compliance/compliance.html#contact-the-compliance-team).

## Access List For Review

#### Access List Generation

Based on how the system access is maintained will determine the method of account and related permissions export for access review.  This will most likely fall to the business or technical owner identified in the [Tech Stack Applications](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit#gid=0).

* A system owned by Infrastructure will require an issue opened in the [Infrastructure Project](https://gitlab.com/gitlab-com/gl-infra/infrastructure) for access listing export request

##### Access List Data Fields

The following fields are the most comprehensive to assist in performing a thorough access review: (all are helpful, but all might not be available)

* Account Name
* User Name
* Email Address
* Access Permissions (level of access - user, admin,etc.)
* Account Creation Date Timestamp
* Last Access Date Timestamp

#### Access Listing Generation Validation

* If you are performing an access review, you must review the [Access Review Guidelines, including Access List Generation procedures](https://gitlab.com/gitlab-com/team-member-epics/access-requests/blob/master/README.md#additional-access-review-and-access-list-generation-guidelines) prior to starting the review process, which includes the user list generation procedures. It is important to understand the population generation requirements so completeness and accuracy of the listing and the review performed can be evidenced.

From the [Access Review](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Access%20Review) template:

* Please attach a system-generated access list along with evidence of how listing was produced, which should include date data was pulled. Timestamp should include the day, month, and year the listing was pulled.
* Evidence of how the listing was pulled generally takes the form of screenshots from within the system interface; the screenshots document the steps taken within the system to generate the user listing.
* If a query was used to generate the list, please provide the query along with a screenshot of system used to pull data, e.g. PostgreSQL query window, making sure screenshot evidences date/time query was run and raw row count. This will be used to evidence completeness of the population.
* To evidence completeness and accuracy, where technically feasible, include a row count or a screen shot of the row count or the generated file hash.

#### How to provide a desktop timestamp screenshot:
1. Please make sure that your workstation system clock (date and time) is visible in your screenshots.

<img src="/images/handbook/engineering/security/access-review/AR_1.png">

1. To enable this, if you are using a Mac, click on the time in the top right corner of your Mac:

<img src="/images/handbook/engineering/security/access-review/AR_2.png">

Open Date & Time Preferences and add date:

<img src="/images/handbook/engineering/security/access-review/AR_3.png">

#### How to hash files for list validation:

GCloud:
1. Open the [Google Cloud console terminal](https://console.cloud.google.com/) and use the hash command to calculate the hashes of local files `gsutil hash [-c] [-h] [-m] filename...`

<img src="/images/handbook/engineering/security/access-review/gsutil_hash.png">

2. Download the file to desktop
3. Open the Terminal app, change directory to location of the file
4. Use the md5 command to calculate the hash of the file `md5 filename...`

<img src="/images/handbook/engineering/security/access-review/terminal_hash_validation.png">

5. The values should be identical, if not, start over at step 1

## Access Review Process Next Steps

### In Progress

* Automation of in-scope systems (FY21-Q2)
    * Chef Data Bags
    * customers.gitlab.com
    * Expensify
    * Google Cloud Platform   
    * NetSuite
    * Zuora

* Documentation of in-scope system permissions for least privilege review

* Development of a standard 

### Future

* Continued automation of in-scope systems

* Develop process for team member manager access review by end of FY21
