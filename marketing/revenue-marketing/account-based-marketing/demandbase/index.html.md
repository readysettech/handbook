---
layout: handbook-page-toc
title: "Demandbase"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## What is Demandbase
Demandbase is a complete end-to-end solution for [Account-Based Marketing](/handbook/marketing/revenue-marketing/account-based-marketing/). We primarily use Demandbase as a targeting and personalization platform to target online ads to companies that fit our ICP and tiered account criteria. Demandbase also has a wealth of intent data that is available to us through its integration with Salesforce. 

We compile the intent data by building audiences, groups of target accounts with the most potential to purchase based on our buyer criteria, which we can then leverage for use throughout the funnel in advertising and SDR/sales follow-up. Demandbase also delivers ongoing signals around behaviors and intent to keep our list up to date. This information helps both marketing and sales focus our efforts on the right accounts. 

### Intent fields & definitions

In Salesforce, you will see a set of fields at the account level under the Demandbase section.  Below is a list of those fields that are populated by Demandbase and their definitions.

**Score** Demandbase uses AI to qualify accounts and give them a score based on their match to our ICP and their engagement on our website, and also offsite intent.  Scores are ranked High, Medium, and Low.  Demandbase's AI uses our ideal customer profile (Intent Keywords/Buyer Titles/Customers) to model and score/rank accounts based on:

*  Intent from target accounts

*  Buying committee titles within profile

*  Firmographics of customers in profile (Revenue, industry, geo location, employee size, etc.)

*  Products sold by customers in profile

**Trending onsite engagement** Shows us which accounts have been more engaged and active on our site over the last week compared to the last two months.

**Page views** The number of unique page views within the last thirty days.  We have scrubbed pages such as the careers page etc that do not show an intent to research or purchase GitLab.

**Sessions** Shows the number of unique visits the account has made to our website in the last thirty days.  A session is defined as a unique visit to our site of up to 30 minutes.  If they spend more than 30 minutes on our site this will count as two sessions.  It is generally considered that an account is engaged if they have three or more sessions in the past thirty days.

**Last Seen** The number of days since an account was last on our website.

**Rank** How an account ranks based on our profile within Demandbase

**Intent** This field will show you the top five keywords the account is researching

**Trending offsite intent** Shows if the account has had a recent spike in offsite research (in the last week compared to the last two months), including competitor research

**Change traffic MOM** Percentage of change, either increase or decrease of traffic on our website from the account month over month.

To date, we use the following Demandbase features:
- [ABM platform](https://support.demandbase.com/hc/en-us/sections/360003540751-ABM-Platform-Solution): identify the companies that meet your buying criteria and are showing the right intent signals
- [Targeting](https://support.demandbase.com/hc/en-us/sections/360003540771-Targeting-Solution): plan and implement targeting strategy
- [Self-serve](https://support.demandbase.com/hc/en-us/sections/360009465252-Getting-Started-with-Self-Serve-Targeting): easily set up, launch, and manage campaigns
- [Conversion](https://support.demandbase.com/hc/en-us/sections/360003566352-Conversion-Solution): give SDR and Sales teams the data and insights they need to better understand and target the right individuals, with personalized messages, within their target accounts, so they can close deals faster.
- [ABM analytics](https://support.demandbase.com/hc/en-us/sections/360003540851-ABM-Analytics-Solution): focus on business outcomes and report on account-level reach, engagement, and sales outcomes.
- [Site analytics](https://support.demandbase.com/hc/en-us/sections/360009288811-Site-Analytics-Solution): provide insight around channel performance (i.e. - display advertising, traffic, campaign influence) 

### Demandbase Audiences  
An audience is a list of accounts in Demandbase that we are using to look at intent or run a campaign against.

#### Audience naming convention:
The name of an audience should tell you who the DRI is (team) and what the list is for.  Audience names are editable so if you are unsure, please name using the following criteria and reach out to the ABM team on slack.

**Example: (FM) 20200901_SecurityWorkshop**

1. Team DRI for the list should be identified by the following:
- (ABS) Account Based Marketing & Strategy
- (FM) Field Marketing
- (M) General Marketing (includes growth, alliance, demand gen, etc)
- (S) Sales requests
2. Name of the list- what doe this list contain?
- campaign tag if it is an audience specific to a campaign
- intent based etc
- Segment- if an audience is a segment of a larger audience.  example: if you wanted to create a segment of this audience: (FM) 20200901_SecurityWorkshop it would be named (FM) Segment-20200901_SecurityWorkshop

#### How to build an audience
There are several ways to build an audience in Demandbase depending on what you are looking to accomplish.
1. CRM Report- you have a target account list that may be updated as the campaign progress.  These audiences are refreshed every Friday and will reflect any changes to the CRM report as such.
1. CSV upload- create an audience by uploading a CSV file to Demandbase.  This should be used with caution as any additions to the audience will need to be manually made both in Demandbase and Salesforce in order to report correctly on the campaign.
1. Site Analytics- create an audience based on intent using page views, hits to a certain page, etc.  This is a good way to build an audience if you are looking for a set of accounts that behave similarly or are researching the same content.

| Source | Dynamic or Static? | Best for |
| ------ | ------ | ------ |
| CRM Report | Dynamic | for account list that may have changes, or if accounts are being added as the campaign progresses |
| CSV file upload | Static | there is a set target list for a campaign that will not change |
| Site Analytics | Dynamic | based on intent using page views, hits to a certain page, etc. |
| Segment of a larger audience | Dynamic | If you want to create a campaign for a subset of an audience |

## Metrics and Reporting
### Demandbase Metrics and Reporting
#### ABM Metrics
- **Lifted Accounts**: Percentage of the target accounts that have more engagement (page views) during the campaign(s) compared to the baseline period of 30-days prior to the start of the campaign(s). Baseline page view counts are normalized for campaign length in calculating this metric.
- **Page Views:** Total page views on your website during the campaign(s)
- **% increase in Page Views:** Percent change in page views during the campaign(s), compared to baseline period of the 30 days preceding the start of the campaign. *Note: Baseline page view counts are normalized for campaign length in calculating this metric.
- **Account Performance by Stage:**
     - **Total Accounts:** The total number of accounts being targeted
     - **Reach:** he total number of accounts that have been served at least one impression
     - **Visited:** The total number of accounts that have been on site during the campaign(s)
     - **Clicked:** The total number of accounts from which clicks have been generated during the campaign(s)
     - **Engaged:** The total number of targeted accounts that have had three or more unique sessions within a 30-day period.
     - **Converted:** TBD
     - **Opportunity:** The total number of accounts with at least one new CRM opportunity created during the campaign(s)
     - **Won:** The total number of accounts with at least one CRM opportunity that has progressed to Closed/Won during the campaign(s)

#### Digital Campaign Metrics & Performance
- **Impressions:** Total ad views served
- **Clicks:** Total ad clicks
- **CTR:** Click-through rate. -> Formula: Clicks divided by Impressions
- **CPM:** Average cost per one thousand impressions
- **CPC:** Cost per click. -> Formula: Cost divided by Clicks
- Top Publishers
- Top Performing Creative
- Top Engaged Accounts

#### Demandbase Reporting: ABM Analytics 
[ABM Analytics](https://support.demandbase.com/hc/en-us/articles/360005054311-ABM-Analytics-Overview) is a native analytics tool within the Demandbase platform. It gives you insight into how your target accounts are performing across your full marketing funnel from engagement to conversion to closed won. 

The [Opportunity Reports Manager](https://support.demandbase.com/hc/en-us/articles/360036023532-Working-with-Opportunity-Reports-Manager) feature allows you to customize which opportunities are used in your reports and analytics within ABM Analytics. To date, you can only filter/segment by opportunity stage/type/status. 

Our Demandbase instance already has a report for each opportunity stage. This lets you select an audience (list of accounts) and ‘filter’ it by opportunity stage. 

##### How to filter using the Opportunity Reports feature
1. Create an audience or leverage one of the audiences already in our DB instance that has all of the accounts you want to see.
2. In DB, navigate to the 'ABM Analytics' tab.
3. Select the audience you want to see the data for from the 'primary audience' dropdown.
4. To narrow the audience by opp stage, check the box 'Filter results by Opportunity Report' and select the opp stage from the dropdown.

### Salesforce Reporting
#### Salesforce Metrics

- **[SAO](/handbook/business-ops/resources/#glossary): Sales Accepted Opportunity:** Sales Accepted Opportunity - an opportunity Sales agrees to pursue following an Initial Qualifying Meeting
- **[Closed Won](/handbook/business-ops/resources/#opportunity-stages):** The terms have been agreed to by both parties and the quote has been approved by Finance.

## Demandbase Display Campaigns
Demandbase enables personalized display advertising for target accounts. Demandbase Display ads are different from [the standard Paid Display ads](/handbook/marketing/revenue-marketing/digital-marketing-programs/digital-marketing-management/#display-ads) we typically run in Google Display Network. We partner directly with Demandbase and do not run these through PMG, our paid advertising digital agency.

### Demandbase Campaign Process
If you would like to target named accounts with paid display ads, create an issue with the appropriate Demandbase Campaign Request template:
- [Campaign Request issue template for Field and Corporate Marketing](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/-/issues/new?issuable_template=Demandbase_Campaign_Request)
- [General Campaign Request issue template (for all other teams)](https://gitlab.com/gitlab-com/marketing/account-based-marketing/-/issues/new?issuable_template=Demandbase_Campaign_Request_Template)

The DMP will then conduct a reach test with Demandbase to determine if your selected accounts are reachable, so please provide estimated budget, campaign duration, geo target, and a list of accounts [formatted for DB (Demandbase)](https://docs.google.com/spreadsheets/d/1sJvmzdhL8k5N6WQPSlE3ndAF0jL8MUTuZcD6dM-1D0w/edit?usp=sharing). If your reach test comes back too low, the DMP will recommend that you add more accounts, expand your geo target, increase your campaign duration, and/or double check to make sure your list is formatted correctly for Demandbase upload. After the reach test confirms reachable accounts and available display inventory, the DMP will send display images and landing page URLs to our DB contacts. Upon receipt, the campaign typically goes live within 1-2 business days.

If your campaign objective is promoting an event or webcast, we recommend launching one month in advance of the event date in order to increase awareness & reach. If your campaign objective is account penetration, we recommend running your campaign as “always-on” to build awareness for your priority accounts and optimize over time with relevant assets. The DMP will provide a UTM report to track inquiries/registrations attributed to your DB campaign. Front-end Demandbase metric reports are also available upon request.

### Demandbase Ads
#### Display Ad Specs
- 728x90
- 300x250
- 160x600
- 300x600
- 970x250

#### Display Ad Copy
- **Top of funnel:** Use a broad value proposition to increase awareness and education, assert your brand value and why prospects should care.
- **Middle of funnel:** Include a tailored value proposition, provide practical how-to content, best practices, and tips and tricks.
- **Bottom of funnel:** Reinforce the value proposition, go into further detail about your offerings with case studies, ROI calculators, and product and solution content.
- **All stages:** Keep it simple and have a clear CTA.

#### Demandbase Campaign Best Practices
##### Campaign Run Time:

- Event promotion: 1 month minimum
- Target account penetration: 2-3 months minimum
- Longer advertising campaigns that span the full funnel can help build awareness and create more engagement. The result is a higher number of accounts that go into the pipeline with a higher average booking value.

##### Budget:
- [Demandbase funnel budgeting](https://docs.google.com/presentation/d/1swa9gWFAttRAas5feGSWPgsbx1HyUwiNtTXYiOL47wE/edit#slide=id.g810b16a717_0_0)
 - Start with a low monthly budget for top of funnel campaigns and increase the budget as you progress to mid and lower funnel campaigns.

##### Audiences:
- You can segment by stage in the buyer’s journey, company size, industry, etc. The core message for each of these groups is different, therefore they shouldn’t receive the same ad creative.
- Segment audiences into High, Medium, and Low intent based on intent data results and serve assets f

### Demandbase Sales Conversion 

**Why conversion?** 
The Sales conversion tool helps SDRs and Sales reps to:
1. Prioritize target accounts 
2. Understand interestes before the prospect raises their hand or registers as a lead
3. Create more personalized experiences for prospects

**Where are insights delivered?**
- Weekly Email Digest 
- Salesforce.com insights (found as a section on the account object for matched accouts)
- Slack alerts (real time)

**Email Digest: Best Practices**
- Sent weekly towards the beginning of the week
- Treats on-site activity or intent like a form fill (without linking to an individual prospect)
- Used to prioritize accounts that are showing an increase in engagement
- Direcly links to LinkedIn Sales Navigator, SFDC, and locations
- Use sales navigator, location data, and salesforce history to identify the most relevant prospects
- Use intent insights to create personalized outreach

**Slack Alerts: Best Practices**
- Shows most recent web activity and real-time account interest
- Helps to better understand effectiveness of email messaging
- Easily access LinkedIn Sales Navigator, Salesforce, and preferences
- Use for real-time account prioritization 
- Use for improved personalization and engaging accounts that are already showing positive buying signals

**Salesforce.com Integration**
- Sum of activity from weekly email digest
- Review web traffic over the last 30 days
- Cross-reference alerts with SFDC account & opportunity history
- Helps to prioritize and personalize
- Review locations where the engagement is happening
- Reach out to best-fit prospects from locations showing higher engagement trends
