---
layout: handbook-page-toc
title: "Stack Overflow response workflow"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Overview

In Zendesk, each advocate [should have Stack Overflow set up as a personal view](/handbook/marketing/community-relations/community-advocacy/tools/zendesk/#view-limits-workaround). New Stack Overflow posts that are tagged `gitlab` are brought into this Zendesk after 4 hours. The delay is to ensure we still encourage community input.

## Workflow

1. View the new question in Zendesk under the `Stack Overflow` view by opening the URL
1. If the question has been answered, apply the `StackOverflow > Solved` macro and close the ticket
1. If the question has been flagged as having insufficient information (usually by a moderator), apply the `Stack Overflow > Insufficient Information` macro and close the ticket
1. If the post has been removed by the user, apply the `Removed` macro and solve the ticket
1. Often people will apply the `gitlab` tag to their post even if the post isn't specific to GitLab (e.g. they're having a problem with Docker, but they happen to be using GitLab). If the question isn't specific to GitLab, apply the macro `Mention`
1. If a question does require us to respond, use the [Involving Experts](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts) workflow to get assistance. Once the question has been answered, apply the `Expert-Responded` macro (since the ticket does not automatically update with responses like e.g. Twitter).

## Best practices

View the [Stack Overflow FAQ](https://meta.stackexchange.com/questions/7931/faq-for-stack-exchange-sites) for info on how to best respond to questions.

## Automation

New mentions are brought into Zendesk using Zapier. There is a 4 hour time delay, and it will only pull in recently created posts. Responses and comments are not pulled in, only initial posts.
