---
layout: handbook-page-toc
title: "Using Timeline"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

The Timeline view in Gainsight gives us a chronological overview of our activities with the customer. It's a valuable tool to see our interactions and progression on success efforts over time.

## Activity types

The following activities can be logged in Gainsight:

- **Update**: General update on the customer, could be from an internal conversation.
- **Call**: Conversation with the customer via Zoom or other synchronous channel.
- **In-Person Meeting**: On-site or otherwise in-person meeting with the customer.
- **Email**: Message sent to the customer, or message thread between the TAM and the customer.
- **Milestone**: This tracks when the customer achieves a major milestone such as Onboarding, time to value, TAM transition, etc.

### Last Activity Date

The "Last Activity Date" field in the customer's record reflects the latest "Call" or "In-Person Meeting" activity entry to be logged for the customer. These are the only entry types that affect Last Activity Date since we want to track when we are having synchronous conversations with the customer.

Please note it may take up to 2 hours after logging a timeline event before the "Last Activity Date" is updated.

Related, there is the "Last Timeline Activity" which looks to any and all activities on the timeline (update, email, call...).

## How to Log Activities in Timeline

To log activities (calls, meetings, updates, etc.), you'll primarily follow these steps:

1. Navigate to the customer
1. Click Timeline at the top
1. Hover over "+ Activity" and choose the appropriate activity type
1. Input a subject
1. Confirm the date and time (it will default to when you clicked "+ Activity") if applicable
1. Add internal and external attendees (more details on that immediately below) if applicable
1. Choose the meeting type if applicable
1. Check off if an executive sponsor attended if applicable
1. Optionally update the TAM and Product sentiments to reflect [health score](/handbook/customer-success/tam/health-score-triage/)
1. Add "Milestone Type" if applicable
1. Add notes (e.g. a link to the Google doc of your [cadence call](/handbook/customer-success/tam/cadence-calls), a summary of health score change, etc.)
1. Add any action items as "tasks"

The other options to log activities are (1) on the Scorecard while recording TAM Sentiment or Product Risk or (2) on the Success Plan to log a Timeline activity specific to the plan.

Attendees will only appear if they are a) a Salesforce user for internal attendees, or b) a contact in the Salesforce account record. If your internal attendee does not have a SFDC account (e.g. Support Engineers or Product Designers), you do not need to log them and can just mention in the notes they were there. If your external attendee is not populating, make sure that they are added to the correct account (child accounts have different contact lists than their parent accounts), and if not feel free to add them by clicking the "Add Contact" button in Salesforce and inputting the required details. New SFDC contacts most likely won't populate in Gainsight until the following day, so this is a great opportunity to create a CTA for yourself!

If you would like to see the activity logging process in action, please watch the [enablement video that covers logging](https://youtu.be/PL9shBdCMmo).

## BCCing Emails

While we recommend BBCing emails to Salesforce instead of to Gainsight, you can do the same with Gainsight. To get your personalize email address, navigate to your settings:

1. Click the person icon in the upper right
1. Click "My Settings"
1. Navigate to "Inbound Emails" and copy the email address (Tip: save it as an email contact for easy reference)

BCCing emails to Gainsight is _not_ a required step. However, if you want an email to appear in both Gainsight and Salesforce, you will need to BCC Gainsight.

1. Emails logged in Salesforce stay in Salesforce
1. Emails logged in Gainsight appear in Gainsight and then are synced to Salesforce during the nightly sync

For more information on using emails with Gainsight, see the [Gainsight workflow handbook page](/handbook/customer-success/tam/gainsight/#emails).

## Timeline View

When going to the timeline from the lefthand sidebar (not for a specific customer), you will see all timeline events for all TAMs. From there, you can filter by clicking the three horizontal lines to customize what events are shown (see picture below). For example, you can search for yourself as the author to find all timeline events you created, or you can search for a company to find all timeline events for a specific customer.

![Gainsight Timeline Filter](/images/handbook/customer-success/gainsight-timeline-filter.png "Gainsight Timeline Filter")
