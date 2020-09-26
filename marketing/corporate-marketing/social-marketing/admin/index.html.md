---
layout: handbook-page-toc
title: "Social Media Administration"
description: Workflows, Templates, and more for GitLab Team Members
twitter_image: "/images/opengraph/social-handbook.png"
twitter_image_alt: "GitLab's Social Media Handbook branded image"
twitter_site: "gitlab"
twitter_creator: "gitlab"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Welcome to the Social Marketing Administration Handbook Page! Please use the table of contents on the right side of the page to find the topic you need assistance with. 👉

**This page is the single source of truth for all administrative tasks, templates, and processes focused on GitLab brand social channels. If your question is "how?", the answer will be here.**

## Requesting Social Promotion <a name="requesting social promotion"></a>

Many requests for social media coverage could sound like one ask, but ultimately have different end-user objectives or where we'll need to promote different assets or links. Please keep the following in mind to help us better manage requests.

### Open a social + [your focus or campaign] epic

If you are requesting coverage for something that is:

- part of an integrated campaign
- has more than one link/asset/audience/or end-user objective
- will have more than one "deliverable"
Please open a new epic in the Corporate Marketing project. This specific epic will be a place to outline strategies, discuss MVCs and changes, and provide reporting updates. Then, open a social request issue for each specific ask. E.g., for integrated marketing campaigns, there are several collateral (a blog, a webcast, and a gated asset landing page). It would be best to open a "child epic" for Social + Campaign Name and create a separate issue for each piece of collateral.

This will allow us all to better understand due dates, milestones, and to close issues promptly when the specific request is fulfilled.

If you're not sure if you need an epic or just an issue, feel free to ask in the #social_media Slack channel.

### Open a new issue to request social coverage

Once you've opened the epic (if the ask is a part of the list above)

- Head to the [corporate marketing project](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues) and create a new issue.
- Select the appropriate issue template:
    - **social-event-request** for coverage of events (tradeshows, etc.)
    - **social-team-advocacy** when the project calls for GitLab Team Members to support our campaign efforts on their personal social channels
    - **social-general-request** for every other request
- Fill out as much information as you can above the first line in the issue.

### Things to remember about social media requests

- For an anything to get promoted on social, **there must be a dedicated social issue**.
- If the need is urgent, send a message to the `#social_media_action` Slack Channel.
- If you have already requested or received images for social (paid) ads, please mark that issue as related in the organic social request issue.
- If you have not already requested or received images: Shortly after you open your social issue, the social team will assess whether there are existing assets we can use on social, or if new ones are needed. They will then request new images from the design team, or remove them from the issue. It is at the design teams' discretion whether they have time to create the images, particularly if you open your issue within ~ 1 week of the need to publish.
- Sometimes it is not possible to schedule posts when desired due to any number of reasons, but the social team will work with you to make sure you're supported.
- The social team reserves the right to not publish for a myriad of reasons including crisis moments, calendar priorities, and other elements. We'll do our best to explain why when asked.

## #️⃣ Organic Social Overview of Integrated Campaign Promotions

The goal of organic social promotion on an integrated marketing campaign is to strategically bring awareness to a designated landing page.

By tailoring polished messaging to our target audience across the [GitLab branded social media channels](/handbook/marketing/corporate-marketing/social-marketing/#primary-social-channels-audiences-and-calendaring-) we are able to drive page views, sessions, engagements, and link clicks. The content that organic social will promote, falls under the awareness funnel that is also mapped out by MPMs in the GANNT sheet under the content journey map and bill of materials.

Integrated Marketing Content promoted on the [GitLab branded social media channels](/handbook/marketing/corporate-marketing/social-marketing/#primary-social-channels-audiences-and-calendaring-) include a combination of blog posts, webinars, case studies, and more. It is important to explain that what is shared via organic, is different than what is advertised through paid social and digital ads. The social media team will not craft copy for content pieces that are mapped in the consideration and purchase funnels.

In an effort to continually improve our ability to derive success of organic social campaigns, a reporting issue will be added to the Organic Social Epic that pulls data from Sprout Social and Google Analytics on a monthly basis.

### 🗓️ Campaign Planning

The social team will create a social-specific child epic for every Organic Social promotion that is tied to an integrated campaign. Marketing Program Managers will open individual issues for each organic social request and relate it back to the specific Organic Social Epic.

1. Integrated Campaign Epic
1. Organic Social: Campaign Name [Integrated Campaign] Epic
1. Organic Social General request issue: content piece name followed by campaign name
1. Relate social back to Organic Social Epic

### Organic Social Epic Creation

The Social Media team member responsible for the promotion of an integrated campaign will create the epic with the following structure - details and links to be added upon creation of documents and timeline defined.

## Organic Social Campaign Epic Template

Epic Name: `Organic Social: CAMPAIGN NAME [Integrated Campaign] Epic`

```
## #️⃣ Organic Social Overview of the CAMPAIGN NAME [Integrated Campaign]

This is the child epic, organizing the issues for the **CAMPAIGN NAME** integrated campaign. The related issues will be included below upon rollout of each piece of content listed in the Awareness category of the GANNT Sheet and its [Content Journey Map]. 

 ## How often will `@gitlab` post?

Frequency of posts will reflect the content in the awareness category. As content goes live- frequency will increase. We will schedule posts per piece of content to expand over the next few months mirroring an always on approach.

## Is there a hashtag `@gitlab` will be using?

Yes. We will base hashtags off of the content we are sharing. These include (but are not limited to) `#INSERT HASHTAGS`

*Please see related issues for details related to specific organic social promotions.*

## High Priority Links

* [Campaign Execution Timeline (GANTT) >>] - Owned by MPM
* [Campaign Brief >>]
* [Live Campaign Page >>] 

## 🔗 UTM for tracking URLs

* Overall utm_campaign - **`INSERT UTM`** 
* More on [when](/handbook/marketing/marketing-sales-development/online-marketing/#url-tagging) and [how](https://docs.google.com/spreadsheets/d/12jm8q13e3-JNDbJ5-DBJbSAGprLamrilWIBka875gDI/edit#gid=0) to use UTMs
```

## Adding Frontmatter to GitLab-owned pages for proper social sharing

When sharing a link on social media, all channels will look for opengraph frontmatter information, allowing the sites to pull a social media sharing card. This includes unique specifics for the page like its title, a description, and a unique image. It's critical that all pages intended to be shared across social media sites have this informaton attached, so that our users are aware of where we're linking them to, as well as, following best practices.

Social Media Sharing tags are set by the post or page frontmatter. Please use the following template and add it to the frontmatter:

``` yaml
title: your page title/cta
description: page description
twitter_image: "/images/opengraph/file-name.png"
twitter_image_alt: "describe the image being used here"
twitter_site: "gitlab"
twitter_creator: "gitlab"
```

Be sure to update the `title`, `description`, `twitter_image`, `twitter_alt_image`, and other non-social tags necessary for your page. The `twitter_site` and `twitter_creator` tags should remain the static value: "@gitlab"

### Description

The `description` meta tag is important for SEO, but it's also a part of Facebook and Twitter social cards. The `description` should be a short summary of the page. You can think of this as a subtitle.

The description is not meant to repeat the post or page title, use your creativity to describe the content of the post or page. Try to make your description less than 100 characters, if possible.

### Twitter_image

Adding an image file to the frontmatter for `twitter_image` should be added to the [www-gitlab-com] project at `/images/opengraph/` and must be named after the page's file name. While listed as an image for Twitter, this code works for all social sharing sites.

### Twitter_image-alt

It is important to be as inclusive as possible, which is why providing an alternative text for your image is necessary. Image alt's provide a written summary of what is in the image for users who prefer to be read what is in the image vs seeing it, think of users who use screenreaders to read social media. Text included here should not repeat the title or description and it is not another way to add additional SEO properties - you should simply describe the image. Is the picture a group of GitLab Team Members gathering at Contribute New Orleans? Then that is your image alt text.

### Static frontmatter like twitter_site and twitter_creator

This frontmatter aides sites like twitter in understanding how to present additional content. When the link is shared on Twitter, a user may see content that Twitter believes is related to the one shared. This is more of an administrative tag that assists on the backend. These values will always be the same and do not require you to update them.

### Testing frontmatter

Frontmatter requires a merge, therefore, you'll need to include this as a step in page creation. Once merged, please test your link. Preview the social cards by adding your link to the [Twitter Card Validator], or the [Facebook Debugger].

## UTMs for tracking URLs

UTMs are used to track traffic sources & reach of posts/links. All posts that contain GitLab-owned URLs must contain a UTM parameter.

### [Organic Social Media UTM Creating Sheet](https://docs.google.com/spreadsheets/d/1RJiPE11ZdFpP7R4vSx3PQPX5V2mr2SCYS39bYLsJEvY/edit?usp=sharing)

[The social team manages their own social media UTM tracking sheet. Viewable to all parties, this sheet is managed only by the social media team.](https://docs.google.com/spreadsheets/d/1RJiPE11ZdFpP7R4vSx3PQPX5V2mr2SCYS39bYLsJEvY/edit?usp=sharing)

### Other UTMs for Tracking

Please see [details in the Digital Marketing handbook](/handbook/marketing/revenue-marketing/digital-marketing-programs/digital-marketing-management/#url-tagging). In short, it's important to outline UTM campaign, content, and other variables if you're looking to measure more deeply. Campaign section is a requirement, and is likely connected to your ongoing marketing campaign. If you have questions or are unsure how to tag a URL please reach out to the Digital Marketing team &/or the Social Media Manager responsible for the campaign.

## Labels

Consider our labels as a way to be transparent about our work at every level of our marketing organization. At any given time and at any given level, a Team Member can recall what volume and mix of work is happening. Not only does this help the social team to better organize, but would allow our Team Members up our organization to better understand their entire team, too.

### Required Labels

Every social media-related issue should have the following labels, each of which covers our organization in a broader look further up the chain.

#### Organizing by line of work

- ~"Social Media" (our team)
- ~"Corp Comms" (our department)
- ~"Corporate Marketing" (our organization)

#### Organizing by status of work

- ~"mktg-status::plan" (net-new issues, not yet accepted to work on)
- ~"mktg-status::wip" (issues that have been accepted by a member of our team, added to a milestone)
- ~"mktg-status::review" (issues where the social media team have delivered "proofs" of posts to stakeholder for approval)
- ~"mktg-status::scheduled" (issues where the social media posts are approved, added to Sprout calendar, and the issue can be closed)
- ~"mktg-status::blocked" (when the social team is waiting on additional information, assets, or other needs and cannot yet complete the work in the issues)

#### Optional Labels

More on optional labels will be available soon.

## Giveaways on Social Media

### Giveaways Process <a name="giveawaysprocess"></a>

**Pre-giveaway**

1. Contact the social media team in the #social_media_action Slack channel to discuss the details and thoughts about the giveaway. If it makes sense, we can commit to supporting the giveaway following legal approval in step 2 below.
1. Work with the legal team to review and approve the contest or sweepstakes. [You can find more info on what legal requires here in the handbook](https://about.gitlab.com/handbook/legal/marketing-collaboration/#contests-and-sweepstakes). Alternatively, [you can head right to the sweepstakes review issue template to file an issue for legal approval](https://gitlab.com/gitlab-com/marketing/marketing-operations/-/issues/new?issuable_template=sweepstakes_legal_template).
1. Once approved, create an issue and tag the Social Marketing Manager to determine the
rules of engagement and the Corporate Events Manager for prizes.
1. Create and publish an [Official Sweepstakes Rules page](#officialrules)

**Post-giveaway**

1. Winners must sign an Affidavit of Eligibility & Liability, Indemnity, and Publicity Release. Use the "Affidavit of Eligibility - Sweepstakes" template found on the google drive.
1. Announce the winners

[Find out more about the swag giveaways here.](https://about.gitlab.com/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/giveaways/)

#### Creating the Campaign

- Set a launch date
- Ask for social image(s) with text (if organic posts only) explaining the offer/ask
- Set an initial deadline for submissions, so you can have multiple pushes at interval & ramp up energy
- Finalize the delivery method: form vs. tweets vs. retweets, depending on the goals of the campaign
    - Pros of a form: Neat, uniform, easy for us to keep track of, no downsides of low engagement (i.e., responses not visible)
    - Pros of asking for submissions via Twitter: we could more easily RT cool responses, get more out of a hashtag, etc.
    - Pros of asking for RTs in exchange for swag: very little backend to do on social afterwards, except to announce the winners of swag
- Finalize the ask, making sure it's extremely clear what you want to happen (`Share your GitLab story!` `Tell us your favorite thing you made with GitLab` `tell us a time GitLab helped you out of a tight spot`)
    - Make sure the ask can be intuitively communicated via whichever delivery method you're using, i.e., the tweet doesn't need to explain everything if you're pointing to a form or blog post. If you're not pointing to anything, make sure the tweet plus possible image text must make sense by themselves. Use threads for more space!

#### Pre-launch

- Finalize the timeline for when the reminders/follow-ups will go out, add to social schedule and leave some space around them to RT/engage with responses
- Finalize copy for all pushes
- If swag is involved, create a google sheet with swag codes from the Event Marketing Manager
- Finalize hashtag
- Ask community advocates to review all copy (tweets, form, blog post) and adjust according to their suggestions
- Make sure the community advocates are aware of the campaign timeline/day-of
- Designate a social point person to be "on duty" for the day-of and one person who can serve as backup
- Let the broader GitLab team know that the social campaign is upcoming and ask for their support

#### Day of giveaway

- If you have entries for the giveaway in a spreadsheet, use [random.org](https://www.random.org/) to generate a random number. Match the number to the corresponding row in your spreadsheet to identify the winner. **Never enter email addresses or personal information of participants into a third-party site or system we do not control.**
- Try to schedule first push or ask a team member to tweet the first announcement early (ex: around 4 am PT) to try to have some overlap with all our timezones
- If you're asking for RTs in exchange for swag, make sure there's a clearly communicated cut-off to indicate that the giveaway will not stretch into perpetuity. One day-long is probably the longest you want a giveaway to stretch, or you can limit to number of items.
- Plan to engage live with people
    - If your promise was to give away one hoodie per 25 RTs, do it promptly after that milestone is crossed. It adds to the excitement and will get more people involved
- Announce each giveaway and use handles whenever possible, tell them to check their DMs
- DM the swag codes or whatever the item is
- In your copy, directly address the person/people like you are chatting with them irl
- RT and use gifs with abandon but also judgment

#### After the Giveaway

- Thank everyone promptly, internal & external
- Write in the logistics issue of any snags that came up or anything that could've gone better
- Amend hb as necessary for next time

### How to Create an Official Sweepstakes Rules Page <a name="officialrules"></a>

1. Create a new directory in `/source/community/sweepstakes` in the www-gitlab-com project. Name the directory the same as the giveaway `/source/community/sweepstakes/name-of-giveaway`
1. Add an index.html.md file to the `/name-of-giveaway/` folder
1. Add the content of the Terms and Conditions provided by Legal during your [Pre-Giveaway process](#giveawaysprocess) to the `index.html.md` file.
1. Create merge request and publish.

## Sprout Social

### Tagging

##### Tag a post after its been published

Tags in Sprout enable social to measure performance outside of general level metrics. If a post needs a tag but did not get one when scheduled, we'll need to tag the posts after they've been published. While this can happen from forgetting to add the tag in Sprout, its most often related to publishing natively on channels. E.g. when we use Twitter Ads/Media Center to publish unique card content or when publishing stories in Instagram.

To tag a post after its been published:

1. head to the `reports` tab
1. select the `cross-network reports` category
1. choose the `post performance` report
1. use channel and publishing date filters to find the posts you're looking for
1. click the outline of the tag icon 🏷, select the tag(s) for the post; the tag icon will now be blue to indicate there are tags added
