---
layout: handbook-page-toc
title: "Handbook Support"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

When contributing to the GitLab Handbook you might run into situations that requires some further support to resolve. The sections below cover common scenarios that team members run into and provides information on how to deal with it.

## How to solve a broken pipeline in a merge request

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/PeopYsoweGU" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

_In the [GitLab Unfiltered](https://www.youtube.com/channel/UCMtZ0sc1HHNtGGWZFDRTh5A) video above, two colleagues share their screens and walk through the process detailed below._

---

If you create a merge request during a period where there is an issue in master causing [pipelines to fail](/blog/2019/09/11/how-to-avoid-broken-master-with-pipelines-for-merge-requests/), you'll notice that failures will continue to occur even if you retry pipeline within the GitLab Web IDE interface.

Once the issue in master is fixed, you can solve this by using terminal to merge the latest version of master into your branch (which you can find in your [merge request](https://docs.gitlab.com/ee/user/project/merge_requests/)).

For those who primarily use Web IDE to interface with GitLab, it can feel foreign to engage [locally](/handbook/marketing/product-marketing/getting-started/102/). Before diving in deeper, be sure to read our [_GitLab 101 – a primer for the non-technical_](/blog/2019/08/02/gitlab-for-the-non-technical/) blog post.

The process is fairly straightforward once you have completed the [necessary steps listed in the GitLab Handbook to edit locally](/handbook/git-page-update/).

Once you are properly equipped to edit locally, open a [terminal window](/handbook/marketing/product-marketing/getting-started/102/#a-little-terminal-time) and execute the following.

1. Navigate to the appropriate project. If you've cloned the project to your root directory, try `cd www-gitlab-com`
1. `git checkout master`
1. `git pull` (This brings in the most recent changes from master to your local machine.)
1. `git checkout MYBRANCH` (Replace `MYBRANCH` with your branch from the merge request. This is easily copied by clicking the **Copy Branch Name** icon to the right of **Request to merge** at the top of your merge request page.)
1. `git merge master` (This takes the changes from master and merges them into your local `MYBRANCH` branch.)
1. `:q` (Entering `:q` followed by a **Return keystroke**  quits vim which is the editor your terminal opened when adding the stock commit message to the merge.)
1. `git push` (This takes local machine files and pushes to the cloud.)

Once this has been executed, you'll see new commits added to your merge request, and the pipeline will automatically begin to re-run. If completed correctly, the pipeline will pass now that the latest master was merged into your branch.

If you are a GitLab team member and you get stuck, please ask for help in the `#mr-buddies` Slack channel.

### Debugging a failed pipeline in the GitLab handbook

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/WlgH-6cX1k8" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

_In the [GitLab Unfiltered](https://www.youtube.com/channel/UCMtZ0sc1HHNtGGWZFDRTh5A) video above, Jean shares a quick overview of how to go about identifying why a pipeline might be failing for a merge request to the GitLab handbook._

### Why is my pipeline failing?

If you've made a merge request, only to see that your pipeline has failed, a troubleshooting process begins.

You can learn more about why pipelines fail, what failures mean, and how to resolve conflicts by viewing this [explainer video](https://youtu.be/Qg0ICfs_Noo) hosted on GitLab Unfiltered.

### Where do I report handbook issues and request help?

For those inside the GitLab organization, you can request help on individual merge requests via [Merge Request Buddies](/handbook/people-group/general-onboarding/mr-buddies/) in the `#mr-buddies` Slack channel.

If you suspect a systemic issue, inquire in the `#handbook-escalation` Slack channel, and check to see if others are reporting similar errors in `#is-this-known`. For more information refer to the [Handbook On-Call page](/handbook/about/on-call/).

The `#handbook-escalation` Slack channel is used for monitoring and responding to infrastructure and configuration related build issues with the `www-gitlab-com` project master branch. This is an excellent first stop to see if there is an ongoing issue impacting your pipeline.

The [Static Site Editor Team](/handbook/engineering/development/dev/create-static-site-editor/) is responsible for enhancing the editing experience for static sites inside of GitLab, including the handbook.

General GitLab handbook discussion occurs in the `#handbook` channel, while an automated feed of merged handbook updates can be found in the `#handbook-updates` channel.

## Resolving linting errors

To the ensure consistency, quality and correctness of the GitLab Handbook we use various linting jobs that run as part of the pipeline. These jobs check that everything is as it should be, and if they detect something is wrong will cause the pipeline to fail.

### Handbook Links and Anchors

There is a special linter that validates links and anchors across the handbook. If your change accidentally breaks a link, then the pipeline job will fail with a similar error message.

![Link linter error](/images/handbook/link-linter-error.png)

1. It is a path to the file where the broken link was detected.
    (filepath - `sites/handbook/source/handbook/total-rewards/benefits/general-and-entity-benefits/pty-benefits-australia/index.html.md`, line number: 87)
1. It is an error message. An anchor `expense-reimbursement` is defined in the file path from step 1 but does not exist in the file path from step 3.
1. It is a path where the header `Expense Reimbursement` needs to be defined. (file path - `sites/handbook/source/handbook/spending-company-money/index.html.md`)

**How to fix the problem**

Double-check that header `Expense Reimbursement` exists in `sites/handbook/source/handbook/spending-company-money/index.html.md`.

If it was moved or renamed, then update the link with the anchor to point to the correct location.
