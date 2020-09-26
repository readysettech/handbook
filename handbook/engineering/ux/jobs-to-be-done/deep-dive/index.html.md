---
layout: handbook-page-toc
title: "Jobs to be Done (JTBD) Deep Dive"
---

#### On this page
{:.no_toc .hidden-md .hidden-lg}
{::options parse_block_html="true" /}

- TOC
{:toc .hidden-md .hidden-lg}

## Jobs to be Done (JTBD) Deep Dive

There are more than a few different frameworks for Jobs to be Done (JTBD) out there. The aim of this documentation is to adapt those frameworks and create a shared understanding of a JTBD process which fits our needs here at GitLab.

Our goal is to make products that people want, as well as make people want our products. Using JTBD can help us do that.

### What is a JTBD?
* JTBD is a framework, or lens, for viewing your products and solutions in terms of the jobs customers are trying to achieve. Instead of looking at the demographic factors of usage, JTBD focuses on what people seek to achieve in a certain circumstance ([see Clayton Christensen's Milkshake video](https://www.youtube.com/watch?v=sfGtw2C95Ms)).
* JTBD is about understanding the goals that people want to accomplish. Achieving those goals amounts to progress in their lives. Jobs are also the needs, motivators and drivers of behavior: they predict why people behave the way they do. This moves beyond mere correlation and strives to find causality.
* JTBD lets you step back from your business and understand the objectives of the people you serve. To innovate, don’t ask customers about their preferences, but instead understand their underlying needs and motivations.
* JTBD is a framework that aims to improve collaboration and communication across disciplines and stage groups. Since JTBD isn't particular to any expertise (for example, product, UX, marketing), it can be used by all of these disciplines to focus team members on the core problem that the business aims to solve for its customers. For example, rather than marketing having personas, UX having user stories, and so on, the company can use JTBD to establish common, high-level definitions all domains can use.

### What isn't a JTBD?
* People “hire” products to get a job done. JTBD is not about your product, service, or brand. Instead of focusing on your own solution, you must first understand what people want and why that’s important to them.
* JTBD are not about specific products or particular solutions in favor of focusing on the process that people go through to solve a problem.
* Read more about [core JTBD principles](/handbook/engineering/ux/jobs-to-be-done/core-jobs-to-be-done-principles/)

### When should I use a JTBD?
Use JTBD throughout the design process, but most notably to:
* Define scope
* Validate direction
* Evaluate existing experiences
* Assess category maturity

### How do I structure a JTBD?
A core strength of JTBD is its structure, which clearly separates out various aspects of achieving objectives. The who, what, how, why and when/where are analyzed individually, giving both precision and flexibility to JTBD methods.

<details>

<summary markdown="span">Job performer (who) - The person who is trying to do the main job; the ultimate end user.</summary>

* Note that these different roles don’t refer to job titles. Instead, they represent different functional actors within the context of getting a job done. 
* In addition to the job performer and the buyer, other functions within the job ecosystem to consider include the following:
   * **Approver:** Someone who authorizes the acquisition of a solution 
   * **Reviewer:** Someone who examines a solution for appropriateness 
   * **Technician:** The person who integrates a solution and gets it working
   * **Manager:** Someone who oversees a job performer while performing the job
   * **Audience:** People who consume the output of performing the job
   * **Assistant:** A person who aids and supports the job performer in getting the job done

</details>

<details>

<summary markdown="span">Jobs (what) - What the job performer wants to accomplish. A job is a goal or an objective independent of your solution.</summary>

* The aim of the job performer is not to interact with your company but to get something done. 
* Because they don’t mention solutions or technology, jobs should be as timeless and unchanging as possible. Strive to frame jobs in a way that makes them stable, even as technology changes. 
* There are several types of jobs you’ll ultimately be looking for. The key distinctions to make are between the main job, related jobs, and emotional and social jobs. 
* JTBD provides a sequence for innovation: meet the needs of the functional job first and then layer emotional and social aspects after that. Targeting emotional and social jobs first often yields an endless number of solution possibilities. 
* There are different types of jobs:
   * **MAIN JOB**
     * This is the overall aim of the job performer or your customer’s primary objective you want to understand.
     * This job defines your overall playing field and sets your scope of innovation. 
     * This job is broad and straightforward and serves as an anchor for all other elements of your JTBD investigation. 
     * This job is often expressed as a utilitarian goal. It’s an act that will be performed and should have a clear end state—the “done” part of jobs to be done.
     * This job shouldn’t include adjectives like quick, easy, or inexpensive. Those are considered to be needs, or the metrics by which job performers compare solutions, which are handled separately. The main job is also different from your marketing message or value proposition statement, which tends to be persuasive to evoke an emotion. 
     * Don’t define the main job too narrowly. A small job will limit your field of vision, but also will constrain your efforts. When in doubt, go broader and define a main job that is larger than smaller. Ask “why?” and “how?” to move the level of granularity of the main job up or down.
     * Examples: prepare a meal, listen to music, or plan long-term financial well-being 
   * **RELATED JOBS** 
     * Related jobs are adjacent to the main job, but are significantly different. 
     * As you define the main job, identify related jobs to understand the overall landscape of objectives as people have multiple goals that collide and intersect. Identifying related jobs as such can help your team understand what the main job is and what it is not. Only then should you decide on a single main job to focus on, keeping related jobs in your peripheral line of sight.
     * Keep in mind that related goals may even compete with the main job and each other. For instance, buying a large-ticket item like a car or house may detract from growing a retirement portfolio. As a result, progress in our lives is the sum of the outcomes of related jobs, and balance is often required.
     * Example: If you define grow retirement portfolio as a main job, related jobs may be finance a new home or balance cash flow. 
   * **EMOTIONAL AND SOCIAL JOBS**
     * Targeting emotional and social jobs first often yields an endless number of solution possibilities, which is why they should be considered *after* main and related jobs.
     * Emotional jobs reflect how people want to feel while performing the job. Statements usually start with the word “feel.” 
     * Example: I want to feel confident in providing feedback on my coworker's code.
     * Social jobs indicate how a job performer fits into a system.
     * Example: I want to help drive cultural change within my organization. 
     * Separating functional jobs from emotional and social jobs helps focus on the individual’s objective, on one side, and experiential aspects of getting the job done, on the other. The rule of thumb is to solve for the functional job first. It’s hard to solve for an emotional or social job if the functional job isn’t fulfilled. 

</details>

```mermaid
graph TD
  A(Main Job to be Done) --> B(Functional Aspects)
  A(Main Job to be Done) --> C(Emotional Aspects)
  C --> D(Personal Dimension)
  C --> E(Social Dimension)

  F[Related Jobs to be Done] --> G[Functional Aspects]
  F(Related Jobs to be Done) --> H(Emotional Aspects)
  H --> I(Personal Dimension)
  H --> J(Social Dimension)
  A --> F
  ```

<details>

  <summary markdown="span">Process (how) - The procedure of how the job will get done; also referred to as the objective of the JTBD. The process follows job performers as they move through different goal stages in order to accomplish their goal.</summary>

  * Understanding the process of the job performer’s intent is key to JTBD. 
  * You can illustrate the main job in a chronological map using a sequence of stages, such as Beginning, Middle, and End.
  * Each stage can contain multiple user stories (also called Little Jobs). Becareful not to get into the tasks/physical activities just yet.
  * Because the job has to be “done,” be sure to formulate the job in a way that has an end state.
  * Once you have the main sequence, specify the tasks needed to complete each user story. 

</details>

<details>

  <summary markdown="span">Needs (why) - Why the performer acts in a certain way while executing the job, or their requirements or intended outcomes during the job process.</summary>

  * Why do the job performers act the way they do while getting the job done? Their actions might be tied to achieving specific outcomes, such as producing a specific report. Their actions might also be tied to requirements or processes they must adhere to.
  * In JTBD, a need is seen in relation to getting the main job done; needs aren’t demands from a solution, but an individual’s requirements for getting a job done.
  * Needs aren’t aspirations either, which are above the main job in terms of abstraction. 
   * Example: If a main job is defined as *file taxes*, needs in getting that job done may be *minimize the time it takes to gather documents or maximize the likelihood of a getting a return*. 
   * Example: Expressions like “have financial peace of mind” or “provide for my family” are motivations beyond getting the main job. These are important aspects to consider later, but not needs related to reaching the objective of filing taxes. 

</details>

<details>

  <summary markdown="span">Circumstances (when/where) - The contextual factors that frame job execution. When and where does the job get done?</summary>

  The contextual factors that frame job execution. When and where does the job get done? 
  * Circumstances typically consist of aspects around time, manner, and place. 
  * A job without context is not complete and cannot provide strategic direction. There is necessarily a dependency on formulating a main job and knowing the circumstances. 
  * JTBD uses circumstances in order to be relevant to an organization. The conditions around the job give it meaning and relevance and therefore must be considered. 
   *  Example: *get breakfast* is a very broad job that could apply to many situations. But for a fast food restaurant, *get breakfast on the go*, is a more precise job to focus on. 
* Adding contextual detail to the situation also helps greatly when designing a solution. 
   * Example: a solution for the job *get breakfast on the go* could include everything from going to a restaurant or diner to eating a packed lunch at a desk. But when considering specific circumstances like *when late for work, while commuting* and *when cost is a factor*, a morning milkshake might be a better solution for the job. 

</details>

### What's the hierarchy in JTBD?

JTBD can be viewed at different levels, rather than just two levels—big and little. Jim Kalbach states that you can view JTBD at four different levels:

1. **Aspirations** - An ideal change of state, something the individual desires to become 
    * Lets you capture a high-level thought, but then move down to the appropriate level of discussion.
2. **Big Job** - A broader objective, typically at the level of a main job
    *  It’s more effective to target a big job and layer aspirations secondarily on top of that.
3. **Little Job** - These are smaller, more practical job(s) that correspond roughly to stages in a big job. They are also referred to as User Stories. 
4. **Micro-Job** - These are the tasks which users complete in order to achieve their user story, or little job. 

### How do I validate a JTBD?

Follow [this guidance](/handbook/engineering/ux/jobs-to-be-done/validating-jobs-to-be-done).
