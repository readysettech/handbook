---
layout: markdown_page
title: "Direct Mail"
---

## Overview
This page focuses on direct mail as a tactic used within marketing campaigns, including account centric campaigns.

### Process in GitLab to organize a direct mail

The project owner is responsible for following the steps below to create the epic and related issues in GitLab.

1. Project owner (FMM) creates the main tactic issue
1. Project owner (FMC) creates the epic to house all related issues (code below)
1. Project owner (FMC) creates the relevant issues required (shortcut links in epic code below)
1. Project owner (FMC) associates all the relevant issues to the newly created epic, as well as the original issue
1. Project owner (FMC) sets due dates for each issue, based on agreed upon SLAs between teams for each task, and confirms accurate ownership for each issue

*Note: if the date of a direct mail changes, project owner (FM) is responsible for changing the due dates of all related issues to match the new date, and alerting the team members involved.*

### Code for direct mail epic

```
<--- Name this epic using the following format, then delete this line: Direct Mail - [Vendor] - [3-letter Month] [Date], [Year] --->

## [Main Issue >>]()

## [Copy for landing page and emails >>]() - [template](https://docs.google.com/document/d/1j43mf7Lsq2AXoNwiygGAr_laiFzmokNCfMHi7KNLjuA/edit)

## :notepad_spiral: Key Details 
* **Project Owner (FMM):** 
* **Field Marketing Coordinator:** 
* **Type:** Direct Mail
* **Campaign Tag:**  
* **Sales Segment:** `Large, Mid-Market, or SMB`
* **Sales Region:** `AMER, EMEA, APAC`
* **Sales Territory (if specific):** 
* **Goal:** `Please be specific on the KPI this is meant to impact. For example, drive MQLs against named account list, increase velocity of MQLs > SAOs, increase velocity of early stage opps to close.`
* **Budget:** 
* **Launch Date:**  [MM-DD-YYYY] (this is the date of the first email, everything is in place to execute on this date)
* [ ] [main salesforce program]()
* [ ] [main marketo campaign]()
* [ ] Campaign UTM - FM to fill in (Format: campaign tag - change to all lowercase, no spaces, hyphens, underscores, or special characters)

## User Experience
[FMM to provide a description of the user journey - from communication plan, to what the user experiences upon reciept, plus triggers on our end like confirmation email and how GitLab fulfils with the vendor, up until receipt by the user and answering whether or not we get confirmation that they received it... what is the anticipated journey after that?]

## Additional description and notes about the tactic
[FMM add whatever additional notes are relevant here]

## Issue creation

* [ ] [Facilitate tracking issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-01-facilitate-tracking) - FMC creates, assigns to FMC or MPM (depending on [program type](https://about.gitlab.com/handbook/marketing/marketing-operations/#marketo-program-and-salesforce-campaign-set-up))
* [ ] [List clean and upload issue created](https://gitlab.com/gitlab-com/marketing/marketing-operations/issues/new?issuable_template=event-clean-upload-list) - FMC creates, assigns to FMM and MOps
* [ ] [Follow up email issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-04-follow-up-email) (*optional*) - FMC creates, assigns to FMM, FMC and MPM
* [ ] [Add to nurture issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-05-add-to-nurture) - FMC creates, assigns to FMM and MPM
* [ ] [Email invitations issue created](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-03-invitations-reminder) (*Optional if target list determined, and form-fill request as part of user experience*) - FMC creates, assigns to FMM, FMC and MPM

**Optional: create the optional issues only if a landing page is required*

/label ~"Field Marketing" ~"Direct Mail" ~"mktg-status::wip"
```
