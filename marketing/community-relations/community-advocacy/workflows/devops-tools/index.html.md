---
layout: markdown_page
title: "DevOps Tools response workflow"
---

## Overview

## Workflow

1. Go through the tickets in Zendesk `Website comments` view
2. See if all comments have received responses
3. Write the response if necessary, involve an expert for assistance if you don't know the answer
4. Post the comment on the original website (not Zendesk) using the link provided in the ticket
5. Solve the ticket with the `Replied` macro (Replied macro will use the public response field in order to track the first reply time)

## Best practices

Where relevant, invite experts who can help answering the comments to the `#devops-tools-comments` Slack channel. This provides a quick way for them to monitor the comments without having to log into Zendesk, and it also brings more eyes to the comments.

As a Community Advocate, you can use the Slack comment to ping experts directly when you need assistance answering a particular question.

## Automation

All the comments from our blog are handled by Disqus. There's an integration with Zapier in place which pipes posts to ZenDesk as tickets and then posts to the `#devops-tools-comments` Slack channel. In Zapier, the integration is under the Community Advocacy folder called `Disqus to Zendesk: devops-tools page`.
