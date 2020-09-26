---
layout: handbook-page-toc
title: "Zoominfo"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### Set Up
Once you receive your login and enter the Zoominfo platform you will need to download the [Zoominfo ReachOut Chrome extension](https://chrome.google.com/webstore/detail/zoominfo-reachout/fofjcndophjadilglgimelemjkjblgpf). You can also find the link by navigating down to the bottom right of your homepage.

It is recommended to add Zoominfo to your tabs in SFDC. 

To do so click the :heavy_plus_sign:>Click `Customize My Tabs`> Scroll down to find Zoominfo>Highlight it>Hit the right arrow button :arrow_right:>Hit the `Save` button.

### Ways to access Zoominfo
Your direct login allows for direct export into SFDC. However you can also access it directly from the lead, contact, account record within SFDC, or from the tab view as shown above. Lastly, the chrome extension allows for additional functionality while browsing LinkedIn or company websites.

### Training

**To access Zoominfo University:**
- Login to Zoominfo 
- Under your name on the right hand side click on Zoominfo University
- Once you've created your Zoominfo University login the links below will give you direct access

**I'm brand new to DiscoverOrg or Zoominfo! Start here:**

| Title | Duration | Summary |
| ------ | ------ | ------ | 
| [Introduction to Zoominfo (condensed version)](https://university.zoominfo.com/courses/101-introduction-to-zoominfo-condensed)| 6:42 | A general overview covering core concepts, profile info, building a search, saving and subscribing, and tagging.  |
| [Best Practices with Zoominfo (condensed version)](https://university.zoominfo.com/courses/102-best-practices-with-zoominfo-condensed) | 6:23 | Using scoops and more advanced features. We do not currently have Intent, so you can skip this section. |
| [Introduction in Salesforce ](https://university.zoominfo.com/learn/course/101-introduction-in-salesforce-on-demand/training-session/101-introduction-in-salesforce) | 31:15 | This is a general overview of how to use the native integration within SFDC.|

**I've been using DiscoverOrg or Zoominfo already or ready to learn more! Skip to topics that interest you:**

| Title | Duration | Summary |
| ------ | ------ | ------ | 
| [Tagging](https://university.zoominfo.com/learn/course/tagging-hosted-by-dan-veillette/knowledge-center/staff-picks-series-tagging) | 4:54 | A quick review on how to use tags. |
| [Scoops](https://university.zoominfo.com/courses/scoops-hosted-by-joy-bernard) | 10:04 | A guide for searching and filtering for Scoops alerts. |
| [ListMatch](https://university.zoominfo.com/courses/listmatch-hosted-by-amber-jackson) | 13:00 | ListMatch allows you to upload a list of contacts or company information in bulk to run through the Zoominfo search. |
| [Technology and Company Attributes](https://university.zoominfo.com/courses/technology-and-company-attributes-hosted-by-william-stevens) | 3:56 | Learn how to access technology information within a company profile. |
| [Exploring the Sunny Side of Saved Searches](https://university.zoominfo.com/courses/exploring-the-sunny-side-of-saved-searches) | 57:26 | **Skip to 6:40** to learn about general info on saved searches. **Skip to 14:32** for building a saved search. **Skip to 21:30** to learn how to set up an email alert for your saved search. **Skip to 29:17** to learn about how to save Scoops alerts. **Skip to 35:14** for learning about targeting personas with saved searches. **Skip to 38:10** to learn about the tagging feature. **Skip to 43:00** for saving and sharing searches with others.|
| [How to Make a (Sales) Splash with ReachOut](https://university.zoominfo.com/courses/how-to-make-a-sales-splash-with-reachout) | 53:12 | **Skip to 14:10** to see how to use it with LinkedIn. **Skip to 17:00** to export into SFDC. **Skip to 18:00** to build a list from LinkedIn and export in bulk by using tags. **Skip to 30:20** to see how to use the extension on a company website.

Do you have a topic not covered you'd like to see? Slack #zoominfo room or reach out to marketing operations.

To access Zoominfo training sessions specific for GitLab follow [this link](https://university.zoominfo.com/courses/gitlab-inc-recorded-trainings).

To access additional Zoominfo on-demand training follow [this link](https://university.zoominfo.com/pages/on-demand-training).

### Credits
-   **Users** -  Monthly credits are set at 1,000 and bulk credits are set at 2,000. 
Each user has 1,000 monthly credits to use for prospecting. A credit is consumed any time a user exports a contact or company out of the platform. These credits reset on the first of each month. When a user pushes "export" it should automatically pull from the monthly credits until a user has utilized all 1,000 of their monthly credits. After those monthly credits are consumed you are then able to use the bulk credits. Bulk credits are adjustable. Monthly credits are not. A user also has 2,000 views in which they can use to click on a contact and view/unlock the contact information.
-   **Accounts** - Max number of accounts a user can export to SFDC is set to 100.
-   **Contacts** - Max number of contacts a user can export to SFDC must match accounts and is set to 100. This is because contacts MUST be associated with accounts in SFDC. When exporting a contact, Zoominfo will check to see if an Account exists within SFDC that matches the company the contact works at. If not, users can create a new account which they will associate the contact to. Enforcing that contact creation is equal to or less than accounts is to make sure there is not a scenario where a contact export fails because they are unable to create the same number of accounts.
-   **Leads** - Max number of leads a user can export to SFDC is set at 1,000. This ensures that the user will not max out their monthly allotment in one export.
-   **Bulk requests** If a bulk download is needed for a campaign, please open an [issue](https://gitlab.com/gitlab-com/marketing/marketing-operations/-/issues/new) for the marketing operations project. Admins have unlimited credits to be able to export bulk lists or a temporary lift can be made for individual users.
-   **Reporting bad leads** - If a lead is found to be incorrect the user can submit a `Suggest Contact Update` and the research team will usually update it within 1-2 business days. When the lead is updated the user can manually append it or re-push the prospect into SFDC without expending a credit (for two months while it's "under management").

### Field Mappings
All current field mappings are documented [here](https://docs.google.com/spreadsheets/d/1lZ2BgNER_OYR5jjYDHreCMRbpODQbprUpGKVRD5TMnY/edit#gid=504148174). 
Custom fields start with [ZI] and will be visible in the Zoominfo section in SFDC. Example name: `[ZI] Company Phone`. All [ZI] fields are set to be able to overwrite the field should new data be available on a lead, contact, or account. The only information mapped to standard fields are fields needed for basic lead, contact, or account creations. Example: `First Name`, `Last Name`, and `Email Address`.

### SFDC Native Integration
- The Salesforce Native App is available on any lead, contact, or account directly within SFDC. 
- The Salesforce Native App only allows users to export 25 at a time. Where as logging in directly and using the standard Salesforce web connector allows you to push up to 2,000 at a time - for any bulk pushes it is recommended you use the normal ZoomInfo website.


## SFDC Account Enrichment
All of Salesforce current accounts in the database have been enriched with Zoominfo. Accounts are scheduled to be refreshed with Zoominfo weekly on Saturdays. Instant Enrich will enrich any new accounts that are created.

### Outreach Integration
Coming soon.
