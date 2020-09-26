---
layout: handbook-page-toc
title: "Involving experts workflow"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Overview

When responding to community messages, you should always strive to involve a resident GitLab expert on the subject if possible.

This gives:

* a higher quality of answers
* shows that our whole company is committed to helping people
* the expert receives more feedback from users
* opportunity to build relationships between community and GitLab team members

## Workflow

### Finding an Expert
1. Assess if a mention requires expert involvement. Use the Best Practices section below to find an appropriate team or expert to involve.
1. Please mention the expert by name in the relevant Slack channel (e.g. in `#frontend` if it's a frontend question) with the following template. If you are unsure of the correct channel, you can ping the experts in the [`#questions`](https://gitlab.slack.com/messages/questions) channel.
1. After reaching out to an expert, apply the 'Reached Out to Expert' macro on the ticket and link the related Slack outreach. This leaves the ticket in an `open` state.

### Zendesk Tickets
The next steps vary for different Zendesk views, based on how tickets are threaded/pulled into our Zendesk instance.

For Twitter:
1. When an expert has responded to the ticket, solve the ticket with the `Expert Responded` and `Expert Response` macros and note the name of the expert who responded in the ticket notes. The expert response will be threaded in the same ticket as the original tweet.


For Blog/Docs Comments:
1. When an expert has responded to the ticket, solve the ticket with the `Expert Responded` macro.
1. The expert's response will come into Zendesk as a new ticket. Solve this ticket with the `Expert Response` macro.

For Hackernews and Reddit:
1. When an expert has responded to the ticket, solve the ticket with the `Expert Responded` macro.
1. If the expert's response mentions `GitLab`, it will come into Zendesk as a new ticket. Solve this ticket with the `Expert Response` macro.
1. If the expert's response does not mention `GitLab`, add a link to the original ticket and solve with both the `Expert Responded` and `Expert Response` macros.



### How to Involve Experts

Advocates can involve experts in community discussions by

* Sharing community feedback in a product slack channel
* Facilitating discussion between community members and the GitLab team by opening an issue and tagging/assigning related experts
* Ask experts to respond directly on a social channel to provide insight and help the community member feel heard

### Questions to ask to help assess if/how to involve experts:

Will involving an expert help the community member feel their input matters?

Is there a direct question being asked to GitLab?
* Is it a question about the product that you can answer by sharing a handbook link, issue, or MR to offer further resources?
* Is there a follow up question or call to action you can include in your response to encourage conversation, like requesting adding feedback to the issue?
* Is it something that only a GitLab expert can answer?: Use Expert Engagement Workflow

Is the mention of GitLab feedback about the product or company?
* Is the comment a misconception?: Share relevant handbook links to clarify false information
* Is there opportunity for a community member to be our voice?: Monitor the post for community engagement, and let our users speak freely about their own experiences
* Is there opportunity to include GitLab experts in discussion?: Use Expert Engagement Workflow



### Best Practices for Expert Outreach

* Refer to the [Product stages, groups, and categories page](/handbook/product/product-categories/#devops-stages) to locate the appropriate expert/team.
* Consider using our [Technical Evangelists](/handbook/marketing/technical-evangelism/) as the first experts to reach out to for questions related, but not limited to: DevOps ecosystem, competitor landscape, industry trends.
  * Contact the Technical Evangelists by mentioning `@techevangelism` on any Slack channels
* If the community has a question about how a tool or feature works, or is looking for additional training, involve the [technical marketing team](/handbook/marketing/product-marketing/technical-marketing/) with outreach in the [#technical-marketing](https://app.slack.com/client/T02592416/CGPBM3JRF) Slack channel. Their team can respond with links to demos and share knowledge.
* When trying to figure out who has expertise on what segment of the product, refer to the ["DevOps Stages"](/handbook/product/product-categories/#devops-stages) section of the [Product stages, groups, and categories](/handbook/product/product-categories/) page in the handbook. The [team page](/company/team/) can also be useful.
* For product related questions, consider if the mention requires a response from the Product Manager. Consider pinging engineering managers or technical writers instead.
* Utilize the customer success team in the #cs-questions Slack channel for questions about using GitLab and best practices.
* For expert responses on blog posts, first check if the blog author is a GitLab team member, and reach out to them directly. If the blog author is not a GitLab team member, the content team may be able to help connect you over email. 
* If an expert is uncomfortable using their individual account to respond, they are welcome to provide a draft for a Community Advocate to use to respond.
* Utilize the Support Stable Counterparts for each product stage. You can find these people by searching for 'Support' on the [product categories page](/handbook/product/product-categories/)

<i class="fas fa-info-circle" aria-hidden="true" style="color: rgb(49, 112, 143)
;"></i> If you are working on a mention that requires an expert from a particular [devops stage](/handbook/product/product-categories/#devops-stages), you can find them in the Slack channels named `#s_<devopstage>` (e.g. `#s_plan`, `#s_verify`, etc.).
{: .alert .alert-info}

### Expert Involvement Template

```plain
@expert_username [LINK TO COMMUNITY COMMENT]
Hello! An expert is needed to respond to this. Could you please answer on [name of social platform] using your own individual account? Even if you are busy, your direct response is a better experience for the requester! If you don't know the answer, could you share your thoughts and ping a specific expert who might? Or if there is a more appropriate channel to ask, could you point me in that direction? It’s our goal to involve GitLab team members in wider GitLab community discussions. Thank you! /handbook/marketing/community-relations/community-advocacy/#can-you-please-respond-to-this
```

* Encourage experts to engage with community following our [Team Member Social Media Guidelines](/handbook/marketing/social-media-guidelines/): **Answer yourself** - We should be personable and human. So if something is delegated to you don't answer the question and have someone else post it. Engage yourself. Make or create an account for the service if needed.
* After reaching out to experts via slack, apply the `Reached out to an expert` macro and link the Slack outreach message.
* Consider responding yourself via the @gitlab handle through Zendesk with as much information as you currently have while you're waiting for the expert. This will enable us to engage with the user faster and assure them that our team will get back to them with more details soon. 
* After the expert has responded, apply the `Expert Responded` macro to the Zendesk Ticket to automatically solve the ticket.


If there is no Zendesk ticket related to the mention (e.g. a HackerNews mention) track it in the [`#community-relations`](https://gitlab.slack.com/messages/community-relations) Slack channel.

## Metrics

### Slack
* The template above has the keyword phrase 'support from an expert' for ease of searching in Slack.
* Search slack using keyword phrase 'support from an expert' to track total number of times advocates reached out to experts

### Zendesk
* Tickets are solved with the `expert-responded` macro and tag.
* In Zendesk, navigate to the Reporting -> Insights section. Make sure that all ticket groups are selected. Scroll down to the sections titled 'Tags with rising usage'.
* Hover over the top of this graph with your curser in the middle of the graph and click on the small triangle that appears.
* Click `View This Report`
* Click `Filters` and then click `Add Filters`
* Choose the filter option `Select form a List of Values (including date ranges)`
* Scroll through the filter options to find the section called `Date (Ticket Created)` and choose the first option with the same name. Then, click `Select`
* Now, you'll see two options to filter the data. Choose the option on the right side of the page in the blue blox that reads `Click to Select Floating Range`
* Choose the `range` option. Make sure both elements in the range are set to `days ago`
* Toggle these days to cover one calendar month. Then, click `apply`
* Finding the Data: If the tag was used less during the month in question than the month before, the data will populate in the `Delta Last 30 Days` column, and appear as a negative number. If the tag was used more during the month in question than the month before, the data will populate in the `Last 30 Days` column, and appear as a positive number.
* Pull the correct data and add it to the [Expert Response Monthly Data](https://docs.google.com/spreadsheets/d/1frxCohA-SZop6GsolX7os9nq3c806FYS9YLKblZUotE/edit#gid=1364826426) Google Sheet, editable by GitLab Team Members.


Advocates can use Google Sheets and Google Slides to create a graph to best communicate this data during the team Group Conversation.

## Automation

TBD: Zendesk
