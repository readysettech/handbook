---
layout: handbook-page-toc
title: "GitLab Security Operations On-Call Guide"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# GitLab Security Operations On-Call Guide

The Security Operations Team (SecOps) is collectively on-call 24/7/365, split into 12-hour shifts Monday to Friday and 48-hour coverage Saturday and Sunday.

On-call scheduling is organized in Pager Duty as the `Security Responder` policy.

## Responsibilities

During those on-call shifts the Security Engineer On-Call has three core responsibilities:

1. Acknowledge and respond to pages
1. Review and engage on issues marked with the `oncall` label
1. Improve Security Operations on-call and incident handling processes

### 1. Engagement: Paging Duties

The on-call Engineer's primary concern is to provide timely engagement to pages sent to Security Operations.  When receiving a page:

1. Acknowledge the alarm in #security-department Slack channel or through PagerDuty directly
1. Review the contents of the page, the associated GitLab issue any other provided details
1. Resolve the PagerDuty alarm (via Slack or PagerDuty)
1. Investigate and mitigate/resolve the issue as priority

If the alarm is not acknowledged within **15 minutes** the Security Incident Manager On-Call will be alerted.

### 2. Review, Engage & The `oncall` Label

Occasionally issues in Security Engineering and Security Operations will be marked with the `oncall` label, and during the on-call shift we should watch for and engage on new, as well as existing, open/active issues to assist towards mitigation/resolution.

These issues are typically generated through automated alerting and may occasionally require human intervention based on the scenario. In the least these should be reviewed twice per shift.

### 3. Improve On-Call, Incident Handling, and GitLab's Security

As we continue to grow and mature in the operational security space we will have many new experiences, succeed and fail at handling security events, and subsequently learn from them. These learnings should be documented through runbooks, processes, and handbook updates. During on-call shifts it's the on-call Engineer's responsibility to take notes, look for improvement opportunities in how we handle scenarios, find steps that can be automated, and ask questions about our tools, services, infrastructure, and try to find questionable security areas or risky decisions so we can improve GitLab's overall security posture.

### 4. Reduce the Backlog

As on-call periods are typically interrupt driven it can be difficult to work on large projects, this is a good opportunity to engage with the queue of `Backlog` issues. It is the responsibility of the on-call Engineer to review the Security Operations Backlog board for items that can be accomplished during the on-call period. When working an issue from the Backlog the on-call Engineer will then own the issue and must see it through to completion. This may include completing it in the week following their on-call schedule.

## Incident Ownership

There's a simple rule to incident ownership: Whoever ACK's the page owns it. Other Engineers and members of Security Operations may engage to maintain 24/7 coverage but ownership remains with whomever ACK'd the page.

Ownership of an incident implies being accountable to:

* Ensuring continued progression to a resolved state
* Maintaining ongoing 24/7 coverage by Security Operations
* Accurate and timely issue tracking and communication with stakeholders

Being accountable does not imply being the sole person to act on these tasks. Hand-off at the end of an on-call shift, or coordinated breaks during extended incidents, would temporarily place another person responsible for these tasks. To coordinate these hand-offs it's essential to equip the next person with all necessary details...

### Incident Hand-off

To best prepare the next Engineer and ensure continued progress, details should be recorded in the page-created issue as well as the Security Operations slack channel. Details like:

* **Issue Summary**: Brief summary of the issue and details of the current state.
* **Related Issues**: Related GitLab issues being worked by other teams (Infrastructure, Product Engineering, etc)
* **Who's Engaged**: Other GitLab team-members engaged on the incident
* **Active Zoom Bridge**: <<Zoom Bridge URL>>
* **Slack Channel(s)/Thread(s)**: #Channel(s) and/or Slack thread link
* **Next Steps**: What are the next steps for the issue and/or what tasks or steps need to be taken by the next Engineer. If other teams are taking action, who's responsible for that work and what are those actions.

### Security Managers On-Call

In addition to the SecOps Engineers being on-call 24/7/365, the Security Managers in the GitLab Security Department act as a backup in the event the Security Engineer On-Call is unable to respond to a page.  PagerDuty will automatically engage the Security Manager on-call if the SecOps engineer doesn't acknowledge a page within `15 minutes`. 

It's the responsibility of the Security Manager on-call to:

* Be available via mobile phone during their on-call shift if the Security Engineer On-Call does not acknowledge a page.
* Attempt to contact the Security Engineer On-Call to acknowledge the page. **Note: If slack is not available or an alternative means of communication is required, PagerDuty has cell phone numbers of GitLab team-members involved in the on-call process.**
* Contact the backup Security Engineer On-Call according to the PagerDuty schedule.
* If the on-call and backup SecOps Engineers are unresponsive, attempt to contact other SecOps Engineers to take on the page.  Prioritise based on timezone and region.
* In the event of a high-impact security incident to GitLab, the Security Manager On-Call will be engaged to assist with cross-team/department coordination.
