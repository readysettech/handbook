---
layout: handbook-page-toc
title: "Website comments workflow"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Workflow

- When the queue of the comments is manageable:
  1. Go through the tickets per-post
  1. See if all comments have received a response
  1. If any comment needs a response, open the link from the ticket and respond **from your personal Disqus account** outside of Zendesk
  1. Solve the ticket with the `Replied` macro (Replied macro will use the public response field in order to track the first reply time)


- When there is a backlog and you're trying to respond to every comment as quickly as possible:
  1. Go through the tickets per-post
  1. See if all comments have received a response
  1. Post the comment on the original website (not Zendesk) using the link provided in the ticket
  1. Solve the ticket with the `Replied` macro (Replied macro will use the public response field in order to track the first reply time)
  
## Best practices

Monitor the `#docs-comments` and `#mentions-of-gitlab` Slack channels for possible internal discussions

Blog comments, Docs Comments, and Dev Tools comments will all appear in the Website Comments Zendesk view. Be sure to check which platform you are responding.


## Docs Comments and Dev Tools Comments

Many docs comments will require expert involvement. Follow the [involving experts workflow](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts/) when necessary.

To find the correct expert to ping, visit the [DevOps Stages page](/handbook/product/product-categories/#devops-stages) and locate the technical writer for the specific stage.

## Automation

All comments from our website are handled by Disqus and we developed a native Zendesk integration for them - [Tanukidesk](https://gitlab.com/gitlab-com/marketing/community-relations/community-advocacy/tanukidesk). It pipes these posts to `website comments` ZenDesk view as tickets.
