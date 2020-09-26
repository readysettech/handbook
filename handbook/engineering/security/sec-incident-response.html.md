---
layout: handbook-page-toc
title: "GitLab Security Incident Response Guide"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Engaging SIRT

If an urgent security incident has been identified or you suspect an incident may have occurred, please refer to [Engaging the Security On-Call](/handbook/engineering/security/#engaging-the-security-on-call).

## Security Responder On-Call

The [SIRT](/handbook/engineering/security#SIRT) team is on-call 24/7/365 to assist with any security incidents. Information about SecOps on-call responsibilities and incident ownership is available in the [On-Call Guide](./secops-oncall.html).

# Incident Management and Review

As part of the incident management and review process the SIRT maintains a recurring meeting that takes place on Monday of each week. During this meeting all of the previous weeks incidents, and any incidents that are currently open are reviewed. The review process covers the incidents scope, impact, the work performed to mitigate and remediate the incident, next steps, blockers, and current status. These meetings are also an opportunity to discuss mishandled incidents and process improvements.

## Incident Identification

Security incident investigations are initiated when a security event has been detected on [GitLab.com](https://www.gitlab.com) or as part of the GitLab company. These investigations are handled with the same level of urgency and priority regardless of whether it's a single user or multiple projects.

Indicators can be reported to SIRT either internally, by a GitLab team member, or [externally](/handbook/engineering/security/#external-contact-information). It is the Security team's responsibility to determine when to investigate, dependent on the identification and verification of a security incident.

The GitLab Security team identifies security incidents as any violation, or threat of violation, of GitLab security, acceptable use or other relevant policies.

## Confidentiality

Security incidents may (and usually do) involve sensitive information related to GitLab, GitLab's customers or employees, or users who (in one way or another) have engaged with GitLab. GitLab, while codifying the [Transparency](/handbook/values/#transparency) value, also strongly believes in and strives to maintain the privacy and confidentiality of the data its employees, customers, and users have entrusted us with.

A **confidential** issue means any data within the issue and any discussions about the issue or investigation are to be kept to **GitLab employees only** unless permission is explicitly granted by GitLab Legal, a GitLab Security Director, the VP of Security, or the GitLab Executive Team.

## Incident Tracking

Security incident investigations must begin by opening a [tracking issue](https://gitlab.com/gitlab-com/gl-security/security-operations/sirt/operations/-/issues/new?issuable_template=Incident_Response) in the [SIRT](https://gitlab.com/gitlab-com/gl-security/security-operations/sirt/operations/-/issues) project and using the Incident Response template. This tracking issue will be the primary location where all work and resulting data collection will reside throughout the investigation.

All artifacts from an investigation must be handled per the [Artifact Handling and Sharing](https://gitlab.com/gitlab-com/gl-security/runbooks/-/blob/master/sirt/external_requests/handling_and_sharing_artifacts.md) internal only runbook.

**NOTE:** The tracking issue, any collected data, and all other engagements involved in a Security Incident must be kept **strictly confidential**.

## Incident Severity

Assigning severity to an incident isn't an exact science and it takes some rational concepts mixed with past experiences and gut feelings to decide how bad a situation may be. When considering severity, look at:

* The type of data involved and how it's classified using the [Data Classification Policy](./data-classification-standard.html)
  * Was this data leaked or disclosed to parties who should not have visibility to it?
  * Was the data been modified in our records? (either confirmed or believed to be)
* Was a user or service account taken over?
  * What level of access did this account have and to what services or hosts?
  * What actions were taken by the compromised account?
* If a vulnerability is present on a host or service, consider the impact it might have on GitLab and the likelihood of it being exploited by using the [Risk Factors and Risk Scoring](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#risk-factors-and-risk-scoring) documentation.
  * Was the vulnerability exploited? If so, how was it used and how frequently?
* What is the scope of the incident?
  * How many GitLab.com users were/may have been impacted?
  * How many hosts or services?
* Has this incident resulted in any hosts or services being unavailable?

After taking these types of questions into consideration, review the [Overall Impact](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#determining-the-impact-of-a-threat-event) to help place a severity rating on the incident.

[Data Breach Notification Policy](/security/#data-breach-notification-policy)

## Internal Engagement & Escalation

Coordinate with internal teams and prepare for the incident investigation:

* Invite all available parties to the SIRT incident response Zoom conference bridge for easier discussion (see topic in the SIRT slack channel, or zoom link in incident issue). The Security Engineer On-Call will begin recording the Zoom conference bridge **to their computer** then upload it to the team drive after concluding the incident bridge.
* Open an incident-focused Slack channel to centralize non-verbal discussion, particularly if the incident is of a sensitive nature. This should follow the naming convention `#sirt_####` where #### is the GitLab issue number in the SIRT project.
* If the incident was created by the security pager a Google Drive Folder and Shared google doc should have been created automatically and linked to the issue. If the incident was created manually:
    * Set up a [shared Google Drive folder or gcs bucket](https://gitlab.com/gitlab-com/gl-security/runbooks/-/blob/master/sirt/external_requests/handling_and_sharing_artifacts.md#storing-and-sharing-files-using-google-cloud-storage) for centralized storage of evidence, data dumps, or other pieces of critical information for the incident.
    * Create a shared Google Doc from the [Security Incident Response Template](https://docs.google.com/document/d/1mYQxuLXGaBr6xwHV7YgRbDt_k597tk_Dr2NFX4qb79s/template/preview) and move it into the shared Google Drive folder to act as a centralized record of events in real-time. Try to capture significant thoughts, actions, and events as they're unfolding. This will simplify potential hand-off's and eventual Incident Review of the incident.

In the event that an incident needs to be escalated within GitLab, the Security Engineer On Call will page the Security Incident Manager On Call (SIMOC). It is the responsibility of the SIMOC to direct response activities, gather technical resources from required teams, coordinate communication efforts with the Communications Manager On Call, and further escalate the incident as necessary.

Characteristics of an incident requiring escalation include but are not limited to the following:

* Incidents involving or likely to involve data with an Orange or Red classification
* Incidents that are likely to impact, or are actively impacting, the availability or functionality of essential services
* Incidents affecting legal or financial resources
* Incidents that are likely to require a breach notification or public notification
* Incidents involving criminal activity or that may require the involvement of law enforcement
* Incidents involving key personnel such as executive leadership

If applicable, coordinate the incident response with [business contingency activities](/handbook/business-ops/gitlab-business-continuity-plan.html).

## Containment

Once an incident has been identified and its severity set, the incident responder must attempt to limit the damage that has already occurred and prevent any further damage from occurring. When an incident issue is opened it will automatically contain the `~Incident::Phase::Identification` label. At the start of the containment phase this label will be updated to `~Incident::Phase::Containment`.

The first step in this process is to identify impacted resources and determine a course of action to contain the incident while potentially also preserving evidence. Containment strategies will vary based on the type of incident but can be as simple as marking an issue confidential to prevent information disclosure or to block access to a network segment.

It's important to remember the containment phase is typically a stop-gap measure to limit damage and not to produce a long term fix for the underlying problem. Additionally the impact of the mitigation on the service must be weighed against the severity of the incident.

When triaging priority::1/severity::1 incidents there may be times that SIRT or Infrastructure are unable to mitigate an issue, or identify the full impact of a potential mitigation. In these cases the [Development Escalation Process](/handbook/engineering/development/processes/Infra-Dev-Escalation/process.html) can be used to engage with the development team on-call. It is important that this process is followed [as documented](/handbook/engineering/development/processes/Infra-Dev-Escalation/process.html#process-outline) and only for priority::1/severity::1 issues.

## Remediation and Recovery

During the remediation and recovery phase the incident responder will work to ensure impacted resources are secured and prepared to return the service to the production environment. This process may involve removing malicious or illicit content, updating access controls, deploying patches and hardening systems, redeploying systems completely, or a variety of other tasks depending on the type of incident. When transitioning from the containment phase into the remediation phase the SEOC will update the phase lable to `~Incident::Phase::Eradication` and when the remediation is complete the label will be updated to `~Incident::Phase::Recovery`.

A Incident Review will be completed for all `severity::1` incidents to guide the remediation and recovery process. Careful planning is required to ensure successful recovery and prevention of repeat incidents. The incident responder coordinates impacted teams to test and validate all remediations prior to deployment.

This phase should prioritize short term changes that improve the overall security of impacted systems while the full recovery process may take several months as longer term improvements are developed. During the post remediation Incident Review process the incident phase label will be updated to `~Incident::Phase::Incident Review`.

## Resolution

Upon completing the containment, remediation, communication and verification of impacted services, the incident will be considered resolved and the incident issues may be closed and the incident phase label will be changed to `Incident::Phase::Closed`.

The incident response process will move on to a post-mortem and lessons learned phase through which the process improvements and overall security of the organization can be analyzed and strengthened.

## Internal & External Communication

Our [security incident communication plan](/handbook/engineering/security/security-incident-communication-plan.html) defines the who, what, when, and how of GitLab in notifying internal stakeholders and external customers of security incidents.

## Engaging Law Enforcement

If during the course of investigating a security event the incident itself, materials involved in the incident (stored data, traffic/connections, etc), or actions surrounding the incident are deemed illegal in the United States, it may be necessary (and advisable) to engage U.S. law enforcement.

1. The Security Engineer On-Call will immediately escalate to the Director of Security Operations to raise awareness of the legal concern.
1. Following review, the Engineer and Director will engage the VP of Security and VP of Legal for validation of next steps.
1. The Director of Security Operations will then contact the appropriate law enforcement agency.

## When You Are Brought into an Incident Channel or Call

In the event of perceived major security incident (which may prove to not be one at a later point), adhoc communication is sometimes required for coordination. This is outlined in the sections above. If you are identified as someone who could assist during the perceived security incident with either the identification, confirmation, or mitigation of the incident, you will be added to a dedicated Zoom call or Slack channel. Upon joining that call/channel, please take note of the following:

* This is crisis management communication channel, that means that it's **private by default**. It may contain business critical or PII information that cannot be shared with the larger company at this time, or ever. Should GitLab Security determine that the content of this particular communication channel can be made internally available or public at a later point, the required changes will be made. 
* **Read the channel history before asking questions**. Get some context, read through past conversations and related documents. The relevant person will reach out to you with specific asks at the right time.
* **Do your best to stay professional**. However, be aware that security incidents are often stressful and we're all humans. People may raise their voice, or use wording that seems unnecessary, harsh or inappropriate. It's important to cut people some slack (no pun intended) during this stressful time, and raise/address any potentially erratic behavior with the relevant manager once the incident is over.
* **Humor is your ally**. No, it really is.
