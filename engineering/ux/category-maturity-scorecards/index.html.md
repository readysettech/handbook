---
layout: handbook-page-toc
title: "Category Maturity Scorecards"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Intro and Goal

The Category Maturity (CM) Scorecard is a [Summative Evaluation](https://www.nngroup.com/articles/formative-vs-summative-evaluations/) that takes into account the entire experience as defined by a Job to be Done (JTBD), instead of individual improvement(s), which are often measured through Usability Testing (i.e. Solution Validation). This specialized process provides data to help us grade the maturity of our product.

The goal of this process is to produce data as objectively as possible given time and resource constraints. For this reason, the process is more rigorous than other UX research methods, and it focuses more on measures and less on thoughts and verbal feedback. 

To produce data in which we have confidence, the data should be as free of subjective judgement as possible, relying on observed metrics and self-reported user sentiment. Our goal is to compare data over time to see how additions and improvements have impacted product maturity in a quantifiable way. To facilitate this, we've made this process prescriptive, so that it can be consistently applied by all Product Designers in all categories of our product.


**Note:** As with any evaluation, it's always a good idea to run a pilot first, so you can identify any improvements needed in the research approach.

**Note:** If you have questions, suggestions for improvement, or find this process doesn’t meet the needs of your users or product category, reach out to the UX Researcher for your group.

Refer to the [Category Maturity](https://about.gitlab.com/direction/maturity/) page to understand scoring. It is important to note that:

* **Minimal:** Category Maturity Scorecard is *not* required.
* **Viable:** Category Maturity Scorecard is conducted with internal users who are dogfooding.
* **Complete and Lovable:** Category Maturity Scorecard is conducted with external users on the JTBDs. 

## Step 0: Jobs to be Done (JTBD)

Category Maturity Scorecards are about judging the quality of experiences against a **defined and validated** JTBD. JTBD are the umbrella component of our product design process which are used as guides to direct our product strategies and the features they are comprised of. Therefore, JTBD(s) for the category should be defined and [validated](/handbook/engineering/ux/jobs-to-be-done/#validating-jtbd) ahead of completing a Category Maturity Scorecard.

Refer to the [JTBD page](/handbook/engineering/ux/jobs-to-be-done/) to learn [how to write JTBD](/handbook/engineering/ux/jobs-to-be-done/#how-to-write-jtbd) and how to use [JTBD in research](/handbook/engineering/ux/jobs-to-be-done/validating-jobs-to-be-done/), including this Category Maturity Scorecard process.

Before you move to Step 1, you need to match the category features you plan to test with your validated JTBD(s). You'll then use the JTBD(s) to create scenarios for the rest of the Category Maturity Scorecard process. The number of scenarios used often depends on the complexity of the features tested. Ideally, no more than 2 JTBD should be tested per Category Maturity Scorecard study.

This is the workflow that should be achieved in this step:

1. The Product Manager chooses up to 3 high-priority JTBD to focus on.
    * Jobs that are targeted during CMS testing should align with the category maturity  criteria. 
    * Tip: We shouldn't test jobs that weren't impacted by the recent updates to the product.
1. The Product Manager defines a set of business requirements and/or features that are needed for the category to move up.
    * This is essentially what the team will be working on, based on Opportunity Canvases, research, market, and competitive analyses. You can find an example of that [here](https://gitlab.com/gitlab-org/gitlab/-/issues/212238).
    * Map those features to the JTBD.
1. Create Scenarios to be used for the rest of this process.

## Step 1: Define and recruit users

During the JTBD creation and validation phases, the Product Designer and Product Manager will have devised a set of user criteria to describe the user(s) you're referencing in your job(s). The same criteria should be used when recruiting for the Category Maturity Scorecard, ensuring you are gathering feedback from the right type of user(s).

To balance expediency with getting a variety of perspectives, we conduct the Category Maturity Scorecard research with five participants from one set of user criteria. If you have multiple user types for your JTBD, it is ideal to recruit 5 from each user type. To keep the study manageable, focus on no more than 2 user types per study. If more than 2 user types are required to accurately measure your JTBD, conduct a separate follow-up study for the remaining user types.

**Example:** A JTBD can be completed by a DevOps Engineer and a Release Manager. In this case, you’d recruit a total of 10 participants: 5 DevOps Engineers and 5 Release Managers.

The recruiting criteria can be based on an existing persona, but needs to be specific enough that it can be turned into a screener survey. [A screener survey should then be created in Qualtrics](/handbook/engineering/ux/ux-research-training/recruiting-participants/#craft-your-screener-user-interviews-and-usability-testing) that your prospective participants will fill out to help you determine if they're eligible to participate. 

The template survey includes a question asking people if they consent to having their session recorded. Due to the analysis required for Category Maturity Scorecards, participants must answer **yes** to this question in order to participate. Once your screener survey is complete, open a [Recruiting request issue](https://gitlab.com/gitlab-org/ux-research/-/blob/master/.gitlab/issue_templates/Recruiting%20request.md) in the [UX Research project](https://gitlab.com/gitlab-org/ux-research/), and assign it to the relevant [Research Coordinator](https://about.gitlab.com/company/team/?department=ux-research-team). The Coordinator will review your screener, reach out to you if they have any issues, and begin recruiting users based on the timeline you give them.

**Note:** Recruiting users takes time, so be sure to open the recruiting issue at least 2-3 weeks before you want to conduct your research. 

## Step 2: Prepare your testing environment

Testing in a production environment is the best choice because your goal is to evaluate the actual product, not a prototype that may have a slightly different experience.

Once you know what scenario(s) you’ll put your participants through, it’s important to determine the interface you’ll use. Some questions to ask yourself:

* **Can your participant use their own GitLab account?** If not, can you set them up with a GitLab.com account and have them use that? 
* **Do you require a self-managed instance?** If yes, do you need to provide one?
* **Do your scenarios require any external actions?** For example, do you need to display a specific alert, or can a participant complete everything on their own?
* **Does your scenario require interacting with anything besides a GitLab web-based interface?** Should they receive an email or do they need to use a command-line interface?

It’s important to thoroughly plan how a participant will complete your scenario(s), especially if you answered "yes" to any of the questions above. Involve technical counterparts early in the process if you have any uncertainty about how to enable users to go through your desired flow(s).

If your JTBD interacts with other stage groups’ areas, reach out to them to ensure their part of our product will support your scenario(s). 

Because this is a summative evaluation of the current experience, all of the available options the participant should need access to must be available in the GitLab instance. When you recruit participants, keep in mind the tools and features they must access to complete the JTBD scenarios.

## Step 3: Document success/failure flows of your JTBD scenario(s)

Before you conduct your research with your participants, it's important to run through the tasks yourself just for a sanity check, and as a forcing function to document the successful path.

**Defining ‘Success’**
* Successful task completion.
* A single task may have several paths to the end goal that result in task completion, and thereby a ‘Success’. The team must identify the end goal prior to the study starting so everyone is aligned.
    * *Why is this important?*  Identifying and being aligned on the end goal allows the moderator to accurately know what is success/failure, which is critical to know since follow-up questions are dependent on passing the task.

**Defining ‘Failure’**
* Unable to complete the task.
* A partial completion of a task.
* When a participant is unable to complete a task, their ratings on the XYZ question are discarded.
* If there is a failure, the team should try their best to understand why it occurred (ex: Was it the way the task was phrased? Was the experience confusing? etc.).
    * *How can this be done?* One way to do this is to go back at the end of the study to have the participant go through that task again. This time, you can ask targeted questions to understand why they took the route they took in the experience. (ex: *‘It looks like you clicked on ‘Issues’. Tell me more about why you selected that menu item.’, ‘You felt you completed the task at this point. What makes you feel confident that you have accomplished the goal of XYZ?’*)

How the participant ended up at the end goal may not be important for the team to document. If the participant took the long path and felt it was or wasn’t easy, that should be reflected in their score.  What matters most is if they ended up at the end goal.

Once you've gone through your scenario(s), have a co-worker complete the scenario as a pilot. Ideally, this person won't be familiar with the scenario, so they don't have an expert-level understanding of how it works. Use this pilot to uncover any issues with how you've formulated your scenario(s). As this is meant as a way to check your scenario/flow(s) plan, it's ok to coach your co-worker a little, using this discussion to get to the heart of any problems your scenario or flow may have. If any problems were found during this pilot run update your scenario flow(s) accordingly.

## Step 4: Complete the test script and conduct the research

Before you can begin running your participants through your scenarios you'll need to write your test script. Because Category Maturity Scorecards are a standardized process, moderators should complete and follow this [testing script](https://docs.google.com/document/d/1QqRhAuGThuDnnBnDHHug5zBBKGvDMGsj9aQUtSgs49M/edit?usp=sharing) as closely as possible. The moderator will typically be a Product Designer, but this is not strictly required. You are encouraged to have any relevant stakeholders attend the sessions to help take notes, but it is very important they remain silent. 

#### The 3 questions we ask

When a participant is successful at completing a task, they are then asked 3 questions to help us measure their experience, which we then tie back to category maturity. Note that if a participant failed at completing a task, there’s no need to ask them the 3 questions.

The following 3 questions were selected because they’re applicable for both the [UX Scorecard](https://about.gitlab.com/handbook/engineering/ux/ux-scorecards/) and CM Scorecard testing. At the root of how we rate/grade experiences, it arguably comes down to two main elements:

1. How easy it was to do something - this is defined as ease-of-use which has components of usability baked within it.
1. How the user rated that experience - given our user segments, they know what a user experience is - so we can ask about it. Understanding how users felt about that experience gives them the opportunity to rate it directly, rather than having us infer their rating based on calculations.

**Question 1: Single Ease Question (SEQ)**

The [Single Ease Question (SEQ)](https://measuringu.com/single-question/) is a newly introduced industry-wide question based on other UX-related questions and measures. This question essentially helps us understand if the task was easy or difficult to complete and provides a simple and reliable way of measuring task-performance satisfaction. Bonus: this question is also used for UX Scorecard testing.

*Q1: “Overall, this task was...”*

* Extremely easy
* Easy
* Neither easy nor difficult
* Difficult
* Extremely difficult

**Question 2: User Experience rating**

Admittedly, the term ‘user experience’ is broad; as it encompasses many components we care about (ex: efficiency, speed, usability, etc) that are completely applicable to how one rates an overall user experience. Because of that, we’re intentionally not defining ‘user experience’ and feel that given our audience, the definition will be collectively understood with a high level of accuracy. What sets this question apart: it closely aligns with the grading and scoring criteria with the UX Scorecard and CM Scorecard testing. Bonus: this question is also used for UX Scorecard testing.

*Q2: “How would you rate the user experience?”*

* Extremely good
* Good
* Neither good nor bad
* Bad
* Extremely bad

**Question 3: UMUX Lite, adjusted**

The [UMUX Lite](https://measuringu.com/umux-lite/) score is based on the UMUX (Usability Metric for User Experience), created by [Finstad](http://citeseerx.ist.psu.edu/viewdoc/download?doi=10.1.1.872.6330&rep=rep1&type=pdf), and it is highly correlated with the SUS and the Net Promoter Score. It's intended to be similar to the SUS, but it's shorter and targeted toward the [ISO 9241 definition of usability](https://www.w3.org/2002/Talks/0104-usabilityprocess/slide3-0.html) (effectiveness, efficiency, and satisfaction).


*Q3: "How would you agree or disagree with the following statement:*

*GitLab's [Category] capabilities meet my requirements."*

* Strongly agree
* Agree
* Neither agree nor disagree
* Disagree
* Strongly disagree

#### Calculating the CM Scorecard score

As participants attempt to complete a task, for our purposes, the end result will either be: Success or Failure. **Task failures are important to note and we can’t discount them**; they must be incorporated as part of the criteria to move category maturity levels. To move to the next category maturity level, a minimum % pass rate is required, along with the minimum score. The chart below illustrates the relationships between: Minimum % pass rate, the UX Scorecard grades, SUS, CM Scorecard level, and the CM Scorecard score.

|  Minimum % pass rate  |  UX Scorecard grade  |  Scale option  |  Scale option value  |  CM Scorecard score range  |  CM Scorecard level  |  SUS (for reference)  | 
|:-:|:-:|---|:-:|:-:|:-:|:-:|
| 100% |  A  |  Extremely good/easy, Strongly agree  |  5.0 |  5.00 - 3.95  | Loveable  |  100 - 78.9  |
| 80% |  B  |  Good/Easy, agree  |  4.0 |  3.94 - 3.63  | Complete  |  78.8 - 72.6  |
| 80% |  C  |  Neither  |  3.0 | 3.62 - 3.14  | Viable  |  72.5 - 62.7  |
| n/a |  D  |  Difficult/Bad, disagree  |  2.0 | 3.13 - 2.59  | --  |  62.6 - 51.7  |
| n/a |  F  |  Extremely bad/difficult, Strongly disagree  |  1.0 | 2.58 - 1.00  | --  |  51.6 - 0  |

The **CM Scorecard score** can easily be calculated for each task:
1. Average how each question scored
    * Ex: Q1 (3, 2, 5, 4, 5 = 3.80 average), Q2 (5, 4, 5, 5, 5 = 4.80 average), Q3 (3, 2, 3, 3, 5 = 3.20 average)
1. Then, average those question averages
    * Ex: Q1 (3.80 average), Q2 (4.80 average), Q3 (3.20 average) = 11.80 total / 5 participants = 3.93 average
1. Finally, find the score in the chart above to determine the resulting grade and CM Scorecard level
    * **3.93 average = ‘B’ CM Scorecard grade = Complete**

Tip: Use this [Google Sheet](https://docs.google.com/spreadsheets/d/1w3GZNc11PSZ9sN_2II5SI3fwK4tH9LLSb2bci_o2mWg/edit#gid=0), which contains the calculations already built into it.

If the Minimum % pass rate is < 80% during a study, the study should stop at that most recent participant to conserve resources. In the event this should occur, the category maturity cannot be moved up a level.  The team should take those learnings, iterate, and retest when they’re ready again. It’s also recommended that a retrospective take place to learn:
- What happened?
- Why weren’t participants able to successfully complete the tasks?
- What will we do to address this?


#### Post-session debriefing

It’s important that the moderator and any stakeholders don’t leave the call when the session concludes. Instead, remove the participant and remain on the call. Use this time for the group to debrief on what they just experienced. The notetaker(s) should take notes on this discussion.

* Have each person talk about what they feel were the major findings of the session.
* Mention any issues with the session or things that should be done differently in the future.
    * **Note:** For Category Maturity Scorecards, no changes can be made to how you conduct the sessions, otherwise the data can’t be compared. For this reason, we suggest running a pilot session to work out any kinks.  
    * Allow anyone to ask any questions about the content covered or otherwise say things they feel need to be said before the session concludes.

#### Resulting data

By following the Category Maturity Scorecard [testing script](https://docs.google.com/document/d/1QqRhAuGThuDnnBnDHHug5zBBKGvDMGsj9aQUtSgs49M/edit?usp=sharing), you will have the following measures to report, per feature, not per scenario. However, scenarios may include more than one feature.

- **Single Ease Question** 
- **User Experience rating**
- **UMUX Lite score**
- **Success/failure** 

## Step 5: Analyze and document your findings

The goal for analyzing Category Maturity Scorecard data is to establish a baseline measure for the current experience as it relates to the JTBD(s). Over time, our product will change as new features/functions are added/changed. We can review the data collected here to understand how these changes impacted the user experience and use it to make improvements.

**To analyze:** Use the [Google Sheet](https://docs.google.com/spreadsheets/d/1w3GZNc11PSZ9sN_2II5SI3fwK4tH9LLSb2bci_o2mWg/edit#gid=0) to aid in calculating the CM Scorecard score, per task. Additionally, look for themes behind the reason why participants scored the way they did. 

**To document:** Document and highlight areas for improvement via issues, utilizing the [‘Actionable Insight’ label](https://about.gitlab.com/handbook/engineering/ux/ux-research-training/research-insights/#how-to-document-actionable-insights), to make further improvements to the experience -or- the level moves up.

Read the UX Research team’s guide for [documenting insights in Dovetail](/handbook/engineering/ux/dovetail/#the-ux-research-teams-guide-to-documenting-insights-in-dovetail).

## Update category maturity

Read the UX Research team’s guide for [documenting insights in Dovetail](/handbook/engineering/ux/dovetail/#the-ux-research-teams-guide-to-documenting-insights-in-dovetail).

### Update JTBD data file

Several groups currently use [jobs_to_be_done.yml](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/data/jobs_to_be_done.yml) to showcase the current maturity of each of the jobs that represent a given categories' overarching problems they are working on solving. Each entry in the YML file consists of the following keys:

| Key | Example Value | Description | Required |
| --- | ---           | ---         | ---      |
| `slug` | group_jtbd_1a | Unique ID of the JTBD | Yes |
| `parent` | group_jtbd_1 | Unique ID of the parent's JTBD | No |
| `short_jtbd` | Measuring Outcomes | A short reference of the JTBD | No (if `jtbd` is defined) |
| `jtbd` | When....I want to...So that | The complete JTBD | No (if `short_jtbd` is defined) |
| `grade` | "A" | The corresponding letter of the score of A, B, C, D, F | No |
| `confidence` | Researched | Confidence level of the grade | No |
| `source` | https://gitlab.com/gitlab-org/ux-research/-/issues/900 | URL pointing to the finished research issue | No |
| `group` | Plan | The group or stage that the corresponding JTBD belongs to | No |


In order to map the CMS score for a given JTBD to a grade letter, use the following criteria:

- A: 3.95 or higher
- B: Between 3.65 and 3.94
- C: Between 3.14 - 3.63
- D: Between 2 and 3.13
- F: Less than 2
