---
layout: handbook-page-toc
title: "Website Handbook"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

GitLab's Marketing Website (about.gitlab.com) is led by the [Growth Marketing Team](/handbook/marketing/growth-marketing/) and anyone can contribute. Please [visit the repo](https://gitlab.com/gitlab-com/www-gitlab-com) to file issues and make merge requests.

## North Star Metric

Metric: Inbound marketing qualified leads.

Specific targets can be found [here](/handbook/marketing/growth-marketing/#goals)

### Supporting Metrics

There are many other digital marketing metrics we track for the website. These include pageviews, unique visitors, time on site, and conversion metrics for key funnels. These detailed metrics are leading indicators for the health of our North Start metric, and are internal to GitLab.

## Objectives

Serve the needs and interests of our key audiences:

1. Users of GitLab: software developers and IT operations practitioners.
2. Buyers of GitLab: IT management, software architects, development leads.
3. Users of and contributors to OSS on gitlab.com.

Generate demand for GitLab by:

1. Showcasing the benefits of the most important GitLab features and how they can save time and money.
2. Compare GitLab vs competing products.
3. Provide customer case studies which illustrate 1 and 2.

## Scope

The GitLab marketing website, or simply the "GitLab Website" refers to all of the content on `https://about.gitlab.com` except the [blog](/handbook/marketing/blog/) and [handbook](/handbook/).

The website does not include
  - The Docs: `docs.gitlab.com`
  - The GitLab.com product: `gitlab.com`
  - The Handbook: `about.gitlab.com/handbook`
  - The blog: `about.gitlab.com/blog`

See [Where should content go?](/handbook/git-page-update/#where-should-content-go) to learn which web property is the most appropriate place to put different types of content. To learn what section of the website different content belongs see [definitions](#definitions).

## Pages supported by Strategic Marketing

The Growth Marketing team supports the design, devleopment, and strategic integration of the following pages with content from Strategic Marketing. You can see the performance of these pages in the [Strategic + Growth Marketing dashboard](https://datastudio.google.com/u/0/reporting/954b4ace-e2ba-4bf6-92ad-848a48a309f2/page/pBbcB). 

- Comparison pages in `about.gitlab.com/devops-tools/`
- Solutions in `about.gitlab.com/solutions/`
- Learn in `about.gitlab.com/learn/`
- Product pages in `about.gitlab.com/stages-devops-lifecycle/`
- Customers in `about.gitlab.com/customers/`
- Analyst Reports in `about.gitlab.com/analysts/`

## Definitions

### Topics

A topic is an industry trend, theme, or technology related to GitLab and our customers. For example, DevOps, GDPR, Containers, etc. Topic pages on our website educate the reader about the topic and share GitLab’s point of view while providing additional links to resources related to that topic. These pages are intended to attract search traffic.

Topic pages should exist at the root level of the website without being nested inside of another directory. e.g. `/continuous-integration`

Examples of other companies who have topic pages:
- [https://www.redhat.com/en/topics/containers](https://www.redhat.com/en/topics/containers)
- [https://pivotal.io/containers](https://pivotal.io/containers)
- [https://pivotal.io/topics](https://www.redhat.com/en/topics/containers)

### Solutions

A solution is a combination of products and services that solve a business problem. For example, accelerating software delivery, enabling remote teams, ensuring compliance, etc. Solution pages on our website show the application of GitLab capabilities and services to address a business problem while providing additional links to resources related to that solution.

Solution pages should be nested inside of the solutions directory. e.g. `/solutions/continuous-integration`

Examples of other companies who have solutions pages:
- [https://www.redhat.com/en/challenges](https://www.redhat.com/en/challenges)

### Product section

The product section of our website has pages that describe what GitLab does and the value provided. The functionality of GitLab is ordered in a hierarchy with 4 levels: Stage, Categories, Capabilities, and Features. You can find details on the [Product Categories Handbook](/handbook/product/categories/)

- Stages relevant to users are listed on the [product overview page](/product) with details about the stage on the [stages page](https://gitlab.com/gitlab-com/www-gitlab-com/issues/2428).
- Categories relevant to users are listed on the [product overview page](/product).
- Capabilities are listed on the category page they belong to. Capabilities may also have their own landing page.
- Features are listed in many places on the website: on the features page, the capabilities page they belong to, the pricing page, comparison pages, and the ROI calculator.

Category pages should be nested inside of the product directory. e.g. `/product/continuous-integration`

Examples of companies who have product/features pages:
[https://mailchimp.com/features/](https://mailchimp.com/features/)
[https://www.groovehq.com/features](https://www.groovehq.com/features)

### Compare sections

There are two comparison sections on our website, `/compare/` and [DevOps tools](/devops-tools/).

The DevOps tools section provides an in-depth, feature by feature comparison of GitLab and our competitors. Pages in the DevOps tools section are maintained by the Competitive Intelligence team, which is part of the [Strategic Marketing](/handbook/marketing/product-marketing/) team.

Pages in `/compare/` are shorter and focused on a single Call to Action that offers relevant resources to visitors arriving via paid advertising. Pages in `/compare/` are maintained by Growth Marketing team and Marketing Program Managers.

Examples of companies who have comparison pages:
[https://postmarkapp.com/compare/sendgrid-alternative](https://postmarkapp.com/compare/sendgrid-alternative)
[https://www.zendesk.com/support/features/zendesk-vs-intercom/](https://www.zendesk.com/support/features/zendesk-vs-intercom/)

### Overlap

Similar content can appear as a topic, solution, and in the product section with different emphases on each page. For example continuous integration:

- A topic page: `/continuous-integration` would talk about what CI is at a functional level.
- A solutions: `/solutions/continuous-integration`. would talk about why CI is important for businesses to adopt.
- A category page `/product/continuous-integration` would talk about the capabilities and features that are part of GitLab's CI functionality and the value it has.

## Ownership and responsibilities

Everyone can [contribute to the marketing website](#updating-the-marketing-website). While the [Strategic Marketing](/handbook/marketing/product-marketing/) and [Growth Marketing](/handbook/marketing/growth-marketing/) teams have primary responsibility over the website, the goal of these teams is to build systems, structures, and processes and empower everyone to contribute. Below is a breakdown of the ownership between Strategic Marketing and Pipe-to-Spend.

### Website team

- The website team (part of marketing) is responsible for the design and development of the website. [Marketing website team documentation and workflow](/handbook/marketing/growth-marketing/brand-and-digital-design/).

### Growth Marketing

- CTAs (Calls to action): The Growth Marketing team owns all buttons on the website including which pages get CTAs, the text used and where they link to. (Note: the website team still owns the design and styles of the buttons to ensure they are consistent and on brand.)
- Build and implement online growth strategy:
  - Search Engine Optimization
  - Paid search and social
  - Conversion Rate Optimization (CRO) and a/b and multivariate testing
      - CRO Process: Not all changes to pages need to be tested, only pages that we want to optimize for conversion activities. These pages/elements are often being tested
          - Homepage
          - Top navigation
          - Pricing page
          - Free trial
          - Contact sales
      - Please check [A/B test issue board](https://gitlab.com/gitlab-com/marketing/online-growth/boards?=&label_name[]=a%2Fb%20test) for pages you plan to update. The URL will be the first word or `HP` for the homepage.  If you have an update to any of the pages in the `Doing` column contact @lbanks. More details on CRO and testing in the [Online Growth Handbook section](/handbook/marketing/marketing-sales-development/online-marketing/)
-  Web analytics, tracking, and reporting
  - [Request a tracking review for a new campaign](http://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issuable_template=verify-campaign-tags)
  - Our [Google Tag Manager system](/handbook/marketing/marketing-sales-development/online-marketing/#gitlab-google-tag-manager-system) is designed to flexibly track a variety of events using Google Analytics across about.gitlab.com. Whenever we launch a new campaign we need to verify tracking performs as expected. Please use this [issue template to verify campaign tagging](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=).
  - These items are values we across about.gitlab.com to maintain our web analytics workflows.
    - CTA buttons must include `cta-btn` in their class.  looks for this value to fire Google Analytics events and without it we won't be able to see how visitors interact with our CTAs.
    - Forms need to push appropriate event label to trigger conversion tracking through Google Tag Manager. See the [Marketing Operations page for the event label list](/handbook/marketing/marketing-operations/#website-form-management).
-  User journey optimization

## Updating the Marketing Website

#### Requesting Support
If your team is unable to update the website, or you need additional levels of support please visit this section for [Requesting Support[(/handbook/marketing/growth-marketing/#website-issue-templates)]

### Naming conventions

Use consistent language across the site when naming links, page names, directory names, page titles, etc. If you see inconsistent language, [log an issue](https://gitlab.com/gitlab-com/www-gitlab-com/issues) to correct. We use [american english](/handbook/communication/#writing-style-guidelines) on the site. Here are some examples below. If in doubt, ask in the `#marketing` slack channel for language help.

Do use nouns when appropriate
- `/product/`
- `/community/`
- `/events/`

Do use the imperative tense as much as possible
- Get started
- Install
- Contribute

Don't use noun forms of verbs
- Installation
- Contribution

Don't use present participle ("ing" words)
- Installing
- Getting started
- Contributing

Nouns may end in "ing"
- Pricing (link to with the imperative "Get pricing" or "See pricing")
- Training (link to with the imperative "Get training" or "Find training")


### Creating new pages

Use [MVCs](/handbook/values/#iteration) to update the website. Create new pages and add the minimal amount of viable content. You can add images and more content in iterative steps.

All pages should use lowercase URLs to help avoid unintentional errors when linking to pages on about.gitlab.com. 

We have 10-20 seconds to tell visitors why they should stay on our pages. Tell visitors what value the page will give them. Start with a high-level summary opening the page. This could be as simple as a single sentence, but we shouldn’t put the burden of discovering the value of the page on visitors.

The page title and URL should include keywords visitors might use to discover the page you’re creating. If you’re not sure what terms a visitor might use, ask the Growth Marketing team for suggestions in your Merge Request. We have a list of high priority topics and recommended keywords to use.



### Website Workflow

Below, view a video that shows a typical workflow to update the website.

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/XKPi9JZkGs0" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

In the [GitLab Unfiltered](https://www.youtube.com/channel/UCMtZ0sc1HHNtGGWZFDRTh5A) video below, Sarah D., marketing operations manager at GitLab, shows Wil S., social marketing manager at GitLab, how to add a new page to your section of the handbook complete with a new main page and table of contents.

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/9NcJG9Bv6sQ" frameborder="0" allowfullscreen="true"> </iframe>
</figure>
<!-- blank line -->

### Creating a new page

To create a new page you for follow these steps:
1. Create an issue in the [website repo](https://gitlab.com/gitlab-com/www-gitlab-com/issues) **Note**: Don't branch from other repos like the marketing repo.
2. Create an MR from the issue by clicking on the "Create Merge Request" button. This will create a new branch for you and link it to your issue and label the MR as `WIP:`.
3. Click on the name of your branch after "Request to Merge" to open that branch in the repository file view.
4. Open the `source` folder. This is where webpages are stored.
5. Click on the directory where you want your webpage to be. For example, if you put a page in the `source` folder it will show up at the "root" level, if you create the new directory inside of another directory it will appear at that path.
5. Click to add a `New directory` from the plus sign drop down.
6. Name the directory in all lowercase with dashes-between-words for what you want the path of your page to be. For example if you want to create a page at [about.gitlab.com/solutions/cloud-native](/solutions/cloud-native) then click on the `solutions` directory and inside the `solutions` directory create a new directory called `cloud-native`.
7. Click to add a `New file` from the plus sign drop down
8. Name the file `index.html.md`
9. Add this code to the top of the file

```
---
layout: markdown_page
title: ""
---
## Subheading

Here is your first paragraph replace this text.
```

10. Inside the quote add the title of your page. For example the title of my cloud native page would be "Building Cloud Native Applications With GitLab". Save your page by clicking "Commit changes". (Using markdown you can add more content to the page. All you need is a title, subheading and a paragraph to get started.)
11. Return to the directory you created. You will see that you now have two files: `index.html.md` and `.gitkeep`. Delete the `.gitkeep` file. This is a placeholder file from when you created the directory since git cannot track empty directories. A quick way to delete the file on the correct branch is to click on "edit" in the changes tab of your MR. This will open the file editor. click "cancel" and dismiss the popup that says "all changes will be lost". This will then place you in the file view for the `.gitkeep` file on your branch. Click the "delete" button to delete the file.
12. **ProTip**: Now that you no longer have a branch with no changes you can use the Web IDE to make further edits. (The Web IDE doesn't work if you have a branch with no changes. [Fix coming in 11.3](https://gitlab.com/gitlab-org/gitlab-ce/issues/48166)
13. **ProTip**: Add a link to the bottom of your page so people can continue reading related content. Popular choices would be `/product` , `/solutions`, `/pricing` or any pages related to your page.
14. If you need help you can ask in the #mr-buddies slack channel.

### @gl-website

If you are seeking assistance or need the attention of the [website team](#website-team), please include @gl-website in the issue description to ensure the website team sees it. The @gl-website handle [is a group in GitLab](https://gitlab.com/gl-website) that the website team uses to be notified of issues and merge requests from others. For community contributed merge requests, this happens automatically with [gitlab-bot](https://gitlab.com/gitlab-bot) and you should see an automated message saying that the website site has been notified of your merge request.

### Analyst Report Pages

How to create an analyst report page in 5 not-so-easy steps. 

#### AR Part 1: Edit the analyst reports YAML

1. Open `analyst_reports.yml` - https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/data/analyst_reports.yml
2. Click “Web IDE” 
3. Add an entry for the new report. For example: 

```
- url: gartner-aro19
  title: "Gartner Application Release Orchestration Report"
  subtitle: "Gartner Cites GitLab as a Challenger in MQ for ARO"
  resource_link: /resources/gartner-aro/
  include_file: /analysts/includes/gartner-aro19
```

4. Edit the url, title, subtitle, resoruce_link, and include_file 
  - Use the url format `<analyst>-<report><year>`. Make a note of this `url` as you'll need it later a few times throughout the process. 
  - Use the official title of the report for the title
  - Subtitle - use analyst approved language
  - If we get the reprint, then uncomment the “resource” line. If not, leave it commented with a `#` at the beginning of the line. You need to coordinate with MPM to create a landing page to download the report to use as the resource link. 
  5. The incue_file should take the format `/analysts/includes/<url>` 
6. Commit the change to create a new MR: 
  - Click “commit”, add a commit message, and click “commit” again, 
  - Add “WIP:” to the title so that it doesn't get merged prematurely ("WIP:" means "don't merge")
  - “Submit merge request” 

#### AR Part 2: Create the include file

1. Open the WebIDE from your MR. 
  - This is a tricky step. If you don't’ open the WebIDE from your MR then you’ll be working on a different branch. Changes you make on that branch won’t show up in your MR. Alternatively, you can keep the WebIDE open in a tab and continue to make changes after you add each commit. As long as you commit to the same branch it will update on the same MR. 
2. Click on the edit tab. It's on the left under the GitLab logo and looks like `</>`
3. Next to the word “edit”, click on “new file” icon (looks like a page with a plus) then add the path 
  - The path will be `/source/analysts/includes/` plus the file name for the report you are adding using the `.html.md` file extension. `<analyst>-<report><year>.html.md` 
  - For example: `/source/analysts/includes/gartner-eapt20.html.md` 
  - This should create a new empty file for you.  
4. Copy an existing include (be sure to leave in the disclaimer at the bottom) 
  - For example: [https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/source/analysts/includes/gartner-eapt.html.md](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/source/analysts/includes/gartner-eapt.html.md) 

5. Update the content 
6. Commit that change to the MR branch 

#### AR Part 3: Create and upload a report image

1. Create an image of the report. Opening a PDF in Mac preview you can go to File > Export and select JEPG to save the 1stst page of the report. For example:  https://about.gitlab.com/images/analysts/cloud-ci-thumb.png. This is a tricky step because what you name the file is very important. It is highly recommended that you use “kabob case” meaning all lowercase letters with dashes in between the words instead of spaces. It looks like shish kabob :)  

2. Upload the image to the `/images/analysts/` folder. 

3. Open the WebIDE from your MR. This is a tricky step. If you don't’ open the WebIDE from your MR then you’ll be working on a different branch. Changes you make on that branch won’t show up in your MR. Alternatively, you can keep the WebIDE open in a tab and continue to make changes after you add each commit. As long as you commit to the same branch it will update on the same MR. 
4. On the edit tab, open the `source` folder, then the `images` folder, then the `analysts` folder. This is kinda tricky because you have to scroll past a lot of folders to find the one you want. The folders are in alphabetical order. 
5. Hover over the `analysts` folder and click on the drop down and select “Upload file”. This is an important step. If you upload the file to a different folder then the image won’t show up on the page. 
6. Choose the image and click “open”. 
7. Commit that change to the MR branch

#### AR Part 4: Edit the haml file
  
1. Open the WebIDE from your MR. This is a tricky step. If you don't’ open the WebIDE from your MR then you’ll be working on a different branch. Changes you make on that branch won’t show up in your MR. Alternatively, you can keep the WebIDE open in a tab and continue to make changes after you add each commit. As long as you commit to the same branch it will update on the same MR. 
 2. Type “t” to open up the fuzzy finder and search for the `source/includes/forrester-reports.html.haml` file. Open it in the WebIDE 
 3. Copy a “section” and paste it at the top underneath `.forrester-waves-container` This is a tricky step because the indentation needs to be exactly the same as the other sections. When you copy you need to copy all the spaces indenting the line. When you paste, be sure to paste with your current not indented at all. This should give you the same spacing. For example: 
  
```
  <!–– Gartner ARO 2019 ––>
  .forrester-wave-row
    .wave-row-content
      = image_tag "/images/analysts/gartner-app-release.jpg", class: "forrester-wave-graphic", alt: "GitLab Cloud CI Forrester Wave thumbnail png"      
    .wave-row-content
      %img.gartner-logo{ src: "/images/home/gartner-logo.svg", alt: "Gartner logo svg" }
      .text-center.forrester-graphic-title
        %p ARO Report
      %p Gartner Cites GitLab as a Challenger in MQ for ARO
      %a.btn.cta-btn.accent.margin-top20.reports-include-button-aro{ href: '/analysts/gartner-aro19/' } Read more
```

 4. Update the block with info from the new report. This is a tricky step because you only want to change some lines. Don’t edit any parts that start with a dot like ` .forrester-wave-row`, `.wave-row-content`, or `.text-center.forrester-graphic-title`. The phrases that start with a dot are CSS classes, so if you edit them the page will be formatted strangely. 
   - PROTIP: Compare your block to a couple other blocks to make sure you are editing the correct lines and while leaving the correct code unedited. 
   - SIDENOTE: The classes are named “forrester wave” because they were originally created for that report, but then they got used for all reports. This is something to ask the web team to clean up sometime in the future. (Ideally, you should never need to edit a `.haml` file. You should only ever need to edit `.md` and `.yml` files.) 
  - IMPORTANT NOTE: Take care when editing the `= image_tag` line. Here you need to reference the image file that you uploaded in the previous step. The image file name here needs to exactly match what you named the file when you created it. It should be “kabaob case” - all lowercase letters with dashes instead of spaces. 
5. Commit your changes to your MR. 

#### AR Part 5: Review 

1. Wait for the pipeline to complete and review your changes in the review app. 
2. You can continue to update the files in the MR. Particularly the include file will have content from the PM and the PMM. However, it is recommended to merge a skeleton page with TBD, then have the PMM open a new MR to add their changes. 
3. If it all looks good, assign to someone to merge. 
4. Pat yourself on the back for successfully completing a website update process designed for people who are software developers. 

### Updating an existing page

1. Click on the "edit" button at the bottom of the page.
1. Edit the page. Note: page content can be in markdown, `haml`, or possibly in a separate `.yml` file that populates fields in the `haml` file. The [hello bar](#editing-the-homepage-promo-banner-hello-bar) is an example of content in a `.yml` file.
1. If you need help you can Ping @gl-website in the MR or ping @website-team in the #website slack channel.

### Moving a page

Great care should be taken whenever moving pages on the website. Ideally, pages should never be moved without implementing an immediate 301 redirect.

The Inbound Marketing team can follows this process to [create 301 redirects](/handbook/marketing/growth-marketing/inbound-marketing/#request-an-aboutgitlabcom-redirect).

### Renaming a page

If you need to rename a page (e.g. change `/company/culture/all-remote/part-remote` to `/company/culture/all-remote/hybrid-remote`, as was achieved in [this merge request](https://gitlab.com/gitlab-com/www-gitlab-com/merge_requests/31109/)), follow the below steps if using Web IDE.

1. Within Web IDE, navigate to the directory that needs renamed, and click the option drop-down to select **Rename**.

1. Rename the folder, then click **Rename folder**.

1. Add a relevant commit message and submit a merge request.

1. Within the newly created merge request, edit  [`redirects.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/redirects.yml).

   1. To put the redirect in place, add a few lines to `data/redirects.yml`. Define "sources", "target", and "comp_op" like so:

```
   - sources:
   	 - /company/culture/all-remote/part-remote/
    	 - /company/culture/all-remote/part-remote
      target: /company/culture/all-remote/hybrid-remote/
      comp_op: '='
```

### Optimize images

When adding an image to a webpage, be sure that you optimize the image first.

1. Select the image you'd like to add to a page and save a copy to your computer.
1. Add your local copy to [ImageOptim](https://imageoptim.com/howto.html) and optimize the image for the web.

### Updating the team page and org chart

1. Both the [team page](/company/team/) and [org chart](/company/team/org-chart/) are updated based on [`team.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/team.yml)
2. Edit [`team.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/team.yml) and create an MR
3. The org chart is built automatically based on `slug` and `reports_to` lines.
4. See the [team structure](/company/team/structure/#specialists-experts-and-mentors) page for more info on specialties, expertise, and mentorship availability to a listing.

### Updating the homepage promo banner (`hello-bar`)

- The homepage promo banner is edited at [`/source/includes/hello-bar.html.haml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/includes/hello-bar.html.haml).
- This banner includes an optional image (logo) to accompany the text.

### Working with Stages, Groups, and Categories

[Categories and stages](/handbook/product/categories/) are defined in the product handbook. Stages are stored in [`data/stages.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/stages.yml) and categories are stored in [`data/categories.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/categories.yml) as the single source of truth for engineering and marketing.

These two files power various parts of the website including the [homepage](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/sites/marketing/source/includes/home/sdlc.html.haml), [product pages](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/product/index.html.haml), and [product categories handbook](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/includes/product/_categories.erb).

They are also used by the automated triage operation ["Stage and group labels inference from category labels"](/handbook/engineering/quality/triage-operations/).

#### Stage attributes

Below are attributes that can be added to a stage in `data/stages.yml`.

* `groups.<group_key>.feature_labels`: A list of all the feature labels that are associated with this group.
  Ideally, feature labels should be associated with a category instead (see
  `feature_labels` in the "Category attributes" section below).
  This list is used in the automated triage operation ["Stage and group labels inference from category labels"](/handbook/engineering/quality/triage-operations/).

#### Category attributes

Below are attributes that can be added to a category in `data/categories.yml`.

* `stub`: the name of the category in lowercase/snakecase with no abbreviations. E.g. "Authentication and Authorization" becomes `authentication_and_authorization`. (Don't abbreviate as this stub is used to create URLs so the full words become SEO keywords).
* `name`: the name of the category in quotes
* `stage`: what stage the category belongs to.
* `label`: The category [label in the `gitlab-org` group](https://gitlab.com/groups/gitlab-org/-/labels?utf8=✓&subscribed=&search=Category%3A).
  By default, the category label is inferred from its name.
  For instance, the `Code Analytics` category is represented by the
  [`Category:Code Analytics` label in the `gitlab-org` group](https://gitlab.com/groups/gitlab-org/-/labels?utf8=✓&subscribed=&search=Category%3ACode+Analytics).
  This attribute allows to override that.
  For instance, the `gitlab-org` label for the `Kanban Boards`
  category is [`Category:Issue Boards`](https://gitlab.com/groups/gitlab-org/-/labels?utf8=✓&subscribed=&search=Category%3AIssue+Boards).
* `feature_labels`: A list of all the feature labels that are associated with this category.
  This list is used in the automated triage operation ["Stage and group labels inference from category labels"](/handbook/engineering/quality/triage-operations/).
* `marketing_page` (optional): the path of marketing page for the category. If you include a `body` section, then a marketing page will be auto-generated at `/product/${lowercase-category-name}`
* `documentation` (optional): the URL of the docs page for the category, required if the category maturity is minimal or above.
* `direction` (required): the URL of the category direction page. Optionally could be the URL of an issue, epic, or issue label search query if a direction page has not yet been created.
* `description`: a short description of the category.
* `roi`: `true | false` should this category appear in the ROI calculator. (omitting the line is the same as `false`)
* `percent_of_focus`: A value of `0-1` detailing the percent of the group this category is assigned to's focus on this category in terms of developing improvements
* `available`: an ISO date for when the feature was or will be available.
* `viable`: an ISO date for when the category will/did move from minimum to viable on the [maturity handbook page](/direction/maturity/).
* `complete`: an ISO date for when the category will/did move from viable to complete on the [maturity handbook page](/direction/maturity/).
* `lovable`: an ISO date for when the category will/did move from complete to loveable on the [maturity handbook page](/direction/maturity/).
* `maturity`: the current maturity of the category on the [maturity handbook page](/direction/maturity/). Valid values are `planned`, `minimal` (available), `viable`, `complete`, and `lovable`. Provided `marketing = true`, a value of `planned` will cause the category to appear in the "coming soon" section of the homepage, while other values will cause it to appear in the "Since 20XX GitLab added" section.
* `marketing`: A value of `true` will cause this category to appear on our marketing pages, in addition to our [handbook](/handbook/product/categories/). For the home page, a `maturity` state is also required. [Internationalizaion](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/categories.yml) is a good example of a category the engineering team works on, but is not a "customer-facing category" that appears on marketing pages.
* `body`: content added in markdown will be [auto-generated](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/config.rb#L133) and turned into a page at `/product/<category>/`. Features and missing features sections are automatically added to the generated category pages based on what category a feature belongs to in `features.yml`. c.f. [Project Management](/product/project-management/) (and auto-generated page from the [`body` section in `categories.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/categories.yml#L148)) with [Continuous Integration](/stages-devops-lifecycle/continuous-integration/) (a [custom page](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/source/product/continuous-integration/index.html.haml).)
* `opportunity`: values can be `Core`, `Adjacent`, `Distant` - is this category considered part of our existing `Core` DevOps platform, a directly `Adjacent` set of capabilities or a `Distant` vision for future breadth.
* `differentiation`: values can be `Winning`,`Compelling`,`Minimal` - is this category sufficiently differentiated from competitors to be considered capable of consistently `winning`, providing an `compelling` additive component to our single platform value or adding only `minimal` differentiated value.
#### Working with category maturity

There are five fields in `categories.yml` that control a category's maturity. These work together to define what the maturity currently is, how it has evolved over time, and our plans to improve in the future.
* `maturity` which represents the current maturity of the category
* `available`, `viable`, `complete`, and `lovable` which are set to ISO dates when we achieved, or plan to achieve, the given maturity.

To change or update the current maturity, set the `maturity` field to the desired value: `planned` (or empty), `minimal` (available), `viable`, `complete`, and `lovable`. Next, ensure that the historical and future maturity values are still consistent. For example, if you incremented the maturity of the category from viable to complete, you should also set the field `complete` to the date of the GitLab release when it changed.

#### Sample template

```
authentication_and_authorization:
  name: "Authentication and Authorization"
  stage: manage
  documentation: https://docs.gitlab.com/ee/administration/auth/
  vision: https://gitlab.com/groups/gitlab-org/-/epics/628
  description: "GitLab features multiple auth mechanisms including LDAP (including Active Directory), OmniAuth, CAS, SAML, Okta, and Authentiq."
  roi: true
  available: 2017-10-01
  viable: 2019-05-22
  complete: 2019-12-22
  lovable:
  maturity: minimal
```

#### Proposing a change

Due to their importance and wide usage throughout the company, changes to Stages, Groups, and Categories need to be reviewed. Open a merge request [using the `Category-Change` template](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/.gitlab/merge_request_templates/Category-Change.md) to get started.

**Major changes**

Any change to a Stage or Group, or a significant change to a Category, is a major change. Examples of significant category changes include their names, their group membership, and presence on our marketing page.

Due to their impact, executive approval for major changes is required in addition to the PMs, PMMs, and EMs responsible. Follow the approval process defined on the [categories page](../../product/categories/#changes).

**Minor changes**

Minor changes to Categories are generally routine changes, like updates to maturity and content links. For example, upon shipping an MVC the maturity would change to `minimal`, and a link to the documentation would be added.

Approvals should be gathered from the responsible PMs, PMMs, and EMs. Also mention the relevant engineering and product directors, so they are aware of the changes. If changes are included in a release post, ensure the approval team and directors are mentioned on the MR.

##### Updating responsible persons for a Group

To update the responsible person for a role, follow these steps:

1. Go to the [GitLab.com / www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com) project
1. Change the name of the responsible person in `source/data/stages.yml` at the relevant position e.g. `pm: John Doe`.
1. Add the markdown reference link of the responsible person in `source/includes/product/_categories.erb`

Here's an [example Merge Request](https://gitlab.com/gitlab-com/www-gitlab-com/merge_requests/22765).

If the person is not yet listed on the [team page](../../../company/team/), please follow [these instructions](../../git-page-update/#11-add-yourself-to-the-team-page) to add them.

### Adding features to webpages

All features and capabilities are listed in a single yaml file
([`features.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/features.yml)) under the `features` section.
It is the single source of truth for multiple pages across the website including:

- [Product pages](/product/) e.g. [continuous integration](/stages-devops-lifecycle/continuous-integration/)
- [Pricing](/pricing/)
- [Compare](/devops-tools/)
- [ROI](/roi/)
- [Features](/features/)

To add a new feature, add a feature block to under the `features:` section of the page. Add the following attributes:
  - **title**: the name of the feature in quotes
  - **description**: a plaintext summary of the value the feature provides in quotes
  - **link_description**: OPTIONAL, anchor text of a link that will appear below the descriptions e.g. `link: https://docs.gitlab.com/ee/user/project/milestones/`
  - **link**: OPTIONAL, the URL of the link (no quotes)
  - **screenshot_url**: OPTIONAL, `screenshot_url: 28-group-milestones.png`
      Just put the filename of the screenshot. Feature screenshots must go in the following directory: 'images/feature_page/screenshots/'.
  - **category**: a list of one or more categories that this features belongs to. Adding a category to a feature causes it to show up in the features section on the product page for that category (e.g. see the [Continuous Integration page](/stages-devops-lifecycle/continuous-integration/))
  - **solution**: REQUIRED legacy field. A [stage of the DevOps lifecycle](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/stages.yml). Will be [removed soon](https://gitlab.com/gitlab-com/www-gitlab-com/issues/2435).
  - **tier**: `true` or `false` is this feature or capability available in this tier? `gitlab_core`, `gitlab_starter`, `gitlab_premium`, `gitlab_ultimate`
  - **gitlab_com**: `true` or  `false` is this feature or capability available on GitLab.com? Because GitLab.com tiers map 1:1 to self-managed tiers setting this will automatically assign the GitLab.com tier. E.g. `gitlab_core: true` + `gitlab_com: true` == `GitLab.com Free`. Adding a tiers fields is what powers the tier badges on product pages and comparison pages, as well as powers the tier [feature comparison of the pricing page](/pricing/self-managed/feature-comparison/).
  - **toolname**<a name="feature_status_defs"></a>: any tool from the `devops_tools:` section such as `jira:`, `circle_ci:`, `blackduck:`, etc. that does or does not have this feature. Holds a value of either `true` or `false` or `partially` or is blank (indicating subfields with details should exist).
    - `true` or `false` or `partially`: Examples of `partially` are if a DevOps tool has some but not all of the feature described, or if they have the feature, but only through a plugin. If using `partially` it is highly recommended to instead add `details` as to what partially actually means (see next)
    - \<blank\>:<a name="feature_status_details"></a> Means that the feature for this particular toolname have a sub-section with details:
      - `valid`: Same as `true` or `false` or `paritally` above
      - `details`: A short statement about the details that need to be shared. For example: "supports 11 languages", or "only supported through 3rd party plug-ins"
  - **pricing_page**: `true` or `false`:  this option was created when the pricing page used to be called the "products" page. Setting true cause the feature to show up on the [pricing page](/pricing/#self-managed). Only a limited number of the most important capabilities should be shown on the main pricing page to keep it easily consumable. Folks can click on "see all features" to see the full list of features ([self-managed comparison](/pricing/self-managed/feature-comparison/), [GitLab.com comparison](/pricing/gitlab-com/feature-comparison/)).

For example:

```

- title: "Group Milestones"
  description: "Create and manage milestones across projects, to work towards a target date from the group level. View all the issues for the milestone you’re currently working on across multiple projects."
  link_description: "Learn more about Group Milestones"
  link: https://docs.gitlab.com/ee/user/project/milestones/
  screenshot_url: 'images/feature_page/screenshots/28-group-milestones.png'
  solution: plan
  category:
      - portfolio_management
  gitlab_core: true
  gitlab_starter: true
  gitlab_premium: true
  gitlab_ultimate: true
  gitlab_com: true
  github_com: false
  github_enterprise: false
  bitbucket_org: false
  bitbucket_data_center: false
  gogs: false
  jira:
    valid: true
    details: 'only through 3rd party extension'
  ca_agile_central: false

```
Copy and paste this template:

```

- title: ""
  description: ""
  link_description: ""
  link:
  screenshot_url: ''
  solution:
  category:
    -
  gitlab_core:
  gitlab_starter:
  gitlab_premium:
  gitlab_ultimate:
  gitlab_com:
  github_com:

```



### Creating a DevOps tools comparison page

The [`/devops-tools`](/devops-tools) section of the website shows info about DevOps tools and a feature comparison of those tools to Gitlab. Comparison pages are auto-generated from `features.yml`. All you need to do is add a tool to the `devops_tools` section and add that tool id to some features and the page will be created.

To add a new comparison page:
1. Edit [`features.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/features.yml)
2. Under the `devops_tools` section add a tool.

Although the `summary` and `include_file` fields are not strictly required by the parser in order to build the page, every tool **should have at least one paragraph** summarizing the comparison using **EITHER** the `summary` field or the `include_file` field (see below for details). `summary` only is deprecated. Use `include_file` method whenever possible.

  - id: a lowercase, snake_case unique identifier (e.g. `travis_ci`)
  - name: the display name of the tool in single quotes
  - logo: the path to the logo, if there's no logo, add it in the `/images/logos/` directory
  - category: a list of [GitLab product categories](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/categories.yml) that this tool is for. Setting a category caused the tool to show up under the category's stage when viewing the table on a comparison page.
  - pick only one field
    - include_file: path to a markdown (`.md`) file that will be embedded on the page. Here is where you can add more robust content about the tool. Please use the template under `/source/devops-tools/misc/tool-template.html.md` and store your new file under `/source/devops-tools/TOOLNAME/index.html.md`.
    - summary: (deprecated) A summary paragraph describing the to tool compared to GitLab. Add a pipe ( `|` ) then add content in markdown indented on the next line. Be sure to add on additional empty line after your content.

  For example:

  With `include_file` (preferred method):
```
  jenkins:
     name: 'Jenkins'
     logo: '/images/devops-tools/jenkins-logo.svg'
     category:
       - ci
       - cd
     include_file: devops-tools/jenkins/index.html.md.erb
```

  With `summary` (deprecated method):
```
  chef:
     name: 'Chef'
     logo: '/images/devops-tools/chef.png'
     category:
       - infrastructure_configuration
     summary: |
       Chef is a configuration management tool that enables deployment and maintenance of state for large scale infrastructure. Chef excels as managing legacy infrastructure like physical servers and VMs. Chef was designed before widespread container adoption and does not implement Kubernetes natively.

       GitLab is a complete DevOps platform, delivered as a single application that includes not only configuration management, but also capabilities for project management, source code management, CI/CD, and monitoring. GitLab is designed for Kubernetes and cloud native applications.

       GitLab can be used together with Chef to enable VM and bare metal configuration management. For Cloud Native applications run on Kubernetes, Chef is not required and GitLab can provide all the functionality natively.
```

Copy and past this template:

```
unique_tool_id:
    name:
    logo: '/images/logos/TOOLNAME.png'
    category:
      -
    include_file: 'devops-tools/TOOLNAME/index.html.md'

```

3. Add features to the comparison section.

Be sure to add features that GitLab has that the other tool doesn't and also features the other tool has that GitLab doesn't so that our comparison are transparent and honest (ie. this shouldn't be one sided).

- On a feature block, add the `tool id` and then `true`, `false`, or `partially` to indicate support for the feature ([what does partially mean?](#feature_status_defs)) Add the same details for gitlab tiers. Adding a tool id to a feature is what causes it to show up on the comparison page for that tool. (e.g. if you don't want a feature to show up on a comparison page remove the tool id line from that feature.)
- What if you want to [**add qualifying details**](#feature_status_details) to the true/false/partially info you are providing for a tool?

For example:

```
  - title: "Free CI/CD with shared or personal Runners"
    capability: true
    description: "GitLab.com has shared Runners that allow you to use GitLab CI/CD completely free up to 2000 build minutes for private projects and unlimited for public projects. Alternatively, you can set up your own Runner for faster build processing, unlimited build minutes, or special requirements."
    link_description: "Explore GitLab.com offerings"
    link: /gitlab-com
    solution: gitlab_com
    gitlab_core: true
    gitlab_starter: true
    gitlab_premium: true
    gitlab_ultimate: true
    gitlab_com: true
    github_com: false
    bitbucket_org: 'partially'
    gitlab_ci: true
    codestar: false
  - title: "Domain Specific Language"
    description: "A Domain Specific Language (DSL) for defining infrastructure configuration allows thinking in resources, not files or commands to write declarative rather than procedural code."
    # link_description: ""
    # link: ''
    solution: missing
    gitlab_core: false
    gitlab_starter: false
    gitlab_premium: false
    gitlab_ultimate: false
    puppet: true
    chef: false

```
4. If you followed the above step, the new comparison page should be reachable
   under `/devops-tools/tool-vs-gitlab.html` and you should see it on the
   devops-tools table on the main page.

5. The last thing you need to do is create the PDF. Follow the
   info in [creating comparison PDFs](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/doc/pdf.md).

### Adding content to resources

The [`/resources`](/resources/) section of the website contains downloadable files and links to helpful content.

1. To add a resource, edit the [`resources.yml`](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/resources.yml) file.
2. To create a new entry for your resource, use this template and add it to the top of `resources.yml`:

```
- title:
  url:
  image: /images/resources/gitlab.png
  type: Pick one --> 'Blog post' 'One-pager' 'Report' 'Webcast' 'White paper'
  topics:
    - Cloud native
    - Code review
    - Continuous delivery
    - Continuous integration
    - DevOps
    - Git
    - GitLab
    - On-demand training
    - Public Sector
    - Security
    - Software development
  solutions:
    - Distributed teams
    - Accelerated delivery
    - Executive visibility
    - Project compliance
    - Security and quality
```

3. **Uploading a PDF**: If the resource you'd like to add is a PDF, it can be uploaded to [`/pdfs/resources/`](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master/source/pdfs/resources/).

4. **Selecting an image**: Each resources has a thumbnail image based on their topic; select the most relevant image for the content. The current thumbnail images are shown below and can be found [here](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master/source/images/resources).
![ALT](/images/resources/resource-page-thumbnails.png)

5. **Selecting a type**: All resource types are listed in the code snippet above; select one that best fits your content. If the resource does not fit the current types, please see [Requesting Website Updates](#requesting-website-updates) to submit a proposal for new resource type(s).

6. **Selecting topics & solutions**: The code snippet above provides all of the current topics and solutions; chose the topics and solutions that best apply to the content. Please note they are case sensitive and incorrect casing or spelling will result in the generation of new, unwanted, topics and/or solutions.

## Creating and publishing your GitLab README

As part of GitLab's [transparency](/handbook/values/#transparency) value, we encourage each GitLab team member to consider adding a README — a great tool for transparently letting others know what it's like to work with you, and how you prefer to be [communicated](/company/culture/all-remote/effective-communication/) with.

### Purpose of READMEs

When people are working together for the first time, there's a certain amount of mental and emotional energy exerted in getting to know someone. You're simultaneously doing the work, while trying to confirm or challenge preconceived notions about how a person prefers to be communicated with.

On an individual level, this requires a person to project the ideal version of themselves into each meeting, as it is assumed that this projection is the only meaningful way for another person to understand who they are and how they prefer to communicate and work.

READMEs provide a genuine report on how a person works, reducing bias/assumption and enabling people to work together based on a common framework.

### GitLab team README examples

GitLab division README pages are linked below for context. Let these serve as a guide and inspiration as you create your own.

* [Product](/handbook/product/readme/)
* [Marketing](/handbook/marketing/readmes/)
* [People Group](/handbook/people-group/readmes/)
* [Engineering](/handbook/engineering/readmes/)
* [Sales](/handbook/sales/readmes/)
* [Finance](/handbook/finance/readmes/)
* [Legal](/handbook/legal/readmes/)

### How to create a GitLab README

1. Copy the [README-template](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/.gitlab/issue_templates/README-template.md) and paste into your favorite Markdown editor. If you do not have a Markdown editor, [Typora](https://www.typora.io/) and [Bear](https://bear.app/) are recommended.
2. Fill out the recommended sections. Note that each section is *optional*. You can remove those you aren't comfortable filling out, and add sections that are germane to you.
3. Once complete, you'll need to [create a new page](/handbook/marketing/website/#creating-a-new-page) and a subsequent merge request to add the page to GitLab's website.
   1. If your [division](/company/team/structure/) *already* has a page to host READMEs (see above), follow the guidelines to [add a new page](/handbook/marketing/website/#creating-a-new-page) within that directory (e.g. [Darren M.](https://gitlab.com/dmurph), a member of the marketing team, would add a new directory and page within `/handbook/marketing/readmes`, creating `/handbook/marketing/readmes/dmurph`)
   2. If your [division](/company/team/structure/) does not yet have a holding page for READMEs, follow the guidelines to [add a new page](/handbook/marketing/website/#creating-a-new-page) (`readmes`) within your division's handbook section *first*, then create your username directory within `readmes`.

### Making your README visible

Once your README is created, consider adding a link to it in the following places.

* Google Doc agendas or calendar invites
* Your GitLab.com profile
* Slack profile
* Email signature

This provides maximum visibility to others, so that they may ingest your README in advance of working with you. This allows them to take your working style and communication preferences into account,  ideally increasing the overall level of empathy expressed.

READMEs are particularly powerful when working with those *outside* of GitLab, who may be unfamiliar with our [values](/handbook/values/). A README is a beacon of [transparency](/handbook/values/#transparency), and helps set the tone for any working relationship.

## Requesting Website Updates

If you'd like to propose new pages for the GitLab website and the update is more complicated than [creating a new page](#creating-a-new-page) on your own, you can request help from the [Website team](/handbook/marketing/growth-marketing/brand-and-digital-design/). New changes or updates with a due date should be requested with sufficient lead time to process the request, allocate resources, iterate, and produce related items.
1. Before requesting help, create the content that you want to go live. E.g. draft the exact words that you want updated.
1. To request help from the website team to update the site, create an issue in the [www-gitlab-com](https://gitlab.com/gitlab-com/www-gitlab-com/issues) project
1. Add the specific content (exact wording and images) in the issue description that you want to put live on the website. Note: If the content is unclear, the issue will be assigned back to you to clarify the content before the website team will begin development work.
1. add the `Website` label
1. ping @gl-website in the MR or ping @website-team in the #website slack channel.

## Merge requests

Merge requests should be reviewed according to our [merge request guidelines](/handbook/marketing/website/merge-requests).
