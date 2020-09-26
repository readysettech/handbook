---
layout: handbook-page-toc
title: "Release Day Duties"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Overview

On the 22nd of every month the GitLab engineers and Product Management team releases a new version of GitLab. Typically a new release triggers a spike in community mentions around the 22nd. To help deal with communication and the infulx of community mentions online, we have a dedicated release day DRI Advocate that owns the effort of keeping the advocates team up to date on new release information. This way the Advocates team can effectively involve experts in community mentions on/after a release.

The two channels that we see the biggest increases in mentions and discussions are:

* [The GitLab blog](/blog/)
* [HackerNews](https://news.ycombinator.com/news)

The Release Day Advocate is different every time, and the responsibility rotates on a monthly basis. If the release day takes place on a weekend, one of the advocates is assigned to monitor traffic and to process mentions. We keep track of the monthly assignments on the [Community Advocates team calendar](https://calendar.google.com/calendar?cid=Z2l0bGFiLmNvbV9xbWM0aXNycGtyNWZyOTlucDZkYnFrbXUwMEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t).

On release day, the best place to go for relevant information is the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ). The channel description of this channel is updated each month with links to the relevant release merge request, preview page, and review app.

### Responsibilities of the advocate DRI Include:
* Connecting with release day Product and/or Engingeering managers leading up to the release
* Communicating important changes and information back to the Advocates team
* Compiling relevant expert outreach data
* Attending the release's retrospective meeting. If this meeting is not within advocate's working hours, it is fine to add notes and data asynchronously to relevant retrospective issues instead.

Note: It is not the sole responsibility of the advocate DRI to take on all expert outreach and involvement for related release day mentions. Instead the DRI will serve as the main point of contact between release day managers and the Advocates team.


## Action Items for Release Day Advocate DRI

On the 15th of the month, a reminder message is generated using the Slack bot to the [#advocates-fyi Slack channel](https://app.slack.com/client/T02592416/C016JETG68Y), as a reminder for the Advocate DRI to review and take action on the following tasks.



### Week Before Release Day Tasks

1. Confirm an Advocate as the DRI for Release Day. The team should consider choosing coverage for 2-3 months ahead of time during daily planning calls. Assignments can be found on the [Community Advocates Google calendar](https://calendar.google.com/calendar?cid=Z2l0bGFiLmNvbV9xbWM0aXNycGtyNWZyOTlucDZkYnFrbXUwMEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t).
1. Before the 18th of the month, review the Preview Page, linked in the channel description of the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ). This will have the most up to date information regarding the next release.
1. After the 18th, review the Release Post Blog View App, also linked in the channel description of the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ) for a finalized list of what new features and changes will be included in the release.
1. The author of this blog post is the Release Day Manager.
1. Reach out to the Release Day Manager in the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ) to confirm they understand the expert outreach process, and to expect pings around the release from the community advocates. Use the following template as an example for outreach:

   ```
   Hi @[release-post-manager] ! Just wanted to touch base here quick before release day - the advocates team will likely be reaching out to you on release day for support in responding to community members/engaging the right GitLab experts in our community response. Thanks! :smile: @advocates FYI
   ```

1. If the content of the release is anticipated to generate an increase in questions, consider engaging with an [Advocate-for-a-day](#advocate-for-a-day) in advance.
1. Begin drafting the highlights post for HackerNews, and ask Advocates team for feedback.

[Example](https://gitlab.slack.com/archives/C3TRESYPJ/p1595266837163300)

### Day Before Release Day Tasks

1. Review the final review app for last minute updates.
1. Share a summary post in the [#advocates-fyi slack channel 
](https://app.slack.com/client/T02592416/C016JETG68Y/) that includes:
	1. a link to the view app
	1. the name of the release post manager
	1. a reminder to post about how to find experts in the #release-post channel
	1. which slack channels (or otherwise) to reach experts for highlighted release content
	1. any additional important notes about the release that Advocates should be aware of

[Example](https://app.slack.com/client/T02592416/C016JETG68Y/thread/C013J9KJTDX-1595365983.016300)

### Release Day Tasks

On release day, a reminder message is generated using the Slack bot to the [#advocates-fyi Slack channel](https://app.slack.com/client/T02592416/C016JETG68Y/), as a reminder for the Advocates to watch for an increase in mentions, and to utilize the #release-post channel for expert outreach.

- Monitor the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ) throughout the day to be ready at the time the release blog post is published. (note: the timing varies month by month.)
- If you are on release duty and will be offline for a period of time, let another Advocate know so they can monitor.

[Example](https://app.slack.com/client/T02592416/C016JETG68Y/thread/CB16DMSLC-1594796408.481100)

#### Zendesk Tickets

When working a Zendesk ticket that relates to release day, check the `Release Day` box in the left pane of Zendesk before closing out the ticket. This will help the team determine how many Zendesk cases on release day are related to the release. The Community Advocates can leverage this information to ensure that Product Managers and release managers are able to help with cases on release day.

[Example](hhttps://gitlab-community.zendesk.com/agent/tickets/129829)

#### HackerNews Highlight Post

After each new release, a community member posts on HackerNews letting our community know we've had another release. This post, however, is usually pretty simplistic and provides little information at a glance. The Advocates team comes in and replies with a snippet of release day highlights, and links to the blog, so our users know what changes to look forward to.

- Copy the overview of the main features or improvements from the beginning of the release blog post and post it to the HackerNews story that comes out during the release. You can use the template below to help build your highlight post: 
   ```
   Hello! Sharing a few highlights from this release, and links with additional information:
   - Highlight #1 [1]
   - Highlight #2 [2]
   - Highlight #3 [3]
   [1] related link to add context to highlight #1
   [2] related link to add context to highlight #2
   [3] related link to add context to highlight #3
   (optional CTA, point to issues where we're asking for feedback, etc.) 
   ```
- Feel free to post the highlight post as soon as the HackerNews story goes live, there is no need to wait.
- After you've shared the highlight on the HackerNews story, post the HackerNews story link to the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ)

<i class="fas fa-info-circle" aria-hidden="true" style="color: rgb(49, 112, 143)
;"></i> Note: GitLab does not share the release blog post on HackerNews, but rather we wait for a community member to share the post and respond with a highlight comment to spark discussion and point people in the right direction..
{: .alert .alert-info}

[Example 1](https://news.ycombinator.com/item?id=23917493)
[Example 2](https://news.ycombinator.com/item?id=19228781)

#### Reddit Highlight Post

- Go to the [/r/gitlab](https://www.reddit.com/r/gitlab/) subreddit and create a new post (instructions can be found [here](https://www.oberlo.com/blog/what-is-reddit#Start_Posting_and_Commenting_on_Reddit).)
- Choose `Link` and copy the release day blog post URL in the `URL` section (the title will autofill)
- Under the `Link` section, click the drop-down that says `Flair` and choose `release`
- Submit the post
- Copy the HackerNews Highlight Post and add that info as a comment on the reddit post. Reddit supports markdown and hackernews doesn't, so you may want to format the comment, but this isn't necessary

[Example](https://www.reddit.com/r/gitlab/comments/hvvzq9/gitlab_132_released_with_planning_iterations_and/)

#### Expert Outreach

- Reach out to release day managers and relevant experts in the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ) with the following template for expert involvement.

   ```
   Hi @expert_username! [LINK TO COMMUNITY COMMENT] An expert is needed to respond to this question/comment about the current release. Could you please answer on [name of social platform] using your own individual account?  If you don't know the answer, could you share your thoughts and ping a specific release day expert who might? Thanks!
   ```

- The release day manager for the release can help to route expert outreach to the right GitLab team members.
- Product Managers should have a strong overview of who is the best expert for each new feature in the release and can also help us find appropriate team member experts for each release.
- You can see which stage each new release element is part of on the release post blog. Next to each release element, there is a symbol that indicates which stage it belongs to. You can hover over the symbol to see the name of the stage, and then reach out to that stage or group in slack to engage experts.
   - For example: in the 13.2 release, you can see that the [container host monitoring and blocking](https://about.gitlab.com/releases/2020/07/22/gitlab-13-2-released/#container-host-monitoring-and-blocking) belongs to the Defend stage based on the stage symbol. You could reach out for related questions to the #s_defend slack channel.

- Engage our Technical Evangelists using the 'normal' involving experts workflow. The Technical Evangelists are tuned in closely with each release and can be excellent experts to involve in discussions on social channels.
- The Principal Product Manager can also support routing expert outreach to the correct manager or Product Manager, and can support expert involvement if Advocates feel that they can't get a timely response. Reach out in the [#release-post Slack channel](https://app.slack.com/client/T02592416/C3TRESYPJ).

[Example](https://gitlab.slack.com/archives/C3TRESYPJ/p1595436041255700)

#### Send MVP Appreciation Gifts

Every release GitLab chooses a [Most Valuable Person (MVP)](https://about.gitlab.com/community/mvp/) and recognizes them for their contributions. The Advocates team then privately sends them some GitLab swag as a thank you.

Our Code Contributors program manager will choose the MVP of the release. Before release day, the release day manager will tag advocates in the #swag Slack channel, or in the Release Day issue, as a reminder to send swag to the chosen MVP.

1. Determine MVP after merge window closes, see `#release-post` channel
1. Find MVP's contact information
  * An email address is usually stored in git commit data
  * A user might have email or twitter info on their profile
1. Generate a giveaway link from the [GitLab Release MVP Giveaway campaign in Printfection](https://app.printfection.com/account/campaign/overview.php?storeid=291968)
   * Click `+ Get New Link` button
   * Copy giveaway link in pop-over 
   * Click `Mark Link as Sent` once it's sent
1. Congratulate the MVP via email using the merch@gitlab.com email alias, or via Twitter direct message (DM), and share their swag giveaway link
  * If a Twitter DM is the simplest avenue for contacting the MVP, use Tweetdeck to send the (DM) via GitLab's main twitter handle: @gitlab
1. Alert the release day manager that the giveaway has been sent

##### Suggested language for MVP Swag email, or Twitter DM:

```
Congratulations on being the MVP for GitLab's (enter release number here. ex. 13.3) release! 🤸‍♂️

https://about.gitlab.com/community/mvp/

We are so amazed by your work and we want to thank you for your contributions: please enjoy some well deserved GitLab swag! We can't wait to see what you do next!

Link to collect swag: 

(paste printfection link here, and opt to add the printfection code as well)

```


### 1 Week Post-Release Day Tasks

The advocate DRI will run a Zendesk report with the Release Day ticket data prior to the release retrospective meeting and deliver that information to stakeholders at the meeting.

Notes: If this meeting is not within Advocates working hours, it is fine to add notes and data to relevant retrospective issues instead.

#### Expert Involvement on Release Day Report
1. In Zendesk, navigate to the `Reporting` tab
1. On the `Insights` -> `Tickets` tab, hover over the `Tickets Created` metric and click the small dropdown arow that appears.
1. Select `View this Report`
1. Click on the `Filter` tab.
1. Click `Add Filter` and choose the `Select from a List of Values` option. For the first attribute, choose `Release Day`, and for the second attribute, select `True`
1. Select the `Table` report option
1. Take a screenshot or download the data table.

#### Retrospective
1. Post the expert involvement data in the release day retrospective issue.
1. If there is a topic that needs to be discussed about expert involvement or community engagement during the release, the DRI advocate for the release should attend the Retrospective meeting following release day to share and reflect on expert involvement data.
1. If there is nothing urgent to report to the release team, or conversations can remain asynchronous, it is not necessary for the advocates to attend the synchronous retrospecitve meeting.


