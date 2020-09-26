---
layout: markdown_page
title: "Reddit response workflow"
---

## Overview

The purpose of this is to monitor all mentions of GitLab within Reddit.

<i class="fas fa-hand-point-right" aria-hidden="true" style="color: rgb(138, 109, 59)
;"></i> There is currently no way to filter whether the mention of GitLab is only from a URL ([example here](https://www.reddit.com/r/ProxyScrape/comments/a7p3je/help_us_translate/)), so there may potentially be a high volume of noise.
{: .alert .alert-warning}

<i class="fas fa-info-circle" aria-hidden="true" style="color: rgb(49, 112, 143)
;"></i> To request [user flair for the /r/gitlab subreddit](/images/handbook/marketing/community-relations/reddit-flair-example.png), ping `@advocates` in the `#community-advocates` Slack channel, and include your Reddit username. Your flair will read `GitLab Team`.
{: .alert .alert-info}

## Workflow

1. Open each ticket in Zendesk in the `Reddit` view.

2. Navigate to the Reddit thread to see if the comment or post has received a response.

3. Respond if necessary using your **personal** Reddit account
   * Post the comment on the original website ([https://www.reddit.com/](https://www.reddit.com/), not Zendesk) using the link provided in the ticket.
   * See the [Response Strategies section](#response-strategies) for ideas on how to respond and engage.

4. If comment/post does not need a response but is still good or valuable, upvote it and apply the `Upvoted` macro.
   * If it is particularly insightful or useful, it may be a good idea to share it on an appropriate Slack channel for visibility.
   * If you see a comment you want all community advocates to upvote as well, ping `@advocates` in the `#community-advocates` Slack channel.

5. Solve the ticket with the `Advocate responded` macro. (Replied macro will use the public response field in order to track the first reply time)

6. If a comment or post does not require a response, solve the ticket with the `Mention` macro.

## Response Strategies

The following outlines an experiement the advocates are currently working on to increase engagement conversations on Reddit about GitLab.

* NOTE: Typically, the only posts that will need responses are those that are questions, support issues, feedback, or are spreading misinformation. Comments such as "I use GitLab and I love it!" should not be replied to as they would on other social media platforms.

Typical Reddit Ticket Categories and Path for Engagement:

Questions:
* This can include questions about GitLab as a product, comparing GitLab to competitors, hiring, developer education, and questions about remote work at GitLab.
* Use the [invovlving experts workflow](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts) to engage experts in answering relevant questions.
* Share [devops tools](https://about.gitlab.com/devops-tools/) pages in conversations comparing GitLab to other tools.
* NOTE: Engagement in these conversations should be focused on providing facts, not opinion. Consider sharing devops tools in threads where users are looking for a tool to provide a solution to their problem.

Support Issues:
* These are often are posted on the [/r/gitlab subreddit](https://www.reddit.com/r/gitlab/).
* Most new posts on the /r/gitlab subreddit should have responses.
* Point the user to relevant docs, issues, or the forum for additional support.
* If needed, [ask an expert for help](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts).

Feedback:
* Use the [invovlving experts workflow](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts) if feedback is directed to a specific team or functionaly of GitLab
* Upvote general positive feedback.
* Do not downvote critical feedback, unless it spreads misinformation. For example, don't just downvote because someone doesn't like the product or mentions a competitor

Misinformation:
* Downvote comments that spread misinformation.
* Reply with evidence in the form of docs, issues, etc. with explaination of truth.

   
## Best practices

* Always be kind and understanding, no matter how the other person acts.
* If you are new to Reddit, it may be useful to review this [beginner's guide](https://lifehacker.com/a-beginners-guide-to-reddit-1798643829).
* Use your **individual** reddit account, not a shared company one (although you may request [user flair](https://mods.reddithelp.com/hc/en-us/articles/360010541651-User-Flair). Feel free to use your personal (non-work) account if you prefer. You can request reddit user flair by pinging `@advocates` in the `#community-advocates` Slack channel. User flair brings more visibility to GitLab team members and it's a transparent and effective way to let the wider community that you are part of the organization. It also makes comments seem more authentic and shows engagement in Reddit.
* If you use Reddit a lot, it may be useful to create a separate, more professional (but still individual) work account to interact with the GitLab community as part of your role.
* [Brush up on your "reddiquette"](https://www.reddit.com/wiki/reddiquette)
* [Make sure your comments are well formatted](https://www.reddit.com/wiki/commenting)

## Common Subreddits Mentioning GitLab

* [r/gitlab](https://www.reddit.com/r/gitlab/)
* [r/learnprogramming](https://www.reddit.com/r/learnprogramming/)
* [r/devops](https://www.reddit.com/r/devops/)
* [r/git](https://www.reddit.com/r/git/)
* [r/Ubuntu](https://www.reddit.com/r/Ubuntu/)
* [r/Terraform](https://www.reddit.com/r/Terraform/)
* [r/coding](https://www.reddit.com/r/coding/)
* [r/homelab](https://www.reddit.com/r/homelab/)
* [r/gnome](https://www.reddit.com/r/gnome/)
* [r/sysadmin](https://www.reddit.com/r/sysadmin/)
* [r/Python](https://www.reddit.com/r/Python/)
* [r/selfhosted](https://www.reddit.com/r/selfhosted/)


## Automation

All mentions of GitLab come in as a new ticket in Zendesk via Zapier.

<i class="fas fa-hand-point-right" aria-hidden="true" style="color: rgb(138, 109, 59)
;"></i> If you notice there have been no tickets for an extended period of time, check the `New Reddit Mention` zap in Zapier to make sure it's working. If you aren't sure if it is, ping `@advocates` in the `#community-advocacy` Slack channel.
{: .alert .alert-warning}

There are often bot posts that include GitLab URLs that generate a lot of unwanted noise. There is a step in the Zapier automation to filter posts like this. If you notice a large number of posts coming from a bot, please add it to the denylist by following these steps in Zapier:
1. In Zapier, go to `Zaps` > `Community Advocacy` > `New Reddit Mention`
2. Go to the `Filter Noise` step
3. Select `Filter Setup & Testing`
4. Click `+ AND`
5. For the first dropdown, select `Username`
6. For the second, select `(Text) Does not exactly match`
7. In the third box, paste the name of the bot to exclude
8. Run a test and continue
9. Zapier automatically turns off processes that have been modified, so make sure you turn it back on
