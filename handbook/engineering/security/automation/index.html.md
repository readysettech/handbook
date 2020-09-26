---
layout: handbook-page-toc
title: "Security Automation"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}


## Vision

`TODO`

https://gitlab.com/gitlab-com/gl-security/engineering-and-research/automation-team/automation/-/issues/7

### Mission

`TODO`

### Initiatives in this Specialty

`TODO`

### Goals

#### Baseline
- Deliver small to medium-sized developments that automate or speed up security-relevant efforts with a quick design and implementation turn around.
- Our differentiating factor is the ability to understand complex systems and infrastructures.
- We execute within the DevOps and DevSecOps model whenever possible with emphasis in delivery but without disregarding maintainability and best practices.

#### Stretch

- Our deliverables ought to be modular and based on decoupled autonomous architecture designs.
- We strive to continuously consolidate and collectively improve SecAuto's products and technology stack.
- When viable and possible, we hand-off functioning proof-of-concepts to other teams to consider as product features.

## Team Members

https://about.gitlab.com/company/team/org-chart/

## Engaging the Security Automation Team

If you have a need or idea for security-relevant projects at GitLab that require automation, please add the `secauto|workflow::new` label directly to your issue as detailed in the `Labels` section. On the other hand, to bring an issue or artifact to our attention without expectation of a deliverable, please add the `secauto|interest` label to it. We review and prioritize issues with those labels during our [Weekly Meeting](#weekly-meeting), which anyone can attend. In case you want to engage us directly, please reach out on Slack in by mentioning `@sec-automation-team` in the #security-department channel. As usual, you can also tag the SecAuto team within GitLab by using `@gitlab-com/gl-security/engineering-and-research/automation-team`

## Task Management and Workflow

The SecAuto team continually works on improving the way in which we work and deliver value to the company. This sections describes our workflow and how we use GitLab to manage our team and projects.

Our workflow is a simplified version of [GitLab's Engineering Workflow](https://about.gitlab.com/handbook/engineering/workflow/) although we might increasingly adopt conventions and approaches referred to in there, our process will most likely perpetually deviate with bias towards simplicity.

## Weekly Meeting

[The SecAuto team's weekly meeting](https://calendar.google.com/calendar/u/0/r/eventedit/M2NyNmNsazJkNGRydHJmMmc2Y3Y3dm1hbzAganNhbGF6YXJAZ2l0bGFiLmNvbQ) is a 50-minute meeting that can also be found on the Security Department Team Meetings calendar.

 * Synchronous Customer Reviews (10 minutes) - Discuss intake issues with customers directly if needed.
 * Show and Tell (10 minutes) - Share work, interesting challenges, etc regarding work accomplished since the last meeting.
 * Issue Refinement (10 minutes) - Refinement of issues as per our [weekly refinement process](#weekly-refinement).
 * Last Week’s Tasks Review (5 minutes) - If necessary, update the team on action items that resulted from the past meeting.
 * Agenda Topics (20 minutes) - Discuss any internally added items to [our agenda](https://docs.google.com/document/d/1YOtmU2XpuxcVkfjXghBfZMyRhxu1GGDlohrjuONy0VA/edit)

### Overview

The best way to get an overview of what the SecAuto team is working on at any time is to use our epics list and issue boards.

Our [OKR Epics List](https://gitlab.com/groups/gitlab-com/gl-security/-/epics?scope=all&utf8=✓&state=opened&label_name%5B%5D=Security%20Management%3A%3ASecurity%20Automation%20Team) tracks all of our outstanding team OKRs as per [Development's Approach to OKRs](https://about.gitlab.com/company/okrs/#example-developments-approach-to-okrs). 

SecAuto's OKRs are team-centric and tackled as a team effort, only issues are assigned directly to DRIs. Epics tracking SecAuto OKRs, we follow the `SecAuto - <OKR Name>` naming convention so they are easily discoverable despite absence of a `secauto|*` label and regardless of the hierarchy level at which they are created. Finally, OKR-epics must be labeled `FY2*`, `OKR` and `Security Management::Security Automation Team` and be ideally created at the https://gitlab.com/groups/gitlab-com/gl-security/engineering-and-research/automation-team/-/epics level. Since epics bubble up the hierarchy, these will still be visible at https://gitlab.com/groups/gitlab-com/gl-security/-/epics/.


We have three issue boards, the [Intake Board](https://gitlab.com/groups/gitlab-com/-/boards/1926147) for use during prioritization meetings, the [In-Progress Board](https://gitlab.com/groups/gitlab-com/-/boards/1930491) to keep track of progress on issues and the [Management Board](https://gitlab.com/groups/gitlab-com/-/boards/1926345), which is meant to give the SecAuto's team manager and the team an overview of OKRs and other matters exclusive to the team's management and operation.

All `secauto|*` labels currently being used by the SecAuto team can be found [in the issue label listing for gitlab-com](https://gitlab.com/groups/gitlab-com/-/labels?utf8=%E2%9C%93&subscribed=&search=secauto).

### Namespaces and where Work Happens

SecAuto has a [main issue tracker](https://gitlab.com/gitlab-com/gl-security/engineering-and-research/automation-team/automation/-/issues/) and [repository](https://gitlab.com/gitlab-com/gl-security/engineering-and-research/automation-team/automation/). However, we also act as maintainers or owners of other namespaces, please refer to the project list section below.

#### What Goes in the Main SecAuto Issue Tracker?

Any issues and associated work concerning the SecAuto team that cannot be clearly assigned to a single, existing SecAuto product and its associated tracker.

#### What Goes in A Project's Issue Tracker?

Issues that are exclusive to a single product or project and for which a repository exists, these shall be labeled with the appropriate `secauto|` labels (task, meta, priority, etc). If a repository doesn't exist but an issue is relevant only to a single project, component or product, a repository should be created.

#### Who is Responsible for Managing Labels?

Everyone in the team is responsible guaranteeing consistency in workflow and labeling. We're a small team and the more organized we are the better we'll be able to collaborate and communicate our results. New issues in the [Main SecAuto tracker](https://gitlab.com/gitlab-com/gl-security/engineering-and-research/automation-team/automation/-/issues/) will be collectively reviewed and labeled before or during the weekly SecAuto meeting. New issues in project-specific trackers will be reviewed and properly labeled by each project's DRI(s) upon creation.

### Intake Process

Most of the work SecAuto does is externally initiated. Opportunities for contributing originate from the day-to-day operations of teams in the Security Department and accross GitLab. These usually arise in Slack conversations, as issues in the GitLab groups `gitlab-org` and `gitlab-com`, etc. SecAuto's processes rely heavily on labels, they inform both customers and the team about the status of issues and other artifacts as detailed in the `Labels` section.

SecAuto's intake process is simple, as detailed in the  `Labels` and `Workflow` sub-sections:

> Once SecAuto creates a task or is made aware of one relevant to the team, the team assigns the label `secauto|workflow::new`.
> All tasks labeled `secauto|workflow::new` are considered part of the SecAuto backlog and must be triaged.

After this has happened, the team will triage the issue, as is done with any issue labeled `secauto|workflow::new`.

Alternatively, the SecAuto team can be made aware of an issue where their awareness, contribution or involvement may be desired by applying the `secauto|interest` label on an artifact.

> `secauto|interest` can be used to mark issues and other artifacts across the company's namespaces that might be of interest to secauto. An issue detailing new guidelines and expectations regarding cost management in GCP environments would be one such example.

### Promotion and Dividing of Tasks

Tasks that are considered too large for a single sprint will be upgraded to epics in our [OKR Epics List](https://gitlab.com/groups/gitlab-com/gl-security/-/epics?scope=all&utf8=✓&state=opened&label_name%5B%5D=Security%20Management%3A%3ASecurity%20Automation%20Team). From there, additional sub-tasks will be created to define iterative sprint-sized or less chunks of work in an attempt to accomplish the epic.

### Labels not Related to Deliverables

`secauto|task::management` is meant for all issues and conversations related to the strategy, tactics and management aspects of the Security Automation team and its projects.

`secauto|interest` can be used to mark issues and other artifacts across the company's namespaces that might be of interest to secauto. An issue detailing new guidelines and expectations regarding cost management in GCP environments would be one such example.

### Stages of a Task

Tasks, issues and other artifacts on which SecAuto is expected to deliver can be in the `new`, `ready`, `in-progress`, `blocked`, `cancelled` or `done` stages.

Once SecAuto or another team creates a task for the team to triage, the label `secauto|workflow::new` must be applied to it. All tasks labeled `secauto|workflow::new` are considered part of the SecAuto backlog and must be triaged.

### Triaging A Task

The next step is for tasks to be triaged and thus be labeled `secauto|workflow::ready` to be worked on by the team. A task will only be labeled `secauto|workflow::ready` once the following holds:

- The task's definition of done is clear and detailed enough as to be considered well-defined.
- The task has a `secauto|customer` label identifiying the customers profiting from the deliverables.
- The task has a priority given by a `secauto|priority` label
- The task has a type given by a `secauto|task` label

Once a task is labeled `secauto|workflow::ready`, work on it can begin, hence labeling it  `secauto|workflow::in-progress`, and eventually be concluded `secauto|workflow::done`.

Such is the ideal, more common path for a task to take.

The `secauto|workflow::blocked` and `secauto|workflow::cancelled` labels can be applied at any time in the life-cycle of task and are mostly used to track how often we are blocked, how many times we triage, prioritize and work on something only for us or our customers to halt the task, etc.

### Task Customers

Every task must have at least one `secauto|customer` label, these labels signal what teams are requesting and will profit from the delivery on a given task. Furthermore, it can be assumed that the author of the issue, the members of their team participating in the issue, and if needed their manager, can act as stable counterparts during the time period the SecAuto team works on said task.

If there are multiple customer teams, each team should have at least one stable counterpart explicitly listed on the issue.

### Task Types

All work performed by SecAuto falls within the following areas:

1. `secauto|task::incident` relates to managerial activities affecting the SecAuto team
1. `secauto|task::incident` reactively mitigates a critical malfunction on product by SecAuto
1. `secauto|task::bug`  reactively addresses a non-critical, undesired condition in a product by SecAuto
1. `secauto|task::improvement` proactively delivers a non-critical related to a product by SecAuto
1. `secauto|task::maintenance` proactively delivers an operative related to a product by SecAuto
1. `secauto|task::infrastructure` proactively delivers value related to a non-product, non-user-facing infrastructure component used by SecAuto, this includes scripts for cleanup, GCP infrastructure.
1. `secauto|task::analysis` delivers information after performing evaluations, analyses, investigations, brainstorming and the like.
1. `secauto|task::documentation` formalizes and documents the results of other task types whenever this is required.

Infrastructure, maintenance and improvement labels exist since the nature of the work is different. As SecAuto, we work with more than features, in our day-to-day we act as developers, architects, consultants, at times even SREs. These labels help capture the nature of that work for strategic and tactical purposes such as metrics gathering.

### Prioritizing Artifacts

`secauto|priority::low` `secauto|priority::moderate` and `secauto|priority::high` are our priority markers. We use this to determine what needs to be done and when.

We assign priority labels based on a simplified version of the [RICE framework](https://about.gitlab.com/handbook/product/product-processes/#using-the-rice-framework) in use by the Engineering Department and define Impact and Effort as follows:

| Impact   | Definition                                                                                             |
| -------- | ------------------------------------------------------------------------------------------------------ |
| Low      | a deliverable will somewhat improve the ability of the customer to act efficiently and effectively     |
| Moderate | a deliverable will improve the ability of the customer to act efficiently and effectively              |
| High     | a deliverable will considerably improve the ability of the customer to act efficiently and effectively |

| Effort   | Definition                                                                    |
| -------- | ----------------------------------------------------------------------------- |
| Low      | producing a deliverable will take one SecAuto team member less than a week    |
| Moderate | producing a deliverable  will take one SecAuto team member less than a month  |
| High     | producing a deliverable will take one SecAuto team member less than a quarter |

Taking this into consideration, we calculate priority as follows:

| Impact   | Effort   | Label                         |
| -------- | -------- | ----------------------------- |
| High     | High     | `secauto\|priority::moderate` |
| Moderate | High     | `secauto\|priority::low`      |
| Low      | High     | `secauto\|priority::low`      |
| High     | Moderate | `secauto\|priority::high`     |
| Moderate | Moderate | `secauto\|priority::moderate` |
| Low      | Moderate | `secauto\|priority::low`      |
| High     | Low      | `secauto\|priority::high`     |
| Moderate | Low      | `secauto\|priority::high`     |
| Low      | Low      | `secauto\|priority::low`      |

These priority calculations assume a good understading of the customers needs, also known as confidence. In cases where a task is not clearly defined or its purpose unclear, a `secauto|task::investigation` issue should be created instead.

### Review

Tasks labeled `secauto|needsReviewManager`, `secauto|needsReviewTeam` or `secauto|needsReviewCustomer` must be looked at by the respective party mentioned in the label in order for work to proceed. For example, the creation of a new, expensive GCP environment should be labeled `secauto|needsReviewManager` anytime a manager's input is needed. Furthermore, work potentially leading to down-time on a product used by a SecAuto customer should be labeled `secauto|needsReviewCustomer`. Finally, for non-code-managed changes where approval cannot happen in an MR or where peer-review is desired, `secauto|needsReviewTeam` should be used.

### Weekly Refinement

The planning activities in the meetings should be limited to 15 minutes.

This process relies on a rotating role of "SecAuto triager" to ensure that issues that do not correspond to project with an existing DRI are triaged asynchronously (see below).

#### Prior to the meeting

Completing the following asynchronous tasks prior to the meeting will keep the synchronous meeting on schedule:

* _All_ team members are responsible for labeling and starting refinement of issues they come across that have not been refined yet.
* The triager and DRIs for each SecAuto project should review ~"secauto|workflow::new" issues for issues relevant to their projects and:
  * Assign `secauto|customer` labels identifying the customers requesting the deliverables.
  * Assign the task an initial `secauto|priority` label
  * Assign the task a `secauto|task` type label

* The SecAuto triager, as DRI but also with distributed assistance by the team, is responsible for making the following determination on priority for new issues:
  * If an issue seems like it needs to be addressed immediately or within the next week, they will label it ~"secauto|priority::high". If so, they are expected to engage the most-likely DRI or raise with the team to find a DRI that will work on the task. This should be done immediately or at the upcoming SecAuto Team Meeting the latest. For other issues, these will remain in the ~"secauto|workflow::new" stage as a backlog items. The triager should note this in a comment to provide feedback for the requester on expected time frames.
  * For issues labeled ~"secauto|workflow::new" and ~"secauto|priority::high", the DRI should make an initial attempt at scoping the work for a weekly milestone. They or the DRI should, if this can be done without the teams consideration, break down the task in smaller issues prior to the meeting that can be scheduled and assigned for delivery during the next and following weeks.

#### During the refinement portion of the meeting

The "SecAuto triager" is responsible for facilitating the refinement portion of the meeting:

* Determine who will be the SecAuto triager for the next week (the current rotation is at the top of the agenda document).
* Based on the [Management Board](https://gitlab.com/groups/gitlab-com/-/boards/1926345), review tasks that might be stalling, are labeled `secauto|workflow:blocked` as well as raise blockers for any unfinished work.
  * Review high-priority tasks that are still marked `secauto|workflow::ready`.
* Based on the [In-Progress Board](https://gitlab.com/groups/gitlab-com/-/boards/1930491), make sure issues labeled `secauto|needsReviewManager`, `secauto|needsReviewTeam` or `secauto|needsReviewCustomer` are addressed and assigned or re-assigned for during the meeting.
* Based on the [Intake Board](https://gitlab.com/groups/gitlab-com/-/boards/1926147), make sure `secauto|workflow:new` issues with high, moderate and low priority, in that order, are discussed and assigned to team members for them to [triage them](#triaging-a-task) and bring them to a `secauto|workflow:ready` state.
* If using a tracking milestone, OKR-epic or the like, make sure issues discussed and assigned are linked to them.

### Working on ~"secauto|type::analysis" Issues

`TODO`

### Project Structure and Management

#### Scaffold
* Ask the team if there are any issues they want to review or discuss.

#### DRI

#### Hand-Off Process


# Security Automation Resources

## SecAuto's Environment

### In the Security Enclave

### In Production

## Literature

### Guiding Principles

### Tech Notes


## Projects

| Project                                                                                                               |
| --------------------------------------------------------------------------------------------------------------------- |
| [Security Pager](https://gitlab.com/gitlab-com/security-tools/security-pager)                                         |
| [HackerOne-GitLab Integration](https://gitlab.com/gitlab-com/security-tools/h1-gitlab)                                |
| [GSuite Group Members Reporter](https://gitlab.com/gitlab-com/security-tools/report-gsuite-group-members/-/pipelines) |
| [Suricata Runner Metrics](https://gitlab.com/gitlab-org/gitlab-runner/-/merge_requests/1545)                          |
| [DELKE](https://gitlab.com/gitlab-com/gl-security/security-operations/sirt/delke)                                     |
