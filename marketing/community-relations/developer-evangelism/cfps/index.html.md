---
layout: handbook-page-toc
title: "Developer Evangelism CFPs"
---

## How we manage CFPs (Call for Proposals)

### Our events list
Every year, developer evangelism prioritizes some key events in our ecosystem for which we run the conference proposal (CFP) process. These events are maintained in a [living list](https://docs.google.com/spreadsheets/u/1/d/1E4J4Kx7Eq8JXuh_o4RfSRbGyjj8IeVCiPRLOGslLcfU/edit?usp=drive_web&ouid=101407496565734994973) as we add suggestions that fulfill our requirements for focus events. You can also find a calendar view of our events below:

<br>

<iframe src="https://calendar.google.com/calendar/embed?src=gitlab.com_5nsh2o42detjnpana2fheauirg%40group.calendar.google.com&ctz=Europe%2FAmsterdam" style="border: 0" width="800" height="600" frameborder="0" scrolling="no"></iframe>

## Requesting a Developer Evangelist to submit a CFP
To request that a Developer Evangelist submit a CFP to your event, please:

1. [Open a new issue](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=technical-evangelist-request) 
1. Ensure you use the `technical-evangelist-request` template, and fill out the External Request section.
1. Label the issue with the `TE-CFP` label.

### CFP Management
For every CFP process, we are participating in a [CFP meta issue](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=CFP-Meta) is created with details about the event, requirements for CFP submissions and any other relevant information that might be useful to potential speakers. Every person who wants to submit a proposal for an event we are tracking should use the [CFP-Submission](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=CFPsubmission) issue template in [Corporate Marketing issue tracker](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues) and mark it as related to the Event's CFP Meta issue. This way, we can track submissions for each event.

#### Issue Workflow

We monitor 2 GitLab issue types for CFPs:

1. A meta issue for the call for proposals
1. Submission issues created by interested speakers that relate to the meta issue

All CFP issues have the with `TE-CFP` label. These issues appear on the dedicated [CFP Issue board](https://gitlab.com/groups/gitlab-com/-/boards/1616902?&label_name[]=TE-CFP).

Afterward, our workflow uses scoped labels to transition the issues through different stages.

| **CFP Labels** | **Issue Type** | **Description** |
| ------ | ------ | ------ |
| `TE-CFP-Meta::Open` | Meta CFP Issue | Identifies a CFP meta issue that is still open for submissions |
| `TE-CFP-Meta::Closed` | Meta CFP Issue | Identifies a CFP meta issue that already has passed due date |
| `TE-CFP-Meta::Cancelled` | Meta CFP Issue | Identifies a CFP meta issue for an event that has been cancelled |
| `TE-CFP-Upcoming` | Meta CFP Issue  |  This labels is used to track CFPs that are near due dates. | 
| `TE-CFP::Draft` | CFP Submission Issue | Identifies CFP (Call for Proposal) Drafts that are under Developer Evangelism Team Radar | 
| `TE-CFP::Review` | CFP Submission Issue | Identifies CFP (Call for Proposal) Drafts that require review by the Developer Evangelism Team | 
| `TE-CFP::Submitted` | CFP Submission Issue  | Identifies submitted CFPs (Call for Proposal) and monitored by the Developer Evangelism team |
| `TE-CFP::Rejected` |  CFP Submission Issue  | Identifies Rejected CFPs (Call for Proposal) and monitored by the Developer Evangelism team |
| `TE-CFP::Accepted` | CFP Submission Issue  | Identifies Accepted CFPs (Call for Proposal) and monitored by the Developer Evangelism team | 
| `TE-CFP::Missed` | CFP Submission Issue  | Identifies CFPs (Call for Proposal) that missed submission | 


For a CFP submission the transition is depicted below:

```plantuml
start
: TE-CFP, TE-CFP::Draft;
: TE-CFP, TE-CFP::Review;
: TE-CFP, TE-CFP::Submitted;
if (CFP is Accepted) then (yes)
    : TE-CFP, TE-CFP::Accepted;
elseif (CFP is Rejected) then (yes)
    : TE-CFP, TE-CFP::Rejected;
elseif (CFP is Waitlisted) then (yes)
    : TE-CFP, TE-CFP::Waitlist;
else  (nothing)
    : TE-CFP, TE-CFP::missed;
endif
stop

```
