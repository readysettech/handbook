---
layout: handbook-page-toc
title: "Distribution Team Merge Request Handling"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Introduction

Merge Requests are the responsibility of all Distribution Engineers. For the most part, we follow the [engineering process for code review](/handbook/engineering/workflow/code-review/).

## Workflow

1. Author opens a merge request in a project.
1. When ready for review, the Author applies the "workflow::ready for review" label.
1. When they are able to work on the merge request, a Reviewer assigns it to themselves, and adds the "workflow::in review" label.
1. The Reviewer works with the Author to get the merge request to a state where they approve it. At this stage, it is expected that the Author and the Reviewer will assign the merge request back and forth as described in [review iteration](#review-iteration).
1. Once approved, the Reviewer assigns the merge request to a Maintainer for final review/merge. If the Maintainer has any comments, then they work with the Author to clarify. It is the responsibility of the Maintainer to find another Maintainer to look at a merge request that is assigned to them if they are unable.

**NOTE**: If you are working on a merge request that requires a response quicker than the [First-response SLO](/handbook/engineering/workflow/code-review/#first-response-slo), please `@` mention the `gitlab-org/distribution` group in order to alert the Distribution team. The team will exercise best effort in handling these requests.

## Reviewers

By default, every Distribution Engineer team member who is not a Maintainer on a project should consider themselves a Reviewer. You are encouraged to spend some of your time looking at Merge Requests in any of our [projects](/handbook/engineering/development/enablement/distribution/#projects) that are either unassigned, or have the "workflow::ready for review" label.

Reviewers are responsible for working with contributors to ensure that changes meet our standards, before approving and passing them on to a Maintainer for final review and merge. Reviewers should confirm that the Merge Request addresses the problem the linked Issue describes. Reviewers are also responsible for verifying that all applicable Merge Request checklist items have been completed. In situations where a checklist item is not applicable, Reviewers should verify that the item is indeed not necessary. When you encounter a situation as Reviewer where you are unsure whether something meets our standards, ping a Maintainer directly within the Merge Request with the question.

Additionally, in the spirit of "everyone can contribute", anyone who is interested is encouraged to be a Reviewer. There should be no barrier preventing anyone from reviewing available merge requests. We encourage any interested party to participate.

Anyone who plans on actively participating in the Reviewer process is encouraged to [update their entry on the team page](/handbook/git-page-update/#11-add-yourself-to-the-team-page).

## Maintainers

Project Maintainers are encouraged to ensure that Reviewers, and in particular Reviewers who have designated themselves [Trainee Maintainers](/handbook/engineering/workflow/code-review/#trainee-maintainer), look at a Merge Request before they spend time on it. There are times when it makes sense for a Maintainer to not wait for a reviewer, so judgment should be used here. For example, we do need to keep the [First-response SLO](/handbook/engineering/workflow/code-review/#first-response-slo) in mind. If an MR is in danger of missing that deadline, a Maintainer should not hesitate to respond.

## Assigning Merge Requests

To help achieve all of this, we should urge contributors to **not** assign merge requests to an individual when looking for initial review, unless there is a specific reason someone should look at a merge request. Rather, the merge request should have the "workflow::ready for review" label applied, and a Reviewer will assign it to themselves when they are beginning to look into it. When looking for a merge request to work on, consider the [First-response SLO](/handbook/engineering/workflow/code-review/#first-response-slo). Anything in danger of breaching that deadline should be looked at first.

If a merge request is assigned directly to you as a Maintainer without prior review, you are encouraged to assign it to an available Reviewer. If a merge request is assigned directly to you as a Reviewer, use your judgment. If you will not be able to work on it soon, try and find another Reviewer to take a look.

## Review iteration

Once the merge request is in review, the "workflow::in review" label should remain on the merge request as the Reviewer/Maintainer and Author iterate through feedback.

When the merge request is ready to be handed back for changes or further review, ensure that the individual responsible for the next step is assigned and signal the handoff with a fresh comment mentioning the individual in the Merge Request.

**NOTE**: By default, Authors should handoff to the Reviewer/Maintainer who previously reviewed the merge request. If that individual is listed as away in their status for longer than two days, then please `@` mention the `gitlab-org/distribution` group in order to alert the Distribution team for a new reviewer.


## References

[Distribution team projects](/handbook/engineering/development/enablement/distribution/#projects) - The full list of projects the Distribution team maintains
[Engineering Projects](/handbook/engineering/projects/) - The full list of supported GitLab projects. Clicking on the project name will bring you to the list of Maintainers and Reviewers for each project.
