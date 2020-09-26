---
layout: handbook-page-toc
title: "Research Insights"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Research Insights
Research insights are the collective findings and learnings that come from a research study.  

At GitLab, we measure the impact of our research by:  

* Distinguishing an insight as “actionable” or "informative"
* Making sure each actionable insight has a clear recommendation or action associated with it
* Tracking the completion of actionable insights


#### Informative insights
Informative insights help us learn about something or someone and don’t result in immediate action. Instead, these insights help build knowledge about our users, industry, competitors, and so on. For example:

* Most developers who took part in the survey were first introduced to GitLab while they were in school.
* Developers use about three other applications in addition to GitLab as part of their jobs.

When documenting informative insights, no special actions or processes need to be followed. These simply get documented into Dovetail, per the [standard process](/handbook/engineering/ux/ux-research-training/documenting-research-findings/).


#### Actionable insights
Actionable insights always have a follow-up action that needs to take place as a result of the research observation or data, and a clear recommendation or action associated with it. An actionable insight both defines the insight and clearly calls out the next step. For example:

> Users weren't able to submit a merge request in the proposed design because they couldn't find the “Submit” button. They expected it to be located at the top of the page. Action: Iterate on the design to relocate the 'Submit' button to the top of the page and retest (link to Issue # XYZ).

> IT Admins want a way to view all of their teams' activity over time, in 15 min increments. IT Admins are being asked to report on this information as part of a new company policy. Action: Explore the feasibility of such a request (link to Issue # ABC).


### How to document actionable insights
Actionable insights need to be handled differently than informative insights. Actionable insights are tracked over time and will include follow-up, so document actionable insights in Dovetail and in GitLab as unique Issues. 

When you document an actionable insight, its three main components are:

1. The insight itself: often the problem, finding, or observation.
1. The “why”: supporting evidence that supports the insight. Often, it’s describing why the problem is happening, or more details behind the finding or observation. 
1. The action: the next step or action that needs to take place as a result of the research. The action should be clearly defined, achievable, and directly tied back to the insight.  

Tips for writing an actionable insight:
* Avoid using words like: consider, possibly, maybe, suggest, etc. People can interpret these actions as optional. 
* Instead, use directive terminology, such as: conduct, explore, redesign, etc. These words contribute to a clear action that needs to be taken as a next step.

To document actionable insights:

* **Step 1:** In Dovetail, preface the actionable insight's title with 'ACTIONABLE:' and clearly describe the next action that needs to be taken.
* **Step 2:** Create a unique issue in [GitLab.com](https://gitlab.com/gitlab-org/gitlab/-/issues/new) using the 'actionable_insight' issue template, which already has the `Actionable Insight` label to keep track of the progress being made regarding the next step(s). To streamline this process, add a link to the Dovetail insight in the GitLab issue, rather than typing out all the details again. (If you want to include details, you certainly can.)
* **Step 3:** Using the related issue feature, link these Actionable Insight issues back to the original Research Issue in the GitLab UX Research project.

#### Who creates and manages actionable insights?
Actionable insights are created and managed by the person closest to the research, which is typically the Product Manager, Product Designer, or UX Researcher.
However, it’s ultimately up to the team to decide who manages actionable insights.

#### How to manage actionable insights

All discussions and decisions made about the actionable insight must be documented within the issue, because these issues are tracked as performance indicators. As we track actionable insights over time, it’s important to understand what kinds of decisions we’re making based on user research.

When closing an actionable insight issue, it’s important to document why it was closed and whether the original action was acted upon.

In some cases, no action will be taken for a number of reasons, such as low priority, too large of an effort, not technically feasible, and so on. Regardless of the reason, document the decisions in the issue when closing it.

#### To what kinds of validation research do actionable insights apply?

Both Problem Validation and Solution Validation need to follow the actionable insights documentation process if actionable insights are discovered. For example:

* **Problem Validation:** If there are insights that result in additional research, a newly identified target for next steps, or an identified problem to address, those are actionable insights.
* **Solution Validation:** If there are insights that uncover a usability issue, a pain point users may experience, or a design issue, those are actionable insights.

The above examples have one thing in common regardless of the kind of research: the insight is actionable, and therefore, must be documented as such.

Additionally, UX Scorecard testing can yield actionable insights. Since UX Scorecard testing is an expert review and/or heuristic evaluation, creating Dovetail insights may not be applicable. Instead, be sure to document the details in the GitLab issue using the actionable insight template in [GitLab.com](https://gitlab.com/gitlab-org/gitlab/-/issues/new).


### Why we track actionable insights

Actionable insights are tracked at GitLab for:

* **Accountability:** If there’s something that needs to be done as a result of conducting research, it should be done. This process helps prevent those actionable insights from getting lost, dismissed, or taking too long to be acted upon.
* **Measuring research impact:** Presently, it’s difficult to accurately measure the impact of a research project on the product. Tracking actionable insights allows us to refer back to a particular research project, see what actions were identified as a result of the research findings, and determine what action was taken within the product since those actions were identified.

The proposed data that will be tracked and possibly measured in the future:

* Percentage of studies using the `Actionable Insight` label
   * Total percentage of studies resulting in using the `Actionable Insight` label.
   * Broken down by Problem Validation and Solution Validation
   * (Sisense chart)
* Number of total actionable insights
   * Total number of Insights with the `Actionable Insight` label, both closed and open, across the total number of research studies conducted
   * Broken down by Problem Validation and Solution Validation, if possible
   * (Sisense chart)
* Number of total actionable insights currently open, no activity (>1 month of no activity)
   * Total number of actionable insights that have not seen activity in at least a month.  These actionable insights will be followed up to understand why there hasn’t been activity.
   * (Sisense chart)
* Number of total of actionable insights currently open, being addressed (activity <1 month ago)
   * Total number of actionable insights that have seen activity within the past month.  It’s implied that these are actively being addressed in some way and not discarded.
   * (Sisense chart)
* Number of total of actionable insights closed, reason: addressed action
   * Total number of actionable insights that have been closed because the action called out in the issue was addressed.  
   * (Sisense chart)
* Number of total of actionable insights closed, reason: not addressing w/ reason
   * Total number of actionable insights that have been closed and not addressed, but there’s a reason associated with it.  
   * (Sisense chart)
Over time, once there's enough data, we might be able to slice this data at the stage/group level to help us understand what is (or isn't) working well. Based on what we learn, we’ll iterate on the approach.


