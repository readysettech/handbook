---
layout: handbook-page-toc
title: "Account Based Strategy"
---
## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Account Based Strategy

## Ideal Customer Profile
The account based marketing team is responsible for developing and managing our ideal customer profile.  An ideal customer profile is the description of our "perfect" customer company (not individual or end user).  The profile takes into consideration firmographic, environmental and additional factors to develop our target list of highest value accounts. 

A few things to note about our ICP: 
- it is that it is fairly broad, mainly because GitLab can ultimately sell to a vast number of companies versus say, a banking solution that would have a much smaller TAM (total addressable market)  
- our ICP is hyper focused on first order logos
- Because of our large TAM we do not target ALL the accounts that fit our ICP at a given time, but rather, focus on a subset based on different variables including propensity to buy and additional intent data.

### Large

|  | **Attribute** | **Description** |
| ------ | ------ | ------ |
| **Core criteria (must haves)** | Number of developers (currently also using company size as proxy) | 500+ |
| | Tech stack (regional) | Includes GitHub, Perforce, Jenkins, BitBucket or Subversion |
| | Cloud provider | AWS or GCP |
| | Prospect | First order logo (not a current PAID customer for GitLab anywhere within the organization)  |
| **Additional criteria (attributes to further define)** | Digital transformation | identified C-suite initiative | 
| | High intent account | Account is trending as high intent based on our data in Demandbase |

### Mid Market

|  | **Attribute** | **Description** |
| ------ | ------ | ------ |
| **Core criteria (must haves)** | Number of employees | <150 & >650 |
| | Tech stack (regional) | Includes GitHub, Perforce, Jenkins, BitBucket or Subversion.  Also include a LACK of tech stack in smaller companies |
| | Prospect | First order logo (not a current PAID customer for GitLab anywhere within the organization)  |
| **Additional criteria (attributes to further define)** | New hire | CIO | 
| | High intent account | Account is trending as high intent based on our data in Demandbase |

## GL4300 & MM4000
Target list of accounts that are first order logos (first paid customer within an organziation) for GitLab and fit our ideal customer profile for both Large (GL4300) and MidMarket (MM4000).  The lists are developed using the current data sources we have at our disposal and are refreshed quarterly.

* GL4300 stands for GitLab & the number of target accounts we are targeting. This list represents only those accounts in our [`Large` segment](https://about.gitlab.com/handbook/sales/field-operations/gtm-resources/#segmentation). 
* MM4000 stands for MidMarket & the number of target accounts we are targeting. This list represents only those accounts in our [`MidMarket` segment](https://about.gitlab.com/handbook/sales/field-operations/gtm-resources/#segmentation). 

### How we developed the list
We take from a variety of data sets currently but the ideal state is to have all data flowing to Salesforce as our single source for qualifying and scoring accounts.
1. Accounts identified by sales as strategic by region and match our ICP
1. Accounts in our database that match our ICP 
1. lookalike accounts: account that act, look & behave like our existing best customers
1. agreed upon sales & marketing identified strategic accounts

### When an account moves to/from our GL4300 & MM4000 target lists
Both target lists will be reviewed and modified during the last 2 weeks of each quarter.  The process is as follows:
##### T-minus two weeks from end of quarter
1. ABM nominations are made by sales

##### Last day of quarter
1. Closed won logos will be filtered out and the lists will be refilled based on next up ideal customer profile accounts. 
1. Accounts not showing an increase or are showing a decrease in engagement will be removed from the target list
1. Any additional accounts identified by sales as not a good target due to lack of budget, etc

##### First business day of new quarter
1. Salesforce is updated with all changes to the target acccount list and shared with the organization

## Accounts are identified in Salesforce by the GTM strategy field in Salesforce:

**Volume**
Default selection for all accounts.

**ICP TOTAL ADDRESSABLE MARKET**
All accounts that fit our ideal customer profile.

**ACCOUNT CENTRIC**
Indicates that an account is a focus for field marketing and account centric campaigns (GL4300 and MM4000).

**ACCOUNT BASED**
This defines that an account is included in one of the three tiers of our account based strategy.  The account list will be a subset of the GL4300 & MM4000 plus no more than 15% expansion opportunities.  If an account is identified with this strategy, the additional field of `ABM Tier ` that will be completed as well which will identify which tier the account falls into in respect to our account based strategy.

**ABM Tier**
This field is a sub field of GTM Strategy and will be populated if `Account Based` is chosen in the `GTM Strategy` field.  This field will identify which tier an account is currently in.

## Account Sources
All accounts in Salesforce that are part of the `ICP Total Addressable Market` will also have the `Net New Logo Target Account` field completed.
**Existing** An account that already existed in our circumstances

**Core** Newly identified core user

**Lookalike** Account identified based on attributes that match our exisitng customer base

## Where can I look to see the GL4300 and MM4000?
Both the GL4300 and MM4000 are identified in Salesforce by the `GTM Strategy` field = `Account Centric`.  From the you can filter by segment to see the respective lists, or by account owner etc to filter further.