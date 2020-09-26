---
layout: markdown_page
title: How to Perform CMOC Duties
category: GitLab.com
---

- TOC
{:toc}

----

## Introduction

As the [Communications Manager on Call (CMOC)](/handbook/engineering/infrastructure/incident-management/#roles-and-responsibilities) it's your job to be the voice of GitLab during an incident to our users, customers, and stakeholders. To do this you must communicate with them through our status page, [Status.io](https://status.io).

The basics of how to create, update, and close incidents in Status.io are covered by their [Incident Overview](https://kb.status.io/incidents/incident-overview/) documentation. However, this document covers how we specifically use Status.io to perform those tasks.

## Things To Know

Before getting into the actual process of managing an incident, the following sections should be noted.

### Frequency of Updates

Status.io should be updated whenever we have new information about an active incident that our stakeholders should be aware of. Outside of that, it should be updated at a consistent rate depending on the severity of the incident as outlined in the table below.

When you enter the situation room, take note of any updates that have been made to Status.io and the time they were made at. Set a timer to remind yourself and stick to the time intervals below unless you make a note of how long it will be until the next status update. For example, if you're in "monitoring" it may be appropriate to specify an hour before the next update.

| Incident Status | severity::1 Update Frequency | severity::2 Update Frequency | severity::3/severity::4 Update Frequency |
|--|--|
|Investigating| 10m | 15m | 15m |
| Identified | 10m | 30m | 30m |
| Monitoring | 30m | 60m | 60m |
| Resolved | No further updates required |

#### What to do if you don't know what to say
- Provide a generic update based on the best information you have:
   - _We're seeing elevated error rates on GitLab.com, investigation is underway in: link_
   - _Some users are reporting connection issues to GitLab.com, we're working on it in: link_
- Craft a draft of what you think is correct. Whenever possible use ["I intend to..." language](https://www.youtube.com/watch?v=7KnPjakwqeI) when communicating with the IMOC and EOCs:
   - _@IMOC - I'm going to post: "We've isolated the network problem to the APAC region and are working with Cloudflare support to get it resolved_.
   - _In my next update I'm going to move the status to "monitoring"_ 
- Bias to action - you can post another update if there was an error in your last update.

- If there are no material updates to report, say something so that people know we care and are working on it. Below are a few example messages:
   1. No material updates to report. We're discussing if we should restore from backup or let the replica catch up first but we have not made a decision.
   1. No material updates to report. We tried starting the Gitaly servers but we're still missing connectivity.
   1. No material updates to report. We are doing a handover to a new CMOC since the current CMOC has been at it for three hours straight.
   1. No material updates to report. We would like to thank Google for the #hugops tweet we received. LINK

- If you really don't know, it really is okay to ask!

### EOC vs. IMOC

In later sections of this workflow it's called out that at times you should be asking the IMOC of the incident for permission to move an incident between certain states (updating, monitoring, resolving). On the rare occasion that an incident does not have an IMOC, you may ask the EOC instead.

### Reviewing Past Incidents

Keep in mind that you can always [review past incidents](https://status.gitlab.com/pages/history/5b36dc6502d06804c08349f7) if you need examples or inspiration for how to fill in the details for a current incident.

### Contacting a User

Whether related to an ongoing incident or not, infra or security may ask you to reach out to one or more users if they detect unusual usage. Please follow the [internal requests workflow](internal_requests.html#contact-request) to log the request.

## The Incident Process

As the CMOC you'll guide the incident through the following three stages.

1. Stage 1: **Incident Creation** - During this stage we're creating the actual incident in Status.io, linking up with Reliability via *The Situation Room* Zoom call, and notifying the Community Advocacy team, if necessary.
1. Stage 2: **Incident Updates** - During this stage we're following along with the work being performed by the EOC and any assisting engineers to resolve the incident and making updates to Status.io along the way while adhering to the [Frequency of Updates](#frequency-of-updates) schedule.
1. Stage 3: **Incident Resolution** - During this stage we're focused on setting the incident to **Monitoring** in Status.io for a period of time to ensure that the issue does not recur before we close it out, eventually setting the incident to **Resolved**, and adding a link to the post-mortem issue in Status.io.

The following sections outline how to perform each of the steps within these stages.

### Stage 1: **Incident Creation**

The following steps should be taken immediately after receiving a PagerDuty page for an incident.

1. Acknowledge the PagerDuty page.
1. Join **The Situation Room** Zoom call.
1. Create the incident in Status.io.
1. Notify the Community Advocacy team.
1. Resolve the PagerDuty page.

#### PagerDuty Status
{:.no_toc}
- **Triggered** - "An incident exists that requires the attention of a CMOC"
- **Acknowledged** - "I have seen the page and am on my way to the incident room"
- **Resolved** - "A tracking issue has been created, the status page has been updated and I am actively engaged in the incident management process"

**NB:** "Resolved" in PagerDuty does not mean the underlying issue has been resolved. 


#### 1. Join *The Situation Room*

Before you create an incident in Status.io, or immediately afterward, you should be joining **The Situation Room**, a permanent Zoom room that is used by the EOC, IMOC, CMOC, and anyone else within GitLab that is assisting with the resolution of an incident. A Zoom link to the room can always be found in the channel topic of [#incident-management](https://gitlab.slack.com/archives/CB7P5CJS1).

Your role as CMOC while in this room is to follow along while the incident is worked and make updates to Status.io either when asked or when it's necessary. Oftentimes chatter in this room will be lively, especially in the early stages of an incident while the source of the issue is being discovered. Use your best judgment on when it's appropriate to speak up to avoid vocalizing at inopportune times. You can always ping anyone on the call through Slack if you need to ask a non-urgent question about the situation.

#### 2. Create the Incident

After logging in to Status.io you should be met with the dashboard that displays various statistics about our current status. A new incident can be created by clicking `New Incident` along the top bar.

![New incident](/images/support/cmoc_new_incident.png)

This takes you to the new incident screen where you'll be asked to fill in the details of the incident. The following is an example of what a new incident would look like if we're experiencing an issue with a delay in job processing on GitLab.com.

![Incident details](/images/support/cmoc_incident_details.png)

Change the following values:

`Title` - Titles should be brief and concise. The incident title should answer the question: **In simple terms, what is the issue?**

`Current State` - In nearly all cases an incident should be created in the `Investigating` state. If it's been communicated to you that we're aware of what is causing the current incident this could be set to `Identified` from the beginning.

`Details` - In keeping with our value of [transparency](/handbook/values/#transparency), we should go above and beyond for our audience and give them as much information as possible about the incident on its creation. This field should **always** include a link to the incident issue from the [production issue tracker](https://gitlab.com/gitlab-com/gl-infra/production/issues) so that our audience can follow along.

`Incident Status` - When creating a new incident this will never be `Operational`. The status of an incident depends entirely on its scope and how much of the platform it's impacting.

`Broadcast` - Always check each box in this section.

`Message Subject` - Always leave this at its default value.

`Affected Infrastructure` - This should almost always be unchecked so that the value of the `Incident Status` field is only applied to the specific aspects of the platform that are affected by the incident. In the example above we're only experiencing an issue with job processing so only `CI/CD` is selected.

#### 3. Notify Community Advocates

The CMOC should make the [Community Advocacy](/handbook/marketing/community-relations/community-advocacy/) team aware of the incident by mentioning them with the `@advocates` Slack handle in the [#incident-management](https://gitlab.slack.com/archives/CB7P5CJS1) channel if the following conditions are met.

- The incident is an **severity::1**
- The incident is an **severity::2**
- The incident is an **severity::3** or **severity::4** but you feel that the CA team should know about it anyway

### Stage 2: **Incident Updates**

To update an active incident click the incidents icon from the dashboard.

![Active incident dashboard icon](/images/support/cmoc_update_incident_dashboard.png)

Then click on the edit button next to the incident.

![Incident edit button](/images/support/cmoc_update_incident.png)

Change the following values:

1. `Current State` - Change this depending on the current state of the incident and whether or not we've identified the cause (Identified) or implemented a fix (Monitoring).
1. `Details` - Be as descriptive as possible about the update and include a link to the production issue.
1. `Broadcast` - Check all boxes.
1. `Current Status` - If the incident has improved or worsened update this value. If neither, leave it as it was from when the incident was created.
1. `Set Status Level` - Uncheck this and keep only the affected component selected unless the incident has increased in scope and now affects other components of our infrastructure. **IMPORTANT** These must be checked individually as in the screenshot below.

A ready to be published update should look similar to the following.

![Incident update](/images/support/cmoc_post_incident_update.png)

### Stage 3: **Incident Resolution**

Closing an incident out has two stages, `Monitoring` and `Resolved`. Once the affected component is back to operating normally a monitoring period should begin where we switch an incident over to `Monitoring` where it remains open for ~30 minutes to ensure that the issue does not recur. We then mark it `Resolved` once we're confident the issue will not recur, which closes the incident.

The two stages of the resolution process are covered in their respective sections below.

#### Monitoring

To start the monitoring period, edit the incident, and configure the update similar to the following.

![Switch to monitoring](/images/support/cmoc_monitoring_stage.png)

Take special note of the changes made to the following fields at this stage.

1. `Current State` - Change this to `Monitoring`.
1. `Details` - If we have not previously mentioned that a fix has been applied, do so at this stage and make specific mention that we're monitoring the system to ensure that a repeat of the issue does not occur. Make sure to include a note that *All systems are online and currently fully operational*.
1. `Incident Status` - At this point, the affected component should be back to normal operation, so we can flip this back to `Operational`. **IMPORTANT**: Each component must be updated to `Operational` manually.

#### Resolved

Once we're confident that the underlying issue that caused the incident has been fully resolved and a monitoring period has been observed, we should close the incident. Before we do so, we should check with the IMOC via Slack for the all-clear. This should be done by starting a thread on the announcement in #incident-management that started the incident and [mentioning](https://slack.com/help/articles/205240127-Mention-a-member) the IMOC in it. The following is what one of these messages looks like.

![Incident announcement in Slack](/images/support/cmoc_incident-slack-thread.jpg)

Once we have confirmation from the IMOC that the incident can be resolved, make an update to the incident and change the following fields.

1. `Current State` - Change this to `Resolved`
1. `Details` - Our message here should include a definitive statement that the issue has been resolved and that the affected component is back to operating normally. We should also aim to again include a link to the relevant issue in the production issue tracker so that any users who missed previous updates know where to go for more info.
1. `Incident Status` - Unless we forgot to change this field to `Operational` when our monitoring phase began we can leave this alone.

Before resolving the incident your draft should look similar to the following:

![Resolve incident](/images/support/cmoc_resolve_incident.png)

#### Post-Mortem

A review will be conducted by production engineering for every incident that matches a [certain criteria](/handbook/engineering/infrastructure/incident-management/#incident-review). Status.io allows us to add a link to a post-mortem after an incident has been resolved which will then be viewable on our status page for that specific incident.

Do the following to add a post-mortem to a resolved incident:

1. From the dashboard click the `Incidents` button.

   ![Active incident dashboard icon](/images/support/cmoc_update_incident_dashboard.png)

1. Scroll down and click on the title of the incident.

   ![Incident history list](/images/support/cmoc_post_mortem_incident_list.png)

1. Click `Add Post-Mortem` and supply the link to the issue being used for the incident review.

   ![Add post-mortem link](/images/support/cmoc_add_post_mortem.png)

### Handover Procedure

At the end of each on-call shift its necessary to inform the next CMOC of any relevant activity that occurred during it or is still ongoing. To perform a handover create an issue in the [CMOC Handover](https://gitlab.com/gitlab-com/support/dotcom/cmoc-handover/issues) issue tracker using the [Handover](https://gitlab.com/gitlab-com/support/dotcom/cmoc-handover/issues/new?issuable_template=Handover) issue template. Create the handover issue even if nothing happened during your shift, signaling that everything is fine is also useful information. It's critical to remember that since we [work out in the open](https://about.gitlab.com/blog/2015/08/03/almost-everything-we-do-is-now-open/) by default, the CMOC Handover issue tracker is open to the public. **A handover issue should be made confidential if it must contain any sensitive information.**

If handover occurs during an active incident where the quick summary you'd provide in the handover issue is insufficient to properly prepare the incoming CMOC of the situation, you are encouraged to start up a quick Zoom call in the [#support_gitlab-com](https://gitlab.slack.com/archives/C4XFU81LG) Slack channel with the incoming CMOC.
Slash commands such as the following can be used to expedite getting the meeting setup.

```plain
/zoom meeting CMOC Handover Briefing
```
