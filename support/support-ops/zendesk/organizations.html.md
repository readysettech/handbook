---
layout: handbook-page-toc
title: Zendesk Organizations
---

# Zendesk Organizations

Organizations are simply a collection of users in Zendesk (much like groups).
We use them to also store metadata (synced from Salesforce), which is used to
determine such things as SLA, ARR, etc.

## Organization Fields

| Field Named | API Name | Data Type | Possible Values |
|-------------|----------|-----------|-----------------|
| Salesforce ID                | salesforce_id | Text     | * |
| GitLab Plan                  | support_level | Dropdown | Basic, Premium, Custom, Bronze, Silver, Gold, Expired, Hold, Starter, Ultimate, Community |
| ARR                          | aar | Decimal  | * |
| Number of Seats (deprecated) | number_of_seats | Number   | * |
| Market Segment (deprecated)  | market_segment | Dropdown | Large, Mid-Market, SMB |
| Sales Segmentation           | sales_segmentation | Text     | * |
| Account Owner                | account_owner | Text     | * |
| Account Type                 | account_type | Dropdown | Authorized Reseller, Customer, Former Customer, Integrator, Partner, Prospect, Unofficial Reseller, Reseller |
| Technical Account Manager    | technical_account_manager | Text     | * |
| AM Project ID                | am_project_id | Text     | * |
| Number of Seats              | seats_decimal | Decimal  | * |
| Manual Support Upgrade       | manual_support_upgrade | Checkbox | True, False |

## How does SLA get determined for an organization?

This stems from the `GitLab Plan` field. It correlates as follows:

| GitLab Plan | SLA |
|-------------|-----|
| Bronze                        | Standard SLA |
| Silver                        | Priority SLA |
| Gold                          | Priority SLA |
| Starter/Basic                 | Standard SLA |
| Premium                       | Priority SLA |
| Ultimate                      | Priority SLA |
| Custom/Expired/Hold/Community | Free tier, no SLA |

When multiple of these tags appear on the same ticket, it will apply the SLA
policy that comes first (order wise). See [Zendesk SLAs](slas.html) for more
details.

### What is an organization has multiple subscriptions?

This is an edge case Support-Ops and Sales-Ops are working on. The current
solution is to apply the correct tag to the organization so it will get multiple
plan tags on newly created tickets. As an example:

> Jason Enterprises has a Gold subscription and a Starter license.
> 
> Salesforce has them as Gold, so the organization in Zendesk shows their
> GitLab Plan as Gold.
>
> To ensure they get the proper support (and the ticket routes properly), we
> need to manually apply the starter tag on the organization.

## Organization Permissions

By default, organizations are setup so that the users within it can only see and
comment on their own tickets. This security measure often doesn't work for some
organizations though.

Because of that, we have the ability to setup Shared Organizations, a term
meaning the users in an organization have heightened permissions and can do see
and/or comment on tickets that are not theirs. 

## User Association

By default, users do not automatically associate with an organization. To
associate a user to an organization, this must be done manually by an Agent.

That said, if the organization has a domain set, then any email address that
uses that domain will automatically be associated to the organization. This can
create a bit of chaos though, as it does not use any measure to authenticate
an email to the organization. It simply looks at the email address and used the
domain portion of it (ie. the part after `@`). 

When multiple organizations are using the same domain, it will not associate the
user to both organizations. This is because users can only be associated with
one organization (as per our setup). Because of this, they will be associated
to the organization with the lower ID number. As an example:

> Bob emails support from his email, bob@awesome-company.com
>
> There are currently two organizations using the domain awesome-company.com:
>
> Jason's Awesome Company (ID: 123)
> Nabeel's Awesome Company (ID: 119)
>
> Because Nabeel's Awesome Company has a lower ID, Bob is associated with that
> organization.

Zendesk does not have a native way to determine if multiple organizations are
using the same domain. As such, you must be careful about setting organization
domain's. 