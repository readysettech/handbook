---
layout: handbook-page-toc
title: "Jobs to be Done (JTBD) Overview"
---

#### On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}


## JTBD Overview

A Job to be Done (JTBD) is a framework, or lens, for viewing products and solutions in terms of the jobs customers are trying to achieve. It's about understanding the goals that people want to accomplish. It lets us step back from our business and understand the objectives of the people we serve. It opens the door to innovation. 

At GitLab, we have our own flavor of JTBD and use it throughout the design process, but most notably to: 

* Define scope
* Validate direction
* Evaluate existing experiences
* Assess category maturity

If you're looking for a deep dive into our JTBD philosophy, you can learn more about [what is and isn't a JTBD](/handbook/engineering/ux/jobs-to-be-done/deep-dive/#what-is-a-jtbd), [JTBD core principles](/handbook/engineering/ux/jobs-to-be-done/core-jobs-to-be-done-principles/), and the [JTBD hierarchy](/handbook/engineering/ux/jobs-to-be-done/deep-dive/#whats-the-hierarchy-in-jtbd).

Watch the following video for a brief overview of why Jobs to be Done are so valuable towards the product development process:

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/H6j1Xd4yufI" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

For a quick how-to, follow the below guidance.

### JTBD terminology
First, let's set the terminology we use for JTBD.

* **Job**: something a customer wants to accomplish. For example, the main job of a GitLab customer could be stated as, "build and deploy software." The job always starts with a verb. 
* **Job Performer**: the person who does the job. Usually, we talk about these people in terms of personas. They are [buyers](/handbook/marketing/product-marketing/roles-personas/#buyer-personas), [developers](/handbook/marketing/product-marketing/roles-personas/#sasha-software-developer), [sysadmins](/handbook/marketing/product-marketing/roles-personas/#sidney-systems-administrator), [and so on](/handbook/marketing/product-marketing/roles-personas/#personas). 
* **Task**: a step in the process of completing a job. 
* **Need**: requirements for the job. These can be a system, business, or user requirement. Examples may include words like fast, inexpensive, efficient, less, more, must have, should have. 
* **Situation**: describes the circumstances a person is in when they need a job done.
* **Outcome**: the desired end state and/or feeling that a job performer has for doing a job. 
* **Job statement**: a succinct statement that brings together the circumstance, goal, and outcome of a job. 

### How to write JTBD
We write our job statements in the following format:

**"When [situation], I want to [job], so I can [outcome]."**

We begin with past knowledge and user research to inform our job statements. 

Job statements are different than user stories and tasks. They are designed to be persona, product, and solution agnostic and have a close relationship with user stories and tasks. This allows us to think more deeply about the context, rather than just a *role with a goal*.

*Example:*

**Job statement:**  

When my development ecosystem begins to mature, I want an overall understanding of my organization’s registries and specific package usage, so I can make effective architectural decisions.

**User story:**  

As an Engineering Leader, I want to know what packages are being used and by which projects, so that I can ensure my team is using the correct versions and not introducing risk into the pipeline.

**Task:**  

View a list of packages we use. 

In its most basic form, you will have a job statement that is associated with one or more user stories that are made up of multiple tasks. You'll use each of these at different moments within the design process.

Job statements offer a high-level view of the main objective. User stories guide your solutions as you create wireframes and tasks become the steps required to complete the job. 

If you want a detailed breakdown of each segement of the job statement, learn more about the [structure of a JTBD](/handbook/engineering/ux/jobs-to-be-done/deep-dive/#how-do-i-structure-a-jtbd). 

#### Determining scope of a JTBD
Job statements can be written at different levels or altitudes. For the majority of our work, we write job statements for stage groups as we craft experiences for features or sets of related features. 

JTBD can also be written for stage or cross-stage jobs to help determine longer-term product direction.

If you're writing a job statement for your stage group, consider this guiding principle to determine the appriopriate altitude: If the job is applicable to more than 3 user types, it's likely the altitude is set too high.   

### Validating JTBD
After writing job statements, you may realize we do not have high confidence in them and need to validate our assumptions with research. [Learn how to conduct JTBD research](/handbook/engineering/ux/jobs-to-be-done/validating-jobs-to-be-done). 


