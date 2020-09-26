---
layout: handbook-page-toc
title: "Secure and Defend UX"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### Overview
We’re designing an experience that enables contributors to commit their most secure work and to defend what they have in production. This is done by merging security into the DevOps process, giving development teams more ownership, commonly referred to as DevSecOps. The experience brings cross-functional stakeholders together to make better, faster, and more security-oriented decisions. We are doing this by focusing the experience on automation, education, empowerment, and shifting security to the left.

**Automation** relates to convention over configuration that helps draw a clear path for the user to produce meaningful results. When it comes to web security, no application will ever be 100% secure. That’s why we are focused on integrating automation into every step of the user’s journey, taking the guesswork out of configuration to open up more time on what’s important: resolving known vulnerabilities and identifying attacks or threats.

**Education** for our users so they understand security basics and are aware of security needs in their applications. We want our users to know where vulnerabilities or threats have been detected, visualize the implications, present resources to understand the problem, and provide the tools to facilitate informed decisions about next steps.

**Empowerment** for all users to resolve security issues is essential as cross-functional departments share ownership of security. Our tools strive for an experience where the developer is responsible and the security team is accountable for the organization's security.

**Shifting left** is taking things like QA and other processes typically found later in the ops cycle and moving them to development. Resulting in security problems being addressed early and more often.

### Customer
Organizations of all sizes benefit from our tools and the experience of bringing teams together. We provide customers value with workflow efficiency, informed team decision-making, lower risk of security breaches, and attaining compliance requirements. We focus on all aspects of the product — starting with the customer experience. When deciding to use our tools, organizations are often considering the following:

* What languages does the tool support?
* What tests do we need to cover?
* What tests does the tool cover?
* Can it be automated?
* How long will setup take?
* What does setup involve?
* How easy is it to use?
* What technologies do you need to use? (ex. Docker, Kubernetes)
* How lightweight is the tool?
* How does it integrate with our tools?
* How does it integrate with GitLab's product?
* What customer support is offered?
* What are the upcoming features? (we are selling contracted services vs monthly)

### Team
* [Justin Mandell](https://gitlab.com/jmandell) - Product Design Manager
* [Tali Lavi](https://gitlab.com/tlavi) - UX Researcher, Secure & Defend
* [Kyle Mann](https://gitlab.com/kmann) - Sr. Product Designer, Secure & Defend
* [Camellia Yang](https://gitlab.com/cam.x) - Sr. Product Designer, Dynamic Analysis & Fuzz Testing, Secure
* [Annabel Dunstone Gray](https://gitlab.com/annabeldunstone) - Product Designer, Dynamic Analysis, Secure
* [Becka Lippert](https://gitlab.com/beckalippert) - Product Designer, Static Analysis, Secure
* [Andy Volpe](https://gitlab.com/andyvolpe) - Sr. Product Designer, Threat Insights, Secure

#### UX pages
* [Secure UX](/handbook/engineering/ux/stage-group-ux-strategy/secure/)
* [Defend UX](/handbook/engineering/ux/stage-group-ux-strategy/defend/) 

### How we work
We follow the [GitLab workflow](/handbook/engineering/workflow/#product-development-timeline) with [additional dates](/handbook/engineering/ux/stage-group-ux-strategy/secure-and-defend/) and actions that directly tie to our work. 

### Team meetings
* Secure and Defend UX (Secure & Defend Design Review) weekly meeting on Wednesdays at 10:00am EST. 
* Product Design and Secure PMs (Secure & Defend UX) bi-weekly on Wednesdays at 11:00am EST
* Product Design does a bi-weekly refinement session on Tuesdays at 10:30am EST

Our weekly meeting is to discuss topics relevant to Secure design, UX, and research. Some example topics could include: 
- Updates on in-flight and planned research
- Updates on design issues
- Issues that might be at risk or have blockers
- Recently discovered insights while conducting researching
- Updates to our UX Scorecards
- Updates on changes to UX workflows and processes
- Updates on pilot initiatives we are working on
- Strategy iterations

Some topics are better suited for a dedicated meeting, and should be created on an as-needed basis:
- Milestone planning and refinement
- Design critiques 
- Research report readouts 
- Syncing on troublesome issues 

##### Labels we use
We use `devops::stage_name` and `UX` labels to indicate issues that need UX effort. We work on user flows that often span multiple categories so we review each of these issues prior to the start of a milestone to determine the design assignee or assignees.

* `UX` + `devops::stage_name`: It is a shared UX effort and the engineering effort has not been determined.
* `UX` + `devops::stage_name`+`Category::name`: There is a DRI for UX (can be shared) and clear engineering collaboration.
* `UX` + `devops::stage_name`+ `UX debt`: Used for follow-up issues when a proposed design was de-scoped or not implemented as planned.  

See our [UX Workflow](/handbook/engineering/ux/ux-department-workflow/#how-we-use-labels) page for more on how we use labels.

##### Problem and solution validation issues 
When working on a `workflow::problem validation` or `workflow:solution validation` issue requiring implementation in the next 2 releases, ensure there is a placeholder implementation issue. This issue must be attached to the epic, have a tentative mileston

#### Planning and refinement
* By month `M-1, 4th` (at least 14 days before milestone `m` begins):
     * PM updates planning boards to propose issues that may be included in the next release (released 22nd of next month).
     * Product Designers hold a UX Planning session to review the issues, make assignments, and discuss capacity. UX proposes additional issues to include in the milestone.
     * Each issue is followed with a discussion (comment) to inform our capacity or request additional information.
* By month `M-1, 13th` (at least 5 days before milestone `m` begins):
     * PM finalizes the Release scope. In-scope issues are marked with milestone `m`; label `deliverable` applied.
     * PM updates the Kickoff document with relevant items to be included.
* By month `M-1, 17th` (at least 1 day before milestone `m` begins):
     * Group Kickoffs calls recorded and uploaded by PM.
* On month `M-1, 18th` (or next business day, milestone `m` begins): Kick off! 📣
     * Company Kickoff call live streamed by PM.
     * Development on milestone `m` begins

##### Understanding capacity
Part of our milestone planning activities include factoring in the amount of effort required for each assigned issue. We use the following scale:   

| Size     | Weight | Description                                                  |
| -------- | ------ | ------------------------------------------------------------ |
| Trivial  | 1      | Mostly small to medium UI changes, smaller UX improvements, without unanswered questions. UX may need to stay involved with the issue but might not have to do work. |
| Small    | 2      | Simple UI or UX change where we understand all of the requirements, but may need to find solutions to known questions/problems. |
| Medium   | 3      | A medium change (lots of UI or UX changes/improvements required). Multiple pages are involved, we're starting to design/redesign small flows. Some unknown questions may arise during the work. |
| Large    | 5      | A complicated change where other team members will need to be involved. Spans across multiple pages, we're working on medium-sized flows. There are significant open questions that need to be answered. |
| Huge     | 8      | A complex change that spans across large flows and may require input from other designers. This is the largest flow design/redesign that we would take on in a single milestone. |
| Gigantic | 13     | A significant change that spans across multiple flows and that would require significant input from others (teams, team members, user feedback) and there are many unknown unknowns. It's unlikely we would commit to this in a milestone, and the preference would be to further clarify requirements and/or break in to smaller issues. |

### Our strategy
The Secure and Defend UX teams are working together to [uncover customers core needs](https://gitlab.com/groups/gitlab-org/-/epics/1611), what our users’ workflows looks like, and defining how we can make our users tasks easier. Our strategy involves the following actions:

* [UX Scorecards and recommendations](/handbook/engineering/ux/ux-scorecards/) (quarterly)
* Internal understanding: stakeholder interviews (annually)
* Iterating on Secure product [foundation's document](https://gitlab.com/gitlab-org/gitlab-design/issues/333) (ongoing)
* Iterating on Defend product [foundation's document](https://gitlab.com/gitlab-org/gitlab-design/issues/547) (ongoing)
* Performing heuristic evaluations on at least 3 competitors, based competitors the 3 user type is using (annually, ongoing)
* We talk to our customer (ongoing)
* We talk to our users (ongoing)
* We outline current user workflows and improve them (upcoming, ongoing)

Additionally, we value the following:
* Testing our features with usefulness and usability studies
* Drinking our own wine and partnering closely with our internal Security and Compliance teams for feedback and feature adoption
* Partnering with our sales and account team to connect directly with customers and learn why customers did (or didn’t) choose our product
* Collaborating with stakeholders on proof of concept discoveries to better understand future consideration
* Collaborating between the Secure and Defend teams to make sure we’re offering a consistent and cohesive security workflow so that our customers can apply reactive findings into proactive measures and make sure their applications are protected throughout the entire application lifecycle 
* Prioritizing issues that are likely to increase our number of active users

The source of truth lives with shipped features, therefore we:
* Make data-driven decisions quickly and thoughtfully
* Optimize to deliver our solutions as soon as possible
* Learn, iterate, test, and repeat

### Follow our work
Our [Secure and Defend UX YouTube channel](https://www.youtube.com/playlist?list=PL05JrBw4t0KrFCe5BgUkzFrZifjforQOz) includes UX Scorecard walkthroughs, UX reviews, group feedback sessions, team meetings, and more.


