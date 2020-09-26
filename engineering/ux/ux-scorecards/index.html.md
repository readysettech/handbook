---
layout: handbook-page-toc
title: "UX Scorecards"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## UX Scorecards

As UX practitioners, we must think strategically about fixing usability challenges within the GitLab product. 

Creating a UX Scorecard with associated Recommendations enables us to *identify, scope, and track* the effort of addressing usability concerns within a specific workflow. When it's complete, we have the information required to collaborate with Product Managers on grouping fixes into meaningful iterations and prioritizing UX-related issues. 

**All of the UX Scorecards can be found in this [epic](https://gitlab.com/groups/gitlab-org/-/epics/1714).**

Below is a recommended step by step process for completing a UX Scorecard. Note that every scorecard is not the same. Product Designers are welcome to adapt the steps to their needs as long as they are as objective as possible and the spirit and outcome remains the same.

### Setup

1. Create a stage group epic with the following title: `UX Scorecard - {{Stage Group}} FY{{YY}}-Q{{Quarter Number}}` 
    > Example: “UX Scorecard - Create:Source Code FY21-Q1”
1. Work with your Product Manager to identify the top tasks (in frequency or importance) for users of your stage group. Ideally, you will base this task list on user research (analytics or qualitative findings).
1. Select one of the top tasks to complete a UX Scorecard.
1. [Create an experience scoring issue](https://gitlab.com/gitlab-org/gitlab-design/issues/new?issuable_template=UX%20Scorecard%20Part%201), using the template “UX Scorecard Part 1”, and add it to the stage group epic. 

    This issue should have the **UX Scorecard** label. If it's related to an OKR, also apply the **OKR** label for easier tracking.
1. [Create a recommendations issue](https://gitlab.com/gitlab-org/gitlab-design/issues/new?issuable_template=UX%20Scorecard%20Part%202), using the template “UX Scorecard Part 2”, to be done after the experience scoring.
1. Follow the instructions in the templates to complete the scorecard, and use the [Grading Rubric](#grading-rubric) below.
1. Once you have completed the walkthrough evaluation and provided your recommendations, remove the "WIP:" prefix from the issue title.

If you'd like to view or edit the templates, you can find them here: 

* [Part 1 - UX Scorecard  ](https://gitlab.com/gitlab-org/gitlab-design/blob/master/.gitlab/issue_templates/UX%20Scorecard%20Part%201.md) 
* [Part 2 - Recommendations](https://gitlab.com/gitlab-org/gitlab-design/blob/master/.gitlab/issue_templates/UX%20Scorecard%20Part%202.md)

#### Grading rubric

| Badge | Summary | Description |
| --- | --- | --- |
| [![Badge level A High Quality/Exceeds](/images/grade/grade_a.svg)](/handbook/engineering/ux/ux-scorecards/index.html#grading-rubric) | Exceeds Expectations | Experience exceeds expectations and the user feels the experience is delightful.<br> - Ease: *Extremely easy* <br> - Experience: *Extremely good* |
| [![Badge level B Meets Expectations](/images/grade/grade_b.svg)](/handbook/engineering/ux/ux-scorecards/index.html#grading-rubric) | Meets Expectations | Experience is viewed as good and is easy to complete.<br> - Ease: *Easy* <br> - Experience: *Good* |
| [![Badge level C Average](/images/grade/grade_c.svg)](/handbook/engineering/ux/ux-scorecards/index.html#grading-rubric) | Average | Experience is viewed as an average experience and is also average in ease.<br> - Ease: *Neither easy or difficult* <br> - Experience: *Neither good or bad* |
| [![Badge level D Poor](/images/grade/grade_d.svg)](/handbook/engineering/ux/ux-scorecards/index.html#grading-rubric) | Poor | Experience is viewed as a poor experience and is difficult to complete.  <br> - Ease: *Difficult* <br> - Experience: *Bad* |
| [![Badge level F Terrible](/images/grade/grade_f.svg)](/handbook/engineering/ux/ux-scorecards/index.html#grading-rubric) | Terrible | Too many users are unable to complete the job. Experience is viewed as extremely bad and extremely difficult to complete. <br> - Ease: *Extremely difficult* <br> - Experience: *Extremely bad* |
| [![Badge level 0 Unknown](/images/grade/grade_-.svg)](/handbook/engineering/ux/ux-scorecards/index.html#grading-rubric) | Unknown | This job has yet to be graded. <br> - Frustration: *Unknown* <br> - Job Completion: *Unknown* |
