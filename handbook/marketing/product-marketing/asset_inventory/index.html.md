---
layout: markdown_page
title: "Strategic Marketing Asset Inventory"
---
This page provides an inventory of assets created and maintained by the [Strategic Marketing](/handbook/marketing/product-marketing/) team.

#### Filter, search, and export Selected Asset List:
*Hover over the lower right corner and click to view this "Full screen." Export your Selected Asset List to Google Sheets with the ⋮ or vertical ellipsis. Scroll down for [more on how to use this Asset Inventory](#more-on-how-to-use-this-asset-inventory).*

<figure class="video_container">
<iframe width="100%" height="100%" src="https://datastudio.google.com/embed/reporting/bb7a37e5-d63e-421a-9b3b-8d1ec80f72dd/page/9yobB" frameborder="0" style="border:0" allowfullscreen></iframe>
</figure>

### More on how to use this Asset Inventory

 - Search is case-sensitive, so 'AWS' will find assets that 'aws' will not.
 - View the inventory full screen by hovering over the lower right corner and clicking the four-corners icon
 - Export your **Selected Asset List** to Google Sheets, or find other options like downloading data as CSV, by hovering over the upper right side of the light purple, Selected Asset List area, then clicking the ⋮ or vertical ellipsis (three dots)
 - See more filters and options by hovering over the lower left corner and clicking the right arrow to the "Next page" or to the right of that, by selecting a page from the menu

### Assets and metadata
Data feeding the Asset Inventory are in a spreadsheet called [Strategic Marketing Inventory Data](https://docs.google.com/spreadsheets/d/1W5oAlbPV610-ylM7LWv_zc6bEqQK9dI0H9Hrn2f6Jwc/edit#gid=0), editable by Strategic Marketing team members and read-only accessible to everyone else at GitLab. The dashboard view of the inventory, as above, is open to the public, so please do not use confidential information in asset titles and metadata.

The Strategic Marketing team member who is the SM DRI for an asset — the primary creator, contributor, and/or decision maker from SM — is responsible for adding the asset to the inventory. The spreadsheet used to add assets to the inventory is currently restricted to Strategic Marketing team members as we work through making the tool more resilient for wider use. If you, as a member of another team, would like to include an asset, please reach out to your SM-aligned person or wait just a bit until our next iteration of the tool.

Metadata include what type of asset it is, the date it was last updated, assignment of a Backup DRI, and an asset's alignment with value drivers, use cases, and campaigns. [The full data dictionary is explained below](#step-2-adding-assets-and-metadata).

#### Step 1: Is this an asset?

{::options parse_block_html="true" /}

<div class="panel panel-info">

**What is or is not an asset?**
{: .panel-heading}

<div class="panel-body">
Assets are useful and unique. Simple enough! but deciding what is an asset can be confusing with a case in-hand, so here are two tests to apply and a few examples.
##### 1. Assets are things that are reusable, and that are useful.

Activities are not assets. In other words, this inventory does not list things we did, it lists reusable things we made.

The fact that we moderated a panel discussion or gave a talk is not an asset, but a recording made or a slide deck produced may be assets — if they are reusable and unique.

Calls and meetings are generally not assets, nor are most files or data created in the process. The agenda or notes, the issue organizing it, a Chorus recording — these are rarely assets.

Exceptions might be those that are reusable as templates or for training, but most files and data like these are not reused. While notes and similar records are useful in process and in aggregate, that's within and handled by other tools instead of this asset inventory.

Before closing out an issue, ensure that you add your asset with the link(s) as FINAL ASSET(S) to the top of the description of the issue.
##### 2. Assets should be unique or close to it.

We should usually inventory just one copy or version of an asset.

If you've updated an existing asset, consider updating its metadata instead of adding a new asset. Decide whether to inventory multiple versions based on what would be useful to others — something like translation into an additional language would warrant adding a separate asset.

</div>
##### **Which assets belong here — edge cases**
{: .panel-heading}

<div class="panel-body">

##### Things Strategic Marketing doesn't own within GitLab, but contributes to

Strategic Marketing often makes significant contributions to assets that are owned by other GitLab teams. Examples include a product release post with a PMM messaging lead, or a Sales enablement resource that heavily relies on competitive research. This raises the question of whether certain assets "belong to" SM enough to be in our inventory. Our bias will be to include these assets. 

If we can identify an "SM DRI" and we made significant contributions, we will inventory the asset. We will also take care to not misrepresent that we wholly created or own the asset.

##### Things GitLab doesn't own or manage, but contributes to

Strategic Marketing also contributes to assets that are owned or managed by others outside of GitLab, such as a recording of us speaking at a conference, or a piece we wrote in an industry publication. When those assets live somewhere GitLab does not manage, we will try to make a GitLab-owned and managed copy of the asset for internal use. Our bias will be to include assets like these in this inventory, even without our own copy of them.

##### Things we just review and approve

We are interested in reviewing, vetting, and then including assets in the SM inventory even when our contributions are minimal or null, other than having reviewed and approved. Our motivations are first, to serve those searching for "everything related to X" and second, for this inventory to serve as a repository of high quality assets. As subject matter experts, SM team members are already, sometimes asked to review and approve of content or other assets. We want to multiply that value by inventorying what we've reviewed. 

We celebrate that GitLab enables any team member, and in many cases even community members, to contribute on the company web site, Unfiltered blog, handbook, Unfiltered YouTube channel, and so on. Those are great examples of GitLab values and culture in action, and it's indisputably generative. We also acknowledge, however that this can result in impedingly uneven asset quality, such as in tone, focus, or technical depth. As a result, it can be difficult for non-SMEs to know whether an asset they find is fit for reuse in contexts with higher quality requirements.

We do not, at this time have a process for ingesting, reviewing, or including assets like these. While we consider adding additional metadata and process, you might already find some in the inventory.
</div>
</div>

#### Step 2: Adding assets and metadata

If you have one or more assets to add, then insert one line per asset in [the spreadsheet](https://docs.google.com/spreadsheets/d/1W5oAlbPV610-ylM7LWv_zc6bEqQK9dI0H9Hrn2f6Jwc/edit#gid=0) and complete each field:

{::options parse_block_html="true" /}

<div class="panel panel-info">

**Data dictionary**
{: .panel-heading}

<div class="panel-body">

| **field name** | **field contents**  | **how to complete** |
|:---------------||:---------------|:-------------|
| **GC Source** | GC when we present the asset | Select from the dropdown menu. |
| **Title** | Title of the asset  | Please follow the naming conventions of similar assets. |
| **Asset Location (URL)**<code>&ast;</code> | Link to the asset | This should be the internal link. If there is both an internal/ungated link and an eternal/gated link, then add the internal/ungated link HERE and add the external/gated link behind the text of the asset Title. |
| **sm_req (issue) or MR** | Link to the specific, related issue or MR | This should be the issue where this work was performed, not a general related issue or epic; if not an issue, then an MR.
| **Type** | Type of content  | Select from the dropdown menu. Notes: Demo videos are "demos" not videos. If you made both a slide deck and a video, and both are reusable and unique, then add two assets. |
| **Authoring Team** | SM Team  | Select from the dropdown menu. |
| **SM DRI** | Primary creator, contributor, decision maker  | Select from the dropdown menu. SM team member who primarily created, contributed to, or managed creation of the asset. |
| **BACKUP DRI** | Secondary creator or SM Manager  | Select from the dropdown menu. Backup person knowledgeable of the asset and/or the DRI's Manager. |
| **Internal/External** | Internal vs. External Audience  | Select from the dropdown menu. The primary audience for whom the asset was created. Should more often be External. |
| **Intended Audience** | Primary Audience  | Select from the dropdown menu. The primary audience for whom the asset was created. |
| **Date Last Update** | Date of Creation or Last Update | Enter in GitLab format, YYYY-MM-DD, the last time the asset was materially changed by Strategic Marketing. |
| **Requested by** | Requesting Team  | Select from the dropdown menu. Team that requested making the asset. Note: 'Media Relations' is an option apart from 'Corp Marketing'. |
| **Intended Purpose** | What part of the Marketing Funnel does this target?  | Select from the dropdown menu. Either the customer journey stage, that the asset was created for Sales Enablement, or Other.  |
| **Value Driver** | Primary Value Driver  | Select the one, best fit from the dropdown menu, or "All 3" or N/A. |
| **Use Case / Topic** | Primary Use Case  | Select the one, best fit from the dropdown menu, or Other or N/A. |
| **Campaign(s)** | Primary Marketing campaign featuring it | Select the one, best fit from the dropdown menu, or N/A. |
| **Keywords** | Search terms to help people find it  | CSV welcomed, while this is a freeform field. Spelling counts! |
| **Notes** | Anything else we need to know  | This is a freeform field. |
{: .custom-class #custom-id}

*<code>&ast;</code> If the asset has a gated link, enter the ungated link (for internal use) in the Asset Location (URL) field, and enter the gated link behind the text of the asset Title.*

</div>
</div>

#### In due course

<div class="panel panel-info">

**Update the inventory**
{: .panel-heading}

<div class="panel-body">

New assets should be added to the inventory as part of our definition of done for SM Support Request Issues, i.e. as part of finishing the asset itself. We'll explore use of the template and whether we can provide useful links and e.g. require checking a particular box that in this issue, assets were either not created or were inventoried.

The team member who is the SM DRI for an asset — the primary creator, contributor, and/or decision maker from SM — is responsible for adding the asset to the inventory.

Creating assets is often a collaboration between Strategic Marketing and other GitLab team members or community members. By inventorying an asset here, we're not indicating it's "owned" by SM v. other parts of the department or company, only whether SM has contributed enough to identify a DRI for our team and in our view, to warrant having it here.

SM leadership will support team members in completion of the inventory, and they will support broader GitLab team members by serving as backup DRIs for their team's assets.

</div>

##### **Lead a group conversation**
{: .panel-heading}

<div class="panel-body">

The SM group conversation lead could share this page and the inventory with the call, showing assets recently created. This handbook-first approach can reduce slides in the deck and relieve some of our six-week scramble to list all the things.

Since GC decks list both assets and activities, we'll need to either still list activities separately or find another source, like tagging Calendar events and pulling those into a shared view...

Demonstrating the inventory briefly and regularly would also encourage self service, before asking if we have a thing, where it is, or for us to make it.

</div>

##### **Ask for help or suggest a change**
{: .panel-heading}

<div class="panel-body">

To make a change request, or if you have questions or need help please open an [SM support request](https://gitlab.com/gitlab-com/marketing/product-marketing/issues/new?issuable_template=A-SM-Support-Request).

You're also welcome to ask in our [#strategic_marketing Slack channel](https://gitlab.slack.com/archives/CPTKGRXHP), but remember it's ephemeral :)

We have a [backlog of change requests](https://gitlab.com/dashboard/issues?scope=all&utf8=%E2%9C%93&state=all&assignee_username=brianglanz&milestone_title=SM%20-%20Backlog&search=Inventory) for the database, dashboard, and project.

</div></div>

## Learn@GitLab Inventory

### Inventory Files

The inventory files provide a standardized way to capture, find, and reference created assets (inventory) which can be used by everyone. The data is kept in the yml files in the /data/inventory/ directory. There is one file per team to make ownership clear and make management easier.

#### Layout

The `inventory` folder lives under `/data` of the website and is organized in the following manner to enable scaling to multiple groups. The thought is that each group can be [CODEOWNERS](https://docs.gitlab.com/ee/user/project/code_owners.html) for their own team inventory, but it should still be easy to search through the inventory of "everything" to find what you are looking for.

<pre>
/data/inventory
     |
     ---- learn.yml (Technical Marketing - will change to team name in another MR)
     |
     ---- pmm.yml (Product Marketing)
     |
     ---- ...
     |
     ---- team_name.yml (Team Name)
</pre>

#### Format

The search through the inventory of "everything" to find what you are looking for it is important that all team files use the same format and data fields. This file represents the SSoT for what that format and fields are. If you are making changes make them here first, then make sure everything else follows.

Accepted field descriptions are (fields in bold are required):

<pre>
- title*:                              (the display name of the asset)
   author*:                            (the author of the asset)
   team*:                              (the name of the team that created the asset)
   asset_type*:                        (currently one entry only. Expect this to grow as teams are added. asset type = video, demo)
   date_published*:                    (month and year content first published. In iso-date format. eg 2020-05)
   last_changed                        (date the asset was last changed)
   gitlab_release:                     (major.minor GitLab release # the asset is built about/on. eg 12.10)
   use_case*:                          (use case the asset focuses on. [Derived from customer use case page](/handbook/use-cases/). Acceptable values are:   )
      - vcc
      - ci
      - cd
      - devsecops
      - agile
      - simplify_devops
      - cloud_native
      - gitops
      - remote
      - other
   stage:                              (multi-select list of stages the asset focuses on. Values should match main entries in [stages.yml](/data/stages.yml))
   category:                           (multi-select list of categories the asset focuses on. Values should match main entries in [categories.yml](/data/categories.yml))
   link*:                              (link to the ungated asset)
   embedded_link:                      (link to embeddable version of asset - typically for videos and demos)
   gated_link:                         (link to the gated asset)
   short_description:                  (a short description of what the asset is about)
   learn:                              (values: true or false or blank. Does this asset show up on learn@gitlab.com. tech marketing team to add this only please)
</pre>

## Getting help

If you have questions or need help please open an [SM support request](https://gitlab.com/gitlab-com/marketing/product-marketing/issues/new?issuable_template=A-SM-Support-Request).
