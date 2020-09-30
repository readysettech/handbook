---
layout: handbook-page-toc
title: "Sigstr"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Uses

Sigstr is a marketing tool used as an advertising channel inside the inbox. 

## Training & Help

1. [Sigstr overview video](https://help.sigstr.com/en/articles/1626095-sigstr-overview-video)
1. [Application training tutorial](https://help.sigstr.com/en/articles/2545315-sigstr-application-training-tutorial)
1. [ABM video tutorial](https://help.sigstr.com/en/articles/1118019-abm-video-tutorial)
1. [Dynamic campaigns tutorial](https://help.sigstr.com/en/articles/1118024-dynamic-campaigns-tutorial)
1. [Groups video tutorial](https://help.sigstr.com/en/articles/1118058-groups-video-tutorial)
1. [Knowledgebase](https://help.sigstr.com/en/)

## Account Settings

### Admin 

From this tab you can view the account owners and admins, set company signature field defaults, set default UTM paramters, and change the default account time zone.

### Recipients

On this tab, you can define the email recipient domains who will receive any campaign designated as internal. This is currently set as `gitlab.com`.

### Transfer ownership

To transfer account ownership, the owner must login and navigate to `Account Settings` > `Ownership`. From this page, click the `Pick New Owner` drop down, select the person whom you will be transferring ownership to, then select `Transfer`.

### Security

Change password or view API keys for third-party integrations.

### Integrations

#### Salesforce

The [integration between Sigstr and Salesforce](https://help.sigstr.com/en/articles/3075787-sfdc-integration-overview) allows marketers to:

1. Sync campaigns lists from Salesforce into Sigstr for use in targeted Sigstr campaigns
1. See which open and closed opportunities have been influenced and generated by Sigstr campaigns
1. Track which email recipients click on a Sigstr campaign and how often on an account and contact level

#### Outreach

Sigstr appends campaign banners to Outreach signatures every 24 hours. If they are changed from Sigstr, campaign banners in Outreach update in real-time. There must be an employee in Sigstr with an email address that matches the user or mailbox in Outreach in order for a campaign banner to be appended.

#### PathFactory

Each Sigstr campaign banner only points to one link. With PathFactory, we can use one link while providing additional content for the receipient to consume.

You can identify who clicks on your email signature banners and track content consumption using PathFactory. Using these insights you can optimize your email signature campaigns and content tracks, while simultaneously identifying highly engaged prospects.

To take the most advantage of this integration, it's recommended that you pair your Sigstr banner campaign with an equally targeted content track. To request a content track for a Sigstr campaign, please open an issue in the marketing operations project using the `pathfactory_request.md` template and assign to `@sdaily`.

### Notifications

Select the type and frequency of system notifications from Sigstr. Daily emails are sent every morning. Weekly emails are sent every Monday morning.

- **Engagement reports** - Emailed daily or weekly and show who has recently clicked a campaign banner. To opt in/out of your individual engagement report email, visit the employee preference center.
- **Install Reminders** - Send reminders to all employees who have yet to install their Sigstr signature. These reminders will be sent automatically based on the selected frequency until the user has successfully installed their signature.
- **Campaign Clicks** - Send real-time notifications to employees anytime someone clicks their Sigstr Campaign banners. These notifications include the date, time, and contact who clicked on the Campaign banner. Employees can opt out of these notifications by editing their profile. This will automatically enable Campaign Click Notifications for new employees added to Sigstr in the future.
    - **Campaign Click Notification Blocklist** - Ignore clicks from some domains (for example, clicks from email security clients). Currently set up to ignore clicks in analytics from GitLab employees.

### Privacy & Data

#### Export Data Archive

Create an archive of a recipient's data from Sigstr. The archive will be emailed within 1-2 business days.

#### Delete Individual Recipient Data

Request to delete a specific email recipient's data. This will delete the click and views recipient data and records if they are on a list. A confirmation email will be sent within 1-2 business days.

#### Data Retention

Configure your account to clear out Sigstr's store of recipient data on regular intervals. This will delete the clicks and views of all affected recipients.

### Verify

Using [Verify](https://help.sigstr.com/en/articles/1633561-sigstr-verify), you can troubleshoot the timing and personalization of Sigstr campaigns. 

1. Click the account avatar in the bottom right-hand corner and choose `Verify`. 
1. Input the `Sender`, `Recipient`, and `Date of Send` to preview the matching campaign. For `Sender`, select a group or specific email address. For `Recipient`, select a recipient list or specific email address. Please note that the `Recipient` section only pertains to `Targeted` and `Internal Campaigns` while the `Date of Send` only pertains to `Scheduled Campaigns`. 
1. The `Results` section details why the campaign was chosen. 

## Best practices

1. [Campaign design guidelines](https://help.sigstr.com/en/articles/1117946-campaign-design-guidelines)
1. [Campaign use cases](https://help.sigstr.com/en/articles/1641514-campaign-use-cases)
1. [Campaign best practices](https://help.sigstr.com/en/articles/1638530-campaign-best-practices)
1. [GIF best practices](https://help.sigstr.com/en/articles/1638798-gif-best-practices)
1. [Internal use cases](https://help.sigstr.com/en/articles/1638968-internal-use-cases)
1. [Signature design guidelines](https://help.sigstr.com/en/articles/1117943-signature-design-guidelines)
1. [Signature best practices](https://help.sigstr.com/en/articles/1638563-signature-best-practices)

### Banner ad image best practices

The image will be constrained to half the size to ensure high density of pixels. Use the same banner ad size for all campaigns.

- 900 wide x 240 pixels tall
- 8px radius corners
- `.png` or `.gif`

## Signatures

### Resources

1. [Signature management](https://help.sigstr.com/en/collections/96989-signature-management)

### Default fields

- First name
- Last name
- Job title
- Company URL

## Campaigns

### Resources

1. [Campaign management](https://help.sigstr.com/en/collections/96983-campaign-management)

### Use cases

- [36 Creative Use Cases for Email Signature Marketing](https://resources.sigstr.com/ebooks-or-reports/36-creative-use-cases-for-email-signature-marketing)

**Content**

1. Whitepapers and eBooks
1. Events & conferences
1. Case studies
1. Product Releases
1. Promotional video & teaser

**Targeted**

1. Region
1. Customer status
1. Persona
1. Industry
1. Past engagement
1. Opportunity stage

### Types

1. **Default** - Display a banner ad as a fallback if no other rules apply
1. **Sender** - Assign banner ads to one or more employee groups
1. **Targeted** - Target banner ads to lists of contacts or accounts
1. **Internal** - Promote internal initiatives and content to GitLab employees
1. **A/B test** - Test two different banner ads to determine a leading variant
1. **Alternate** - Provide employees with a banner ad they can subtitute on compose
1. **Shuffle** - Promote up to five banner ads each with their own unique URLs

### Create a campaign

Before creating a Sigstr campaign, you need to [request a Sigstr banner ad](https://about.gitlab.com/handbook/marketing/growth-marketing/#brand-and-design-issue-templates) from the growth marketing team. All Sigstr banner ads should use the same dimensions (900 wide x 240 pixels tall; 8px radius corners) and be delivered in a `.png` or `.gif` format.

1. Select `Campaigns` from the side menu (flag icon).
1. Click the `Create Campaign` button in the top right.
1. Select your desired [campaign type](/handbook/marketing/marketing-operations/sigstr/#types), name your campaign, and click `Get Started`. You are redirected to edit the campaign details.
1. Name your banner ad, enter alt text for the image, and upload the banner ad. All banner ads uploaded to Sigstr must have consistent dimensions to all other banners in our instance for consistency of output. Please follow [best practices](/handbook/marketing/marketing-operations/sigstr/#best-practices). 
1. Under `Clickthrough URL`, choose your desired link type (manual clickthrough URL, mailto, or PathFactory experience). Note that you must already have a finalized PathFactory URL before selecting `PathFactory Experience`.
1. Select the `UTM Parameters` drop down to add additional parameters for your campaign. If you do not enter additional paramters, the default parameters will be applied: `source=email_signature&medium=sigstr&content=employee_email` Note that your campaign name became the default parameter for campaign. You also have the option of adding custom UTM parameters if desired. It is highly recommended that you apply UTM parameters to your campaigns to properly report success.

### Review and activate a campaign

1. On the left side of the campaign edit page, click `Review`. You can also select the `Next` button to accomplish this same action.
1. Verify the look of your campaign. Ensure that the banner image does not appear blurry. If it appears blurry, try reuploading the banner image. If you still experience issues, please create an issue in the marketing operations project and assign `@sdaily`. 
1. Confirm the banner ad properties including the name, alt text, and clickthrough URL. Please test the URL to ensure it's working and that it leads to your desired location.
1. Choose your desired schedule for this campaign from the `Schedule` pane. You can choose to start the campaign immediately or at a later date/time. You can also set your campaign end date/time or let it run indefinitely.
1. If there is anything missing from your campaign, Sigstr will show you in the `Activate` pane below `Verify` pane. Before you can activate a campaign, you must enter all required campaign attributes (banner ad, clickthrough URL). 
1. Once finalized, click `Activate this Campaign`. You can also choose `Save Campaign & Exit` to save the campaign as a draft and activate at a later date.