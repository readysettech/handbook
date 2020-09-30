---
layout: handbook-page-toc
title: How to Engage with Product Management
---

This document describes how to engage with the product management team.

## On this page

{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Where to reach product managers

{:.no_toc}

- [**Public Issue Tracker (for Product)**](https://gitlab.com/gitlab-com/Product/issues); please use confidential issues for topics that should only be visible to team members at GitLab.
- [**Chat channel**](https://gitlab.slack.com/archives/product); please use the `#product` chat channel for questions that don't seem appropriate for the issue tracker.

## Which product manager should I contact?

Please see the [Product Categories](/handbook/product/categories/) to know which product manager handles which category.

## What does Product do?

At GitLab, the PMs lead their specialization. That is, the Create PM decides
what the Create group works on, for which release, and makes sure this furthers
our goals. This includes bugs, features, and architectural changes.

The PM can't be expected to parse every single bug or issue that comes by, so
they have to rely heavily on the input of the various stakeholders. To be able
to achieve this, both the PM and the stakeholders have to actively work
together. It's a two-way street.

In general terms, if you require something to happen with the product or if you
need engineering staff for a particular change, you approach a PM. Preferably
through creating an issue (the GitLab way), and mentioning them there.

In the same vein, PMs are required to ask for feedback from the stakeholder of
particular changes. If a change will affect GitLab.com and its maintenance, a PM
should proactively reach out to infrastructure engineers to help with the scope,
design, and decisions regarding this change.

It is then up to the PM to weigh all these inputs and decide on a [prioritization](#prioritization).
It is to be expected that they are the best equipped to make this
prioritization, while also keeping in mind all goals of GitLab.

### Examples: A customer has a feature request

If you hear a feature request from a customer, you should follow the normal
procedure: create an issue and label it correctly. Let's say the customer
requests an enhancement to Issues. You know by reading above that you'll have to
label this with `Discussion` and you can mention or reach out to the Plan PM to
expedite this if warranted.

A salesperson for an organization asking for a paid-tier feature request shall
work with the product manager to arrange conversations to further explore the
feature request and desired outcome. The process will be:

- Sales schedules 1 hour zoom meeting with product manager, customer, and
themselves. Call recorded if customer gives permission.
- Product Manager prepares any additional questions they would like answered, beyond what is below.
    - What version of GitLab are you currently using? CE / Starter / Premium?
    - How are you currently doing source code management? GitLab merge requests or another tool? How about CI/CD?
    - How are you currently doing issue management? How are you using HP ALM? Agile/Kanban? What do your sprint/iterations look like? 1 week? 1 month? 2 months?
    - What is the integration like between issue management and source code management?
    - How do teams manage multiple repos? Does a team typically work on one repo at a time? Or do they work on multiple repos at the same time?
- Sales sends questions to customer prior to meeting.
- Meeting is created in Salesforce.com
- Sales creates a Google document for notes from call with customer. Google Doc shared with product manager and sales manager
- Sales and product manager schedule 15 minute pre-meeting to share what we know about the customer thus far, so as to not waste time asking questions we already know the answer to. Notes from this pre-meeting are added to the Google document.
- Sales adds a link to the Google document under the account object as a note.

In the event that a paid customer is willing to pay for us to develop a specific
feature, we should still respond as above. It's great that they're willing to
pay for it: that means they really need it. However, we will not make a custom
version of GitLab; even gitlab.com is running on GitLab Ultimate, and we move
faster that way by minimizing technical complexity to determine features to
follow after, it’s a trade off to make. This doesn’t mean that "no" is always
going to stay "no." We keep an open mind for improvements.

### Example: Many support requests come in about a bug with CI

Same as before, make sure an issue is made and make your case with the PM that
this is becoming a problem and needs to be fixed. The PM will make sure that
this is fixed or resolved in some other way.

### Example: I think creating new files is slow

Everything in GitLab should be fast and creating files falls under the
repository, so you create an issue and make the PM aware of it by mentioning it.

The PM in turn will investigate whether this is a general problem or one
specific to GitLab.com, in collaboration with infrastructure and others and
schedule any necessary changes for an upcoming release.

## How do I share feedback?

If you have any product-related questions, comments, input, or otherwise, the
product manager is the primary person you should talk to, _if creating an issue
does not suffice_. Otherwise, [read this section on how to create an](/handbook/product/product-processes/#how-to-submit-a-new-issue)
issue.

This includes, but is not limited to, features, bugs, and other changes that need
to be prioritized, changed, discussed, or need more attention.

Product managers will reach out to stakeholders when making or communicating any
decision. The pressure of balancing priorities while ensuring we build excellent
software is on the product managers and they need all the input they can get to
achieve this.

Paid features fall under their respective PMs, not under one PM in particular.
For instance, Service Desk falls under the Plan PM, because it's part of our Issues.

## A customer expressed interest in a feature

Whenever you're sharing feedback on an issue (e.g. "Customer X wants this"),
please make sure to do the following:

- Link to the source. Usually this is a link to Salesforce or Zendesk
    - Use the Salesforce Account URL when it's a paying customer and you want to relate the ARR
    - Use the Salesforce Opportunity URL when it's related to a specific deal (Opportunity)
- Provide context: if a customer wants this feature, include _why_ they are interested in this. If you don't know,
make sure to ask or bring the relevant PM in contact with the customer
- Include any further useful context (e.g. what kind of software is this customer building, or how big are they)
- Mention the [product manager](/handbook/product/categories/), and ask them anything that isn't clear to you
(e.g. it's not clear what the status is of the issue, etc)

If a customer expresses interest by simply mentioning an issue number or e.g. "an integration with X",
that is not sufficient information. Make sure to ask them:

- why do you want this?
- what parts of this issue / integration are important to you and why?
- have you tried workarounds?
- how important is this to you?

The product manager is responsible for figuring all of this out, but being one step ahead of them
will speed things up.

You can use [this feedback template](#feedback-template) to make this easier.

### Good example

A customer with more than 1000 users mentioned they are interested in this feature to be able
to do their sprint planning more effectively. They are using software X to do this today,
but would be able to move to GitLab if we would do this.

@productmanager this issue doesn't have a milestone right now, are we planning to address this
in the near term?

### Bad example

salesforce.com/blabla

### Feedback template

You can copy/paste this to make sure you don't miss anything:

```
- Link to request:
- Why interested:
- Current solution for this problem:
- How important to them:
- Questions:
- PM to mention:
```