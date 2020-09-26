---
layout: handbook-page-toc
title: "Incident Review"
---

## On this page

{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Incident Review

> The primary goals of writing an Incident Review are to ensure that the incident is documented, that all contributing root cause(s) are well understood, and, especially, that effective preventive actions are put in place to reduce the likelihood and/or impact of recurrence.[^1]

### Review Criteria
If an incident matches any of the following criteria, an incident review must be completed:

1. Incident was declared an severity::1/severity::2
1. A service disruption occurred
1. Data loss of any kind
1. A resolution time longer than 30 minutes
1. A monitoring failure

A review can be optionally conducted for incidents which do not meet the above criteria. In cases where an optional review is conducted, it is *not* necessary to fill out a complete review. For the sake of expediency, you can complete areas of the review which highlight what you, as the review author, want to bring to the attention of the larger organization.

## Incident Review Process

### Authoring the Incident Review

The first step in the Incident Review process is the synchronous review of the incident by representatives of the teams involved in the resolution of the incident. This step is conducted as close to the incident date as possible and does not require a complete Incident Review write up. The outcome of this first step should be a published Incident Review, per defined [timelines](#incident-review-timeline).

### Review of Root Causes and Corrective Actions

Incident reviews second step is engaging with the customer, through the point of contact such as a TAM. This should always involve sharing the findings from the first step in an async form. In case of a customer requiring a sync to discuss the finding, the Infrastructure management will organise the discussion with important stakeholders of this process, per defined [timelines](#incident-review-timeline)

1. IMOC for the Incident updates the TAM team on expected AIR timelines.
1. IMOC provides TAM published review. IMOC can also include a recording of the review, if the recording does not contain sensitive information.
1. TAM communicates to IMOC whether their customer(s) would like a synchronous review and the TAM schedules a review with the customer.
1. TAM facilitates Customer access to the review and the Customer can add a set of questions prior to the meeting and all participants can collaborate on any changes or additions to corrective actions.

## Incident Review Timeline

1. **Immediately following the incident**: The incident review is started in the original incident issue and the [EOC and IMOC are assigned](#incident-review-issue-creation-and-ownership).
   1. IMOC and EOC invite stakeholders for involvement in authoring the incident review. This can include one of more of:
       1. Appropriate **development team(s)**, involved in changes that contributed to the incident.
       1. A **Quality-engineering team**, in order to look for improvements to the QA process could have mitigated or reduced the length of the incident.
       1. The **Delivery team**, when release processes contributed to the incident.
       1. The **Scalability team**, when scaling bottlenecks contributed to the incident.
       1. The **Dev-Escalation engineer** for the incident.
       1. The **CMOC**, if necessary.
       1. **Product Managers**, for example, if the incident could have been avoided by the prioritisation of specific ~Infradev/technical debt work.
       1. **Technical Account Managers**, if the incident directly impacted one of more major accounts
       1. For severity::1 incidents, **directors** responsible for the invited teams should also be invited.
   1. For teams, the manager should be invited, and, if they wish, can delegate responsibility to another member of the team.
1. **Within seven working-days of the incident**: Incident Review is authored and ready for review by stakeholders.

## Incident Review Issue Creation and Ownership

Incident Reviews are conducted in the incident issue and their workflow is tracked on the [Production Incidents Board](https://gitlab.com/gitlab-com/gl-infra/production/-/boards/1717012?label_name[]=incident).

1. Every incident and its review must be assigned a DRI. The DRI is the Engineer on Call (EOC).
   1. The Incident Manager on Call (IMOC) is also assigned to the issue.
1. The output of an incident review should include one or more issues labeled `~Corrective Action`.  Labeling and linking existing issues as corrective action is appropriate.
1. The DRI is responsible for selecting and assigning corrective actions that should be prioritized and resolved within a specific timeframe.
   1. Check the `Target SLO` for `~Corrective Action` in this table:

   | Corrective action of issue severity | SLO (days after issue has been created) |
   | ------ | ------ |
   | severity::1 | 1 week |
   | severity::2 | 30 days |
   | severity::3 | 60 days |
   | severity::4 | 90 days |

   (coming from this [link](https://gitlab.com/gitlab-com/gl-infra/infrastructure/-/issues/10516#note_375948861))
 
1. All issues labeled `~Corrective Action` must have an assigned priority label, it is the responsibility of the DRI to ensure that the priorities are set.
1. After discussion on the Incident Review issue has ended, all `~Corrective Action` issues have been linked, and notes from the review are incorporated into the Incident Review issue, the incident review issue can be closed.

## Synchronous Review Meeting Sessions

Incident review sessions are open on the GitLab Team Meetings calendar with the title `Incident Review Recurring Sessions` and occur at the following two times: 
1. Tuesdays at 13:30 - 14:20 UTC
1. Tuesdays at 22:00 - 22:50 UTC

The assigned IMOC is responsible for properly labeling the Incident Review issue (see [Incident-Management#labeling](/handbook/engineering/infrastructure/incident-management/#labeling) `~Incident::Review-Scheduled` and adding it to the [agenda](https://docs.google.com/document/d/1Llm9tXHC2dNt_eercRUUXlUyWmOVw00wmXWQQbWvv2c/edit#).

GitLab team members are encouraged to review the issues listed in the [agenda](https://docs.google.com/document/d/1Llm9tXHC2dNt_eercRUUXlUyWmOVw00wmXWQQbWvv2c/edit#) and add questions/comments. The IMOC assigned to a review is responsible for ensuring that stakeholders outside of Infrastructure are aware of the review. This can be achieved by inviting them to the Google Calendar event for when the incident will be discussed, posting in their teams' Slack channels, at-mentioning them in the issue, and assigning them directly in the Google Doc&mdash;or some combination of those options. If the participation from stakeholders outside of Infrastructure department in either the async or sync review is not sufficient to create sufficient understanding of the situation and corrective actions, the IMOC will envoke the [infradev process](/handbook/engineering/development/#continuous-delivery-infrastructure-and-quality-collaboration) and escalate to the appropriate stakeholders.

The purpose of these sessions are to encourage discussion, asking questions and ensure that all aspects of the incident are reviewed, including:

1. Is the incident review completed to the appropriate level?
1. Were our monitoring systems effective?
1. Is there a sufficient understanding of the circumstances that led to the outage? If not, is there a plan to improve observability to improve understanding in future?
1. Were the root causes explored in sufficient depth?
1. Are the corrective actions appropriate and have the appropriate assigned priorities?
1. Do the stakeholders agree with the findings?

## Updating the GitLab SaaS Infrastructure Meeting

In order to circulate the findings of the incident review across a wider audience, the IMOC should include a link to completed incident reviews in the [GitLab SaaS Infrastructure meeting](/handbook/engineering/infrastructure/#gitlab-saas-infrastructure) [agenda](https://docs.google.com/document/d/1fLQQBKt0mShmTk_mJ-BmBM6OFjal63-AH7yKSbMg6_s/edit#).

---

[^1]: Google SRE Chapter 15 - Postmortem Culture: Learning from Failure
