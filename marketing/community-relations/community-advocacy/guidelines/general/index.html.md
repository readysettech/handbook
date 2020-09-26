---
layout: handbook-page-toc
title: "General guidelines"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Handling mentions

### Urgent and important mentions

It's important to be able to recognize events that are both _important_ **and** _urgent_. Some might be important but not urgent, others urgent but not important while some are neither important nor urgent. However, mentions that are both urgent and important should be handled as top priority. [HackerNews](#hacker-news) is a channel that commonly sees this type of mentions.

* **Important mentions** are mentions whose content bears a lot of weight and is important to the company - it's often content about our policies, product and/or marketing pieces (blog posts, articles, etc.)
* **Urgent mentions** are mentions whose content is time-sensitive by nature - often when the spotlight and discussion enthusiasm are perishable - such as HackerNews threads

These mentions might be intimidating and/or hard to answer by yourself. Please [involve several topic experts](/handbook/marketing/community-relations/community-advocacy/workflows/involving-experts) to respond instead.

When this type of mention comes up during a weekend, please ping more people than you would usually do. It's not considered rude (anyone and everyone can always snooze Slack notifications during weekends), you're just increasing the chance someone sees it in time.

#### Examples

|Mention|Important|Urgent|Explanation|
|-|-|-|-|
|<https://news.ycombinator.com/item?id=17032274>|✖|✖|The OP mentions GitLab out of context.|
|<https://news.ycombinator.com/item?id=17101902>|✖|✓|This required an urgent response because the thread momentum was very perishable.|
|<https://news.ycombinator.com/item?id=16914775>|✓|✖|The OP expressed dissapointment with his support experience - This is important to address, but not time sensitive (a one or two hour response time woudln't have any difference in impact compared to a 6h response time).|
|<https://news.ycombinator.com/item?id=13537052>|✓|✓|Content is volatile and affects a lot of users and the company image. This needed to be addressed as soon as possible and with care.|

## Community interaction archetypes

### Stability complaints

- Apologize for the inconvenience
- Search for an active issue that could be the cause of instability (deployment downtime, load spikes, ...)
    - [Sentry](https://sentry.gitlab.net/gitlab/)
    - [Infrastructure Issue Repository](https://gitlab.com/gitlab-com/infrastructure/issues/)
    - [`production`](https://gitlab.slack.com/messages/production) Slack channel
- Determine if the user is still affected
- Link to the relevant issue

### Feature requests

- Look for existing issues for the feature request and ask for input on the issue
- If an issue doesn't exist, ask the user to open a [new feature request issue](https://gitlab.com/gitlab-org/gitlab/issues/new?issuable_template=Feature%20proposal)
- Thank the user for the contribution (See [our Social Media Guidelines](/handbook/marketing/social-media-guidelines/))
- Link back to the community member to provide further feedback on the issue

### General questions and issues with gitlab.com

- Gauge the complexity of the question
- Search related issues / documentation
    - [GitLab CE Issues Tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues/)
    - [GitLab Documentation](http://docs.gitlab.com/)
- Forward to [forum.gitlab.com](https://forum.gitlab.com) unless it's one of the [supported issues for GitLab.com free users](/support/statement-of-support.html#free-plan-users) or a client, in which case redirect to [open a support ticket](https://support.gitlab.com).

### Reports of Spam

Users might take to Twitter to report instances of spam on the [GitLab.org Issue Board](https://gitlab.com/gitlab-org/gitlab/issues). To report this, post in the [#abuse slack channel](https://gitlab.slack.com/messages/abuse) with a link to the issue board and the timing of the spam report. Respond to the user and thank them for getting our attention on the issue.

The same workflow can be applied for spam reports that come through on other social channels, however, Twitter is the most common place for these reports.

### Bug Reports

- Search for existing issue on the [GitLab's Issue page](https://gitlab.com/gitlab-org/gitlab/issues)
- Try to reproduce the bug
- Ask the community member to open one of the following issues:
     - [New Documentation Issue](https://gitlab.com/gitlab-org/gitlab/-/issues/new?issuable_template=Documentation)
     - [New bug report](https://gitlab.com/gitlab-org/gitlab/-/issues/new?issuable_template=Bug)
     - [General production issues](https://gitlab.com/gitlab-org/gitlab/-/issues)
- If you don't want to ask the community member to open an issue, you can open an issue and share the link with them:
    - [GitLab CE Issues Tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues/)
    - [GitLab EE Issues Tracker](https://gitlab.com/gitlab-org/gitlab-ee/issues/)
    - Label the issue
- Link back to the community member
- (Optional) Link in the appropriate chat channel

### Reports of credential stuffing events

- Connect with the Security team in the [#security Slack channel](https://app.slack.com/client/T02592416/C248YCNCW/thread/C248YCNCW-1590526482.323800) for up-to-date information and communication guidance for specific events
- Consider one of the following response templates:
     - `Thanks for reaching out! Our team has seen increased activity around cred stuffing lately. If you believe your account could be affected, visit the GitLab sign-in page and select "forgot password": https://gitlab.com/users/sign_in .`
     - `Unfortunately, cred stuffing is becoming increasingly common. Our secops team works to limit the impact of active attacks. Users should be sure to create strong, unique passwords for every site/service (a password manager can help) and enable #mfa: https://gitlab.com/profile/two_factor_auth`

### Feature Requests

- Search for an existing [GitLab feature proposal issue](https://gitlab.com/gitlab-org/gitlab/issues)) and ask the community member to contribute to the discussion.
- If an issue doesn't exist, share the [New feature proposal](https://gitlab.com/gitlab-org/gitlab/-/issues/new?issuable_template=Feature%20proposal) issue template and ask user to open a new issue

### General positivity

Tweets expressing positivity about GitLab.

- Like the message
- Respond positively

Sample responses:

- "Thanks for using GitLab."
- "Thanks for writing about GitLab."

### Choosing the Correct Zendesk Macro

Zendesk macros serve two main purposes in the Community Advocate workflow: 

1. They simplify and speed up processes in Zendesk
2. They help organize and provide data on what the team focuses on, via tags and status 

#### Commonly Used Zendesk macros are: 

**No Response**

Just as important as finding the right expert, or engaging in a friendly way, is knowing when *not* to engage. When our judgement or a process tells us not to engage in a mention online, we use one of the macros in the parent `No Reponse` macro. You will see details further drilled down into reasons for choosing not to respond. (ex. `No Response::Media Mention`, `No Response::IPO status`, `No Response::Non-English`, etc.) Choose the appropriate macro under the parent `No Response` macro and it will automatically provide a private note in the ticket, and will leave the ticket in an Open or Solved state, depending on the macro.

**Involving Experts**

Use these macros when you have reached out for an expert's assistance, and again once the expert has answered. The parent macro is `Involving Experts` and the choices are `Involving Experts::Reached out to an Expert`, which will put the ticket in an Open state, and `Involving Experts::Expert Responded`, which will put the ticket in a Solved state. 

**Advocate Responded**

Use this macro when you yourself, or a fellow Community Advocate, were able to resolve or reply. This could be something as simple as a "thank you", providing links to the docs, or an issue, etc. This macro puts the ticket into a solved state.


### Others

- EE Customer issues / GitHost customers / anyone who cannot access GitLab.com (including 2FA reset queries) -> Forward to [Support](https://support.gitlab.com)
- For issues related to our marketing site -> Forward to [www-gitlab-com Issue Tracker](https://gitlab.com/gitlab-com/www-gitlab-com/issues)
- For issues related to self-managed instances -> Forward to [Community Forum](https://forum.gitlab.com)


### Special types

- Event Sponsorship Requests -> Forward to [emily@gitlab.com](mailto:emily@gitlab.com)
- Spam -> Mark as spam
- GitLab package reported as compromised -> [immediately stop packagecloud via Slack](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/stop-or-start-packagecloud.md)
- Any kind of political questions / remark (even if they're just asking if we're politically neutral or not) -> Do not respond (They tend not to be productive.)

## External resources

When responding to community messages, you may face a situation where our documentation doesn't have an official solution. In these circumstances, you can consider replying with a link to an external resource.

Before that, consider documenting the missing piece. It is time-consuming, but it saves time for both you and your colleagues when this comes up again. Respond after updating the documentation. This approach encourages immediate documentation improvements/edits, and it allows avoiding all external resources. If you have any questions about writing the documentation, ask the relevant Technical Writer or Product Manager. When your content is ready, assign it to one of them for review.

If you determine that this question is too specific for our documentation and decide to use an external resource, please make sure that:
* The author has a solid reputation - we don't want to share suspicious posts
* The post isn't related to [countries we don't do business in](/handbook/sales-process/images_sales_process/#export-control-classification-and-countries-we-do-not-do-business-in-)

## Notes / remarks

- When asking something in Slack that's relevant for a ticket, leave a link to the chat message as an internal comment in the ticket
- Always be sure to check if an issue (bug or feature proposal) exists before opening one / asking a user to open it

## Topics where Community Advocates Don't Respond

There are some common topics that surface in our community where the advocates team does not respond or engage experts.

Exceptions can be made if these are pressing issues, or if an expert is needed to correct misinformation. It's best practice to collaborate with Legal or External Communications teams before making these exceptions.


| Topic | Why We Don't Engage |
| ------ | ------ |
| Location Based Pay | Most participants in these conversations already have their mind made up on their perspective of our compensation model. Many conversations will naturally share relevant links from GitLab. There is no new information we can add to these conversations, and involvment on our part could just make people in the conversation angry. |
| GitLab's IPO Status & Being a Public Company | Anyone can read about [the company's goals and plans in the handbook](/handbook/being-a-public-company/#gitlab-as-a-public-company), however, use caution when dealing with these questions and err on the side of not commenting at all. Experience tells us that this conversation moves quickly to speculation and assumptions. |
| Country Specific Hiring Restrictions | All information about country hiring guidelines can be found in our [GitLab Jobs FAQ section](https://about.gitlab.com/jobs/faq/#country-hiring-guidelines). We can share this list if users are asking questions, but we can add little value if users are angry about the policies. |
| Harasment by Community Members | We do not engage with members of our community who harras anyone on the GitLab team, or who do not follow our [Code of Conduct](https://about.gitlab.com/community/contribute/code-of-conduct/). |
| Politically Sensitive Topics | We do not engage with politically sensitive topics unless there is a clear company response relayed to the advocates. If an advocate is unsure whether we shouldn't respond to a topic, we should reach out to [corporate communications](/handbook/marketing/corporate-marketing/#corporate-communications-and-pr-public-relations) for clarity. |
