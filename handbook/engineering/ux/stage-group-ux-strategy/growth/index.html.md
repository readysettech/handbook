---
layout: handbook-page-toc
title: Growth UX Team
---
## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Overview

The Growth area is made up of Fulfillment, Telemetry and four Growth groups which focus on improving specific metrics. We don't have our own product. Instead, we make the experience of paying for GitLab and managing licenses as easy as can be. We also look for strategies to help customers discover the value of the product, thereby increasing the number of customers and users. GitLab believes that **everyone can contribute**, and this is central to our strategy.

- [Fulfillment Product Direction](https://about.gitlab.com/direction/fulfillment/)
- [Acquisition Product Direction](https://about.gitlab.com/direction/acquisition/)
- [Conversion Product Direction](https://about.gitlab.com/direction/conversion/)
- [Expansion Product Direction](https://about.gitlab.com/direction/expansion/)
- [Retention Product Direction](https://about.gitlab.com/direction/retention/)
- [Growth Engineering Pages](/handbook/engineering/development/growth/)

## UX team members

The Growth UX team aligns closely to user experience flows rather than with PMs. Designers are not “assigned” to a particular PM, rather they are the first point of contact on UX related to that flow, with flexibility built in to even out the workload and ensure UX experts work on things they are subject matter experts on. This will allow us to cover all the areas of Growth, including fulfillment. It allows designers to own one area but to also have expert knowledge of other areas of Growth's responsibilities.
We also have designated leads for large experience areas, as noted below.

- [Jacki Bauer](/company/team/#jackib) ([Jacki's ReadMe](https://gitlab.com/jackib/jacki-bauer/blob/master/README.md)) - UX Manager
- [Tim Noah](/company/team/#timnoah) - Senior Product Designer, Renewals, True-ups and Internal Tools (works most on Retention). Lead for Account Management and Internal Tools.
- [Emily Sybrant](/company/team/#esybrant) - Product Designer, Sign-up, Purchase and Account Management (works most on Acquisition)
- [Matej Latin](/company/team/#matejlatin) ([Matej's ReadMe](https://gitlab.com/matejlatin/focus/blob/master/README.md)) - Senior Product Designer, Upgrades and Onboarding (works most on Expansion). Lead for Onboarding.
- [Kevin Comoli](/company/team/#kcomoli) - Product Designer, Trialing GitLab, Free to paid upgrades and Onboarding (works most on Conversion)
- [Jeff Crow](/company/team/#jeffcrow) - Senior UX Researcher, Growth

Not sure which designer to talk to about a particular issue? Create your issue and tag it with UX. You can also reach out to the Growth Slack channel (#s_growth) or mention the product designers in issues @gitlab-com/gitlab-ux/growth-ux.

## How We Work

We follow the [Product Designer workflows](handbook/engineering/ux/ux-designer/) and [UX Researcher workflows](/handbook/engineering/ux/ux-research/) described in the [UX section](handbook/engineering/ux/) of the handbook. In addition:

- we have issue boards so we can see what everyone is up to.
    - [by assignee](https://gitlab.com/groups/gitlab-org/-/boards/1254597?label_name%5B%5D=UX&label_name%5B%5D=devops%3A%3Agrowth)
    - [by group](https://gitlab.com/groups/gitlab-org/-/boards/1334665?&label_name%5B%5D=UX&label_name%5B%5D=devops%3A%3Agrowth)
    - [by workflow](https://gitlab.com/groups/gitlab-org/-/boards/1346572)
- we **label** our issues with UX, devops::growth and group::.
- we use the [workflow labels](https://gitlab.com/groups/gitlab-org/-/labels?utf8=%E2%9C%93&subscribed=&search=workflow%3A%3A) for regular issues and [experiment workflow labels](/handbook/engineering/development/growth/#experiment-workflow-labels) for experiment issues.
- we use **milestones** to aid in planning and prioritizing the four growth groups of Acquisition, Conversion, Expansion and Retention.
    - PMs provide an [ICE score for experiments](https://docs.google.com/spreadsheets/d/1yvLW0qM0FpvcBzvtnyFrH6O5kAlV1TEFn0TB8KM-Y1s/edit#gid=0) and by using [priority labels](https://docs.gitlab.com/ee/development/contributing/issue_workflow.html#priority-labels) for other issues.
    - The Product Designer applies the milestone in which they plan to deliver the work (1-2 milestones in advance, or backlog for items that are several months out. For example, if an issue is not doable for a designer in the current milestone, they can add the next milestone to the issue, which will communicate to the PM when the work will be delivered.
    - If the PM has any concern about the planned milestone, they will discuss trade-offs with the Product Designer and other Growth PMs.

#### UX Capacity Planning

This is a pilot process we're kicking off in 12.10. The UX team will start weighting UX issues in order to better estimate capacity, realistically break down our work, and give PMs a little insight into how much work we can take on in a milestone. We aim for [velocity over predictibility](/handbook/engineering/#velocity-over-predictability). This means that we don't need to be accurate, we just need to get better. This paragraph has a [useful explanation of estimation](/handbook/engineering/development/growth/acquisition-conversion-be-telemetry/#estimation) that captures the spirit of what we want to accomplish with this pilot.

##### UX Weight Definitions

| Weight | Design Tasks | User Research Tasks |
| ------ | ------------ | ------------------- |
| 1 | Mostly small UI changes leading to small incremental UX improvements. No users’ workflow involved in these changes. Requirements are clear and there are no unanswered questions. _For example: A copy experiment, changing a button styling..._. | Synthesizing previous research findings and generating recommendations based on them. |
| 2 | Simple UI or UX change where we understand all of the requirements but may need to find solutions to known questions/problems. These changes should blend in with an actual user workflow. <i>For example: [Simplify Sign in / Register process the in trial flow](https://gitlab.com/gitlab-org/growth/product/-/issues/1471)</i>. | Running a first click test or other type of unmoderated research study |
| 3 | A well-understood change but the scope of work is bigger. Several pages are involved and/or we're starting to design/redesign small flows or connect existing flows between each other. Designers may conduct extensive background research (previous issues, support tickets, review past user research, review analytics, etc). Some unknown questions may arise during the work. <i>For example: [Update the customer portal checkout page to allow subscription and billing information input](https://gitlab.com/gitlab-org/growth/team-tasks/-/issues/96), [Experiment with adding a contact sales option in app](https://gitlab.com/gitlab-org/gitlab/-/issues/197235)</i>. | A moderated, narrowly scoped research study with specific questions to answer, such as a usability review of a single page |
| 5 | A complex change where input from group members is needed as early as possible. Spans across multiple pages, and we're working on medium-sized flows that potentially connect with another area of the product There are significant open questions that need to be answered. The product designer may need to do some research on their own or in collaboration with a researcher, but this isn't always the case. Possible research activities might be to find and/or validate a Job To Be Done, conduct user testing or card-sorting, or do a survey. <i>For example: UX Scorecard, [How can we improve the dismiss action in upgrade moments](https://gitlab.com/gitlab-org/gitlab/-/issues/213344)</i>. | A research study evaluating the usability of an end-to-end flow or multiple related features, or a usability study with a minor exploratory component |
| 8 | Complicated changes introducing a new user flow that connects with other large flows and may require input from other designers, product managers, or engineers from the same or another stage group. This change would most likely be added to our [Log of major changes](/handbook/engineering/ux/stage-group-ux-strategy/growth/#log-of-major-changes). This is the largest flow design/redesign that we would take on in a single milestone. This requires research where the designer may or may not be working with a researcher to plan and conduct exploratory interviews or user testing sessions. <i>For example: [Onboard new signs up through an onboarding issue board](https://gitlab.com/gitlab-org/growth/product/-/issues/107)</i>. | An exploratory study investigating broad-based behaviors related to a single stage, including one or more distinct user groups |
| 13 | Highly significant changes impacting multiple user flows, a large new feature, and/or a complete redesign. This issue could significantly impact product strategy and would require critical input from others (the wider GitLab community, e-group, customers), and there are many unknowns. This necessitates research where the designer could team up with a researcher and other designers to gather input data, plan and conduct exploratory interviews, lead user testing sessions… These changes should be added to our [Log of major changes](/handbook/engineering/ux/stage-group-ux-strategy/growth/#log-of-major-changes). It's unlikely we would commit to complete this issue in a milestone, and the preference would be to further clarify requirements and/or break it into smaller issues planned in several milestones. <i>For example: [An improved free trial sign-up experience for GitLab.com SaaS users](https://gitlab.com/groups/gitlab-org/-/epics/377)</i>. | An exploratory study investigating broad-based behaviors across multiple stages and multiple types of users, potentially involving team members from the different stages. |

##### Process

There is a limit to our product, which is that issues have a single field dedicated to issue weight, and this is usually used by the engineering teams. To pilot issue weights, teams will need to work around this limit for now, and look for opportunities to enhance the product.

**One way to do issues weights is to use Parent-Child issue labels**. For teams using this method, follow these suggested steps, but feel free to adapt to match your teams workflow:

- First, break the work down into one or more UX parts. For example, your issue structure might look something like this:
    - A parent issue will use label `link::parent` and contain high level discussion and links to child issues. This should also be the SSOT for the design work.
    - The product manager and product designer can create child issues based on their understanding of the work. Child issues will use the label `link::child`. So for example, you can have a child issue for the UX work (`workflow::problem validation` and `workflow::design`), or you can break these down even further for a large project. You might also have a separate linked issue for UX Research work, as per the process by which the UX Research team works.
- Label child issues with `UX` or `Engineering` but not both. This will make sure there is no confusion as to what the weight is for.

**For teams that use epics and don't want to use Parent-Child issues labels**, you can proceed as follows. Again, as this is a pilot, these steps are a suggestion but can be adapted as we go and we can make updates here as we refine the process.

- Label the issue for UX work with `UX` and assess the issue weight. Issues larger than an **8** should be broken down further.
- When the UX work is ready to be transitioned into Engineering, apply the workflow lable `workflow::planning breakdown`.
- The Engineering team can create a new issue or issues with the broken down work, and apply issue weights. These issues should be labeled `Engineering`.
- Label issues with `UX` or `Engineering` but not both. This will make sure there is no confusion as to what the weight is for.

**In terms of milestone planning, the UX team is following these guidelines:**

- The UX team will estimate the capacity of a designer to work on issues as part of the milestone, vs their other responsibilities such as visual reviews and Pajamas work.
- For the first milestone we will meet as a team and use the definitions to apply weights to issues as best we can. At first we will be guessing a bit and that's OK. When we get better at this, we can do it async.
    - A weight of 8 or 13 indicates that we should break down the issue further. We can break an issue down into a problem validation issue, a user workflow issue, a design issue, and/or a solution validation issue, for example. Or, we could break up the work into smaller pieces as in a part of a feature, or a part of a workflow. There's no one right way to do this, so let's discuss and learn as we go.
- If a new issue is added during the milestone, we will need to add a weight to it.
- After the milestone, we will compare what we planned with what we actually delivered and the number of person days we had to get the work done. Then we will use that as a baseline for the next milestone.
- The UX team will copy the capacity planning template below into the respective groups planning issue to track capacity.

> Milestone Capacity:
> 
> 
> - **Total weights completed last milestone:** XX
> - **Average capacity (last 3 months completed):** XX
> 
> 
> Current Milestone:
> 
> 
> - **Estimated capacity:** XX (use the average capacity from the previous milestones and include a brief explanation if it's higher or lower)
> - **Total current weights:** XX
> - **Percentage of time:** [write percent of your time you will dedicate to this group and other groups, for example 50% retention, 50% fulfillment, or 75% capacity due to childcare / time off]

**We do not need to apply a weight to**

- Really small issues, like a bug or other issue where UX is consulted. This is where the weight would be even less than a 1. These issues don't need to be split up.

**We should apply weights to**

- Most UX issues
- UX Scorecards
- Pajamas related issues

#### Sharing Designers Across Stage Groups

To start with, we follow [GitLab internal communication](/handbook/communication/internal-communications) guidelines. In addition the following tips will make it easier to collaborate with Product Designers who span multiple groups:

- Overcommunication is better than undercommunication, especially in this case.
    - Communicate priorities clearly and transparently. Communicate UX priorities via priority labels (ie ~"milestone::p1"), due dates and issue boards instead of in 1:1 docs or Slack channels. The PMs from both covered stage groups, all the product designers and the UX manager need to be able to access those priorities.
    - When you need a designers immediate attention, don't hesitate to ping them in more than one channel (GitLab + Slack + email) and/or more than one time. You might feel like you are being annoying, but remember that the designer has to juggle a couple task lists with separate priorities. It can be easy to miss something.
- Include the UX Manager more than you normally would, because the UX Manager can help balance priorities or address situations where one designer has an overload of work to do.
- On our monthly planning issues, each designer should indicate a couple of extra items:
    - An estimate of how their time will be split (e.g. 40% Fulfillment, 50% Retention, 10% Design System)
    - Links to the high priority or time consuming issues from other stage groups. A link to the other planning issue is fine too, just so it's easy for the UX Manager and Product Managers to navigate to this information.
- Minimize meetings: Designers who span stage groups have 2-3 times more meetings than a designer on 1 stage group, so their teams can help them by ensuring we follow GitLab's async meeting practices to allow them to miss those meetings without negative consequences.

#### Communicating Due Dates

The order in which we approach our work can be complex, as we have priorities and severities, milestone plans, and the product design team has their own [guidance on selecting the next thing to work on](handbook/engineering/ux/ux-designer/#priority-for-ux-issues). Additionally, some UX issues need to be delivered earlier in the milestone than others. To help with communication you can use the Due Date field. As a PM, if you choose this route, please do the following:

- Continue using priority labels and issue weights. The due date isn't a substitution for these.
- Add an issue comment and suggest the due date. Mention the product designer.
- The product designer should respond within one day as to whether or not the due date is doable. If the due date works, the product designer will add the Due Date. If it doesn't work, they will offer trade-offs for the PM to consider.
- If the due date changes, comment in the issue and @mention people who will be impacted. Note that Due Date changes do not result in a notification.
- When changes are communicated via Slack or in a 1:1, update the issue so everyone else can see the change. Consider sharing in sync meetings.

#### Visual Reviews of MRs

The engineering team applies the `UX` label to any MR that introduces a visual, interaction or flow change. These MRs can be related to new issues, bugs, followups, or any type of MR. If the engineer isn't sure whether the MR needs UX, they should consult the designer who worked on the related issue, and/or the designer assigned to that stage group, or the UX manager.

Visual reviews are required for any MR with the `UX` label. When the MR is in `workflow::In review`, the engineer assigns the MR to the designer for a visual review. This can happen in parallel with the maintainer review, but designers should prioritize these reviews to complete them as quickly as possible.

There are times when it isn't possible or practical for a designer to complete their visual review via Review Apps or GDK. At these times the designer and engineer should coordinate a demo.

## Themes and Focus Areas

[Q3 Growth UX OKR Issue](https://gitlab.com/gitlab-org/gitlab-design/-/issues/1304)

While Growth UX work focuses on designing experiments that change user behavior, we also work on improving UX overall across a variety of themes.

For Growth, these themes are:

- [Easy to Trial GitLab](https://gitlab.com/groups/gitlab-org/-/issues?label_name%5B%5D=UX+Team%3A++Easy+to+Trial+GitLab+Theme)
- [Feature Discoverability](https://gitlab.com/groups/gitlab-org/-/issues?label_name%5B%5D=UX+Team%3A++Feature+Discoverability+Theme)
- [Onboarding New Users](https://gitlab.com/groups/gitlab-org/-/issues?label_name%5B%5D=UX+Team%3A+Easy+Onboarding+Theme)
- [Easy Upgrade Flows](https://gitlab.com/groups/gitlab-org/-/issues?label_name%5B%5D=UX+Team%3A+Easy+Upgrades+Theme)

For Fulfillment, these themes are:

- [Eliminate Multiple Logins](https://gitlab.com/groups/gitlab-org/-/issues?label_name%5B%5D=UX+Team%3A++Eliminate+Multiple+Login+Theme)
- [Easy to Buy GitLab](https://gitlab.com/gitlab-org/gitlab/-/issues?scope=all&utf8=%E2%9C%93&state=all&label_name%5B%5D=UX%20Team%3A%20Easy%20to%20Buy%20Theme)
- [Implement Pajamas Design System](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=all&label_name%5B%5D=UX%20Team%3A%20Implement%20Pajamas%20Theme)

Applying theme based labels to UX issues allow us to track our work more holistically against big areas we've identified for UX improvement.

### Customer Journey/Process for Fulfillment/Customer Transactions

When working through transactional issues related to sign-up, trials and upgrades it helps to break down the task into pieces. This way of working through issues enables product designers to document the beginning and end of a user journey in an easily digestible way for everyone. It's based very loosely on a talk from Jared Spool regarding "Content and Design".

- Entry Point(s): The initial touch points of user interactions. (i.e. A Page, CTA or Form etc)
- Decision: Giving users the ability to decide on Products, Options or Packages.
- Confirmation: Summary of a successful or unsuccessful purchase.

These steps won't always be needed and won't always be linear. For instance, an Entry Point may also be a point at which a user selects a Product.

## UX Scorecards

All of the planned, in progress and completed UX Scorecards for Growth can be found in this [epic](https://gitlab.com/groups/gitlab-org/-/epics/2015).
For more information, read about [UX Scorecards](/handbook/engineering/ux/ux-scorecards/).

##### Scorecard: Renew a GitLab Plan

- Job Description: _TBD: When (situation), I want to (motivation), so I can (expected outcome)._
- UX scorecard issue (with walkthrough and video): [113](https://gitlab.com/gitlab-org/growth/product/issues/114) (WIP)
- UX scorecard Score: TBD
- Recommendations Epic: TBD

##### Scorecard: Start a GitLab trial

- Job Description: _When creating a new account, I want to start a trial, So I can test GitLab.com Gold features._
- UX scorecard Epic (with walkthrough and video): [1332](https://gitlab.com/groups/gitlab-org/-/epics/1332)
- UX scorecard Issue: [1355](https://gitlab.com/groups/gitlab-org/-/epics/1355)
- UX scorecard Score: D- (Q2, 2019)
- Recommendations: [1356](https://gitlab.com/groups/gitlab-org/-/epics/1356)

##### Scorecard: User onboarding

- Job description: _When I sign up for a GitLab account, I want to see what are its main features and benefits for my role/team, so I can find out if it’s potentially valuable to our company._
- UX scorecard issue (with walkthrough and video): [170](https://gitlab.com/gitlab-org/growth/product/issues/170)
- UX scorecard Score: C- (Q4, 2019)
- [Recommendations Epic](https://gitlab.com/groups/gitlab-org/growth/-/epics/4)

##### Scorecard: Upgrade a GitLab Plan

- Job Description: _When I realise my team needs a feature from a higher tier than our current paid one, I want to quickly and easily upgrade (to that tier), so that they can benefit from it as soon as possible._
- UX scorecard issue (with walkthrough and video): [113](https://gitlab.com/gitlab-org/growth/product/issues/113)
- UX scorecard Score: C- (Q4, 2019)
- [Recommendations Epic](https://gitlab.com/groups/gitlab-org/growth/-/epics/22)

##### Scorecard: Buy add-on CI minutes

- Job Description: _When I realise that we're running out of CI minutes, I want to quickly and easily buy more, so that our team can continue building and delivering software uninterrupted._
- UX scorecard issue (with walkthrough and video): [531](https://gitlab.com/gitlab-org/gitlab-design/issues/531)
- UX scorecard Score: C (Q4, 2019)
- [Recommendations Epic](https://gitlab.com/groups/gitlab-org/growth/-/epics/26)

##### Scorecard: Upgrade a GitLab.com subscription tier

- Job Description: _When I realise my team needs a feature from a higher plan than our current paid one, I want to quickly and easily upgrade (to that plan), so that they can benefit from it as soon as possible._
- UX scorecard issue (with walkthrough and video): [947](https://gitlab.com/gitlab-org/gitlab-design/-/issues/947)
- UX scorecard Score: C (Q1, 2020)
- [Recommendations Epic](https://gitlab.com/groups/gitlab-org/growth/-/epics/32)

## Log of major changes

This is a log of major changes introduced by the Growth UX team as part of their work with the [Growth subgroups](/handbook/engineering/development/growth/). It serves as an easy way to track down when and why a major change to a user experience was introduced.

We define "major changes" as:

- Major layout/IA changes on a single screen
- User experience changes across multiple screens (flow changes)
- Increasing/decreasing the number of interactions it takes to complete a task
- Changing the content of something at a critical step for the users (a banner warning for example)
- Changing when and where something that is triggered by the system happens (when and where a banner shows up and what triggers it)

### Introduced the new, simpler free trial signup flow

Feb 18, 2020, [Epic](https://gitlab.com/groups/gitlab-org/-/epics/377) - _Released in 12.4_

Last year we introduced a simpler free trial sign up in which a user could complete the process by interacting with one app only. Before, they had to create a separate account in the Customer Portal app which often led to confusion.

### Provide more context and guidance for true-ups in the renewal flow

Jan 30, 2020 - [Issue](https://gitlab.com/gitlab-org/growth/engineering/issues/40) - _MVC expected in 12.8_

Users didn’t know what number to put into the _Users over license_ field in the renewal flow which resulted in new licenses that threw errors. They also didn’t know what number to put into the _Users_ field so we renamed it so it aligns with the data and labels in the Admin Overview. The MVC will be shipped without the illustrations but is still considered a major improvement. This change as a whole is an intermediate step before we move towards automatically collecting the data.

### Changed the appearance, content and behavior of renewal and auto-renewal banners

Jan 30, 2020 - [Issue 1](https://gitlab.com/gitlab-org/growth/product/issues/102), [Issue 2](https://gitlab.com/gitlab-org/growth/product/issues/143) - _Expected to be delivered in 12.8_

Existing banners were confusing the users because they lacked contextual information. Auto-renewal banners, for example, didn’t make it clear that the subscription will automatically renew. Banners were also non-dismissable and shown to all users instead of just the instance admins. This change introduced a new appearance, new behaviour (who they’re shown to and when) and more contextual content.
<!-- Template
### Short, descriptive title for the change

Timestamp (MMM DD, YYYY) - [Issue](link_to_issue) - *When was it delivered (milestone)*

Short description of the change and why it was made. 
-->