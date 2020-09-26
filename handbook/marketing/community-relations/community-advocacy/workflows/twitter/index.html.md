---
layout: handbook-page-toc
title: "Twitter response workflow"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Overview

### Handles

| HANDLE | RESPOND FROM | GUIDELINES |
| - | - | - |
| [@GitLabStatus](https://twitter.com/GitLabStatus) | Zendesk | Post service updates |
| [@GitLab](https://twitter.com/GitLabs) | Zendesk | Respond to mentions and questions |
| [@MovingToGitLab](https://twitter.com/MovingToGitLab) | Tweetdeck | Respond to mentions and questions |

- The [@GitLabStatus](https://twitter.com/GitLabStatus) account should only be used to give updates on the availability of [GitLab.com](https://gitlab.com) and to follow up on users reporting that [GitLab.com](https://gitlab.com) is unavailable or responding to a previous availability update on [@GitLabStatus](https://twitter.com/GitLabStatus).
- Only the infrastructure team should be posting updates on [@GitLabStatus](https://twitter.com/GitLabStatus). There is a [defined process](/handbook/engineering/infrastructure/incident-management/) for this describing who should do this, how and what channels should be alerted.
- When a tweet mentions more than one handle described above, always reply from the main [@GitLab handle](https://twitter.com/GitLab), unless it's about GitLab availability status
- If a wrong handle is used in a response, take note and respond from the correct one in the follow-up (if there is one)

## Workflow

<i class="fas fa-hand-point-right" aria-hidden="true" style="color: rgb(138, 109, 59)
;"></i> All initial Twitter responses should be sent from Zendesk. If a follow up tweet from a user warrants a response, follow the Tweetdeck workflow below.
{: .alert .alert-warning}

- Reply to almost all tweets, following the [social media guidelines](/handbook/marketing/social-media-guidelines/), regardless of whether the tweet is of a technical nature or not.
- Follow up with the support team if the issue is too complex to handle.

When resolving Twitter tickets in Zendesk you should:

1. Use [Play mode](https://support.zendesk.com/hc/en-us/articles/203690856-Working-with-tickets#topic_avj_hfg_vt) in the Twitter view. The default Twitter view will sort tickets by created date (ascending).
1. Not skip any tickets
1. Assign the ticket to yourself or ask in the appropriate chat channel if you don't know how to answer it
1. Not cross assign tickets

## Best practices

## General

- Tweets use short links which require you to visit that link to make sure you understand the context.
- Clarify if the request refers to GitLab.com or an externally hosted GitLab instance as we can only handle requests for [GitLab.com](https://gitlab.com).


### Tweets regarding GitLab downtime

Check if we're experiencing any issues with our system on [GitLab System Status](https://status.gitlab.com/) page or if there were any official updates on our [Twitter GitLab.com Status](https://twitter.com/gitlabstatus/) profile. If you find anything that might be related, please follow up with the user forwarding that link and asking if they are still experiencing issues. 


### Support Related Questions

Often, users will tweet their support related questions to the main @gitlab account. Solving support related questions via twitter is not the preferred method, as the character limit is difficult to work with, and resolutions could be lost for future use.

The [involving experts workflow](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts/) can sometimes be an effective way to response to users. In addition, advocates should consider utilizing the GitLab support zendesk instance to find sharable resources, or direct users to post their question on the [GitLab Forum](https://forum.gitlab.com/)

#### Using GitLab Support Zendesk

*  All advocates should request access as a ['Light Agent' on the Support Zendesk Instance](/handbook/support/internal-support/#viewing-support-tickets) during onboarding.
*  From the support related tweet, pull out keywords that best describe the user's problem. Try to keep these to short phrases to avoid limiting your Zendesk search.
*  In the support Zendesk instance, use the search function to sort through all support tickets with these key words.
*  To find new information about bug reports, status issues, or urgent matters, click on the 'Updated' column to sort the newest tickets to the top of the results. 
*  To find solved tickets that address common issues GitLab users face, but that are not restricted to time, add `status:solved` to your search.
*  Skim through the first few tickets to see if you can find a user who has submitted a similar question. In this step, the advocates needs to do a little bit of searching to find related issues, solutions, or resources to share back with the user.
*  If the advocate can find an issue link or resource to share in a short tweet, they should respond from the @gitlab account via Zendesk.
*  If the question involves a detailed response, they should use the [steps to direct users to the forum](#directing-users-to-the-forum).

#### Directing Users to the Forum

Advocates should first try to find a related question in the forum and share a direct link asking for input. If no similar post exists, share the link to the most appropriate forum category.

Consider using language like this in your tweet to best encourage forum use: 
* `Posting in the forum allows the GitLab team and the wider community to help find solutions for your needs, create issues for long-term solutions, and update our documentation.` 
* `In order to troubleshoot your issue, please post your question in our forum at https://forum.gitlab.com! This way you'll have the whole power of the community to help.` 
* `It's likely these community experts will be able to help: (link to forum topic) since they have worked through something similar before. Post your question and we'll check in on it!`

Related experts can be found in [#support_gitlab-com](https://gitlab.slack.com/messages/support_gitlab-com), [#support_self-managed](https://gitlab.slack.com/messages/support_self-managed), and [#support_managers](https://gitlab.slack.com/messages/support_managers) in Slack.

#### Escalate a Support Ticket

Users will often tweet to bring attention to a ticket they submitted to support. Advocates can respond by

* Asking the user for their ticket number and searching the Support Zendesk instance to check on the status
* If the ticket has not been addressed, [follow the Slack process to raise attention to a support ticket](/handbook/support/internal-support/#i-want-to-escalate-a-ticket)
* Respond back to the user to let them know you've reached out to support, and that the team is working on their request.


### Usage of Likes

Use "Likes" on Twitter for promoting positive feedback about our product, since we direct users there when we want to show that people really love the product. Avoid using it for anything else.

### Retweeting

Advocates shouldn't retweet anything from the official GitLab Twitter accounts. If you see something that should be retweeted, paste the tweet in [`#social_media_action` Slack Channel](https://gitlab.slack.com/archives/C4UGNMF9A) for the social team to review.

### Direct Messages

We have direct messages disabled in our Twitter accounts, but they can be used if we first send a direct message to a user. This should only be used when the user needs to communicate with us privately (e.g. to give a mailing address).

## Automation

Tweets that mention [@GitLab](https://twitter.com/GitLab), or [@GitLabStatus](https://twitter.com/GitLabStatus) will create a ticket in Zendesk, and show up in the "Twitter" view.

If a tweet is responded to from TweetDeck, this risks duplicate responses. Responding from Zendesk also enables us to track our response times vs. [our internal SLA](/handbook/support/#sla).

## Tweetdeck

The Twitter/Zendesk integration does not correctly thread Twitter conversations. Follow-up tweets sent via Zendesk will appear as a response to the user's first tweet rather than any subsequent tweets. To work around this, advocates use Tweetdeck to respond directly from the @Gitlab account.

If a user's response to your initial tweet sent from Zendesk warrants a response, open the tweet in Tweetdeck. Respond directly to the tweet via Tweetdeck. Add a link to your response in an internal note on the Zendesk ticket.

Tweetdeck can also be used to delete tweets if something is sent accidentally from Zendesk.

