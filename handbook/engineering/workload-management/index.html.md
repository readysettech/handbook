---
layout: markdown_page
title: "Workload Management"
---

## Overview

As the Engineering organization grows, particularly within the context our asynchronous nature, so do our collaboration and cross communication needs. These require having stable (but by no means *static* and certainly not inflexible) conventions regarding how we manage our workload and how we do so across teams, so that we can manage expectations effectively and efficiently. Having standarized workload management guidelines and workflows will help us on both fronts, as teams can better understand how to cooperate by sharing a commom language and workload management framework.

This framework is not intended to be strictly prescriptive, and its adoption is not mandatory. The intention is to put forth a framework baseline that yields enough gains that critical mass is organically achieved across Engineering. Thus. teams are free to chose to adopt the framework or not, or extend it as they see fit to serve specific needs. In any event, it is expected to undergo multiple iterations before it will serve the needs of an organization as diverse as Engineering. 

When a team adopts the framework, it requires everyone's involvement and cooperation, from individual contributors and managers alike, and the discipline to keep issues, milestones and epics tidy so we can better help everyone self-serve their needs for information about our work.

## Tools

This framework is centered around the use of GitLab, and its adoption will entail adjusments over time, both as we make modifications to fulfill our needs and as GitLab as a product evolves in its capabilities. GitLab is our tool of choice so that we live with our own product to not only helps us manage our workload but so that it helps us improve the product.

#### Issues

Issues represent our **basic unit** of trackable **work**. While we can outline tasks within an issue, the issue as a whole represents a self-contained block of work. It is critical we consistency and diligently fill out the approprate issue metadata so that we can more easily understand its purpose, context and state, and so that we can automate the production of reports and other artifacts necessary to drive standups, retros, and other reports.

*  Issues must contain a concise title and a complete description that includes expected, verifiable outcomes. 
* An issue must always have an assignee (a DRI) once work commences on it (see *Issue States* below).
* An issue should generally belong to an epic when it reflects project work. There are exceptions: task oriented issues can be part of regular work (e.g., access requests) but not part of a project. Also, there's unexpected work that crops up, which is considered (and should be labeled as) *unscheduled*.
* An issue should always belong to a milestone. When planning the milestone, issues should be in the `Ready` state. Issues should always be in milestone when `In Progress`.
* Due dates are desirable once an issue is ready for work on a milestone.
* Issue weights help asses the complexity of an issue, but there are no strict guideliines on their meaning. In general, they are useful to asses the velocity of a team so that we can gather this data and improve milestone planning.

##### Issue States (Labels)

It is important to understand the current state of an issue: we need to know what work is *ready* to begin, what work is currently *in progress* (which will always be a part of a milestone), and what work is blocked by external factors that likely requires a manager's involvement.

States are tracked through scoped labels (`workflow::<state>`).

| Label         | **Status** | Description                                                  |
| ------------- | ---------- | ------------------------------------------------------------ |
|               | Open       | An issue that needs to be triaged (i.e., complete its description, prioritize, etc). |
| `Ready`       | Open       | An issue is ready to be worked on as soon as someone is available to begin working on it. The issue has a complete description of the problem or task at hand, and describes the expected outcomes. Issues in this state must have a priority assigned to that issues can be ordered by priority and *what's next* is clear. |
| `In Progress` | Open       | An issue is currently being worked on. Issues `In Progress` must always be part of a milestone and must always have an assignee. Issues can be added to a milestone in any state. |
| `Review`      | Open       | An issue is not being actively worked on and it's awaiting review. This might be for example when an MR that is part of the issue has been assigned for a review or when an Access Request awaits approval. |
| `Stalled`     | Open       | Work on an issue is stalled but not blocked: we have simply decided, for whatever reason, to postpone the issue short-term, and it can be restarted at any time without being blocked by any external factors. |
| `Blocked`     | Open       | An issue is blocked when work cannot proceed until some other work is completed or some external condition is met. It is critical to clearly idenfity when an issue is blocked so that we (managers when necessary) can prioritize unblocking it. |
| `Verified`    | Open       | An issue is verified when the work outlined by the issue has been validated as being complete and working correctly. |
|               | Closed     | An issue is closed when work on it has completed and the issue has been verified. Depending on the type of issue, *completed* may mean *deployed to production*. |

###### Stalled vs Blocked

There is a subtle but critical difference between a **stalled** issue and a **blocked** issue. 

* When an issue is stalled, it means we have commenced work on it but have *voluntarily* decided to postpone said work short-term, generally due to other high-priority work. In that regard, `Ready` and `Stalled` are similar: they're both ready to start or restart work.
* When an issue it blocked, work on it has been *involuntarily* postponed due to some external blocker (perhaps another issue that must be completed or a decision that needs to be made). Blockers signal to managers that they need to keep an eye, and perhaps get involved in, unblocking an issue.

##### Issue Priorities (Labels)

It is critical to assign priorities to issues so that people who complete work and are looking for the next item to work on have a clear idea of what work is next. 

Priorities are tracked through labels (`priority::<n>`, where `1 <= n <= 4`). Each team, department, function adopting this framework should contextualize these priorities, as the ones [defined in the documentation](https://docs.gitlab.com/ee/development/contributing/issue_workflow.html#priority-labels) are very release-oriented.

| Label | Description |
| ----- | ----------- |
| `priority::1`  |             |
| `priority::2`  |             |
| `priority::3`  |             |
| `priority::4`  |             |

The group scoped label is defined for all groups of the devops cycle. The other departments, including Infrastructure, Security and Quality, do not use these labels at the moment.

##### Teams

Depending on the department, it may be necessary to assign group ownership of an issue. This is done through the `team::<team>` scoped labels. All issues should have an explicit team label after triage. The `team:<undefined>` label can be used to specifically denote that a team determination has not been made yet.

### Epics and Milestones: Issue Contextual Containers

We don't work in a vaccum, and issues do not generally exist without some context. There are two contexts needed to manage deliverables: *semantic* context, in which an issue is part of achieving a larger goal, and *timing* context, (i.e., time-boxing) which we use to track our progress towards reaching said goal.

Two logical containers to group issues are available, covering the two contexts mentioned above:

* **[Epics](https://docs.gitlab.com/ee/user/group/epics/)** are goal-based and define the final state of a group of issues, thus providing *semantic* context. While epics can be time-bounded, time is not the primary driver in an epic: its goal is. 
* **[Milestones](https://docs.gitlab.com/ee/user/project/milestones/)** are time-bounded sprints to group tasks and checkpoint progress on an epic; thus provinding *timing* context.

Issues should always belong to an epic when they reflect planned work. All issues should always end up belonging to a miletone, especially one they enter the `In Progress` state. For instance, unscheduled work such as acccess requests may not be part of an epic, but should always be part of a milestone (and labeled accordingly so we can later measure the amount of unscheduled work we face).

##### Epic States (Labels)

Managers are the primary maintainers of epics. As with issues, epics have should have state associated with them, again via the use of scoped labels: (`workflow::<state>`).

| Label         | **Status** | Description                                                  |
| ------------- | ---------- | ------------------------------------------------------------ |
|               | Open       |                                                              |
| `Ready`       | Open       | An epic is ready to be worked on as soon as someone is available to begin working on it. The epic has a complete description of the problem or task at hand, and describes the expected outcomes. |
| `In Progress` | Open       | An epic is currently being worked on. Epics `In Progress` must always have issues actively being worked on. |
| `Stalled`     | Open       | Work on an epic is stalled but not blocked: we have simply decided, for whatever reason, to postpone the epic, and it can be restarted at any time without being blocked by any external factors. |
| `Blocked`     | Open       | An epic is blocked when work cannot proceed until some other work is completed or some external condition is met. It is critical to clearly idenfity when an epic is blocked so that we (managers when necessary) can prioritize unblocking it. |
| `Verified`    | Open       | An epic is verified when the work outlined by the epic has been validated as being complete and working correctly. |
|               | Closed     | An epic is closed when work on it has completed and the epic has been verified. Depending on the type of epic, *complede* may mean *deployed to production*. |

##### Epic Priorities (Labels)

It is critical to assign priorities to issues so that people who complete work and are looking for the next item to work on have a clear idea of what work is next. 

Priorities are tracked through labels (`priority::<n>`, where `1` <= n <= 4).

| Label | Description |
| ----- | ----------- |
| `priority::1`  |             |
| `priority::2`  |             |
| `priority::3`  |             |
| `priority::4`  |             |

##### Milestone Naming

Standardized milestone names are important, especially in teams under the same departmetal umbrella. This is one area, however, where a team's context is an overriding factor. When naming milestones, said names should be consistently used, and as milestones are time-bounded, their names should transmit said boundaries.

### Boards: Other Issue Contextual Containers

There are times when we need other points of view when managing our work, and boards provide a tool to craft the necessary filtering to allow us to view issues under these circumstances. Boards dynamically respond to changes on issues. 

#### Recommended Boards

##### Your Board

Individual contributors and managers alike should have a personal board filtered by Assignee, with columns for issue states. For engineers, this should likely be your daily guide to work you have on deck. For managers, this is helpful in assessing an engineer's load when determining issue priorities and assignment.

##### Team Boards: Overall and Milestone

Each team should have a board filtered by their team label with columns for issues states and a board filtered by team label and current milestone.

## Workflows

### Setting up Goals and Objective: Epics

Epics capture ideas, goals and objectives and their corresponding outcomes in a *semantic* container that allow us to scope and break down the work towards achieving a goal. Epics can contain other epics when we are managing large and complex projects that have to broken down in smaller (but still complex) blocks. Epics are not strictly time bound (tho they likely have deadlines associated with them).

### Runtime and Checkpoints: Milestones

Quoting John Doerr on *Measure What Matters*,

> Ideas are easy. Execution is everything.

Workflow management is geared towards providing the framework (tools and workflows) that allows us to execute. Humans operate on time-based cycles, and our visibility horizon gets increasingly diffused as it moves further into the future. Regular checkpoints are necessary to ensure we can plan on relatively short spans of time with a relatively high-level of accuracy. Milestones provide both the short-term horizon spans of time and checkpoints to better track and evaluate progress towards achieving our objectives.

#### Start of Milestone

* Create the new milestone.
* Review previous milestone and ensure there are no issues open left in it.
* Issues must either be closed or migrated to the new milestone.

#### In-Flight Check-ins

Depending on the length of the milestone, do regular check-points. For instance, for a two week milestone, a good checkpoint might be on the Thursday of the first week and on the Wednesday of the second week. If issues are kept up to date, managers can gather the information they need and ensure things are moving at the expected speed. They can also watch out for `unscheduled` work added throughout the milestone and adjust accordingly.

#### End of Milestone and Milestone Retro

All issues in a milestone should be updated with the approprite workfow states.

## Roles

### Individual Contributors

As an individual contributor, it is imperative that you manage your issues appropriately: diligently and timely.

### Managers

TBD







