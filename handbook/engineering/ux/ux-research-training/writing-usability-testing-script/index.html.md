---
layout: handbook-page-toc
title: "Writing a usability testing script"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### What is a usability testing script, and why you should have one
Usability testing is a systematic approach for testing whether users can carry out scripted tasks successfully, finding what their preferences for completing a task are, and uncovering opportunities to improve the product.   
At the heart of a usability study stands the script, which the moderator follows during test sessions.

A script:
* Helps to make sure you will be covering what you set out to cover - your research objectives - and that you’ll come out of the study with the answers you need to make progress on your project.
* Keeps you consistent between sessions, making sure you ask the same of all of your participants. This consistency is important for a solid methodology, and will also make your life easier once it’s analysis time.
* Assists with collaboration, and particularly with letting others review your work.
* Helps you keep time during sessions.

It is virtually impossible to practice solid usability research without having a script. Don’t go in without one.

#### How to write your first draft
Use this template as your starting point for writing a first draft for your usability study:  

* [Usability Testing Script template](https://docs.google.com/document/d/1_5Qu2JR9QE5LE6cK4eq9yJs-nXv2rlWWifcjacaiWdI/edit?usp=sharing).

A usability script typically follows 4 main parts:
1. Introduction
2. Warm up questions
3. Tasks
4. Wrap up questions and closing words

Here is a bit about each part (you may want to read this while going over the template).

#### Introduction
This is where you introduce yourself and other attending members of the team. You also tell the participant how the session is going to go, and double check that you have their consent for recording and sharing the session.  

Use this part to build rapport with the participant. People are often hesitant, nervous or even a little standoffish at the beginning of a research session. Simple comments such as "Oh I've been to where you live and I loved it" can go a long way to making people feel comfortable and helping the study to run smoother.

Remember to distance yourself from the solution you are testing. Do not present yourself as the person who created the design or prototype. Emphasise that the participant won’t hurt your feelings regardless of what they say during the testing. Remind them that the main purpose of this exercise is to receive their candid feedback.

#### Warm up questions
Warm up questions are meant to further break the ice as well as getting relevant background information on the participant.

Here are some standard warm up questions to consider:
1. What’s your current role?
1. How long have you been in that role?
1. Do you have experience dealing with X?
1. Have you ever used GitLab? If so, what for?

**Tip 1**: Even if you don’t have anything you want to ask, have at least 2 quick questions here, as it will help to break the ice and make the participant feel more at ease. 

**Tip 2**: Consider asking questions that will help you to understand the participant’s mental model and expectations, prior to interacting with your designs (e.g. "We have a page called Security Dashboard. What tasks would you expect to be able to accomplish with the help of that page?".)

**Tip 3**: If needed and you have the time for it, you might want to include some more interview-y questions here that would benefit either this study or a different one (if it’s a different study, make sure it shares the same participant profile with this one!). In particular, consider asking questions that might be used later on as part of a persona or a JTBD study (e.g. "What would you say are your top 3 tasks?").

#### Tasks
This is the heart of the script, and the part that takes the longest to write. Usability studies usually consist of 3-4 tasks (though your mileage may vary).

**How to define good tasks**  
When sitting down to write your tasks you should already have [defined your research goals, objectives and hypotheses](/handbook/engineering/ux/ux-research-training/defining-goals-objectives-and-hypotheses/). To form good usability tests, start by going over your research objectives (which detail what you and your stakeholders want to get out of the study), and consider how to best translate them into user tasks.

The key thing to remember when moving from objectives to tasks is that **your tasks should reflect realistic user goals**.

For example, perhaps one of your objectives entails finding out whether users can quickly locate a CTA. But since no user ever goes into a website with the goal of locating a button, your task should never be “Can you find and click the button?”. Rather it should be about why the participant might want to click the button in the first place (e.g. “You want to enable feature X for your project. Can you do that please?”).
	
Another objective of yours might be identifying potential improvements to the flow. Since real users don't generally go into websites with the sole purpose of finding faults in it, instead of asking the participant “Can you please complete the following steps and tell me what we should improve?”, ask them to perform a task that would necessitate them to attempt to go through that flow and observe them carefully to see where they fail, struggle or hesitate.

Finally, pay close attention to how you phrase your tasks to avoid bias, leading the participant, and other common pitfalls. To learn more about writing good tasks we highly recommend going over this helpful NN/g’s article:
[Write Better Qualitative Usability Tasks: Top 10 Mistakes to Avoid](https://www.nngroup.com/articles/better-usability-tasks/).

**How to structure each task**  
For each task, consider whether some set up is required to provide context and appropriate motivation for the participant. If so, describe a relevant scenario prior to giving the task. For example:  

Scenario: “Let’s say this is a project you’re working on, and you just committed some new code”.  
Task: “Please test to see whether that code contains any security vulnerabilities”.

Then, consider adding some more specific questions and prompts that the moderator can utilise as the task unfolds, in case the participant isn't bringing these topics on their own. Examples:
* What are you seeing on this page?
* What is this page about?
* Is SAST running right now?
* What would you do next, if anything?

**Tip 1**: For each task, add a link in your script for the prototype/webpage that’s relevant for that task. Not only will it help your teammates who will be reviewing the script to understand what the task is about, but it will allow you to quickly resend the relevant link should the participant need it again.

**Tip 2**: Consider noting under each task, in light gray, ‘What we expect them to do’ (e.g. "Follow the CI pipeline and go into the SAST job output"), to remind the moderator of the possible paths for completing the task. This would assist the moderator in helping participants to recover, in case they failed a task which is a prerequisite for the following task.

**How to order your tasks**  
* If your tasks can build on top of each other in a sensible way, make sure you order your tasks to reflect that. For example, Task 1 could be around navigating to a certain page, and Task 2 around reviewing that page.
* Cluster together tasks that belong to the same topic or area of the product.
* As a rule of thumb, start with the tasks that matter most to you. It will take time mastering moderating usability sessions, and it is common to fall behind on time when you’re just starting out. Therefore, start with what matters most to you and leave what’s merely nice to have to the end of the test.

#### Wrap up questions
Here you can get the participant’s broad impressions about what they saw and experienced. Here are some standard questions to consider:
1. What do you think about this process you just went through?
2. How does what you just experienced with GitLab fare in comparison to the tool you normally use?
3. Anything else you’d like to add?

Conclude the script with thanking your participant and mentioning when they are expected to get their compensation.

#### You've completed your draft script. Now what?

##### 1. Review your draft
Once your draft is more or less done, give it another read and ask yourself:
1. Does it cover the project’s objectives?
2. Does it make sense time-wise? Estimating time will get easier with experience. Keep in mind that usability tests should normally take between 30-45 minutes.

##### 2. Let others review your draft
Edit as needed based on feedback received from your stakeholders/teammates.

##### 3. Test the test
Run a dummy test with a colleague/an internal participant to make sure your task instructions are clear and that you’re keeping time. Edit as needed, and notify your stakeholders of any big changes.

### A crash course on remote, moderated usability testing

<!-- blank line -->
<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/5MvpxvN9vLU" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

**Slides**

[View the slides](https://drive.google.com/file/d/1AqmTX0atvxRsag5EIdyFduGRfzNQLjRC/view?usp=sharing)
