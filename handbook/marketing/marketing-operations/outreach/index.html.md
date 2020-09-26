---
layout: handbook-page-toc
title: "Outreach"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### Set-Up  
User set-up instructions can be found [here](https://docs.google.com/document/d/1VJpZaoDoGtwN4Dp21g_OuhVauN2prHNyUtmIWKuROUY/edit#heading=h.v6blhaepsusl).

### Sequences  
Sequences are one of the main features of Outreach. Users can create a series of touchpoints in order to communicate and automate their workflows.
We currently have two types of sequences. Master and personal. Master sequences are created to be shared and used across teams. Personal are for your own use.

Naming convention for master sequences include the following:

- MASTER
- LOW or HIGH touch
- Name of campaign
- Region or language (NORAM, APAC, EMEA or Spanish, French, Russian, ect)

Example: | **MASTER - HIGH - Just Commit - NORAM**

When creating a new master sequence or shared event sequence, please tag marketing ops on the issue for QA review prior to enabling it. The sequence is reviewed to ensure it has the correct rulesets, tags, collections, throttles, variables and other settings. Personal sequences do not need to be reviewed unless you wish to have an additional pair of eyes on it.

### Sequence Settings
You may choose the best delivery schedule and ruleset applicable to your goals. 
You may choose whether or not others can see and use your sequence or if you would like to keep it private. 
All sequence must have Throttle's enabled. This helps to stagger the volume of prospects moving through a sequence at one time. 
It is necessary to help prevent users from hitting the email provider's mailing limits. 
If you have too much volume this may result in you being kicked out of your email inbox by our provider. 
**Max adds per user every 24 hours are to be set up to 75.** 
If you need to request special sequence settings please reach out to Marketing Operations with your use case.

### Collections
Collections are an easy way to group sequences, snippets, and templates that get assigned to user groups for easier access. 
Examples associated to our SDR groups include our `SDR Inbound 2020` and `2020 Events` collections. 
You may request new collections by opening an issue in the Marketing Operations Project.

### Rulesets
- **Default** - Does not make tasks on your behalf. Prospects can be added to these sequences more than once, if not already active. prospects are not able to be added to other exclusive sequences, but can be added to a non-exclusive sequence. Updates prospoects to appropriate stages. Resumes out of office prospects after 5 days.
- **Campaign** - Follows the same rules as the default settings except out of office are resumed 1 day after.
- **Create Call Task** - Follows same rules as the default except it will create call tasks on opened emails. Minimum email opens needed: 2
- **Event** - Prospects can only be added to this sequence once. They are not exclusive to this sequence. Out of office are resumed 1 day after.

### Outreach Meetings
The current meeting templates will sync to an SFDC event. 

|Meeting Type|Use Case|Notes|
|----|----|----|
|IQM (30)|For qualified prospects being sent from the SDR team to Sales to determine next steps with GitLab.| If no template is selected in the drop down this is the default meeting type used.|
|Discovery Call (30)|To be used as an intro call for potential clients and qualify their needs.|
|Evaluation Orchestration Call (25)|A deeper dive into a potential clients needs.| 25 minute evaluation.|
|Evaluation Orchestration Call (45)|A deeper dive into a potential clients needs.|This is a longer duration at 45 minutes rather than 25.|
|Pricing Call (25)|This is for potential clients who want to know about GitLab pricing. May also be used for renewal discussion with current clients.|

Outreach is able to sync some custom information about these meetings into events including:

|Event Field|Notes|
|----|----|
|`Subject`|If using a template the subject line is provided as the `Title` of the meeting.
|`Description`|If using a template the `Description` is already filled in for you. If not it will be whatever you are writing to who you are inviting to the meeting.
|`Location`|The zoom link associated to the meeting.
|`Start Date`|Date and time the meeting is booked for.
|`End Date`|Date and time the meeting ends.
|`Name of Prospect`|This is the person who is attending the meeting.
|`Owner of the Meeting`|Who the meeting is assigned to.
|`Related Opportunities`|When booking meetings you can associate the event to an open opportunity.
|`Outreach Meeting Type`|This displays the name of the meeting template used for the meeting.
|`Booked By`|If you book a meeting on someone else's behalf this displays the name of the person who booked it.
|`Attributed Sequence Name`|The last known sequence name will be brought over into this field.|
|`Meeting Source`|The Source field will display one of two values (App or Sync) so that you can distinguish whether a meeting was booked through Outreach or if it was booked prior to connecting with Outreach and retroactively synced back to SFDC.|
|`Meeting Cancelled`|Outreach can not delete events in SFDC. If a meeting is deleted within Outreach it will check the `Meeting Cancelled` checkbox.|

| Outreach.io Call Disposition | Notes|
|---|---|
`Correct Contact: Answered`| The correct contact actully picked up the phone and you had a conversation with the contact|
|`Correct Contact: Left Message`| You were able to reach the voicemail for the correct contact and you left a message on their machine or with their Personal Assistant |
|`Correct Contact: Not Answered/Other`| You were able to reach the correct contact through a company directory but it kept ringing. You reached the contacts voicemail but their voicemail was not set up so you could not leave a message |
|`Busy`|Get a busy tone when calling|
|`Bad Number`|The phone number is not valid|
|`Incorrect Contact: Answered`| The wrong person answered the phone number that you had for this contact and it is the wrong persons phone number (They were not a personal assistant). They didn’t take a message for the correct person or give helpful information|
|`Incorrect Contact: Left Message`|The wrong person answered the phone and it is the wrong persons phone number (They were not a personal assistant). They took a message for the correct person/gave you the correct number for the contact|
|`Incorrect Contact: Not Answered/Other`| You got through to the voicemail but the voicemail was for someone other than the person who you were trying to contact. Or the person was not listed in the company directory and you were calling the companies main number|

### Sending Email Using Outreach   

Outreach is **not** meant for mass communications nor bulk email sends it is intended for very targeted account and prospect communications. The Outreach platform is directly integrated to the GitLab Gmail account and each users email is linked through OAuth therefore all activity in Outreach has the potential to impact the IP reputation of the GitLab domain with all major email services providers.   

As such there are [sending limits built into the Outreach platform](https://support.outreach.io/hc/en-us/articles/205022518-Individual-Email-Limits-Safeguards) as well as [limits put in place by Gmail itself](https://support.google.com/a/answer/166852?hl=en).   

#### Sending Limits   
* Individual users can send up to 2,000 emails *combined* between Outreach and Gmail inbox in a rolling 24-hour period.    
    * This is the maximum across both systems, if you max out in Outreach, you **will be** maxed out in Gmail.   
* Outreach has a **hard limit** of 5,000 emails in a rolling seven day period.  
    * If you max out in Outreach, your emails will be queued to try again in 24 hours, when your account drops below this hard limit.

### Importing SFDC Reports

Step 1:
Create your SFDC report and save it into the `Unfiled Public Reports` folder.
- Report can only be a lead or contact report
- Limit to 2000 records per import
- Minimum Required fields:
    - Lead ID
    - Email
    - First Name
    - Last Name
 - Note: you may only map fields that already exist within Outreach, but the import is set up to load additional data points during the upload. You do not need to create your report with a bunch of fields to get them into Outreach.
  
Step 2:
Navigate to the &#9889;Quick Actions button and choose `Bulk Create`.
- Select your `Import Type` as `Prospects Salesforce Report`
- You will need to enter the report ID or choose the name of your report from the dropdown
- Choose the frequency as `Once`

Step 3:
Next you will review the mapping of the above 4 fields in the Outreach plugin. These usually auto-populate if Outreach can determine the correct field.
   - If a field is not mapped please select it from the drop down
     - If you need additional guidance while mapping please contact Marketing Operations
   - Please do not try to map fields that do not exist already in Outreach it is ok to the leave these fields as `Not mapped`
   - Outreach will prompt you that there are unmapped fields and you can hit continue

Step 4:
On the next screen you will be prompted with more fields. To prevent from overriding important data please select the following:
- Owner - `Use owner from data`
- Stage - `Use stage from data`
- Timezone - Leave blank
- Source - Leave blank
- Additional Tags: You may assign tags as you need them
- Load additional data from Salesforce - Prechecked check box
- What to do with duplicates? - `Skip`

Step 5:
Select the `Start Import` button on the next screen.

### Outreach Stages
Outreach stages are a 1:1 match with SFDC Status. The rulesets help push prospects along into the correct stage/status based on their actions. This eliminates the need for triggers to match status to stage.

### Outreach Automation
Outreach will make updates based on these scenarios. Triggers fire in order of operation.

| Trigger Name | Prospect Conditions | Account Conditions | Trigger Actions |
|---|---|---|---|---|
|00 - Inactive Contact and Lead|Inactive Contact or Lead Checkbox is True||Stop All Sequences
|01 - Community Queue|Owner is Community Queue||Stop All Sequences
|02 - Set Nurture Status Reason|Stage is `Nurture`| |Set `Nurture ` Status Reason to `No response`
|03 - Set Unqualified Status Reason|Stage is `Unqualified`||Set `Unqualified` Status Reason to `Unsubscribe`
|04 - Set Bad Data Status Reason|Stage is `Bad Data`||Set `Bad Data` Reason to `Bounced email`

### Outreach Merge and Delete

Outreach will automatically merge and delete lead, contact, and account information based on those actions taking place in SFDC. Outreach checks for these data changes in SFDC once a day.

If a lead or contact is currently in an active sequence Outreach will let that lead or contact finish the sequence. This allows the SDR to complete their outreach if working on a duplicate prospect. Once a prospect has been marked as finished. The next time Outreach looks for changes in SFDC it will merge or delete the prospect accordingly.

Prospects that get deleted in Outreach live in the recycle bin until permanently deleted. Both Sales Enablement and Marketing Operations have the ability to remove leads from this recycle bin and bring them back into Outreach if there is ever a scenario that requires this action.

### Keeping Outreach Tidy

Marketing Ops will be responsible for pausing and locking sequences owned by former team members and for deleting tasks owned by former team members. The MktgOps team will also be responsible for monitoring and cleaning the SAL's and AE's unused sequences and overdue tasks, as necessary. Procedure for the former team members clean up process is as follows:
- During the deprovisioning process, any former team member with an Outreach profile will be added to the `Former Team Member` Outreach team. This instruction has been added to the deprovisioning template.
- Use the `Sort & Filter` function of Outreach to track tasks and sequences owned by members of the `Former Team Members` team. Tasks can be outright deleted, sequences deactivated and locked. Instructions for locking sequences below.
- If there are sequences owned by members of the `Former Team Members` team that are being used by current GitLab team members, change ownership of the sequence to a current team member. MktgOps users are preferred, but change to a team member using the sequence where appropriate.

SDRs are asked by SDR Leadership to periodically remove their older, unsued and inactive sequences from view and use. To qualify for clean up, a sequence needs to meet these criteria:
- There are no active prospects in the sequence
- If there are active prospects in the sequence, check the date when the prospects were added. If prospects have been stuck on a step or paused for a prolonged period of time, consider those prospects inactive
- The sequence has not been used in 13 months or longer

Outreach sequences are a useful source of a/b testing data for customer responses, so the best course of action is not to outright delete sequences. Instead, follow these steps:
- Deactivate/pause the sequence. If there are prospects still in the sequence, there will be a warning regarding the outcome of those prospects' path through the sequence. Assuming the prospects have been deemed inactive, proceed in deactivating the sequence
- From the `Sort & Filter` view, select the checkbox on all applicable sequences
- Proceed to the top of the page and click the padlock icon, which shows the Lock and Restore feature. Select [Lock to lock the unneeded sequences](https://support.outreach.io/hc/en-us/articles/115005151633-Locking-vs-Deleting-Sequences)

Congrats! You've just helped keep Outreach as a tidy tool for yourself and your teammates. Reward yourself with a tasty treat, if desired. 
