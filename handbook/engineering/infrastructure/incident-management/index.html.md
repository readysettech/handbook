---
layout: handbook-page-toc
title: "Incident Management"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

If you're a GitLab team member and are looking to alert Reliability Engineering about an availability issue with GitLab.com, please find quick instructions to report an incident here: [Reporting an Incident](#reporting-an-incident).
{: .alert .alert-danger}

If you're a GitLab team member looking for who is currently the Engineer On Call (EOC), please see the [Who is the Current EOC?](#who-is-the-current-eoc) section.
{: .alert .alert-info}

If you're a GitLab team member looking for help with a security problem, please see the [Engaging the Security On-Call](/handbook/engineering/security/#engaging-the-security-on-call) section.
{: .alert .alert-info}

## Incident Management

Incidents are **anomalous conditions** that result in&mdash;or may lead
to&mdash;service degradation or outages. These events require human
intervention to avert disruptions or restore service to operational status.
Incidents are _always_ given immediate attention.

The goal of incident management is to organize chaos into swift incident
resolution. To that end, incident management provides:

1. well-defined [roles and responsibilities](#roles-and-responsibilities) and [workflow](#incident-workflow) for members of the incident team,
1. control points to manage the flow **information** and the **resolution path**,
1. a **root-cause analysis** (RCA),
1. and a post-incident review that assigns a **severity** classification after assessing the impact and scope of the incident.

When an [incident starts](#declaring-an-incident): we use the #incident-management slack channel for chat based communication.  There is a Situation Room Zoom link in the channel description for incident team members to join for synchronous communication.  There should be a link to an incident issue in the [`#incident-management`](https://gitlab.slack.com/archives/CB7P5CJS1) channel.  We prefer to keep status updates and main comments in a thread from that issue announcment.  This makes it easier for incoming oncall for EOC and CMOC to look for status on handoffs.


### Ownership

There is only ever **one** owner of an incident&mdash;and only the owner of
the incident can declare an incident resolved. At anytime the incident owner
can engage the next role in the hierarchy for support. With the exception of
when GitLab.com is not functioning correctly, the incident issue should
be assigned to the current owner.


### Roles and Responsibilities

It's important to clearly delineate responsibilities during an incident.
Quick resolution requires focus and a clear hierarchy for delegation of
tasks. Preventing overlaps and ensuring a proper order of operations is vital
to mitigation. The responsibilities outlined in the roles below are
cascading–**and ownership of the incident passes from one role to the next as
those roles are engaged**. Until the next role in the hierarchy engages, the
previous role assumes all of the subsequent roles' responsibilities and
retains ownership of the incident.

| **Role** | **Description** | **Who?** |
| -------- | ------------------------| --- |
| `EOC` - **Engineer On Call** | The EOC is the usually the first person alerted - expectations for the role are in the [Handbook for oncall](/handbook/on-call/#expectations-for-on-call). The checklist for the EOC is in our [runbooks](https://gitlab.com/gitlab-com/runbooks/blob/master/on-call/checklists/eoc.md). If another party has declared an incident, once the EOC is engaged the EOC owns the incident. The EOC can escalate a page in PagerDuty to engage the IMOC and CMOC. | The Reliability Team **Engineer On Call** is generally an SRE and can declare an incident. They are part of the "SRE 8 Hour" on call shift in PagerDuty. |
| `IMOC` -  **Incident Manager On Call** | The IMOC is engaged when incident resolution requires coordination from multiple parties. The IMOC is the tactical leader of the incident response team&mdash;not a person performing technical work. The IMOC assembles the incident team by engaging individuals with the skills and information required to resolve the incident. | The **Incident Manager** is an Engineering Manager, Staff Engineer, or Director from the Reliability team. The IMOC rotation is currently in the "SRE Managers" Pager Duty Schedule. |
| `CMOC` - **Communications Manager On Call** | The CMOC disseminates information internally to stakeholders and externally to customers across multiple media (e.g. GitLab issues, Twitter, status.gitlab.com, etc.). | The **Communications Manager** is generally member of the support team at GitLab. Notifications to the `Incident Management - CMOC` service in PagerDuty will go to the rotations setup for CMOC. |

These definitions imply several on-call rotations for the different roles.

#### Engineer on Call (EOC) Responsibilities

1. **As EOC, your highest priority for the duration of your shift is the stability of GitLab.com.**
1. The Single Source of Truth (SSOT) for who is EOC is the [SRE Schedule in Pagerduty](https://gitlab.pagerduty.com/schedules#P05EL5A).
1. Alerts that are routed to Pagerduty need to acknowledged within 15 minutes, otherwise they will be escalated to the oncall IMOC.
   1. Alert-manager alerts in [`#alerts`](https://gitlab.slack.com/archives/alerts) and [`#alerts-general`](https://gitlab.slack.com/archives/alerts-general) are an important source of information about the health of the environment and should be monitored during working hours.
   1. If the Pagerduty alert noise is too high, your task as an EOC is clearing out that noise by either fixing the system or changing the alert.
   1. If you are changing the alert, it is your responsibility to explain the reasons behind it and inform the next EOC that the change occurred.
   1. Each event (may be multiple related pages) should result in an issue in the `production` tracker.  See [production queue usage](/handbook/engineering/infrastructure/production/#implementation) for more details.
1. If sources outside of our alerting are reporting a problem, and you have not received any alerts, it is still your responsibility to investigate. [Declare a low severity incident](#declaring-an-incident) and investigate from there.
   1. Low severity ([S3/S4](/handbook/engineering/infrastructure/production/#severity)) incidents (and issues) are cheap, and will allow others a means to communicate their experience if they are also experiencing the issue.
   1. **"No alerts" is not the same as "no problem"**
1. GitLab.com is a complex system. It is ok to not fully understand the underlying issue or its causes. However, if this is the case, as EOC you should engage with the IMOC to find a team member with the appropriate expertise.
   1. Requesting assistance does not mean relinquishing EOC responsibility. The EOC is still responsible for the incident.
   1. The [GitLab Organizational Chart](/company/team/org-chart/) and the [GitLab Team Page](/company/team/), which lists areas of expertise for team members, are important tools for finding the right people.
1. As soon as an [S1/S2](/handbook/engineering/infrastructure/production/#severity) [incident is declared](#declaring-an-incident), join the `The Situation Room Permanent Zoom`. The Zoom link is in the `#incident-management` topic.
   1. GitLab works in an asynchronous manner, but incidents require a synchronous response. Our collective goal is high availability of 99.95% and beyond, which means that the timescales over which communication needs to occur during an incident is measured in seconds and minutes, not hours.
1. Keep in mind that a GitLab.com incident is not an "infrastructure problem". It is a company-wide issue, and as EOC, you are leading the response on behalf of the company.
   1. If you need information or assistance, engage with Engineering teams. If you do not get the response you require within a reasonable period, escalate through the IMOC.
   1.  As EOC, require that those who may be able to assist to join the Zoom call and ask them to post their findings in the incident issue or active incident Google doc. Debugging information in Slack will be lost and this should be strongly discouraged.

1. By acknowledging an incident in Pagerduty, the EOC is implying that they are working on it. To further reinforce this acknowledgement, post a note in Slack that you are joining the `The Situation Room Permanent Zoom` as soon as possible.
   1.  If the EOC believes the alert is incorrect, comment on the thread in `#production`. If the alert is flappy, create an issue and post a link in the thread. This issue might end up being a part of RCA or end up requiring a change in the alert rule.
1. _Be inquisitive_. _Be vigilant_. If you notice that something doesn't seem right, investigate further.
2. After the incident is resolved, the EOC should start on performing an [incident review](/handbook/engineering/infrastructure/incident-review) (RCA) and [assign themselves](#incident-review-issue-creation-and-ownership) as the initial owner. Feel free to take a breather first, but do not end your work day without starting the RCA.

#### Guidelines on Security Incidents

At times, we have a security incident where we may need to take actions to block a certain URL path or part of the application.  This list is meant to help the Security Engineer On-Call and EOC decide when to engage help and post to status.io.

If any of the following are true, it would be best to engage an Incident Manager:

1. There is a S1/P1 report or security incident.
2. An entire path or part of functionality of the GitLab.com application must be blocked.
3. Any unauthorized access to a GitLab.com production system

In some cases, we may choose not to post to status.io, the following are examples where we may skip a post/tweet.  In some cases, this helps protect the security of self managed instances until we have released the security update.

1. If a partial block of a URL is possible, for example to exclude problematic strings in a path.
2. If there is no usage of the URL in the last week based on searches in our logs for GitLab.com.


#### Incident Manager on Call (IMOC) Responsibilities

1. The SSOT for who is IMOC is the [SRE Managers Schedule in Pagerduty](https://gitlab.pagerduty.com/schedules/PQEEYGD)
1. The IMOC should monitor ongoing incidents and engage with the incident if it escalates to a user-impacting (S1 or S2) incident.
1. The IMOC should engage if requested by the EOC.
1. The time that the IMOC engages should be recorded in the incident issue by the IMOC co-assigning themselves to the issue. If GitLab.com is down, record the time in the Google working doc.
1. For non-critical issues, or critical (S1, S2) issues with a short duration, the IMOC will also take on the role of CMOC.
1. The IMOC should ensure that the appropriate team members from other teams engage within an appropriate amount of time.
   1. During a user-impacting incident, the appropriate time response time is minutes.
   1. If the IMOC is unable to obtain a response through Slack channels, they should escalate to a manager or director to obtain assistance.
1. They evaluate information provided by team members, lend technical direction, and coordinate troubleshooting efforts.
1. If applicable, coordinate the incident response with [business contingency activities](/handbook/business-ops/gitlab-business-continuity-plan.html).
1. After the incident is resolved, the IMOC is responsible for conducting the [post-incident review](/handbook/engineering/infrastructure/incident-review).
1. In the case of high severity bugs that affect a customer, the IMOC will also be responsible for making sure Incident Reviews are coordinated with Engineering and go through the proper Incident Review process.

To page the Incident Manager on call, see [Reporting an incident](#reporting-an-incident)

1. Run a [response play](/handbook/on-call/#site-reliability-engineers-sres)
1. Type `/pd trigger` in the `#production` channel

#### Communications Manager on Call (CMOC) Responsibilities
For serious incidents that require coordinated communications across multiple channels, the IMOC will select a CMOC for the duration of the incident during the incident declaration process.

The GitLab support team staffs an oncall rotation and via the `Incident Management - CMOC` service in PagerDuty.  They have a section in [the support handbook](/handbook/support/workflows/cmoc_workflows.html) for getting new CMOC people up to speed.

During an incident, the CMOC will:

1. Be the voice of GitLab during an incident by updating our end-users, internal parties, and executive-level managers through updates to our [status page](https://status.gitlab.com/) hosted by Status.io.
1. Update the status page at regular intervals in accordance with [the severity of the incident](/handbook/support/workflows/cmoc_workflows.html#frequency-of-updates).
1. Notify GitLab Community Advocates via Slack using the `@advocates` handle at the start of an incident.

##### How to engage the CMOC?

If, during an incident, EOC or IMOC decide to engage CMOC, they should do that
by paging the on-call person:
- Using the `/pd-cmoc` command in Slack
or
- Directly from PagerDuty in the [Incident Management - CMOC Rotation](https://gitlab.pagerduty.com/escalation_policies#PNH1Z1L)
schedule in PagerDuty. That can be done by navigating to [Incidents page in PagerDuty](https://gitlab.pagerduty.com/incidents),
and then creating the new incident while picking **Incident Management - CMOC** as
**Impacted Service**.

### Runbooks

[Runbooks](https://gitlab.com/gitlab-com/runbooks) are available for
engineers on call. The project README contains links to checklists for each
of the above roles.

**In the event of a GitLab.com outage**, a mirror of the runbooks repository is available on at https://ops.gitlab.net/gitlab-com/runbooks.

### Who is the Current EOC?

The chatops bot in the [`#production` Slack Channel](https://gitlab.slack.com/archives/production) will tell you this with `/chatops run oncall prod`.

### When to Contact the Current EOC

The current EOC can be contacted via the `@sre-oncall` handle in Slack, but please only use this handle in the following scenarios.
1. You need assistance in halting the depolyment pipeline. note: this can also be accomplished by [Reporting an Incident](/handbook/engineering/infrastructure/incident-management/#reporting-an-incident) and labeling it as `~severity::2`.
1. You are conducting a production change via our [Change Management](/handbook/engineering/infrastructure/change-management/) process and as a required step need to seek the approval of the EOC.
1. For all other concerns please see the [Getting Assistance](/handbook/engineering/infrastructure/team/reliability/#getting-assistance) section.

The EOC will respond as soon as they can to the usage of the `@sre-oncall` handle in Slack, but depending on circumstances, may not be immediately available. If it is an emergency and you need an immediate response, please see the [Reporting an Incident](/handbook/engineering/infrastructure/incident-management/#reporting-an-incident) section.

### Reporting an Incident

If you are a GitLab team member and would like to report a possible incident related to GitLab.com and have the EOC paged in to respond, choose one of the reporting methods below. Regardless of the method chose, please stay online until the EOC has had a chance to come online and engage with you regarding the incident. Thanks for your help!


#### Report an Incident via Slack

Type `/incident declare` in the [`#production`](https://gitlab.slack.com/archives/C101F3796) channel in GitLab's Slack and follow the prompts (detailed description and screenshot below). This will open an incident issue and notify the engineer on-call (EOC).  You do not need to decide if the problem is an incident.  We have triage steps below to make sure we respond appropriately.  Reporting high severity bugs via this process is the preferred path so that we can make sure we engage the appropriate engineering teams as needed.

![Incident Declaration Slack window](incident-declare-slack.png)<br/>*Incident Declaration Slack window*

| Field | Field Instructions |
|---|---|
| Title | This is the title of the incident issue, place a brief description of what you are witnessing on GitLab.com. |
| Detailed Description | Add any additional details here to assist the EOC responding to the incident. |
| Severity | If unsure about the severity to choose, but you are seeing a large amount of customer impact, please select S1. More details here: [Incident Severity](#incident-severity). |
| Tasks | You can safely ignore the first two options, if you'd like to ensure that the incident manager on-call (IMOC) and/or the communication manager on-call (CMOC) is notified via a page to their mobile device, select one or both of those options. Note: the engineer on-call (EOC) is notified via this workflow. |


#### Report an Incident via Email

Email [gitlab-production-eoc@gitlab.pagerduty.com](mailto:gitlab-production-eoc@gitlab.pagerduty.com). This will immediately page the Engineer On Call.


### Definition of Outage vs Degraded vs Disruption

This is a first revision of the definition of Service Disruption (Outage), Partial Service Disruption, and Degraded Performance per the terms on Status.io.
Data is based on the graphs from the [Key Service Metrics Dashboard](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1)

Outage and Degraded Performance incidents occur when:

1. `Degraded` as any sustained 5 minute time period where a service is below its documented Apdex SLO or above it's documented error ratio SLO.
2. `Outage` (Status = Disruption) as a 5 minute sustained error rate above the Outage line on the error ratio graph

![degraded and outage](/images/handbook/engineering/infrastructure/incident-management/SLI-degraded-outage.png)

SLOs are documented in the [runbooks/rules](https://gitlab.com/gitlab-com/runbooks/blob/master/rules/service_apdex_slo.yml)

To check if we are Degraded or Disrupted for GitLab.com, we look at these graphs:
1. Web Service
  - [Error Ratio](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=8&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=web&var-stage=main&var-sigma=2)
  - [Apdex](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=web&var-stage=main&var-sigma=2&fullscreen&panelId=7)
2. API Service
  - [Error Ratio](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=8&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=api&var-stage=main&var-sigma=2)
  - [Apdex](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=7&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=api&var-stage=main&var-sigma=2)
3. Git service(public facing git interactions)
  - [Error Ratio](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=8&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=git&var-stage=main&var-sigma=2)
    - [Apdex](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=7&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=git&var-stage=main&var-sigma=2)
4. GitLab Pages service
  - [Error Ratio](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=8&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=pages&var-stage=main&var-sigma=2)
    - [Apdex](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=7&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=pages&var-stage=main&var-sigma=2)
5. Registry service
  - [Error Ratio](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=8&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=registry&var-stage=main&var-sigma=2)
    - [Apdex](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=7&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=registry&var-stage=main&var-sigma=2)
6. Sidekiq
  - [Error Ratio](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=sidekiq&var-stage=main&var-sigma=2&fullscreen&panelId=8)
    - [Apdex](https://dashboards.gitlab.net/d/general-service/service-platform-metrics?orgId=1&fullscreen&panelId=7&var-PROMETHEUS_DS=Global&var-environment=gprd&var-type=sidekiq&var-stage=main&var-sigma=2)

A Partial Service Disruption is when only part of the GitLab.com services or infrastructure is experiencing an incident.  Examples of partial service disruptions are instances where GitLab.com is operating normally except there are:
1. delayed CI/CD pending jobs
1. delayed repository mirroring
1. high severity bugs affecting a particular feature like Merge Requests
1. Abuse or degradation on 1 gitaly node affecting a subset of git repos.  This would be visible on the Gitaly service metrics

#### High Severity Bugs

In the case of high severity bugs, we prefer that an incident issue is still created via [Reporting an Incident](/handbook/engineering/infrastructure/incident-management/#reporting-an-incident).  This will give us an incident issue on which to track the events and response.

In the case of a high severity bug that is in an ongoing, or upcoming deployment please follow the steps to [Block a Deployment](https://about.gitlab.com/handbook/engineering/releases/#deployment-blockers).

### Security Incidents

If an incident may be security related, engage the Security Operations on-call by using `/security` in Slack.  More detail can be found in [Engaging the Security On-Call](/handbook/engineering/security/#engaging-the-security-on-call).

## Communication

Information is an asset to everyone impacted by an incident. Properly managing the flow of information is critical to minimizing surprise and setting expectations. We aim to keep interested stakeholders apprised of developments in a timely fashion so they can plan appropriately.

This flow is determined by:

1. the type of information,
1. its intended audience,
1. and timing sensitivity.

Furthermore, avoiding information overload is necessary to keep every stakeholder’s focus.

To that end, we will have:

1. a dedicated Zoom call for all incidents. A link to the Zoom call can be found in the topic for the [`#incident-management`](https://gitlab.slack.com/archives/incident-management) room in Slack.
1. a Google Doc as needed for multiple user input based on the [shared template](https://docs.google.com/document/d/1NMZllwnK70-WLUn_9IiiyMWeXs-JKPEiq-lordxJAig/edit#)
1. a dedicated [`#incident-management`](https://gitlab.slack.com/archives/incident-management)  channel for internal updates
1. regular updates to status.gitlab.com via status.io that disseminates to various media (e.g. Twitter)
1. a dedicated repo for issues related to [Production](https://gitlab.com/gitlab-com/production) separate from the queue that holds Infrastructure's workload: namely, issues for incidents and changes.

### Status

We manage incident [communication](#communication) using status.io, which updates [status.gitlab.com](https://status.gitlab.com). Incidents in status.io have **state** and **status** and are updated by the incident owner.

Definitions and rules for transitioning state and status are as follows.

| **State** | **Definition** |
| --------- | -------------- |
| Investigating | The incident has just been discovered and there is not yet a clear understanding of the impact or cause. If an incident remains in this state for longer than 30 minutes after the EOC has engaged, the incident should be escalated to the IMOC.|
| Identified | The cause of the incident is believed to have been identified and **a step to mitigate has been planned and agreed upon**. |
| Monitoring | The step has been executed and metrics are being watched to ensure that we're operating at a baseline  |
| Resolved | The incident is closed and status is again Operational.  |

Status can be set independent of state. The only time these must align is when an issues is

| **Status** | **Definition** |
| ---------- | -------------- |
| Operational | The default status before an incident is opened and after an incident has been resolved. All systems are operating normally. |
| Degraded Performance | Users are impacted intermittently, but the impacts is not observed in metrics, nor reported, to be widespread or systemic. |
| Partial Service Disruption | Users are impacted at a rate that violates our SLO. The IMOC must be engaged and monitoring to resolution is required to last longer than 30 minutes. |
| Service Disruption | This is an outage. The IMOC must be engaged. |
| Security Issue | A security vulnerability has been declared public and the security team has asked to publish it. |

## Severities

### Incident Severity

**Incident severities encapsulate the impact of an incident and scope the resources allocated to handle it**. Detailed definitions are provided for each severity, and these definitions are reevaluated as new circumstances become known. Incident management uses our standardized severity definitions, which can be found under [availability severities](/handbook/engineering/quality/issue-triage/#availability).

### Alert Severities

1. Alerts severities do not necessarily determine incident severities. A single incident can trigger a number of alerts at various severities, but the determination of the incident's severity is driven by the above definitions.
1. Over time, we aim to automate the determination of an incident's severity through service-level monitoring that can aggregate individual alerts against specific SLOs.

## Incident Workflow

### Purpose
In order to effectively track specific metrics and have a single pane of glass for incidents and their reviews, specific labels are used. The below [workflow diagram](#workflow-diagram) describes the two paths an incident can take from `open` to `closed`. The two paths are dictated by the severity of the issue, `S1` and `S2` incidents require a review. In certain cases an `S3` or `S4` incident can take the review workflow path. [Details here](/handbook/engineering/infrastructure/incident-review/#review-criteria)

### Labeling
The following labels are used to track the incident lifecyle from active incident to completed incident review. [Label Source](https://gitlab.com/gitlab-com/gl-infra/production/-/labels?utf8=%E2%9C%93&subscribed=&search=Incident%3A%3A)

In order to help with attribution, we also label each incident with a scoped label for the Infrastructure Service (Service::) and Group (group::) scoped labels.

| **Label** | **Workflow State** |
| ---------- | -------------- |
| `~Incident::Active` | Indicates that the incident labeled is active and ongoing. Initial severity is assigned.|
| `~Incident::Mitigated` | Indicates that the incident has been mitigated, but immediate post-incident activity may be ongoing (monitoring, messaging, etc.) |
| `~Incident::Resolved` | Indicates that SRE engagement with the incident has ended and GitLab.com is fully operational. Incident severity is re-assessed and determined if the initial severity is still correct and if it is not, it is changed to the correct severity. |
| `~Incident::Review-in-Progress`  | Indicates that an incident met the threshold for requiring a review (S1/S2) or the IMOC or EOC for the incident chose to include a review (S3/S4) for the purposes of deriving and creating needed corrective actions. |
| `~Incident::Review-Scheduled`   | Indicates that the incident review has been added to the agenda for an upcoming review meeting. |
| `~Incident::Review-Completed`   | Indicates that an incident review has been completed, but there are notes to incorporate from the review writeup prior to closing the issue. |


In certain cases, additional labels will be added as a mechanism to add metadata to an incident issue.

| **Label** | **Workflow State** |
| ---------- | -------------- |
| `~self-managed` | Indicates that an incident is **exclusively** and incident for self-managed GitLab. [Example self-managed incident issue](https://gitlab.com/gitlab-com/gl-infra/production/-/issues/2651) |

### Workflow Diagram
 
```mermaid
graph TD
  A[Incident is declared] --> B[Incident::Active]
  B --> C[Incident::Mitigated]
  C --> D[Incident::Resolved]
  D -->|S1/S2| E[Incident::Review-in-Progress]
  D -->|S3/S4| Z[Closed]
  E --> F[Incident::Review-Scheduled]
  F --> G[Incident::Review-Completed]
  G --> Z
```

### Incident Board
The board which tracks all GitLab.com incidents from active to reviewed is located [here](https://gitlab.com/gitlab-com/gl-infra/production/-/boards/1717012?&label_name[]=incident).


## Near Misses

A near miss, "near hit", or "close call" is an unplanned event that has the potential to cause, but does not actually result in an incident.

### Background

In the United States, the Aviation Safety Reporting System has been collecting reports
of close calls since 1976. Due to near miss observations and other technological improvements,
the rate of fatal accidents has dropped about 65 percent.
[source](https://en.wikipedia.org/wiki/Near_miss_(safety))

As [John Allspaw states](https://qz.com/504661/why-etsy-engineers-send-company-wide-emails-confessing-mistakes-they-made/):

> Near misses are like a vaccine. They help the company better defend against
> more serious errors in the future, without harming anyone or anything in the process.

### Handling Near Misses

When a near miss occurs, we should treat it in a similar manner to a normal incident.

1. Open an [incident](/handbook/engineering/infrastructure/incident-management/#reporting-an-incident) issue, if one is not already opened. Label it with the severity label appropriate to the incident it would have caused, had the incident actually occurred. Label the incident issue with the `~Near Miss` label.
1. Corrective actions should be treated in the same way as those for an actual incident.
1. Ownership of the incident review should be assigned to the team-member who noticed the near-miss, or, when appropriate, the team-member with the most knowledge of how the near-miss came about.
