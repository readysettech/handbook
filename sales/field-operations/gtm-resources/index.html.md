---
layout: handbook-page-toc
title: "Go to Market"
description: "Operations, Procedures, Documentation"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

----
{::options parse_block_html="true" /}

## Reaching the Teams (internally)

##### Issues and Projects

- [Sales](https://gitlab.com/groups/gitlab-com/sales-team/-/issues) - general sales related needs & issues
- [Marketing](https://gitlab.com/groups/gitlab-com/marketing/-/issues) - all issues related to website, product, design, events, webcasts, lead routing, social media and community relations
- [Customer Success SA Triage](https://gitlab.com/gitlab-com/customer-success/sa-triage-boards) - technical pre-sales requests

##### Slack: A short list of the helpful Slack channels
- `#customer-success`
- `#sales-support`
- `#sfdc-users`
- `#sdr_global`
- `smb`
- `#mktgops`
- `#outreach`
- `#it_help`
- `#marketing_programs`
- `#marketing`

## Glossary

| Term | Definition |
| :--- | :--- |
| Accepted Lead | A lead a Sales Development Representative agrees to work until qualified in or qualified out |
| Account | An organization tracked in salesforce.com. An account can be a prospect, customer, former customer, integrator, reseller, or prospective reseller |
| AM | Account Manager |
| AE | Account Executive |
| APAC | Asia-Pacific |
| CS | Customer Success |
| EMEA | Europe, Middle East and Africa |
| EULA | End User Licence Agreement |
| High intent | an event, webcast, demo that is a strong indicator of purchase or evaluation |
| Holdover Account | Account ownership retained by someone other than the territory owner |
| Inquiry | an Inbound request or response to an outbound marketing effort |
| IQM | Initial Qualifying Meeting |
| LATAM | Latin America (includes all of Central & South America) |
| MQL | Marketo Qualified Lead - an inquiry that has been qualified through systematic means (e.g. through demographic/firmographic/behavior lead scoring) |
| MVC | [Minimal Viable Change](/handbook/product/product-principles/#the-minimal-viable-change-mvc) (not Model View Controller)|
| NCSA | North, Central, South America (legacy region being phased out) |
| NORAM | North America |
| Qualified Lead | A lead a Sales Development Representative has qualified, converted to an opportunity and assigned to a Sales Representative (Stage `0-Pending Acceptance`) |
| RD | Regional Director |
| ROW | Rest of World |
| SAL | Strategic Account Leader |
| Sales Admin | Sales Administrator |
| Sales Serve | A sales method where a quota bearing member of the sales team closes the deal |
| [SAO] | Sales Accepted Opportunity - an opportunity Sales agrees to pursue following an Initial Qualifying Meeting |
| SDR | Sales Development Representative |
| Self Serve | A sales method where a customer purchases online through our web store |
| SLA | Service Level Agreement |
| SQO | Sales Qualified Opportunity |
| TAM | Technical Account Manager |
| TEDD | Technology, Engineering, Development and Design - used to estimate the maximum potential users of GitLab at a company |
| Won Opportunity | Contract signed to Purchase GitLab |

[SAO]: /handbook/marketing/revenue-marketing/sdr/sales-sdr-alignment/#criteria-for-sales-accepted-opportunity-sao

## Customer Lifecycle

A customer lifecycle is a term used to track the different milestones prospective customers go through as they learn about GitLab and interact with our sales and marketing teams.
Each subsequent milestone is a subset of the previous milestone, and represents a progression from not knowing GitLab to being a customer (and fan) of GitLab.

At the highest level of abstraction, we use the terms `lead`, `opportunity`, and `customer` to represent a person's progression towards becoming a customer of GitLab.
Those three terms also correspond to record types in salesforce.com.

Lead => Opportunity => Customer

However, there are more granular steps within the above milestones that are used to track the above process with more precision.
They are tracked as follows:

| Funnel stage | Record Type | Status or Stage |
| :----------- | :---------- | :-------------- |
| Raw | [Lead or Contact] | Raw |
| Inquiry | [Lead or Contact] | Inquiry |
| Marketo Qualified Lead | [Lead or Contact] | MQL |
| Accepted Lead | [Lead or Contact] | Accepted |
| Qualifying | [Lead or Contact] | Qualifying |
| Qualified | [Lead or Contact] | Qualified (converted) |
| Pending Acceptance | [Opportunity] | 0 - Pending Acceptance |
| [Sales Accepted Opportunity] | [Opportunity] | 1 - Discovery |
| Sales Qualified Opportunity | [Opportunity] | 2 Scoping - 5 Negotiating |
| Customer | [Opportunity] | 6-Closed Won |

For the definition of the stage please click the record type link.

When going from Qualifying to Qualified Lead the lead is duplicated to an opportunity, and the lead is set to qualified and not being used anymore.

[Lead or Contact]: #lead--contact-statuses
[Opportunity]: #opportunity-stages
[Sales Accepted Opportunity]: #criteria-for-sales-accepted-opportunity-sao

Note: Our lifecycle is undergoing a revamp! See how things are progressing [here](https://gitlab.com/gitlab-com/marketing/marketing-operations/issues/298).

## SAL Sales Capacity

The following calculation is used to measure/plan for sales capacity.
This is a calculation only and should be used to set goals and plan.
Sales capacity is an individual metric that is based on several factors (lead source, tenure of salesperson, competitive landscape, geographic location, rep productivity) not included in the formula below:

* Days to close - 180 days
* Months to close - 6 months
* Win rate - 33%
* Months to lose - 3 months (half of months to close, expecting constant fallout)
* Months on average - 4 (33.3% times 6 and 66.7% of 3)
* Capacity Goal (active opportunities in [Stage 1-6](#customer-lifecycle)) - 40 opportunities
* [SCLAU](#glossary) per month - 10 (40 opportunities / 4 months)

## How tos & Setup

##### Events 
Conferences, Field Events, Owned Events

Event details are owned by the Field Marketing Team with execution of system tracking, landing pages, reminders, and follow up completed by Marketing Program Managers.
See the [events handbook page](/handbook/marketing/events/) for more details.

#### How to do Step 1 cleanup of lead lists before passing to MktgOPS

[List cleaning instructions](/handbook/marketing/marketing-operations/list-import/#import-cleaning-template)

## Record Management

##### MQL Definition and Scoring

A breakdown of MQLs and lead scoring can be found in the [marketing operations handbook](/handbook/marketing/marketing-operations#mql-scoring-model).

##### Segmentation

Sales Segmentation is based on `Total Employee` count of the `Global Account`.
If a `Global Account` has a lower segment than any of its child accounts, the `Global Account` will adopt the largest sales segment of any of its child accounts.
  * `Large` = 2,000+ total employees
  * `Mid-Market` = 100-1,999 total employees
  * `SMB` (Small Business) = 0-99 total employees

`Total Employee` count is based on the number of employees that our data tools return for that account **as determined in the [sales segment review process time period](#Sales-Segment-Review-Process)**.
We use a hierarchy structure to determine what the number of employees is for the account.
The hierarchy of our data tools on *Accounts* as they relate to the `Total Employee` count is shown below.

1. DataFox.......(Default Value)
2. Zoominfo...(Only used if DataFox Employee Count field is blank)

LinkedIn/Websites are not designated data sources.
If a prospect communicates a different employee size from DataFox/Zoominfo that conflicts with segmentation of what is determined by DataFox/Zoominfo then SalesOPS should be notified via chatter on the record.
Admins have the ability to override the `Number of Employees` and bypass this hierarchy but only during our [sales segment review process](#Sales-Segment-Review-Process).

##### Sales Segment and Hierarchy Review Process

In order to address issues when it is believed that the `Total Employee` count is incorrect the Sales Ops team on a Yearly schedule (Fiscal Q4) will review accounts where individuals think that the segment is incorrect as well as any account that has had their number of employees changed (according to our data sources).
Reviews for updates to the `Total Employee` count field that do not result in a change of segment will not be reviewed.

For an individual to submit an account for review as it relates to the number of employees at the account they must fill out the following two fields on an accounts:
* `[User Input] Employee Count` - This is a number field that you think the number of employees should be
* `[User Input] Employee Source` - This is a URL field that links to where the above information was found

For an individual to submit an account for review as it relates to the hierarchy and final address of the account they must fill out the following four fields on an account:
*  `Account Zip - Manual - User` - This is a text field to be populated with Global Account HQ's Zip
*  `Account State - Manual - User` - This is a text field to be populated with Global Account HQ's State
*  `Account Country - Manual - User` - This is a text field to be populated with Global Account HQ's Country
*  `Account Address - Manual Source - User` - This is a URL field that links to where the above information was found

Examples of valid sources include but are not limited to financial filings, newspaper articles, reports directly from the company.
As a rule LinkedIn is not accepted as a valid source.
During the Sales Ops review period it is at the discretion of the Sales Ops team to have the `Total Employee` count updated or to have it remain the same.

If the number of employees, according to our sources based on our hierarchy as described in [Segmentation](#Segmentation) has changed, the Sales Ops team will automatically update the accounts segment and resulting ownership at the completion of the review process.

While the review process occurs over the course of Q4 the results of the process will not be put into place or enforced until the begining of Q1 (or as announced by the Sales Ops team).

##### Region/Vertical

  * **VP Commercial Sales** (Mid-Market & Small Business): Ryan O'Nell
  * **[Europe, Middle East and Africa](#emea)**: Jon Burghart, Regional Director
  * **[Asia Pacific](#apac)**: Anthony McMahon, Regional Director
  * **[North America - US East](#us-east)**: Mark Rogge, Regional Director
  * **[North America - US West](#us-west)**: Haydn Mackay, Regional Director (Timm Ideker - Interim)
  * **[Public Sector](#public-sector)**: Paul Almeida, Director of Federal Sales

### Territories

[Territory tables](/handbook/sales/territories) are maintained within the Sales Handbook.
Both maps & written tables are kept up to date with all pairings and territory assignments.
Our LeanData routing workflows and SFDC reports are based on these tables.

The Location of each account used to determine its Sales Territory is determined by a combination of 3rd party data systems (Datafox, Zoominfo) and manual overrides.
This address is stored in "Account - Territory" on the Account object in SalesForce.
This field inherits data from other fields in the following priority: 1. Admin Manual Override (if present) 2. Datafox 3. Zoominfo 4. Shipping Address 5. Billing Address.


### Account Ownership Rules of Engagement

1. **Source of Data**: The data source priority order for `Employee` count, `Address`, `Industry` and `Corporate Hierarchy` will be Datafox, Zoominfo, Linkedin; otherwise <blank> or `[[unknown]]` until resolved through manual research.
Any disputes must follow the Final Decision Escalation Process below.
These data points are locked in during [the sales segment review process](#sales-segment-review-process) .
1. **Account Ownership**: Will be determined by the **Sales** `Segment`, `Address` and `Corporate Hierarchy` and all children accounts, regardless of physical location.
All of the accounts will be owned by the *Global Account* owner unless it is either a Named Account (see point 3) or it has been agreed upon by both reps and their managers that the customer is best serviced by the *Territory* rep (see point 13).
1. **Named Account**: Defined as an account that is owned by a sales rep regardless of corporate headquarters.
A sales rep will own no more than 30 named accounts.
1. **Transfer of Named Accounts**: A transfer and ownership time frame of a Named Account should be agreed upon by both sales reps and their managers.
1. **Open Opportunities of Transferred Accounts**: Any open opportunity on an account subject to transfer to the *global account* owner will remain with the original owner for a period of no more than 180 days after opportunity creation.
No later than the 120 day mark, the original owner can request an extension and must provide sufficient evidence that the deal will close within the next 90 days.
If the evidence is insufficient, the *global account* owner can request that the opportunity be transferred immediately.
The are two reports that track holdover opportunities: [New Business/Add Ons](https://gitlab.my.salesforce.com/00O61000004hitu) and [Renewals](https://gitlab.my.salesforce.com/00O61000004hmUy).
These reports should be reviewed weekly by new account owners expecting to receive a holdover opportunity that has stalled or existing opportunity owners whose opportunities may be subject to transfer to the new account owner.
1. **Reassigning to a Territory Rep**: The *global account* owner can reassign any child account to a *territory rep* if it is determined that the client/prospect would be best serviced by a local rep.
To do this, please Chatter the *territory rep* and provide an explanation on the transfer.
Please review point 12 'Considerations for Transferring an Account to a Local Rep'.
1. **Requesting Reassignment**: A *territory rep* can request reassignment of a child account if they feel that the client/prospect would be best serviced by a territory rep as opposed to the *global account owner*.
To do this, the *territory rep* must Chatter the *global account* owner and provide an explanation, (please see point 12, “Considerations for Transferring an Account to a Local Rep”).
It is at the discretion of the *global account* owner to keep or reassign the account, but they must provide a compelling and explicit reason why a *territory* account should be managed globally.
If the *territory rep* does not agree with the decision, it can be discussed by their respective managers.
1. **Parent/Child Segmentation**: All Accounts in a hierarchy will adopt the MAX Segmentation of any account in the hierarchy.
1. **Changes to Ultimate Parent Details**: In the event of a merger or acquisition, or any other changes that impact the ownership of an account, such as a move of headquarters to another territory, either the *global account* owner or *territory* sales rep should submit the updated information in accordance with [the sales segment review process](#sales-segment-review-process), who will then initiate a review of all affected accounts.
A transition plan (if needed) should be agreed upon by all reps and their managers.
1.  **Exceptions**:
    1. **Spirit of Collaboration**: All requests and or actions must adhere to the GitLab Value of “Collaboration” and proactively communicate the inquiry and/or intent to all parties affected.
    1. **Indisputable** (not including Employee Count): reps must provide evidence and Sales Ops will render ruling; otherwise escalates to Final Decision Escalation Process.
    1. **Screenshots of data**: Since datasources may change over time, please capture screenshots of Employee count/location data that contradict our sources of data and save in a Google doc to share with Sales Operations.
    1. **Newly updated accounts**: will be reviewed in the annual review process as this impacts TAM and quota assignment.  Holdover of an active deal will be dealt with on a case-by-case basis following the Final Decision Escalation Process.
    1. **Stand-alone Child Account**: can be considered if the Child Account clearly has their own buying authority and purchasing process. For example:
        1. Private Equity or Holding Company : Child Accounts
        1. Government Holding Entity : Child Entity
        1. HQ : Franchises or Consultants (Note: Franchises do not count towards HQ Total Employee Count)
1. **Final Decision**: For a final decision on account ownership, the current and next ASM or above must both agree to transfer of ownership.
In all situations where an agreement between the ASM/RDs and/or VPs cannot be reached; CRO will determine final ruling.
1. **Ownership**: All Leads are to be owned by the owner of the Account (RD/SAL/AE) while All Contact ownership is determined by their assoaciated Accounts Segment, Type and respective team members assigned to the account as [per the handbook](#record-ownership).
**NOTE: Working a deal does not mean ownership.**
1. **Considerations for Transferring an Account to a Local Rep**: If the decision-making power, end users, PO and Terms (or a majority combination) are confined to the child account, the Ultimate Parent owner should hand off the Lead to the appropriate Territory owner as this would be in the best interests of the customer and for GitLab.

##### Website
Since an accounts `Website` is a key data point in determining [the accounts segment](#segmentation) and [the accounts address](#account-ownership-rules-of-engagement) and thus the resulting territory and ownership, the website on an account in salesforce is a required field on the layout.
In the event that the account is linked to an individual that uses a free email domain (or other similar cases) than the value of `[Blank]` should be used as the value for the accounts website.

##### Initial Source
 A breakdown of `Initial Source` can be found in the [marketing operations handbook](/handbook/marketing/marketing-operations/#initial-source).                                                     

##### Lead & Contact Statuses
 A breakdown of lead and contact statuses can be found in the [marketing operations handbook](/handbook/marketing/marketing-operations/#lead-and-contact-statuses).

##### Routing
Routing is determined by `Sales Segmentation`, `Region`, and `Global Account Ownership`. Routing through Lean Data when a record has no less than 30 points, this means that they have engaged with at least one piece of content or visited a high value page.

##### Routing & LeanData

**LeanData** works within the Salesforce ecosystem and is the primary tool leveraged to manage all routing workflows.
The Marketing Operations team is responsible for on-going management and customizations within LeanData.
For more information see the [dedicated LeanData page](/handbook/marketing/marketing-operations/leandata). 

##### Contact Requests

All `Contact Us` requests must be followed up within **one (1) business day** Service Level Agreement (SLA) and follow up must be tracked as an activity on the record within Salesforce.

U.S. Public Sector: Routed to the U.S. Public Sector Inside Sales team.
- [GitLab Public Sector Rules of Engagement](/handbook/sales/public-sector/)

##### Professional Service Requests

`Professional Service Requests` are treated like a [`Contact Us` request](#contact-us-requests) and followed up within **one (1) business day** Service Level Agreement (SLA).
Follow up must be tracked as an activity on the record within SFDC.

Requests submitted through the professional services page will be routed following `Global Account Ownership` rules.
Notification of form submission will be sent to the Strategic Account Leader (SAL) and Sales Development Representative (SDR) as well as Customer Success manager.
Initial response to form submission is the responsibility of the Account Owner (i.e. SAL).

##### Trial Requests

Trials can be requested through [web form](/free-trial/) or within product UI for both self-managed or SaaS.
Default trial length is thirty (30) days, but can be manually extended by the GitLab team for both the SaaS and self-managed products. Trial extensions for the SaaS product use the [`plan_change_request` issue](https://gitlab.com/gitlab-com/support/internal-requests/issues/new?issuable_template=plan_change_request) template found in the `dotcom` Group, `internal-requests` project.
Extending self-managed trials requires access to the internal `Licensing App`.

##### Universities

United States
- **Public** University = [Public Sector team](/handbook/sales/territories#public-sector)
- **Private** University = [Public Sector team](/handbook/sales/territories#public-sector)

Rest of the World
- **Any** University = appropriate regional Sales Development Representative

##### Record Ownership

Contact Ownership follows the rules as laid out below:
- Large Accounts
   - SDR (If present otherwise AE)
- MM & SMB Accounts
   - Customer Accounts
      - AE
   - Non-Customer Accounts
      - SDR (If present otherwise AE)

When an SDR is assigned to an Account to support and assist with outreach, the SDR will be added in the `SDR Assigned` lookup field to the account in Salesforce.
This field then populates down to the related Contact records.
Only SDRs are able to edit the `SDR Assigned` field and if there is a need to mass update the `SDR Assigned` on many accounts then the SDR should reach out to a member of the Sales Ops Team for support.

Records, both `LEAD` and `CONTACT`, need to be synced to Outreach to ensure email activity is properly mapped back to `Activity History` in SFDC.
The owner of the record in SFDC **does not** need to match the owner in Outreach.

##### Record Ownership and Record Visibility

In order to meet compliance standards our SFDC instance uses a private model.
This private model allows for some records to be visible by all Gitlab team members who use Salesforce, while other records may not be visible to them.
Currently this is in place as it pertains to records owned by the Public Sector team.
All salesforce records (leads, contacts, accounts, opportunities etc.) owned by the Public Sector team are only visibily to other members of the public sector team and a group of supporting staff who have been reviewed and permitted to view the these records.
All other records (owned by non-public sector team members) maintain their standard visibility levels.

This is important as it relates to inbound records or accounts in a sales reps name.
If you believe you have been incorrectly assigned a record that should belong to the public sector team member please coordinate with your manager, the sales-ops team or a member of the public sector team to review the record.

## Changing Ownership in Salesforce

##### Changing Account Ownership in Salesforce

Everyone in Salesforce has **some** ability to change the ownership of accounts.
When accounts have their owners changed, by anyone other then an admin, there will be an email notification go out to both the previous account owner and the new account owner.
This is to allow individuals to change ownership of accounts if they think they should belong to them.
If there are any questions in regards to who should own an account Sales Ops will assist in that decision and you can mention @sales-ops in salesforce.
It's also important that just because a user can change the owner of an account does not mean that they should own the account.
Please refer to the criteria for reassigning accounts and our account territories for more information.

Criteria for Reassigning Accounts:
*  The account must have its address in the account owners territory.
If the account has a parent account or the parent account also has a parent account the address that determines the final owner of the account is the address of the ultimate parent.
This address follows our data hierarchy - with Datafox being our primary source of data (Link to come).
*  The account must also have a matching sales segmentation that the owner should be working.
Any Account adopts the highest sales segment that exists within an account hierarchy.
Segment is determined by our data hierarchy - with Datafox being our primary source of data (Link to come).
*  Any owner of an account must follow our guidelines for [Record Ownership](#record-ownership)

1.  Any account owner can reassign their own account to someone else
2.  Any RD can reassign any account
3.  Any Team Lead can reassign any account that is located within their region
4.  Anyone can reassign any account as long as the following criteria is met
    A.  The account does not have a parent account
    B.  The account is located in the same region as the individual transferring ownership of the account
    C.  Datafox has enriched the number of employees on the account
    D.  The sales segment of the account is the same as the segment that the user is working on (SALs/Large,AEs/Mid-Market)
5.  Any Admin can reassign any account

##### Changing Contact Ownership in Salesforce

Contact Ownership follows the rules as laid out below. This contact ownership cannot be updated as it is maintained by an [automated process in Salesforce](/handbook/sales/field-operations/sales-systems/gtm-technical-documentation/#contact-ownership)

- Large Accounts
   - SDR (If present otherwise AE)
- MM & SMB Accounts
   - Customer Accounts
      - AE
   - Non-Customer Accounts
      - SDR (If present otherwise AE)

##### Changing Lead Ownership in Salesforce

Everyone is able to change the owner of a Lead as long as they are either changing the Lead Owner to match the Account Owner or they are the current Lead owner.
Lead ownership is set by LeanData due to specific rules by segment and by region/territory which may include round robin. Any lead unable to be routed, is routed to an SDR Queue for the SDR management team to determine proper ownership. For the most part, Leads are owned by SDRs.
##### Default Ownership

*  In the event that Ops encounters that there is not enough information to assign a record to a specific user in Salesforce it is to be assigned to the default user: [`Sales Admin`](https://gitlab.my.salesforce.com/00561000000mpHT?noredirect=1&isUserEntityOverride=1).
**This user should only be used by ADMINS. Non-Admins should not be reassigning records to this user**.
Before assigning to this user, admins should do their best to assign records to the actual users within Salesforce.
If you are unsure of who to assign it to please coordinate with the SalesOps Team.
This is also only a temporary solution until we have a more scalable solution in place that will reassign records to individuals who can and will actually be able to work records.

##### Record Creation in Salesforce

ACCOUNT/CONTACT records in Salesforce are created in a number of ways - [list imports](#list-imports), [mass creation screen flows](#mass-create-contact-on-opportunities-with-contact-roles), field event booth scans, research, networking, webcasts, content downloads.
Ideally all ACCOUNTS exist in Salesforce and team members are only creating CONTACT records; however, if a connection is made at an event and follow up needs to be done *prior* to official event list upload occurs team members should do the following:
   - Search Salesforce to be sure ACCOUNT does not already exist **AND** search using the person's email address to ensure duplicate record is not created
   - Record **does not** exist:
        - Create `Standard` ACCOUNT type - required fields are `Account Name` & `Account Type`
        - Create `Standard` CONTACT type - required fields are `Last Name`, `Account Name` (use lookup tool to find ACCOUNT just created) & `Initial Source` (i.e. where is this name coming from `Conference` = Field Event, `SDR Generated` or `AE Generated` = regular networking event, etc)
        - Be accurate where the name is collect from, `Unknown` is **not** acceptable.
        - The `Initial Source` on a CONTACT record *does not* equal `Source` on an opportunity. Refer to [`Initial Source`](#initial-source) for guidance on why this is important.
   - Record **does** exist:
        - If LEAD or CONTACT is unowned or "owned by Sales Admin, James Harrison or Chad Malchow", this record is adoptable by anyone - change `Record Owner` to your name
        - If LEAD or CONTACT is owned by SDR team member, **before** reaching out Chatter on the record asking SDR to transfer ownership. Ownership *must* be transferred **before** reaching out to avoid confusion, cross-communication and/or multiple people reaching out to same contact.

When official event list import is completed the created ACCOUNT or CONTACT record will be appended with the additional data collected at the event.
If there are any questions or you need assistance, please ping Marketing or Sales OPS in Slack `#sfdc-users` channel.

##### Best practices

1. Be as accurate with your data as possible.
If you do not have a Contact `Phone` do not substitute the Account `Phone` - Leave it blank on the Contact record.
2. Search the database for duplicates before creating new records.
3. When merging records, retain the `Initial Source` of the record that was created first.

##### Mass create contacts on opportunities with contact roles

This process is specific for the unique cases of creating totally new contacts for an account that also have to be associated with an opportunity.
An example of when to use this process is when you meet a number of new contacts at an account during a demo for a specific opportunity.
The process to create these contacts for that account and to have them related with that opportunity would be through the steps listed below or as demonstrated in this [video](https://drive.google.com/file/d/1iEO4dQUAfa4tkbEmip1Xne7-9Tg2nR6h/view?usp=sharing):

1. Navigate to the Opportunity record in Salesforce that these contacts should be associated with
2. Click on the button `New Contacts & Opp Contact Roles`
3. Follow the screen flow and instructions for creating all contacts and associating them with the opportunity, providing all required and known information
4. If there is additional information for any of the contacts that you have but you were not able to input the information via the screen flow, navigate to the contact(s) once the operation is complete and fill in any additional information you have for the contact(s)

It is important to note that by following this process that all contacts must meet the following criteria:
1. All of the contacts that are created are to be associated with both the account and opportunity for that opportunity record.
2. All of the contacts are net new and do not exist within Salesforce already - as either contacts or leads.
3. All of the contacts will be assigned a contact role on the opportunity.
4. There already is a primary contact, or one of the new contacts will be the primary contact on the opportunity.

##### Rules of Engagement

Named Accounts are owned and worked by the designated Strategic Account Leader (SAL) and the paired Sales Development Representative (SDR).
This pairing owns all records (LEADS and CONTACTS) associated to a Named Account and any related Child accounts within SFDC.
See [global ownership](#global-account-ownership) and [named account](#named-account-ownership) descriptions above.

Territories are assigned based on [Sales Segmentation](#segmentation) and routing for each type of inbound request is [listed above](#lead-routing).

LEAD/CONTACT Records with the `Initial Source` of `GitLab.com` are **not** to be engaged, prospected or targeted unless they have taken a handraising 'active' activity, such as `Trial - Enterprise`, `Trial - GitLab.com`, `Contact Us`, `Demo`, 'Webcast', 'Content' and/or engaged in `Web Chat`.

For information about GitLab's email policy and the types and number of emails we send, please see our [Email Communication Policy](/handbook/marketing/marketing-operations/index.html#email-communication-policy).

##### Active vs. Passive

`Initial Source` cannot be used to determine if a lead is 'active' or 'passive' since the Initial Source is set upon first touch attribution; therefore, looking at the `Last Interesting Moment` field is the primary field used to begin determining if a record is actively being worked.
Reviewing the `Activity History` in Salesforce is another factor considered when evaluating 'active' or 'passive'.

A LEAD or CONTACT is considered 'Active' if they have taken an `Trial - Enterprise`, `Trial - GitLab.com`, attended a high intent live webcast or demo and/or engaged `Web Chat`, these are all handraising 'active' activities.
These types of records are considered 'Active' for a minimum of 60 days from the date of the handraising activity.
For example: the record is considered 'Active' for entire duration of EE trial, plus 30 days after `EE Trial End Date`.

## Campaigns
Salesforce campaigns are used to track efforts of marketing tactics - field events, webcasts, content downloads, etc.
The campaign types align with how marketing tracks spend and align the way records are tracked across three of our core systems (Marketo, Salesforce and Bizible) for consistent tracking.
Leveraging campaign aligns our efforts across Marketing, Sales and Finance. For information on integrated campaigns (managed by Marketing Programs), please see the [Integrated Campaigns handbook page](/handbook/marketing/campaigns/) and to learn more about planned, in progress, and previously executed campaign tactics, please see the [Marketing Programs handbook page](/handbook/marketing/revenue-marketing/digital-marketing-programs/marketing-programs/).

## System Set-up

##### Marketo Programs

The Marketo programs for the corresponding campaign types have been prebuilt to include all the possible necessary smart campaigns, email programs, reminder emails and tokens that are to be leveraged in the building of the program.

You can find a breakdown of all Marketo program types and progression statuses in the [Marketing Operations handbook](/handbook/marketing/marketing-operations/#campaigns)

##### Reports and Dashboard Naming Convention 

Naming convention for reports and dashboards will leverage sequence of periods (.) to help identify importance. 

- . [Name of Report or Dashboard]
- **Example**:  
   - . Sales Dashboards 
   - .. APAC ENT Dashboards
 
## Opportunities

##### Criteria for Sales Accepted Opportunity (SAO)

The following criteria are **required** for all SAOs:
An Opportunity is deemed a Sales Accepted Opportunity (SAO) when the Opportunity is moved from Stage `0-Pending Acceptance` to `1-Discovery` by the Strategic Account Leader.

The following criteria is required for an SDR to submit an opportunity to sales:

**Authority**
The prospect being met is directly involved in a project or team related to the potential purchase of GitLab within this buying group, either as an evaluator, decision maker, technical buyer, or *influencer.
*If the “influencer” is not directly involved (i.e. is related to a "decision maker" in another group/division or someone who is not directly tied to the opportunity at hand) the SDR will continue to own the opportunity and will seek to set-up the next meeting with a key contact in the buying group (leaving 0-pending status until date/referral is confirmed), updating the current opportunity with the new directly-involved point of contact in the buying group once it's acquired.

**Initiative**
An initiative the company is working on has been identified and GitLab can potentially help the initiative.
Identified by either a business problem (i.e too many tools), strategic direction or modernization interest (impetus to change).

**Fit**
The following fields have been obtained:
* Current DevOps or software development lifecycle tools (from conversation or credible data source)
* Expected entry point use case (e.g. SCM or CI)
* Potential seats of the first opportunity (if this is a new account or buying group)

**Timing**
After the initial qualifying meeting with the account leader/executive, there must be a next step that is set to occur within a *60 day timeframe.
(*If next step isn’t within a 60 day timeframe, the opportunity remains in stage 0 and in SDR ownership to nurture until the next step is actualized.)

_**SDR best practice:**_
Ask prospect about their environment, what they develop software for etc. to try build a picture of the company and how we will be able to help them.
Share relevant resources with the point of contact.
Add other potential influencers/buyers from that company into our database and the Outreach cadence in an effort to build more momentum within that organization.

_**Before the IQM with the account leader/executive, the SDR will also aim to gather:**_
* SaaS vs. Self Hosted
* Potential Future Seats in the Buying Group
* Total Seats Available Estimate at the company

_**Post IQM:**_
Opportunities in `1-Discovery` stage are accepted and owned by the account leader/executive.
The account leader/executive is responsible for the progression, activities, engaging other resources, and converting this early engagement to a mutual win.
The Sales account leader/excutive is responsible for taking the next step within 60 days, or reverting the opportunity back to SDR ownership or disqualifying the SAO if ultimately there is no opportunity.
Managers should be able to use the 'NEXT STEP DATE' field to determine if the IQM has taken place but opportunity has not been moved to new stage.
Opportunities should be moved to new stage within 48 hours of IQM.

##### How to create an Opportunity

An OPPORTUNITY can be created in Salesforce a) when converting a LEAD to CONTACT; b) from a CONTACT.
**All opportunities** should be created with a Stage = `00-Pre Opportunity` regardless of how you create the OPPORTUNITY.
Once the initial setup is complete, the [OPPORTUNITY Stage](#opportunity-stages) can updated based on the criteria below.

##### Creating a New Business Opportunity from CONTACT record
{:.no_toc}

1. On CONTACT record, click the `New Opportunity` button. Required fields are:
     * Opportunity Name - using [Opportunity Naming Convention](#opportunity-naming-convention)
     * Account Name = This should NOT need to be changed as it pulls from the CONTACT object
     * Type = `New Business`
     * Initial Source = DO NOT CHANGE
     * Close Date = if no time frame defined, **SDR** set close date rolling 9-months
     * Stage = `00-Pre Opportunity` - starting stage for ALL opportunities
     * Add as much detail on the OPPORTUNITY record as you can.
     * Click `SAVE`
2. Scroll down OPPORTUNITY record to the `Contact Roles` section, **click** `New`. CONTACTS associated to the ACCOUNT will be listed (up to 50 records). You must select a CONTACT as **Primary** and define the `Role`.
     * If you do not define a **Primary** CONTACT marketing attribution & activity influence on the OPPORTUNITY will not be accurately captured.
3. Change the OPPORTUNITY Owner to the `Account Owner` (i.e. SAL/AM). Click `Save`.
4. Within the OPPORTUNITY record, click the `Initial Qualifying Meeting` button. Enter the required fields (Start/End dates, Type) and update the description field with any notes the SAL/AM should have and review *before* taking the scheduled meeting.
     * Fill in the `Related to` section for BOTH the CONTACT and the OPPORTUNITY
     * Change the `Assigned to` field to the OPPORTUNITY owner
     * Click `Save`
5. Update the OPPORTUNITY Stage from `00-Pre Opportunity` to the correct stage -> normally `0-Pending Acceptance`.
6. Update the 'NEXT STEP DATE FIELD' with the date of the next action step (most often an IQM).
7. Enter in 'NEXT STEPS' with details that correlate to the NEXT STEP DATE FIELD.

##### Creating a New Business Opportunity from LEAD record
{:.no_toc}

1. On LEAD record, fill out the required qualification questions, add additional notes to the optional sections if gathered AND update to `Lead Status` = `Qualified`. Click **`Save`**.
2. Click the `Convert` button:
     * Change `Record Owner` to the Account Owner (based on [Global Ownership rules](#global-account-ownership))
     * Check the "Send Email to the Owner" box
     * Lookup the correct `Account Name` - if unsure assign OPPORTUNITY to the "Parent" account
     * Opportunity Name - using [Opportunity Naming Convention](#opportunity-naming-convention)
     * Click `CONVERT`
          * If CONTACT record exists, associate converted LEAD to existing CONTACT. *Do not create duplicate if possible*
3. The OPPORTUNITY will need to be updated with the following:
     * Click `Edit`
     * Type = `New Business`
     * Initial Source = DO NOT CHANGE
     * Close Date = if no time frame defined, **SDR** set close date rolling 9-months
     * Add as much detail on the OPPORTUNITY record as you can.
     * Click `SAVE`
4. Scroll down OPPORTUNITY record to the `Contact Roles` section, the converted LEAD will automatically be set as **"Primary"**. Click `Edit` and define the `Role`.
     * Add any additional CONTACTS and define their `Role` that need to be associated with the OPPORTUNITY
     * Opportunities must have a **Primary** CONTACT defined so marketing attribution & activity influence is accurately captured.
Change the OPPORTUNITY Owner to the `Account Owner` (i.e. SAL/AM). Click `Save`.
5. Within the OPPORTUNITY record, click the `Initial Qualifying Meeting` button. Enter the required fields (Start/End dates, Type) and update the description field with any notes the SAL/AM should have and review *before* taking the scheduled meeting.
     * Fill in the `Related to` section for BOTH the CONTACT and the OPPORTUNITY
     * Change the `Assigned to` field to the OPPORTUNITY owner
6. Update the OPPORTUNITY Stage from `00-Pre Opportunity` to the correct stage -> normally `0-Pending Acceptance`.
7. Update the 'NEXT STEP DATE FIELD' with the date of the next action step (most often an IQM).
8. Enter in 'NEXT STEPS' with details that correlate to the NEXT STEP DATE FIELD.

##### Creating an Add-on Opportunity
{:.no_toc}

An `Add-On` OPPORTUNITY will inherit information from the *original* `New Business` OPPORTUNITY.
The steps to create an `Add-on` OPPORTUNITY varies slightly from the instructions above because this type of OPPORTUNITY is created from the `New Business` OPPORTUNITY **not** from a converted LEAD or CONTACT.

This creates a parent-child relationship between the *original* `New Business` OPPORTUNITY and the `Add-on` OPPORTUNITY.

1. Navigate to the *original* `New Business` OPPORTUNITY (this will become the "parent" opp).
     * Example: If you are selling additional seats to an existing subscription - you should go to the original `New Business` OPPORTUNITY.
2. Click the `New Add-on Opportunity` button.
3. **UPDATE** the OPPORTUNITY Name - see the [Opportunity Naming Convention] guidelines
4. Define:
     * `Initial Source` = see the [definition table](#initial-source) to choose the most correct source. It is important to be accurate as this does impact reporting and marketing attribution.
     * Close Date = if no timeframe defined input close date on a rolling 9-months.
     * Stage = All opportunities start as `00-Pre-Opportunity`
5. Add any additional details on the OPPORTUNITY record
6. Click `Save`

Within the parent-child OPPORTUNITY hierarchy some information will pass from the parent (`New Business`) to the child (`Add-on`). This information will be used in our reporting and analysis to track add-on business OPPORTUNITIES to their `Initial Source` and contributing team members.

There are additional validation rules that are presently in effect:
- The **Parent** OPPORTUNITY must either be a `New Business` or `Renewal` OPPORTUNITY.
- A **Parent** OPPORTUNITY *cannot* be another `Add-on` OPPORTUNITY
- All sales-assisted non-portal `Add-on` OPPORTUNITIES **must** have a parent opportunity.

##### Creating an Upside IACV Opportunity
{:.no_toc}

An `Upside IACV` OPPORTUNITY will inherit information from the *original* OPPORTUNITY.
The steps to create an `Upside IACV` OPPORTUNITY varies slightly from the instructions above because this type of OPPORTUNITY is created from the OPPORTUNITY **not** from a converted LEAD or CONTACT.
An `Upside IACV` OPPORTUNITY has a minimal amount of fields as it's only for tracking the potential upside amount.

This creates a parent-child relationship between the *original* OPPORTUNITY and the `Upside IACV` OPPORTUNITY.

1. Navigate to the *original* OPPORTUNITY (this will become the "parent" opp).
2. Click the `Upside IACV` button.
3. **UPDATE** the OPPORTUNITY Name - see the [Opportunity Naming Convention] guidelines
4. Define:
     * Close Date = if no timeframe defined input close date on a rolling 9-months.
     * Amount = the upside value in addition to the Parent OPPORTUNITY value. If Parent OPPORTUNITY amount is $100,000 and total OPPORTUNITY amount potential is $150,000, then the Upside IACV amount is $50,000
6. Click `Save`

When the PARENT OPPORTUNITY is changed to "Closed Won" or "Closed Lost," please update the stage of the UPSIDE IACV OPPORTUNITY to "Duplicate."
In order to save this change, you must also enter the PARENT OPPORTUNITY name in the "Duplicate Opportunity" field on the UPSIDE IACV OPPORTUNITY.

Note: Upside IACV opportunities exist for tracking purposes only.
All final IACV (including any won upside IACV) will be attributed to the PARENT OPPORTUNITY.

##### Creating a Professional Services Opportunity
{:.no_toc}

A `Professional Services` OPPORTUNITY will be used to cover any integration, consulting, training or other service that a Sales rep will sell to a prospect/client and needs or wants to be invoiced separately.
To invoice separately a new quote and opportunity must be created.

A full list of professional services can be found [here](/handbook/customer-success/professional-services-engineering/#professional-services-offerings).
See [Working with Professional Services](handbook/customer-success/professional-services-engineering/working-with/) for workflow details.

##### Steps for creating a Professional Services opportunity in SFDC

1. Navigate to the *original* OPPORTUNITY (this will become the "parent" opp).
2. Click the "New PS Opportunity" button and fill out the following:
     * OPPORTUNITY Name = will already be set correctly; do not change
     * Type = do not change it will populate from parent OPPORTUNITY
     * Initial Source = do not change it will populate from parent OPPORTUNITY
     * Close Date = if no timeframe defined input close date on a rolling 9-months.
     * Stage = All opportunities start as `00-Pre-Opportunity`
     * Professional Services Value (ProServe Value) = enter dollar value, which is defined as the total value of all consulting, training, integration, or other professional services as outlined in the Statement of Work.
     * ACV = **do not populate** an automated workflow will fill this information
     * Amount = **do not populate** an automated workflow will fill this information
     * Professional Services Description, Project Scope, Task Schedule and Key Assumption fields = these will push to the Statement of Work when a PDF is generated from Zuora.
     * Verify the `Professional Services` OPPORTUNITY has the *original* OPPORTUNITY in the `Parent Opportunity` field. If this is not a validation rule error will occur while attempting to save the OPPORTUNITY.
3. Click `Save`
4. To create a quote, see the ['Creating Accounts, Contacts, Opportunities and Quotes'](/handbook/sales/#creating-accounts-contacts-opportunities-and-quotes-in-salesforce) and begin with Step 4. Here is a [video](https://drive.google.com/file/d/142csIZyrzIfSJOSJkIAK6d9c1JwTO_Rq/view?usp=sharing) that hightlights the process.

##### Tracking Sales Qualified Source in the Opportunity

Sales Qualified Source is dimension used when analyzing pipeline creation, lead conversion, sales cycles, and conversion rates.
Sales Qualified Source may be different from the Lead Source of an Opportunity, which captures the original source (event, campaign, etc).
For example, if a prospect originates from a trial (lead source), that prospect can be qualified by a SDR, Account Executive, Channel Partner, or the Web (sales qualified source).

The logic for the Sales Qualified Source is as follows:

2. If the Sales Development Representative field (Opportunity) is populated, regardless of opportunity owner, the Sales Qualified Source is "SDR Generated"
3. If the Sales Development Representative fields are NULL and the opportunity owner is:
   * a Regional Director, Account Executive, or Account Manager, the Sales Qualified Source is "AE Generated"
   * a GitLab team-member that is not a Regional Director, Account Executive, or Account Manager, the Sales Qualified Source is "Other"
   * an authorized reseller, the Sales Qualified Source is "Channel Generated"
   * the Sales Admin, the Sales Qualified Source is "Web Direct Generated"

##### Reseller Opportunities

Opportunities utilizing a reseller require slightly different data:

Lead/Contact:
The partner record should be converted to their company channel type account.
The end user record should be converted to the end user standard account type.

Opportunity Name:
If the partner is an authorized reseller, rename the opportunity with the partner’s nick-name in front, then a dash.
For instance; if it is a Perforce deal, the opportunity name should start with P4 - (whatever your opportunity name is)
This is important for the workflow that solicits updates from the reseller.

Account Name:
It is important that opportunities using a reseller are created on the END CUSTOMER’s account, and not the reseller’s account.
The account name on an opportunity is never a reseller.
Resellers do not buy licenses; they purchase them on the behalf of an end customer.
For instance, the account name field on an opportunity should never be SHI.

Opportunity Owner:
The AE/SAL/Channel Manager who is working the deal with the reseller

Deal Registrant:
The reseller who registered the deal.

Associating Contact Roles:
After creating the opportunity, click “New” in the contact section to associate contacts with the opportunity.
 - The primary contact should always be a contact at the end user’s account and not a contact at the reseller.
 This is important as resellers come and go, and if we do not capture the contact at the end user account, we will not be able to sell to this account if the reseller ends their relationship with us or with the end account.
 - A reseller contact (say, the sales rep at ReleaseTEAM) can, and should be added to the opportunity with the role of Influencer.
 NOTE: A contact that works for a reseller should never be added to an end user account.
For instance an employee of SoftwareOne should be a contact of the SoftwareOne account only, and not the Boeing account.

Associating Partners to an Opportunity:
After creating the opportunity, click “New” in the Partners section to associate the reseller with the opportunity.
 - You can associate multiple partners with an opportunity if there is more than one reseller involved in the opportunity.
 This is not uncommon for government opportunities, or opportunities where the customer is asking multiple fulfillment houses (like SHI and SoftwareOne) to fulfill the order.
 - Unofficial resellers should never be marked primary
 - If there are any authorised resellers associated, at least 1 must be marked as primary
    - In order of precedence this would be:
        - The deal registrant (`Deal Registrar` field in SFDC, This should be confirmed with the appropriate channel manager)
        - The deal fulfiller (i.e.: The one issuing the PO)
        - The distributor

Opportunity Team List:
Add the reseller user to the Opportunity team list with the role of “Reseller” or else they cannot see the opportunity.

##### Opportunity Naming Convention

Opportunities for subscriptions will use the following guidelines:

- **New Business**: [Quantity]
   - [Name of Company]- [Quantity] [Edition]
   - Example: Acme, Inc- 50 Starter

- **Add-On Business (seats only)**:
   - [Name of Company]- Add [Quantity] [Product]
   - Example: Acme, Inc- Add 25 Starter

- **Add-On Business (Upgrade from Starter to Premium)**:
   - [Name of Company]- Upgrade to Ultimate
   - Example: Acme, Inc- Upgrade to Ultimate

- **Renewal Business (no changes)**:
   - [Name of Company]- [Quantity] [Product] Renewal [MM/YY]
   - Example: Acme, Inc- 50 Premium Renewal 01/17

- **Renewal Business + Add On Business (seats)**:
   - [Name of Company]- [Quantity] [Product] Renewal [MM/YY]+ Add [Quantity]
   - Example: Acme, Inc- 50 Premium Renewal 01/17 + Add 25

- **Renewal Business + Upgrade**:
   - [Name of Company]- [Quantity] Upgrade to Premium + Renewal [MM/YY]
   - Example: Acme, Inc- 50 Upgrade to Premium + Renewal 01/17

- **Professional Services**:
   - [Name of Company]- Professional Services [MM/YY]
   - Example: Acme, Inc- Professional Services 06/18

- **Refunds**:
   - [Original Opportunity Name] - REFUND
   - Example: Acme, Inc- 50 Upgrade to Premium + Renewal 01/17 - REFUND

## Opportunity Types

There are three things that can be new or existing:

- Account (organization)
- Subscription (linked to a GitLab instance)
- Amount (dollars paid for the subscription)

That gives 4 types of opportunities:

1. **New account** (new account, new subscription, new amount): This type should be used for any new subscription who signs up either through the sales team or via the web portal.
Paid training also falls under this type if the organization does not have an enterprise license.
This should be marked as New Business.
1. **New subscription** (existing account, new subscription, new amount): If an existing account is purchasing a new license for another GitLab instance, this will be New Business.
1. **Add On Business** (existing account, existing subscription, new amount): This type should be used for any incremental/upsell business sold into an existing subscription division mid-term, meaning not at renewal.
This may be additional seats for their subscription or an upgrade to their plan.
If an existing account is adding a new subscription, this would be new business, not an add-on.
1. **Renewal** (existing subscription, existing subscription, existing amount): This type should be used for an existing account renewing their license with GitLab.
Renewals can have their value increased, decreased, or stay the same.
We capture incremental annual contract value growth/loss as a field in Salesforce.com.
Renewal business can be a negative amount if renewed at less than the previous dollars paid for the subscription (renewal rate).
Only the part that is more or less than the old amount is IACV, the rest is part of the renewal opportunity.
 * In the event that the customer wants to reset their contract, this would be considered a renewal.
For example, a customer starts January 1st for 12 months, but wants to reset starting April 1st for another 12 month term.

**New business** is the combination of new account and new subscription

##### Opportunity Stages

To help move sales through the sales process, [here](https://docs.google.com/document/d/1ag7YY9aJ93j0CRZb-DrbfgH3vmHprTEdjG7l3O57xEk/edit) is a list of questions to ask at each stage

**00-Pre Opportunity**- This stage should be used when an opportunity does not meet our opportunity criteria. However, there is a potential for business, and it should be tracked for possible business.
* What to Complete in This Stage:
  * Schedule a discovery call with prospect to determine if there is an opportunity to pursue; or
  * If there is no opportunity then the stage would be updated to 9-Unqualified.
* Creating an Opportunity in this stage from Contacts
  * If you are qualifying a contact for a new business opportunity, open an opportunity in this stage and use the qualification questions in the qualification section on the opportunity while qualifying the contacts.
  * "Convert" Opportunities from this stage to **0-Pending Acceptance** when the opportunity meets [our criteria for an opportunity](/handbook/marketing/revenue-marketing/sdr/sales-sdr-alignment/#criteria-for-sales-accepted-opportunity-sao)
  * Follow [our process](/handbook/sales/field-operations/sales-operations/deal-desk/#zuora-quote-configuration-guide---standard-quotes) on creating opportunities from a contact record.

**0-Pending Acceptance**: This is the initial stage once an opportunity is created.
* What to Complete in This Stage:
  * For SDR sourced opportunities, the opportunity meets [Sales Accepted Opportunity criteria](/handbook/marketing/revenue-marketing/sdr/sales-sdr-alignment/#criteria-for-sales-accepted-opportunity-sao).
  * The SDR has scheduled a call via Google Calendar, sent invites, created an event on the account object, named the event: GitLab Introductory Meeting - {{Account Name}}
  * Once it is confirmed that the opportunity meets our Sales Accepted Opportunity criteria, the SAL or AE should move the opportunity to the next stage and the `Amount` field must be populated with estimated pipeline. The date the opportunity moves from this to the next stage in the sales cycle will populate the `Sales Accepted Date` field on the opportunity record.
  * If the details on the opportunity do not meet our Sales Accepted Opportunity criteria, the SAL or AE should move the opportunity to an `8-Unqualified` stage (this is the only time an opportunity can move into `8-Unqualified` stage) or to `00-Pre Opportunity` if passed back to an SDR for further qualification.
  * All Opps that are sales assisted must first enter this stage before they can be moved further in the pipeline. If they do not enter this stage at some point you will encounter a validation rule error.

**1-Discovery**: Uncover as much intelligence about the project as you can, which will be confirmed at later stages throughout the sales cycle.
* What to Complete in This Stage:
  * Begin filling out [MEDDPICC](/handbook/sales/#capturing-meddpic-questions-for-deeper-qualification)
  * Send Plan Letter/Recap Email to Attendees- [Example](https://docs.google.com/document/d/16Gurj_MVREmKoqXTdB1F0OQ3eyq1gzbTNU8LNHHuoEM/edit)
  * Scheduled Scoping Call
  * Provide an estimate for the `Expected Number of Users`  and the `Expected Product` for the Opportunity. This information is used to help the customer success team to predict their future workload as well as to help them with their hiring plans.
  * Should the opportunity progress from `1-Discovery` to the next stage (not 7-Closed Lost or 9-Duplicate), it will be considered a `Sales Qualified Opportunity`. The following values are entered once the opportunity progresses from this stage:
     * `Sales Qualified` is True.
     * `Sales Qualified Date` is the date the opportunity moves from this stage to the next open or won stage.
     * `Initial IACV` captures the value in the `Incremental ACV` field. `Initial IACV` is a snapshot field that will not change, even when the `Incremental ACV` field is updated and will be used for `Deal Size` analysis.

**2-Scoping**: Uncover business challenges/objectives, the competitive landscape, realizing fit.
* What to Complete in This Stage:
  * Complete a Demo (Optional)
  * Schedule a Technical Evaluation Call
  * Confirm and collect new [MEDDPICC](/handbook/sales/#capturing-meddpic-questions-for-deeper-qualification) information.

**3-Technical Evaluation**: Confirming technical requirements. A proof-of-concept (POC) might occur at this stage. This is also the stage to confirm information before a proposal is delivered.
* What to Complete in This Stage:
  *  Enter POC Notes and POC Success Criteria (if applicable) and enter into the POC Notes and POC Success Criteria fields related to the opportunity.
  *  Confirm *Technical Requirements, POC Scope*
  *  Confirm *Technical Win/POC Success*
  *  Confirm and collect new [MEDDPICC](/handbook/sales/#capturing-meddpic-questions-for-deeper-qualification) information.

**4-Proposal**: Business and technical challenges and been uncovered and resolved. A proposal is drafted and delivered to the prospect.
* What to Complete in This Stage:
  * Confirm Bill to Information (who will receive the invoices), Sold to Information (who will receive the license key). You should also confirm whether or not the customer will issue a PO, and whether there is a vendor registration form required by the customer.
  * Deliver formal contract to the prospect with complete bill to and sold to information. Remember that quotes with incomplete or incorrect information will be rejected by Deal Desk.
  * An MSA may be delivered separately
  * Clear understanding of purchase/contract review process and a close plan (actions to be taken, named of people to complete actions and dates for each action) documented in the Purchasing Plan field.

**5-Negotiating**: The prospect or customer has received the proposal and is in contract negotiations.
* What to Complete in This Stage:
  * Agreement on business terms
  * All proposals should include the standard GitLab [Terms](/terms/#subscription/)
  * Determine if customer will be referenceable when the opportunity closes. If the answer is:
       * "Yes" update the `Referenceable Customer` section on the Account object with appropriate reference information
       * "No" the discussion of being a reference can be revisited at a later date
  * Modifications will not be accepted to the standard terms for any opportunity that is less than $25k, or for Starter edition.
  * If the above threshold is met, requests for modifications to the standard terms should be sent to Legal by creating a legal case in SalesForce, following the process found [here](handbook/business-ops/order-processing/#process-for-agreement-terms-negotiations-when-applicable-and-contacting-legal).
  * If the Account is seeking to use their own paper, requests will only be entertained if the opportunity is greater than $100k, and the request should be sent to Legal by creating a Legal case in SalesForce, following the process found [here](handbook/business-ops/order-processing/#request-for-gitlab-review-of-customer-edits-to-gitlab-template-or-review-of-customer-agreement-template).

**6-Awaiting Signature**: The prospect or customer has verbally agreed to the terms and conditions outlined in the proposal and has submitted for signature.
* What to Complete in This Stage:
  * Received signed order form, which signals agreement of all pricing and legal terms.
  * Obtain a purchase order, if applicable.
  * Work with GitLab AR to deliver any tax and/or complete any vendor registration processes.
  * Ensure all relevant documents, MSA, PO, and other forms uploaded to SFDC in the Notes and Attachments section of the opportunity record.
  * EULA (End User Licence Agreement) has been accepted by end-user organization (if applicable).
  * If this is a large/strategic account, or if IACV is +$12,000, enter `Closed Won Details` summarizing why we won the opportunity.
  * Subscription created in Zuora.
  * Opportunity has been submitted for Finance approval.

**7-Closed Won**: Congratulations!! The terms have been agreed to by both parties and the quote has been approved by Finance.
* What to Complete in This Stage:
  * Introduce Customer Success/Account Management (if applicable)
  * Set a calendar reminder for 30 day follow up
  * If applicable, initiate Customer Onboarding or Premium Support onboarding

**8-Closed Lost**: An opportunity was lost and the prospect/customer has decided not to pursue the purchase of GitLab.
* What to Complete in This Stage:
  * Select all applicable Closed Lost Reasons
     * If the loss is due to Competitive Loss, you are required to select the competitor(s) from the opportunity's `Competitor` field
     * If the loss is due to Product Maturity, you are required to select the product stage(s) from the opportunity's `Product Maturity: Product Line` field.
  * In the `Closed Lost Detail`, enter as much detail as you can as to why we lost the deal. For example:
     * If they selected a competitor, why? Was it due to features or pricing?
     * If decided not to move forward with a project, what were the reasons? Did they not understand the value? Was there not a compelling event or reason?
     * Again, please be as thorough as you can as this information will prove valuable as we learn from these experiences.
  * Please note that for new business deals where the opportunity is with a Large/Strategic account OR the Incremental Annual Contract Value (IACV) is equal or greater than USD 12,000, then a notification will be sent to the [#lost-deals](https://gitlab.slack.com/messages/C8RP2BBA7) Slack channel.
  * Uncover a time for follow up (incumbent solution contract expiration date)
  * Note that if an opportunity is dead/stalled, mark the Stage as 8-Closed Lost. Should the prospect/customer re-engage before 30 days, you can reopen this opportunity. However, if they re-engage beyond 30 days, you will need to create a new opportunity.
  * If the `Closed Lost Reason` is "Merged into another opportunity" please link this closed opportunity to the opportunity you are merging it into by using the `Merged Opportunity` lookup field. Otherwise, you will encounter a validation rule error.

**9-Unqualified**: An opportunity was never qualified.
* What to Complete in This Stage:
  * Update Reason for Closed Lost and add any pertinent notes as to why the opportunity was not qualified.
  * A notification will be sent to SDR Team Lead and a feedback session should be scheduled between AE and Team Lead.

**10-Duplicate**: A duplicate opportunity exists in the system. This usually happens when a web direct opportunity is won when an existing opportunity already exists in Salesforce. Another reason could be multiple renewals created for the same opportunity. This stage **should not** be used when disqualifying an opportunity or if it is discovered at some point after acceptance that the opportunity is really part of a larger initiative. If the opportunity was accepted, it cannot be marked as a duplicate. Instead, you must mark the opportunity as `8-Closed Lost` and select the appropriate reason. Possible selections could include "Consolidating order - part of another subscription" or "Merged into another opportunity" as reasons why a duplicate opportunity may have been created.
*  What to Complete in this stage:
  *  Move the Opportunity into this stage
  *  Fill out the lookup field `Duplicate Opportunity` with the opportunity that this opportunity is a duplicate of. If this field is not populated you will encounter a validation rule error.

##### Opportunity Stage Movement Considerations

Note that once you qualify an opportunity via our standard qualification process, you cannot revert an opportunity back to the following stages: `00-Pre Opportunity`, `0-Pending Acceptance`, or `9-Unqualified`.
If you need to revert an opportunity you've previously qualified to one of these stages, please contact Sales Operations and we can determine why the opportunity (once qualified) is no longer qualified.

##### Reverting an Opportunity to a Previous Stage

If a previously met criteria has become unmet, you are required to revert back to the latest stage where all activities were completed.
For example, if a prospect had previously signed off on GitLab from a technical standpoint, requested a quote and has begun contract negotiations, you would set the opportunity to `5-Negotiating`.
However, if at any point during the negotiations, additional technical questions or requirements arise that result in a re-evaluation of GitLab's technical capabilities, you would revert the opportunity back to `3-Technical Evaluation`.
After the opportunity has once again met the stage completion criteria, you are able to move the opportunity to either `4-Proposal` if a new order form was created as a result of the additional technical requirements, or back to `5-Negotiating` if no changes were made to the original order form.

##### Locking Opportunities as a result of their "At Risk" potential

In order to be in compliance with US Regulations there is a need to screen opportunities against known individuals and organizations with whom we are not allowed to do business.
In order to comply with these regulations, opportunities are screened when they are created through a third party application, Visual Compliance.
Visual Compliance is a dynamic screening tool that constantly compares our account information with those sanctioned parties listed on various Denied Party Lists.
Visual Compliance will screen new information and will monitor existing information to ensure the integrity and legality of the parties with whom we do business.
The more **accurate** information in the Account--the better! Partial information may trigger a false ‘hit’ and cause delays.
Please provide the full company name, company address, country and contact name(s).

If you receive an error referencing export when attempting to update an Account:
(i) Check if the Visual Compliance Section of the Account says “Pending”-- Wait 15-30 minutes for the system to run its initial check and update.
(ii) If the Visual Compliance Section of the Account says  “Yellow” or“Red”-- The legal team is manually reviewing the Account to ensure compliance. Manual reviews of hits are conducted three (3) times a day.  
Changes by Legal will automatically update the Account, although updates may take 15-30 minutes to sync.
 - If the status has been updated to “Clear”, the order will process and account functionality will resume.
 - If the status is updated to “Escalate”, there is a concern with either the company itself or there is an attempt to sell in an embargoed country.  Escalated orders will not process.
(iii) If the Account requires immediate attention (i.e., to close a deal), open a Chatter message in the Account and message “@legal”.  Upon receipt of a request, the Legal team can review and update in Visual Compliance.  
Please understand that if Legal finds a problem, the flag and the account will remain locked down.

##### Executive Account Sponsorship Program

This program adds a member of e-group to be a dedicated part of the sales Account Team on a specific account.
The exec will maintain direct relationships with people at the account and participate in both remote and in-person meetings as appropriate.

Goal: Leverage our executive team to ensure great customer experience and direct two-way connection with GitLab and executive visibility into a small number of high-value customers.
This is intended to both support the customers to be successful and to provide insights to ensure GitLab is sucessful.
Examples of executive sponsor responsibilities may include (and not limited to) participation in quarterly account planning meetings, communications with the customer as well as helping to facilitate internal conversations & resources where necessary.

Very few accounts will have named sponsors; execs are still available as needed:
1. Only a small number of accounts can have exec sponsorship, so there is no guarantee for any account to necessarily have an assigned exec sponsor
2. Even though most accounts will not have an assigned exec sponsor, the exec team is available to support an engage all customers as needed.

Accounts are selected for and matched to an executive sponsor:
1. Total accounts with named sponsors: 10
2. Accounts may be nominated by Sales VPs and Confirmed by CRO after agreement with the named sponsor.
3. Sponsored accounts typically represent deep product utilization, large opportunity, and/or a broad vision for success and engagement with GitLab.

Example activities for sponsors:
1. SAL Exec briefing & initial Zoom w/customer exec champion
2. Quarterly Account Review Meetings
3. Two in-person meetings with account / yr
4. 1 year on the account

Process: 
1. Executive sponsors are to be involved in accounts *with and without* active opportunities. 
1. Once approved, Sales Operations will update the "Executive Sponsor" field.
1. Executive Sponsored Accounts are [listed in Salesforce](https://gitlab.my.salesforce.com/00O4M000004e2Ma)
1. Executive Sponsor [Briefing Template](https://docs.google.com/document/d/1No6Hzv2UoeFi6Bl8qtVUYYy2hDA7ChwoVENboh8wuVs/edit#)

## Types of Accounts

##### Accounts Created in Salesforce utilizing CE Usage Ping Data
The [CE Usage ping](https://docs.gitlab.com/ee/user/admin_area/settings/usage_statistics.html) provides GitLab with some limited insight into how end users are utilizing the platform.
The raw information is cleaned, enriched and then pushed to SFDC as an Account by the Data Team.

If there is not an existing account match in Salesforce, a new account record will be created with the following information populated:

| SFDC Field | Default Value |
|---|---|
| Account Name |  |
| Account Source | `CE Download` |
| Number of Employees |  |
| Billing Street |  |
| Billing City |  |
| Billing Zip |  |
| Billing Country |  |
| Account Type | `Prospect - CE User` |
| Account Website |  |
| Industry | Populated by Clearbit (since been deprecated) |
| Active CE Users | Populated by Usage Ping |
| CE Instances | Populated by Usage Ping |
| Account Owner | Sales Admin by Default |
| Using CE | Checked True |

**Process**
1. Sales Team members can use this data to proactively identify `Prospect - CE User` accounts that fit their target segment(s). Accounts owned by `Sales Admin` can be adopted by a Sales Team member changing ownership in Salesforce.
The adoption of any `Sales Admin` owned records will trigger an email alert that is sent to the Account Research Specialist for transparency and awareness of what account records have been claimed.
2. The Account Research Specialist will be responsible for reviewing the `Prospect - CE User` accounts on a regular basis to determine additional account records that should be worked either by a Sales Team member or Outbound SDR.
3. When an account record has been identified for follow up, the Account Research Specialist will work with the appropriate Regional Director (RD) to determine Outbound SDR assignment based on work load and available capacity.
4. The assigned Outbound SDR will work the `Prospect - CE User` account the same as any other known `CE User` account leveraging the tools at their disposal (Zoominfo, LinkedIn Sales Navigator, etc) to add contacts to the account record and populate the firmographic profile of the account.
