---
layout: markdown_page
title: "Paid Surveys"
---

## Overview
This page focuses on paid surveys through external vendors as a tactic used within marketing campaigns, including account centric campaigns.

### Process in GitLab to organize epic & issues

The project owner is responsible for following the steps below to create the epic and related issues in GitLab.

1. Project owner (FMM) creates the main tactic issue
1. Project owner (FMC) creates the epic to house all related issues (code below)
1. Project owner (FMC) creates the relevant issues required (shortcut links in epic code below)
1. Project owner (FMC) associates all the relevant issues to the newly created epic, as well as the original issue
1. Project owner (FMC) sets due dates for each issue, based on agreed upon SLAs between teams for each task, and confirms accurate ownership for each issue

*Note: if the date of a survey changes, Project owner (FM) is responsible for changing the due dates of all related issues to match the new date, and alerting the team members involved.*

### Code for epic

```
<--- Name this epic using the following format, then delete this line: Paid Survey - [Vendor] - [3-letter Month] [Date], [Year] --->

## [Main Issue >>]()

## [Copy for landing page and emails >>]() - [template](https://docs.google.com/document/d/1j43mf7Lsq2AXoNwiygGAr_laiFzmokNCfMHi7KNLjuA/edit)

## :notepad_spiral: Key Details 
* **Prjoect Owner (FMM):** 
* **Field Marketing Coordinator:** 
* **Type:** Paid Survey
* **Sales Segment:** `Large, Mid-Market, or SMB`
* **Sales Region:** `AMER, EMEA, APAC`
* **Sales Territory (if specific):** 
* **Goal:** `Please be specific on the KPI this is meant to impact. For example, drive MQLs against named account list, increase velocity of MQLs > SAOs, increase velocity of early stage opps to close.`
* **Campaign Tag:**  
* **Budget:** 
* **Launch Date:**  [MM-DD-YYYY] (this is the date the survey begins through the vendor)
* [ ] [main salesforce program]()
* [ ] [main marketo campaign]()
* [ ] Campaign UTM - FM to fill in (Format: campaign tag - change to all lowercase, no spaces, hyphens, underscores, or special characters)

## User Experience
[What is the anticipated user experience? FMM to provide a description of the journey as if they were the end user - from communications received (both from GitLab and/or from vendor), to what the user provides in survey, what happens after they submit, what do they receive from us after we upload the leads, and beyond... what is the end-to-end journey for the user?]

## Additional description and notes about the tactic
[FMM add whatever additional notes are relevant here]

## Issue creation

* [ ] [Facilitate tracking issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-01-facilitate-tracking) - FMC creates, assigns to FMC or MPM (depending on [program type](https://about.gitlab.com/handbook/marketing/marketing-operations/#marketo-program-and-salesforce-campaign-set-up))
* [ ] [Follow up email issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-04-follow-up-email) (*optional*) - FMC creates, assigns to FMM, FMC and MPM
* [ ] [Add to nurture issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-05-add-to-nurture) - FMC creates, assigns to FMM and MPM

**Optional: create the optional issues only we have rights to survey results and content is worth gating*

/label ~"Field Marketing" ~"mktg-status::wip" ~"Paid Survey"
```


### SimplyDirect <> Marketo Integration
SimplyDirect and Marketo are integrated, so that SimplyDirect can send leads to Marketo immediately without a list upload. You must follow [these directions](https://about.gitlab.com/handbook/marketing/marketing-operations/#marketo-program-and-salesforce-campaign-set-up) exactly, each time you set up a new survey program, or else the integration will not work. 
