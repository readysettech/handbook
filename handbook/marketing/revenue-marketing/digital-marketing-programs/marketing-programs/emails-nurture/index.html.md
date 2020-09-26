---
layout: markdown_page
title: "Emails & Nurture Programs"
---

# Overview
This page focuses on emails and nurture programs, owned and managed by Marketing Programs.

### Holiday coverage for severity::1 security vulnerabilities email communication

In the event of an severity::1 (critical) security vulnerability email communication is needed during the holidays, please create an issue using *[Email-Request-mpm template](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/blob/master/.gitlab/issue_templates/Email-Request-mpm.md)* and ping in [#marketing_programs](https://gitlab.slack.com/archives/CCWUCP4MS) tagging @marketing-programs

## Email marketing calendar

The calendar below documents the emails to be sent via Marketo and Mailchimp for:
1. event support (invitations, reminders, and follow ups)
1. ad hoc emails (security, etc.)
1. webcast emails (invitations, reminders, and follow ups)
1. milestones for nurture campaigns (i.e. when started, changed, etc. linking to more details)

*Note: emails in the future may be pushed out if timelines are not met for email testing, receiving lists from event organizers late, etc. The calendar will be updated if the email is pushed out. Please reference the MPM issue boards (described below on this page) to see progress of specific events/webcasts/etc.*

<figure>
  <iframe src="https://calendar.google.com/calendar/b/1/embed?showPrint=0&amp;height=600&amp;wkst=1&amp;bgcolor=%23FFFFFF&amp;src=gitlab.com_bpjvmm7ertrrhmms3r7ojjrku0%40group.calendar.google.com&amp;color=%23B1365F&amp;ctz=America%2FLos_Angeles" style="border-width:0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
</figure>

## Email Marketing Best Practices

**Content**
*  Email copy should be shorter and more conversion-oriented 
*  Avoid walls of text when possible
*  Use extremely clear wording and remove words that don't provide value
*  Minimize CTAs (calls-to-action)
*  Take advantage of content hierarchy
*  Use humor when it makes sense 
*  Craft compelling subject lines and employ the preview text as a complement to the subject line
*  Focus on value-first content and CTAs. Ask yourself: "what's in it for the subscriber?"

**Design**
*  Consider resposive design
*  Code all text in HTML
*  Minimize CTAs
*  Images should add to the goal of your email and not take away from it
*  An email is not a landing page
*  Consider accessibility

**A/B Testing**
*  Each test group should include at least 1000 people
*  You need a bigger test group if you're testing for click-through rate versus testing for open rate
*  Have a goal and idea regarding what you want to improve and how your test is going to help with that
*  Test _one_ variable at a time
*  Due to our small sample sizes, we recommend a full 50/50 split versus a 10/10/80 or 20/20/60 split
*  Remember your subject line or "from name" (testing open rates) could have an impact on click-through rate and conversion rate
*  Let the MPM know at the beginning of the project if you're interested in running an A/B test and what your goals/hypothesis is
*  Keep track of the split test learnings so we can learn and innovate!

## Ad-hoc (one-time) emails - requesting an email

To request an email, create an issue in the [Digital Marketing Programs project](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=Email-Request-mpm), using the `Email-Request-mpm.md` issue template. Be as complete as possible providing all requested detail related to the email, goal, target audience and any other pertinent details. Please review the `Email Review Protocol` section below for more detail. 

**SLA:** Email requests should be submitted **no less than** `72 hours` before intended send date so that the new request can be directed to the appropriate Marketing Program Manager (MPM) and for select cases (see email review protocol below) into the Content Marketing team's workflow. The responsible MPM will be determined by type of email requested ([see division of duties](https://about.gitlab.com/handbook/marketing/revenue-marketing/digital-marketing-programs/marketing-programs/#responsibilities)).

**Urgent security emails are exempt from this SLA.*

All links in email sends, going to about.gitlab.com will need to be appended with utm parameters, following the nomenclature outlined in this [document](https://docs.google.com/spreadsheets/d/12jm8q13e3-JNDbJ5-DBJbSAGprLamrilWIBka875gDI/edit#gid=0). This is the way we track and give attribution to emails.

#### Need-to-know details for the email request

Below are the information from the issue template that will need to be filled out before the MPM will create the email in the appropriate system:

- **Sender Name**: Typically we use GitLab Team for most outgoing communications; for Security Alerts we use GitLab Security. Choosing a name that is consistent with the type and/or content of email being sent is important, if unsure make a note and we will make recommendation.
- **Sender Email Address**: What email address should be used?
- **Approvers**: All approvers must be listed on the email request. At least one individual who will receive the replies to the email must be listed an as approver. For example, if the email is coming from security@, someone who will receive replies to the email should be listed as one of the approvers. See approval table below.
- **Subject Line**: 50 character max is preferred (30-40 characters for mobile devices)
- **Email Body Copy**: Can be a text snippet within issue, clearly identified comment on issue or attach a Google Doc with copy. The copy must be approved before requesting the email.
- **Target Date to Send Email**: at a minimum a few days notice is preferred because we need to balancing the number of emails being sent to our database so they are not perceived (or marked) as spam; however, a simple email can be turned in a few hours if absolutely necessary
- **Recipient List**: Emails can be sent to one of the [existing segments](https://about.gitlab.com/handbook/marketing/marketing-operations/marketo#geographic-dma-list ) or a recipient list can be provided as a .csv file
    -  Audience should be appropriately segmented and tokens selected for personalization (if applicable) 
    -  All subscribers are selected list are opted-in to receive your message
    -  If supplying a .csv file, the file must include the following fields:  Email address, First Name (or Full Name)
    -  If personalizing the email to reference a specific project or page, that field must be included in the .csv file and clearly marked using the same terminology used in the email copy. The email copy must clearly identify {{Project}} or {{Page}} where the applicable personalization should be inserted.

#### Types of email requests

- **Marketing Emails**: Marketing emails are designed to generate leads. The request process outlined is used for ad-hoc marketing emails (not events, webcasts, integrated campaigns, etc as these all have a separate established process). These emails are sent through Marketo using the marketing database or [existing segments](https://about.gitlab.com/handbook/marketing/marketing-operations/marketo/#geographic-dma-list).
- **Terms of Service or Privacy Policy Updates**: Terms of Service or Privacy Policy emails are sent to the user base and are not marketing-related. These emails are sent through MailChimp and may require additional approvals, based on the content or number of recipients.
- **Support emails**: Support emails are typically sent to a subset of impacted users and are not marketing-related. These emails are sent through MailChimp.
- **Security emails**: Security emails are sent either to the entire user base or a subset of users and are not marketing-related. They are often urgent, but in the case of the monthly security release, they are scheduled. The monthly security release email is sent through Marketo. Urgent notifications are typically sent through MailChimp.

#### Approvals and notifications for email requests

Marketing related ad-hoc emails are sent at the discretion of the MPM team.

Terms of Service or Privacy Policy updates that impact all users must be announced on the company meeting, in the `#whats-happening-at-gitlab` and `#community-advocates` Slack channels, and approved according to the table below prior to submitting the Email Request.

Support and Security emails sent to a small subset of users should be announced in `#community-advocates` and `#support_managers` Slack channels, and mentioned in `#whats-happening-at-gitlab` if relevant.

The approval table below applies to non-Marketing emails.

|  **Users to be contacted** | **Approval by** |
| --- | --- |
|  <1,000 | reply-to owner |
|  1,001-4,999 | PR, reply-to owner, community advocate |
|  5,000-499,999 | PR, reply-to owner, community advocate, director+ in originating department |
|  500,000+ | PR, reply-to owner, community advocate, director+ in originating department, e-group member |

#### Email review protocol

All MPMs and reviewers should adhere to the following protocol for every marketing email that is sent to ensure brand consistency and quality in our email program. 

We use both Marketo and Mailchimp to send ad-hoc emails. Marketo is the primary system for all marketing emails and the regularly scheduled security updates. Mailchimp should be used for emails to gitlab.com users as these users are not in our marketing systems (unless they have signed up for content). *Examples of emails to be sent through Mailchimp: Critical security updates, support updates that impact a specific subset of users, suspicious account activity notifications.*

 - Once an email request is received using the process above, the MPM determines which system to send the email from. This is usually Mailchimp unless it is a marketing email to our database.
 - Log into Mailchimp and select "Audience."
 - Select "View Audiences" from the "Manage Audience" drop down on the right side of the screen.
 - Select "Create Audience" and name the audience using ISODate_CampaignName. Complete the Default From email address and name (usually info@, but can be security@ or support@ depending on the email). For "Remind people how they signed up to your audience" select "Entire Database" then click Save.
 - For instructions on adding contacts, review this [documentation](https://mailchimp.com/help/import-contacts-mailchimp/). You can also copy and paste the contacts if the list is small enough. You will be asked to map the fields on your import to the database fields prior to upload.
 - Select "Campaigns." Find a prior campaign that used the same type of email you want to use (plain text or regular). Security emails, privacy policy updates, and terms of service updates use plain text, support emails can use regular.
 - Select replicate, then select the audience you created above. If you do not have the list yet, you can select an existing audience and change it later during the review process.
 - Name the campaign using ISODate_CampaignName. Lay out the email as normal. For information about using Merge Tags, review this [documentation](https://mailchimp.com/help/getting-started-with-merge-tags/).
 - Send a test email to yourself first to confirm email is correct and the links work properly. Then, make any changes and send a test to the designated approvers.
 - Once fully approved, review the audience (and update if necessary), sender, subject line, email and schedule to send.

## Email Nurture Programs

### Visualization of current nurture streams

<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://www.lucidchart.com/documents/embeddedchart/7889a7fb-e1f0-4c67-92ae-7becd009625f" id="XA5ojeoO~Tej"></iframe></div>

### Requesting to add leads to a nurture program

**Note: in our future state nurture system, leads would be nurtured appropriately through logic based on:**
* Stage in the buyer lifecycle
* Indicated topic(s) of interest (either through inbound source, self-selected, or segmentation)

These future state nurture programs will be aligned to Use Cases, with three streams to clearly designate the stage of the [buyer journey](https://about.gitlab.com/handbook/marketing/corporate-marketing/content/#content-stage--buyers-journey-definitions) (Awareness, Consideration, and Purchase/Decision) and therefore deliver content relevant to their stage of the buyer journey.

#### Interim additions to nurture programs (while future state and system requirements being built out)

While the future state nurture system is in progress, to request to add a segment of leads to a nurture, please [create an issue for MPM](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=MPM-05-add-to-nurture). The marketing program manager will assess the request and can add the leads to the proper stream via a 'Request Campaign' marketo flow step.

- In order to prevent people currently in a stream from switching streams due to a manual add to nurture, the MPM will exclude anyone in the '*Member of Engagement Stream*' Smart List. 'Member of Smart List' -> Person NOT IN '*Member of Engagement Stream*'. The '*Member of Engagement Stream*' Smart List includes anyone who has not exhausted content in their current stream or is not paused in a stream.
- Flow step to add leads to TOFU nurture 'Cloud Native' track -> 'request Smart Campaign: TOFU nurture. Add to stream 1: Cloud Native (trigger)'
- Flow step to add leads to TOFU nurture 'CI/CD' track -> 'request Smart Campaign: TOFU nurture. Add to stream 4: CI/CD (trigger)'
- Flow step to add leads to TOFU nurture 'Reduce Cycle Time (Generic DevOps)' track -> 'request Smart Campaign: TOFU nurture. Add to stream 2: Reduce Cycle Time_Forrester (trigger)'

### Current Nurture Programs

#### SaaS trial nurture

SaaS Gold trial nurture communication are sent via Marketo and Outreach throughout the 30-day free trial period.

**Goal of the Marketo nurture:** Educate trialers on key features within GitLab Gold SaaS tier.

**Goal of SDR Outreach nurture:** Qualify and meetings setting for SaaS Gold trialers.

**[>> Email copies for SaaS Gold package trial nurture](https://gitlab.com/groups/gitlab-com/marketing/-/epics/98)**

#### Self-hosted trial nurture

Self Hosted Ultimate trial nurture communication are sent via Marketo and Outreach throughout the 30-day free trial period.

**[>> Email copies for Self-hosted Ultimate package nurture](https://docs.google.com/presentation/d/1KSAZFwz3nvSTIXOP8urGWW6dJWhtpawVKFcaoFLDPdg/edit#slide=id.g2ae1ad1112_0_22)**

#### Integrated campaign nurtures

- [CI Use Case Nurture](https://gitlab.com/groups/gitlab-com/marketing/-/epics/741) - contains streams for awareness, consideration, and decision/purchase stages.
- [French CI Use Case Nurture](https://gitlab.com/groups/gitlab-com/marketing/-/epics/752) - contains streams for awareness, consideration, and decision/purchase stages. All email content and linked assets in this program is in French.
- [DevSecOps Use Case Nurture](https://gitlab.com/groups/gitlab-com/marketing/-/epics/901) - contains streams for awareness, consideration, and decision/purchase stages.
- [GitOps Use Case Nurture](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/-/issues/2769) - contains streams for awareness, consideration, and decision/purchase stages.
- [AWS Partner Nurture](https://gitlab.com/groups/gitlab-com/marketing/-/epics/624) - contains streams for awareness, consideration, and decision/purchase stages.
- [Jenkins Take Out](https://gitlab.com/groups/gitlab-com/marketing/-/epics/282): The messaging for this track is centered around why GitLab built-in CI/CD solution is a better alternative than Jenkins plug-in solution. This track is targeted towards director, tools owner, and chief/prinicipal architects in the functions of applications, development, QA, and DevOps.
- [Version Control & Collaboration Use Case](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/-/issues/2435) - contains streams for awareness and consideration

### Newsletter

#### Process for bi-weekly newsletter

Open an issue using the [Newsletter Request Template](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/-/issues/new?issuable_template=Newsletter), including the newsletter send date in the issue title.

**[Epic of Past and Upcoming Newsletters](https://gitlab.com/groups/gitlab-com/marketing/-/epics/179)**

#### Creating the newsletter in Marketo

A day or two before the issue due date, create the newsletter draft. It's easiest to clone the last newsletter in Marketo:

1. Go to Marketing Activities > Master Setup > Outreach > Newsletter & Security Release
1. Select the newsletter program template `YYYYMMDD_Newsletter Template`, right click and select `Clone`.
1. Clone to `A Campaign Folder`.
1. In the `Name` field enter the name following the newsletter template naming format `YYYYMMDD_Newsletter Name`.
1. In the `Folder` field select `Newsletter & Security Release`. You do not need to enter a description.
1. When it is finished cloning, you will need to drag and drop the new newsletter item into the appropriate subfolder (`Bi-weekly Newsletters`, `Monthly Newsletters` or `Quarterly Newsletters`).
1. Click the + symbol to the left of your new newsletter item and select `Newsletter`.
1. In the menu bar that appears along the top of your screen, select `Edit draft`.

#### Editing the newsletter in Marketo

1. Make sure you update the subject line.
1. Add your newsletter items by editing the existing boxes (double click to go into them). It's best to select the `HTML` button on the menu bar and edit the HTML so you don't inadvertently lose formatting.
1. Don't forget to update the dates in the UTM parameters of your links (including the banner at the top and all default items such as the "We're hiring" button).

#### Sending newsletter test/samples from Marketo

1. When you're ready, select `Email actions` from the menu at the top, then `Send sample` to preview.
1. Enter your email in the `Person` field, then in `Send to` you can add any other emails you'd like to send a preview too. We recommend sending a sample to the newsletter requestor (or rebecca@ from the content team for marketing newsletters) for final approval.
1. When you are satisfied with the newsletter, select `Approve and close` from the `Email actions` menu.

#### Sending the newsletter

1. When the edit view has closed, click on the main newsletter item in the left-hand column.
1. In the `Schedule` box, enter the send date and select `Recipient time zone` if the option is available.
1. Make sure `Head start` is checked too.
1. In the `Approval` box, click on `Approve program`.
1. Return to the newsletter issue and leave a comment telling requestor (@rebecca from the content team for marketing newsletters)  to double check all has been set up correctly. Close the issue when this is confirmed.