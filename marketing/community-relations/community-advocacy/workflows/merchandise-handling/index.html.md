---
layout: handbook-page-toc
title: "Merchandise Workflow"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Common Merchandise Requests

You might have landed on this page looking for answers to questions about swag, giveaways, etc.

| --- | --- |
| Hosting a Giveaway? | Please follow the steps on the [GitLab Giveaways page](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/giveaways/) |  
| Requesting swag for a community member, customer, or speaking event? | Follow the processes outlined on the [Swag Requests page](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/swag-requests/) |

## Merchandise Overview

Community Advocates manage the merchandise store. This includes:
- Adding and removing items to and from the store
- Fulfilling orders
- Maintaining inventory levels
- Responding to store support requests
- Supporting GitLab teams with giveaway requests
- Tracking and refunding swag that has been lost in shipping
### Accounts overview

Shopify is our storefront vendor
- URL: `https://shopify.com` — Use `gitlab.myshopify.com` if prompted for the store address.
- Login: See 1Password secure note for details
- Account permissions: [Staff account](https://help.shopify.com/en/manual/your-account/staff-accounts) is required to access the admin. Staff accounts can only be created by the [store owner](https://help.shopify.com/en/manual/your-account)
- Note: Community Advocates use a shared account, as the number of staff accounts for our [current subscription](https://www.shopify.com/pricing) is limited to 5.

Printfection is our main inventory vendor for general merchandise
- URL: https://www.printfection.com/
- Account Permissions: `print`, `manage`, `admin` 
- Login: Use Community Relations 1Password credential from the marketing vault.
- Note: We are currently using a shared account, but we should migrate to individual accounts for each Community Advocate. If we do migrate to individual accounts, we all need to use the merch@gitlab.com email address so that updates are kept in Zendesk.

Stickermule is our main inventory vendor for stickers
- URL: https://www.stickermule.com
- Login: see 1Password secure note for details

Other current vendor accounts include: Nadel, Panda Bear Creative, WASD Keyboards. 

You can see the items we've ordered from Nadel [on this Google sheet, visable to GitLab team members](https://docs.google.com/spreadsheets/d/17_nqCA_YdlE3sRY6vksRBYHBDPRpaMMTd9qnWedLRyo/edit?ts=5df92d5e#gid=0)

### Shopify and Printfection Integration

When a customer visits the [GitLab Store](https://shop.gitlab.com/), they see available products on the front end Shopify store. Advocates manage customer orders using Shopify's backend, and fulfills/ships orders on the Printfection backend.

### Shopify/Printfection Zapier Integration

All the orders received via [shop.gitlab.com](https://shop.gitlab.com/) are automatically forwarded from Shopify to Printfection via the Printfection-Shopify Zapier integration. On Printfection, we manually process orders and fulfill shipments.



## Merchandise Workflows

Advocates have daily, weekly, and monthly tasks to complete for merchandise.

### Where to Find Merchandise Notifications
* Notifications from Shopify and Printfection are sent to merch@gitlab.com and can be managed in the Merchandise view within Zendesk.
* GitLab team members often use the #swag Slack channel to ask questions about merchandise and orders. 
* When communicating with contributors, users or customers regarding swag, use the merch@gitlab.com email alias.

<i class="fas fa-hand-point-right" aria-hidden="true" style="color: rgb(138, 109, 59);"></i> Please bear in mind the [list of countries we do not do business in](/handbook/sales/#export-control-classification-and-countries-we-do-not-do-business-in).
{: .alert .alert-warning}


### Daily Tasks

#### Daily Task #1: Fulfill Swag Store Orders

GitLab team members can use the Unfiltered Youtube Channel to watch the following trainings: [CA Training, Merchandise: Daily Swag Store Tasks](https://youtu.be/Uybr00uCbQE) and [Daily Merch Tasks Video tutorial](https://drive.google.com/file/d/16pcdtfwbNye0SmtX20QOhqwP0TYbijVG/view?usp=sharing)

The [Daily Swag Order Reminder calendar](https://calendar.google.com/calendar?cid=Z2l0bGFiLmNvbV9iZnJhODA3czFpOGQ2cnNncXZvcWJmNDlhY0Bncm91cC5jYWxlbmRhci5nb29nbGUuY29t) is integreated with Zendesk via Zapier to create a daily Zendesk ticket in the Merchandise view as a reminder to place Shopify Store Orders in the correct Printfection campaign. In order to process these orders, they needs to be fulfilled in both Shopify and Printfection.

After the daily orders are placed, the advocate who placed the orders should mark the ticket as `solved`.

##### Step 1: Fulfill Shopify Orders

GitLab uses Shopify as a customer facing online store and backend order fulfillment. Fulfilling orders in Shopify serves to send the actual notification that an order has been processed, including the invoice for the customer.

1. Login to Shopify
2. Navigate to 'Orders'
3. All new orders will appear highlighted with the yellow Unfulfilled tag
4. Before fulfilling orders in Shopify, begin the Printfection order fulfillment process. It is important to confirm that Shopify and Printfection orders are the same before fulfilling.
5. Select all order you'd like to fulfill by clicking the small checkbox on each order.
5. Click on 'actions' -> fulfill selected orders
6. Make sure that the default "send a notification" option is selected and press the fulfill button

That's all, the customers should receive their confirmations automatically.

##### Step 2: Place Printfection Orders

GitLab uses Printfection as both a vendor and a warehouse. Fulfilling orders in Printfection means that Prinfection will pack and ship items to the customer.

1. Login to Printfection
2. Navigate to the Collection Orders and choose "Shopify Store Orders."
3. Go to the Manage tab
4. Make sure that all unfulfilled orders from Shopify are shown in Printfection and that everything is okay.
5. If an order appears in Shopify but not in Printfection, follow the workflow to manually add an order
6. Press the "Place Orders"

That's all, Printfection will handle the rest. 

Note: Printfection sends email confirmations to the customer when the order is placed, processed, shipping, and delivered.

#### Daily task #2: Process Zendesk Tickets, Swag Channel Questions, and Common Swag Order Issues

Zendesk and the #swag Slack channel are the most common places that community members or GitLab team members will ask questions about swag. Use this chart to determine the best action on how to solve each inquiry.

If you are ever unsure about the status of a swag store order, please reach out to support@printfection.com via the merch@gialb.com email alias and include the order number.

| Ticket/Question Topic | Action Steps |
| ------ | ------ |
| An order was placed, but we're out of stock for that item | Send the Out of Stock Email Template to the customer from merch@gitlab.com or via slack message with a $15 discount code|
| A GitLab team member wants to send swag to a customer or community member | Share the [Swag Requests Process Link](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/swag-requests)| 
| A GitLab team member wants to add special swag to a customer or community order | Offer our current swag requests processes, and suggest they discuss with their manager if they can purchase and expense additional items |
| Someone shares a great idea for new swag | Ask them to document their ideas on the [GitLab Swag Ideas and Process Improvements Issue](https://gitlab.com/gitlab-com/marketing/community-relations/community-advocacy/general/-/issues/56) |
| A order from the swag store never arrived | Check the status of the order by searching both Shopify and Printfection using the user's email address. If the package was shipped at least 1 month before and as not been delivered, assume it is lost and follow the [Delayed and Lost Merchandise Shipment process.](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#delayed-and-lost-merchandise-shipments) If the package was shipped within one month, ask the customer to wait for 1 month before taking action. If one month has passed, share a $30 discount code. If you need additional information, email the Printfection warehouse at <support@printfection.com>. |
| A customer reports their swag is stuck at customs  | Follow guidelines in the [Customs Issues for Shipments Outside of the USA](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#customs-issues-for-shipments-outside-of-the-usa) |
| Someone is wondering about when items will come back into inventory | Refer them to the most recent swag order epic or issue for the most up to date information |
| StickerMule reaches out about delivery issues with sticker order | Coordinate with customer via merch@gitlab.com on case by case basis to provide necessary information to Stickermule and UPS |
| Someone reports their discount code doesn't work | Confirm where the customer received the discount code. Reshare the code and a direct link. If the code still does not work, [generate a new discount code](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#creating-shopify-discount-codes) and share via email. |
| A vendor sends a general email or fulfillment update | For updates sent automatically from Printfection, Stickermule, Sendoso, or Shopify, apply the `vendor-update` macro to solve the ticket |


##### Common Order Problems

###### Delayed and lost merchandise shipments

From time to time it may happen that the package never arrives to the customers. Customers usually complain via <merch@gitlab.com>, however, keep an eye on Twitter, the #swag Slack channel and other related threads.

If the customer's package has been in transport over 1 month, take the following action:

1. First, ask the customer to reach out to <support@printfection.com>(for swag store orders) or <help@stickermule.com>(for sticker orders) and ask them to inquire about their order status. Use the 'Ask Customer to Contact Princection' email template using the 'Swag::Ask Customer to Contact Printfection' macro.
1. If instead you would rather reach out to Printfection for updates, uses the 'Printfection Order Support' email template using the <merch@gitlab.com> alias from your Gmail account.
2. If Prinfection support determines the package is still in transit and Printfection believes the order will be deleiverd soon, Printfection will let the customer know to continue to wait, and will provide updated shipping information. 
3. If the customer reaches back out to the swag team, ask them to wait at least another 2 weeks for their order before assuming it is lost.
4. If Printfection determines the package is lost or determined undelivereable, they will direct the customer back to the swag team.
5. In this case, follow the [Refunding Orders](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#refunding-orders) process and send the lost order email template.

###### Customs Issues for Shipments outside of the USA

Since all swag in the store ships from our warehouse in Denver, CO, USA, customers outside of the US may have issues with customs tax payments upon delivery of their package.

Swag used in the swag store and in giveaways is sent from a warehouse in the USA. GitLab is not responsible for costs related to taxes and customs required to receive swag. These costs are at the responsibility of the customer or recipient of the giveaway.

The Advocates team is working on the possibiliy of creating a customs statement for swag shipments to avoid these costs. Updates can be followed in [this issue](https://gitlab.com/gitlab-com/marketing/community-relations/merchandise/general/issues/12).

If a customer orders swag and reports the swag is being held at customs in their country, follow these steos:

1. The customer will likely email merch@gitlab.com and ask why their order hasn't arrived yet. This is most common with orders that have a $0 invoice or value, since they are flagged for review as 'gifts' at many customs stops.
1. Look up the customers order via their email in Printfection. In the order, you can see a tracking number from USPS. Check the status there. If you cannot determine the location of the package from USPS, check the tracking page for a local tracking number. Copy and past that local tracking number into Google to search international shipping agencies for the location. Here, you will likely see the status reads as 'held at customs'. This language will vary by nation and shipping agency.
1. If the order is stuck in customs, you need to generate an invoice for the customer.
1. Log into Shopify and find the customer's order.
1. Click the 'print' option and save the page as a PDF to your computer.
1. Respond to the customer's ticket and attach the invoice. Advise them to reach out to their local post and share the invoice so they can confirm the recipet of the swag.
1. If you need support in doing this, or if the customer reports they cannot communicate with the shipping agency, ask printfection via the support@printfection.com email if they can provide the local shipping agency with the invoice.

Until the customs statement is created, the following strategies can be used to avoid customers paying the tax.

1. At checkout in the Shopify store, customers can choose Expedited or Priority Shipping and email merch@gitlab.com for reimbursement of shipping costs.
2. If a customer reports their swag cannot be delivered due to a customs issue, advcoates can place a new order via Printfection and choose the 'Ship By Date' option to insure delivery.
3. For large orders of swag, or orders with multiple items, customers and advocates can break up the order into multiple, smaller orders. This may prevent packages from being stopped for customs tax.


#####  Swag Email Templates

###### Out of Stock

```
Thanks for placing an order in the GitLab store!

We're sorry to report that since placing your order, our <out of stock item> has gone out of stock.

We've gone ahead and cancelled your order and processed and necessary refunds.

Please use the discount code <link discount code> for a future purchase in the GitLab swag store.

Thanks!
```

###### Lost Order

```
Dear {Customer Name},

I'm reaching out regarding your recent order from the GitLab swag store. Unfortunately, due to shipping and handling issues, your order has been lost.

I've gone ahead and refunded you the cost of your initial order.

Please use this discount code `link discount code` to use on a future purchase

Thanks for your patience and let us know if you have any questions,

Sincerely,
{Your Name}

```

###### Ask Customer to Contact Printfection

```
Thanks for reaching out about your Swag order!

Can you please email our warehouse, Printfection, at <support@printfection.com> to inquire about your order status? Please include your order number and email used to purchase in your email to their support team.

If they determine your package is lost, please forward their email to our team at <merch@gitlab.com> and we will get you set up with new GitLab swag.

Thanks for your patience!

{Your Name}
```
###### Printfection Order Support

```
Hi Printfection team! I need some support in finding the order status of order number `enter order number`. Can you please let me know any updates on this order's shipping status, or if it has been lost or returned to the warehouse?

Thanks!

{Your Name}
```


### Weekly Tasks

#### Weekly Task #1: Inventory Check

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [CA Training, Merchandise: Update Shopify Store Inventory](https://youtu.be/SGKvQraQfs4)

**The Printfection inventory is our single source of truth for merchandise totals.** Since many campaigns pull from the same Printfection inventory, our Shopify storefront does not stay up to date on its own. Right now, there is no way for our storefront to know about inventory use outside of the store campaign, so we must do a manual update.

The [Weekly Swag Inventory Check Reminder calendar](https://calendar.google.com/calendar?cid=Z2l0bGFiLmNvbV90dHRpZDMzNmtyamFkMzZzMTI1ZW81MTZxNEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t) is integreated with Zendesk via Zapier to create a weekly Zendesk ticket on Tuesday in the Merchandise view as a reminder to update Shopify inventory totals to match our single source of truth inventory in Printfection.

It is required for community advocates to compare Shopify and Printfection inventories 1x per week to avoid out of stock orders from being processed. This is a high priority for products with low inventory.

Advocates can review the weekly Printfection inventory email reminder that gets sent to the `merch@gitlab.com` email domain every Monday. This email has GitLab's Printfection inventory numbers organized in a spreadsheet. Advocates can filter the spreadsheet format by the amount of Printfection items in stock. (recommended you filter low to high) Once the Advocate has a good sense of what is out of stock, or low in stock, the Advocate can update inventory or proceed as needed. 

##### Update Shopify Inventory Using Printfection
1. Log into Printfection
2. Click on the `Inventory` tab
3. On the Inventory page, click on `Inventory Levels`
4. The data colummn titled 'Physically Available' is the most important data point. This represents the number of that item that currently available in the warehouse 
5. Log into Shopify
6. Click on `Products`. This page will show an overview of the inventory available for each item. 
8. Compare each item's inventory in Shopify with the Physically Available inventory information in Printfection. 
9. If inventory totals in Shopify differ, click on each item and edit the inventory totals. Click `save` after each item update.




### Monthly Tasks

At the end of each month, advocates should follow the steps to [Report use of Bulk Swag](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#reporting-on-use-of-bulk-swag-orders) to finance for appropriate billing.


## Additional Merchandise Workflows

### Common Printfection Workflows

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [CA Training, Merchandise: Edit, Resolve Issues, and Delete Printfection Orders](https://youtu.be/W6TGM74rnTk)

#### Printfection Collections 

Printfection's Collection campaign is a way to easily collect orders, review them, and then place them all at once. You can manually key-in orders, import orders from a CSV file, or allow other parties to place orders through a hosted landing page.

##### Create a new Collection campaign

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [Create a Collection Campaign](https://youtu.be/5mwwvpbHZ_I)

1. Go to Campaigns tab then click Collections 
2. Click the **+COLLECTION CAMPAIGN** button. 
3. Enter the name,
4. Select the option that turns on External Ordering (this option will provide you a link that allows users to place orders for this campaign).
5. Press **CREATE CAMPAIGN** button.
6. Go to the **Items** tab in the navigation menu.
7. Click **Add Items to Campaign** and simply choose the items you want to offer in your Collection.
8. Go to **Settings** in the navigation menu and update the GitLab branding (see the existing givaway settings). You'll also need to specify a payment method on this page.
9. In the **Settings** tab, add the relevant campaign or finance tag in the `PO` section. This is required to start your collection.
10. Turn the campaign from **Paused** to **Running** in the top right navigation menu. And that's it, you're ready to give some swag!

Last, but not least, you'll want to review the orders from the Manage page within your Collection campaign. Here you can change, update, or remove orders. Review your totals, fulfillment cost, and other details.  When you're ready hit Place Orders and place them all at once!

#### Restoring Users in Printfection

GitLab team members can use the Unfiltered Youtube Channel to watch the following training:[CA Training, Merchandise: Restore Users in Printfection](https://youtu.be/QCuCqjXkmW8)

When Printfection users become inactive on the platform, their accounts need to be restored. This happens most often when the GitLab sales team tries to use the sale swag campaign.
 
1. Hover over your profile image and navigate to the 'Manage Users' section
2. First, search for the user in the Active User List using their email. If their account shows here, they can access Printfection. 
3. If you do not see their account in the Active User List, scroll down to the Disabled User List. Search for their account using their email in this list.
4. To restore their account, click on the blue 'RESTORE' button. Make edits to their account based on the permisssions you'd like to grant. Most often, GitLab team members should only have the 'request' permission enabled.
5. Communicate via slack with the GitLab team member and have them retry logging into Printfection.

#### Canceling any external order on Shopify and Printfection

You can always cancel the pending/processing orders. All the orders including the orders via Shopify Collections using Discount Codes can be canceled.

1. From your Printfection home page go to the **Shopify store orders** collection.
2. Under the **Manage** tab, search for the order you want to cancel.
3. Click **Delete order** button.
4. You are done. The order won't be fulfilled by Printfection

Please note that you should always change the status of the orders in Shopify as well.

1. From your Shopify admin page go to the **Orders** page
2. Click on the order you want to change
3. Press **More Actions** button in order to see the drop menu options
4. Select **Cancel order** option

#### Manually Add Orders to Printfection

If orders unfulfilled orders appear in Shopify but are not in Printfection, you might need to manually add the order to Printfection before fulfilling the order.

Before manually adding orders, use the search tool in Printfection to check for orders that are unfulfilled in Shopify. Sometimes, a user will fulfill orders in Printfection without checking Shopify. If you find that an order has already been fulfilled in Printfection, simply fulfill the order in Shopify.

If you cannot locate the order in Printfection, you'll need to manually add the order.

1. Login to Printfection
2. Navigate to the Collection Orders and choose "Shopify Store Orders"
3. Go to the Manage tab
4. Click the "Add Order" button
5. Click the "Add an Item" button to add items from the GitLab Shopify store to the order. Use the original order from Shopify as a guide to choose the correct product and size
6. Use the original order from Shopify to copy all relevant customer information into the Printfection order. Be sure to include name, shipping address, and email address
7. Click the "Save Order" button then the "Place Order" button
8. Complete the workflow for fulfilling the order in Shopify

#### Removing Products from Printfection

Items can be archived from the Printfection warehouse when the inventory is 0 and the item is removed from active kits and campaigns.

1. Log into Printfection
1. Navigate to the Inventory tab
1. Select the 'Archive' button for any items you'd like to remove from the warehouse.
1. You can verify/view all archived items in the 'Archived' inventory tab.
1. You may be promted to remove the items from related kits and campaigns before it can be archived. Remove the items from active kits and campaigns, then try to click the 'Archive' button again.

#### Finding Tracking IDs

The Tracking ID is usually assigned by Printfection 2-3 days after the order is received. Sometimes, users may request their Tracking ID.

Please follow these steps if the user requests the Tracking ID:
1. Look for the requester's **name/email**
2. Go to the Printfection **Reports** page
3. Search for the order using the name/email
4. Copy the **Tracking ID**
5. Confirm that order's details match the requester. You can double check this via Shopify:
    * Search for the same order/person in Shopify
    * Compare if the **items**, **full name**, **email** and the **dates** are correct
6. Email the **Tracking ID** or the full **Tracking Link** to the requester
    * You can always open the full **Tracking Link** by clicking on the **Tracking ID**.
7. (Optional step) Assign the **Tracking ID** to the requester's order in Shopify:
    * Find the order in Shopify
    * If you already fulfilled the order in Shopify, click **Add tracking** button and paste the ID.
    * If the order is unfulfilled in Shopify, mark it as **fulfilled** and then add the **Tracking ID**

#### Creating External Order Links
External order links are an efficient way for GitLab team members to place swag orders. For example, the Sales team uses an external order link for Sales employees to send merchandise to customers and prospects.

External order links can only be used by users with the @gitlab.com domain, so they are not an efficient tool for wider community orders.

1. First, create a new collection campaign. Navigate through Campaigns -> Collections -> + Collection Campaign to create a new one.
2. Name your campaign and click the blue 'Create Campaign' button.
3. Add items to your campaign by clicking the 'Items' tab and selecting swag from the inventory. When adding an item with variable sizes, choose any size as a place holder. When customers access the order link, they can select/edit sizes and qualities.
4. Next, on the 'Overview' tab, scroll down to the section titled 'External Orders'. Toggle this setting to 'On'.
5. You can make additional edits to the External Order form by clicking the 'Settings' tab. Here you can make changes to the UI of the external order link.
6. In the 'Overview' tab, you'll see the external order link you can send to GitLab employees where they can place their order. You'll have to manually approve orders in Printfection in order for them to be fulfilled.

#### Archiving Items
1. If you've used all your swag, follow the steps to [archive your items](https://help.printfection.com/hc/en-us/articles/216948387-How-to-archive-items).

#### Naming Items in Printfection

Many teams at GitLab use Printfection to manage swag for giveaways. Since we all share one Printfection platform, naming conventions are essential to keep swag organized.

Use the following naming convention for items that are reserved for a specific team or program. This swag is **ONLY** available to the team included in the naming convention.

`Team Name - Item Name`

Use the following naming convention for items that are available for company wide giveaways at GitLab.

`Item Name - Giveaway Option`

If an item does not have a clear naming convention and you aren't sure if it is available for use, always ask in the [#swag Slack channel](https://app.slack.com/client/T02592416/C66R8N98F/thread/C0R04UMT9-1597854168.038500) before using the merchandise.


### Common Shopify Workflows

#### Removing Products from Shopify

1. Log in to Shopify
1. Open the Products page
   - Click on the product you want to remove
   - Scroll to the bottom of the page where you can find the delete button

<i class="fas fa-info-circle" aria-hidden="true" style="color: rgb(49, 112, 143)
;"></i> For more information, see this [official guide](http://shopifynation.com/shopify-tutorials/delete-products-variants-shopify/)
{: .alert .alert-info}

#### Refunding Orders

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [Refund Shopify Orders](https://youtu.be/yG8SGV0LVxY)

Sometimes orders need to be refunded to the customer. An example of this could be if a customer places an order for an item that is out of stock. Refunds are processed through Shopify.

1. Find the order in Shopify
2. Check Paid notes to see the total amount paid by the customer
3. Click 'Refund'
4. Add a reason for the refund. This is an internal note
5. Add the total amount for refund
6. Click the 'Refund' button to process the refund to the user
7. Find the user email address on the order and send them an email via the merch@gitlab.com email address. Explain the reason for the refund and include a link to a discount code to be used on a new order.

#### Creating Shopify Discount Codes

In order to create a coupon code on Shopify, please check out this [video tutorial](https://drive.google.com/file/d/1h9ZJgktR2iGxJqz7Fqy9FqMjVtF19YJ9/view?usp=sharing).

#### Downloading CSV Order Files

In Shopify, you can downlaod a CSV file of orders. This file can be used to manually upload orders into Printfection if the Zapier intergration is broken or there is an issue with inventory levels.

* Navigate to Shopify -> Orders
* Use the filters at the top of the page to set restrictions on what information should be included in the file
* Click the 'Export' button and choose '50+ orders matching your search' for the 'Export' category and 'CSV for Excel, Numbers, or other spreadsheet programs' for the 'Export As' file type
* Shopify will send an email to merch@gitlab.com with this CSV file. If you do not see the email come through the Merchandise Zendesk view, check the Suspended Tickets view.
* Remember that downloading CSV files from Shopify involves customer's contact information, including email, phone number, shipping address and  billing address. Before sharing the data with a third party (e.g. via e-mail), advocates should review emails, Slack messages, or GitLab issues with at least 1 other community advocate to reduce the risk of incorrectly sharing personal information




## Ordering New Swag

### Tracking Swag Orders Using GitLab

Consider using GitLab Epics and Issues in the [Merchandise project](https://gitlab.com/gitlab-com/marketing/community-relations/merchandise/general) to track swag orders each month. Here is an [example from the swag order from March/April 2020](https://gitlab.com/groups/gitlab-com/marketing/community-relations/-/epics/12).

### Choosing a Vendor

Most swag items are purchased through Printfection. 

As a general rule, consider using [Stickermule](https://www.stickermule.com) for sending stickers, since the Printfection inventory is limited. If Stickermule doesn't work for you, then use Printfection instead.

If the merch shipment includes:
* only stickers -> always use Stickermule
* a small number of items (depending on Printfection inventory) -> use Printfection
* a large amount of stickers and other merch -> consider using both Stickermule and Printfection
* items that Printfection doesn't print -> refer to our vendors list for the best fit

### Creating, Replenishing, and Ordering New Swag Items

The Marketing team aims to create swag that is "small batch, limited edition and themed for the community to collect." To uphold this value, swag store items are frequently swapped out and replenished with new and different swag. Follow these steps to create new swag items for the Shopify store.

1. First, review the [Corporate Marketing Swag handbook page](/handbook/marketing/corporate-marketing/#swag). Keep these swag requirements in mind while planning and brainstorming new items.
2. Consider brainstorming with other GitLabbers in the #swag channel. Post a poll or a open an issue and ask for swag requests. See this [issue](https://gitlab.com/gitlab-com/marketing/community-relations/community-advocacy/general/issues/56) for an example.
3. Review the GitLab [press kit logos](https://about.gitlab.com/press/press-kit/) to ensure the artwork you choose aligns with the compnay brand.
3. View the [Printfection Catalog](https://www.printfection.com/swag/) for item inspiration.
4. If you cannot find and item you like in Printfection, consider using another vendor to fulfill the order.
5. After deciding on a product, collect the following information: Item Cost, Size/Dimensions, Weight, and Color Options
6. Open a [Brand and Design Issue issue](https://about.gitlab.com/handbook/marketing/growth-marketing/#brand-and-design-issue-templates). If you are asking for approval of a swag mock up, use the [Requesting Brand Review issue](https://gitlab.com/gitlab-com/marketing/growth-marketing/growth/-/issues/new?issuable_template=request-brand-review). If you need a new design creaated for your swag, open a [Requesting a new design issue](https://gitlab.com/gitlab-com/marketing/growth-marketing/growth/-/issues/new?issuable_template=request-design-general) All new swag requests must go through the Brand and Design team for design/artwork consistancy.
7. Share final artwork with the vendor. At this point, you are ready to request a quote for the total order from the vendor.
8. Open an issue in the [GitLab Finance project](https://gitlab.com/gitlab-com/Finance-Division/procurement-team/procurement/-/issues/new) using the `general_vendor_contract_request` template. This template should be used for new swag orders with both new and existing vendors. Name the issue with either `Swag Store Merchandise Request- New Vendor` or `Swag Store Merchandise Request- Existing Vendor`. 
9. On the finance issue, be sure to use the correct finance tag. If the order is for merchandise for the store, use the tag `swag_ownedevents`. If the order is specific to community team use, use the tag `swag_community`. For both new and existing vendors, upload the quote to the issue for approval. For new vendors, upload any necessary contracts to the issue. Obtain all necessary approvals on this finance issue prior to placing any swag orders.
10. When filling out the issue template, don't be worried if you don't know how to fill in most of the informaiton. This issue template is not meant to be used for spend approvals, but it is th best current iteration. Focus on Step 1, 4, 6, and 10, and leave the others blank. 
11. After receiving finance approvals, work with the vendor to place an order to be shipped to the Printfection warehouse. Be sure to request pre-production samples to be sent to your home or a teammates home for review before place orders for new swag items.
12. Follow steps to add products to Shopify and create send orders to Printfection.

### Replenish Printfection Inventory

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [Replenish Inventory in Printfection](https://youtu.be/RnZ9zfnPkcg)

Community Advocates should watch inventory levels for products in Printfection and order more inventory when inventory is low. Replenish orders typically take 2-3 weeks until items are physically available in the warehouse.

1. Log into Printfection
2. Click on Inventory
3. On the Inventory page, click on Replenish Inventory
4. Click the green 'Replenish Inventory' button
5. Choose the 'Print' tag option
6. Give a name to your print order that describe the inventory you are ordering
7. Click the 'Start Replenish Order' button
8. Add Printfection items to the order. Specify the quantity for each item. Notice that some items have a minimum order number. Be mindful of total cost of items and try to order items in bulk, as the price per item decreases for larger quantity orders
9. Add the appropriate finance or campaing tag to the order in the `PO` section. If ordering for the swag store, use `swag_ownedevents`
9. Follow stepsm 8, 9, and 10 in the [Creating, Replenishing, and Ordering New Swag Items workflow](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#creating-replenishing-and-ordering-new-swag-items)
10. When you've received all necessary approvals on the issue, completed your replenish order by clicking the 'Buy Items' button.

### Ordering on StickerMule

StickerMule is the preferred Vendor for orders that include only stickers, or orders that include a large number of stickers. StickerMule orders for the Community team should be placed with the Corporate Marketing credit card.

Examples of events where you might order stickers in large quantities from StickMule include:
* Hackathons
* Conferences
* MeetUps

1. Log in to StickerMule
2. Navigate to the 'Reorder' tab
3. Select the sticker you'd like to order based on stickers created from previous orders. New stickers can be created, but if possible, it is faster to reorder an existing sticker.
4. Exisiting stickers vary in size, but most are between 2.64"x3"
5. Stickers must be orders in batches of 10
6. Follow stepsm 8, 9, and 10 in the [Creating, Replenishing, and Ordering New Swag Items workflow](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#creating-replenishing-and-ordering-new-swag-items)
7. Enter sticker quantity and process Stickermule order using the corporate marketing GitLab card.
8. Send orders to the wider community member, Meetup organizer, customer, or Printfection warehouse. The Printfection warehouse address is: 700 W 48th Ave, Denver, CO 80216
9. When adding shipping information, add the project title or finance tag to the `Company` line so that orders can be tracked.
10. If shipping to Printfection, follow steps in Printfection to create a 'Send' inventory order.

### Send Items to Printfection Warehouse

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [Creating Send Orders](https://youtu.be/9sGyazdLE4g)

Printfection does not produce all items we sell in the store. To ship items from another vendor to Printfection, you must create an 'Item Research Request' and a 'Send' inventory order. Refer to [Printfection's guide on customer sourced orders](https://help.printfection.com/hc/en-us/articles/115002120194-Understanding-customer-sourced-inventory) for more information. If you need to ship a package to the Printfection warehouse, please ping @advocates in the [#swag slack channel](https://app.slack.com/client/T02592416/C66R8N98F) for the address.

#### Add new Item to Printfection

1. Log into Prinfection
2. Visit the [Item Research Request page](https://app.printfection.com/account/items/custom_item_request.php) Note that this is intended to trigger a search by the Printfection team, but instead we're using it to register items that will be coming from another warehouse or vendor.
3. Add the item name, description, and select that you'd like to 'stock these items'. If you're adding custom swag for your team's giveaway, please title the swag as 'Your Team Name - Item Name'.
4. Add the item type, color, and quantity shipping to the warehouse. You can ignore the target cost-per-item unless you know the value, then it can be entered.
5. Click the 'submit item research request' button
6. Email support@printfection.com or our current sales rep with photos of the item.
7. After the item is added to the Printfection portal, continue to creating a send order.

#### Creating the Send Order

1. Log into Printfection
2. Click on Inventory
3. On the Inventory pate, click on Replenish Inventory
4. Click on the green 'Replenish Inventory button'
5. Choose the 'Send' tab option
6. Add items you'd like to send to Printfection by clicking the 'Ship to PF' button, then click 'Save and Continue'
7. Enter the total quantity of items you're sending, then click 'Save and Continue'
8. Enter name for Customer-Sourced Shipment and click 'Start Replenish Order'
9. Confirm your order and click 'Get Packing Slip'
10. On the packing slip page, there are 2 pieces of information to include. Since we are shipping from a vendor to Printfection, ignore the steps for printing the packing slip and adding it to the package. Instead, make an estimate of how many boxes will be shipped to Printfection and add it in the 'How Many boxes are you sending' section. If you have only 1 tracking number, add it to the form as well. If you have more than one, you'll need to email all the numbers to support@printfection.com or to our account rep.
11. At this point your order is placed. Continute communication with the account rep to confirm delivery of package and processing into the Printfection warehouse. When the items are processed in the warehouse, they are ready for use.
12. Please note that holding items in the Printfection warehouse costs $25 per month per item. This $25 charge is applied the same way whether you're storing 100 socks or 1,000 stickers.


### Adding Products to Shopify

1. Gather item inventory data from Printfection and Product Vendor. You will need: product description, title, weight, high resolution image, SKU, and Size IDs (if item has variants). Most information can be found direction in Printfection within each item view. If items are missing, follow up with the product vendor via email.
1. Log in to Shopify
1. Open the products page
   - Click the Add Product button
   - Fill out information about the item. Include the title, size description, weight, and size variants.
   - Use non-gendered descriptions for clothing items. For example, 'box cut' may be used to describe 'unisex' or 'mens' shirts, and 'fitted' may be used to describe 'womens' shirts. Consider adding a note to the description to make this clear to the customer. For example, add a note saying '(You may have seen this cut shirt sold as 'Men's/Unisex')'
   - Include the SKU and Size ID numbers, found in Printfection.
   - Upload an image for the product. Be sure it is high resolution. Shopify suggests using images with 2048 x 2048 pixel resolution for square product photos.
   - Fill out the price for the item.
   - Select "Shopify tracks this product's inventory"
   - Check the product availability and select Online Store.
   - Before saving the product, please check search engine listing preview
   - After saving the new item, navigate to the Collections tab and select the 'catalog' collection
   - Add the new item to the catalog.
   - In order for the new item to show on the Shopify store, you may need to edit the UI of the Shopify store. To do this, choose the Online Store tab. Naviagate to Themes -> Customize -> Home Page. Edit the number of rows and products per row to include all catalog items. A maximum of 25 items can appear on the home page at 1 time.

<i class="fas fa-info-circle" aria-hidden="true" style="color: rgb(49, 112, 143)
;"></i> For more information, see this [official guide](https://help.shopify.com/en/manual/products/add-update-products)
{: .alert .alert-info}


## Giveaways

### Giveaway Requests from GitLab Teams
Community Advocates may be asked to support other teams at GitLab who are organizing a giveaway promotion. 

**Trying to organize a giveaway?** Please follow the steps on the [GitLab Giveaways page](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/giveaways/) to start a giveaway.

**Requesting swag for any other reason?** Review the [Swag Giveaway Request page](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/swag-requests/)

#### Advocate Workflows for Supporting Giveaways

##### Create a new Giveaway campaign

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [Create a Giveaway Campaign](https://youtu.be/w7MHwP8JB74)
 
1. Go to Campaigns tab then click Giveaways 
2. Click the **+ GIVEAWAY CAMPAIGN** button. 
3. Enter the name and press **CREATE CAMPAIGN** button.
4. Go to the **Items** tab in the navigation menu.
5. Click **Add Items to Campaign** and simply choose the items you want to offer in your Giveaway.
6. Click the **Manage** in the navigation menu and choose how many initial links you want to giveaway (you can always add more later).
7. Go to **Settings** in the navigation menu and update the GitLab branding (see the existing givaway settings). You'll also need to specify a payment method on this page.
 In the **Settings** tab, add the relevant campaign or finance tag in the `PO` section. This is required to start your giveaway.
8. Turn the campaign from **Paused** to **Running** in the top right navigation menu. And that's it, you're ready to give some swag!

Note: Once a redemption is complete you will have the option to cancel it from the 'Recipients & Redemption' section at the bottom of the 'Overview' page. Just use the 'Cancel' button next to the order. This cancelation option is only available until the order is processed, you'll want to review orders same-day or earlier if you want to cancel them.

##### Create a new Giveaway Kit

GitLab team members can use the Unfiltered Youtube Channel to watch the following trainings: 
1. [Create a Kit](https://youtu.be/6i2olZgTg3c)
1. [Add Kits to Giveaways](https://youtu.be/mQ-pPzh9LKM)


Giveaway kits in Printfection are an efficient way to create bundles of swag to send to community members because they allow you to set limits on item totals. For example, these could be utilized for Meetup organizers to place orders for a giveaway kit of tshirts, stickers, and notebooks.

1. In Printfection, start by creating a giveaway kit with your desired items. For details, follow [the documentation to start a new kit](https://help.printfection.com/hc/en-us/articles/360006335613-How-to-start-a-new-kit).
2. After creating the kit, use [the documentation to create a giveaway campaign](https://help.printfection.com/hc/en-us/articles/360026589734-Using-kits-in-Giveaway-campaigns).
3. Kits can be added to giveaway campaigns just like a regular swag item, as defined in the documentation above.
4. When your giveaway kit is created, you can generate order links in Printfection. Send these links to the desired community member so they can self place their orders.
5. Note that whatever you name your giveaway campaign will be visable by the customer, so be sure to make it clear and accurate.
6. Important Note: Each giveaway kit link will redeem 1 single kit. If a customer needs more swag, consider sending them multiple giveaway kit links.

##### Generating Giveaway Links

GitLab team members can use the Unfiltered Youtube Channel to watch the following training: [Generating Giveaway Links](https://youtu.be/MZSGwwM9W3Y)

###### Manually Generate CSV File with Links

1. Login to Printfection.
2. Go to your giveaway campaign.
3. Click on the Manage tab.
4. Generate new links.
5. Make sure to download the CSV file of the freshly created links only

Please check out this [video tutorial](https://drive.google.com/file/d/1uggqOMkywNbqoPBJjkjAAJAcGz-HQjZH/view?usp=sharing) no how to generate new giveaway links.

###### Use Printfection Chrome Extension

1. Install the [Printfection Link Generator Chrome Extension](https://chrome.google.com/webstore/detail/printfection-giveaway-lin/ckfdccfmknbfmkkibilbhpajmojbglmf?hl=en-US)
1. Follow the steps to [Integrate the Chrome Extention with Printfection Giveaways](https://help.printfection.com/hc/en-us/articles/218893267-Integrating-Google-Chrome-Printfection-create-Giveaway-links-)
1. Use the chrome extension as you are sending links to generate 1 link at a time.

##### Sending Giveaway Links

There are many ways to send links and document the use of giveaways. This outlines the best practices used by the Community Advocates team while [supporting teams hosting giveaways](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#giveaway-requests-from-gitlab-teams)

###### Sending Via Email

1. Generate giveaway links and download the CSV file
2. Use a mail merge to share unique link with contact list

###### Using Mail merge

Process updates coming soon

###### Sending Via Twitter DM
1. Download the Printfection Chrome Extension
2. Use the chrome extention to send unique links to each person via twitter. Consider writing a response template to keep outreach consistant.

###### Using Mass Twitter Direct Messages

Process updates coming soon

##### Closing Out Completed Campaigns
1. Follow the steps to [delete your campaign in Prinfection](https://help.printfection.com/hc/en-us/articles/114094187834-How-to-delete-a-campaign)



## Monthly report sharing

The GitLab accounting team has access to Shopify and Printfection. Accounting manager Kim S. runs monthly reports for the swag store.

Previous month reports can be viewed in this [google folder](https://drive.google.com/drive/folders/1uCUfakIR7E188hPg14pBcLZWsoz6KT7O) accessible only by GitLab team members.

If an advocate needs more information about how to access reports in Shopify and Printfection, please follow the steps in this [video tutorial](https://drive.google.com/file/d/1TiVxM9an0SIFrqp7ESj4QiqIj0ekAZ3F/view?usp=sharing).

### Reporting on Use of Bulk Swag Orders

In most cases, it makes financial sense to place large orders of commonly used items in Printfection, like tshirts. Since multiple teams use this swag inventory, we need to run a monthly report for the finance team so they can allocate budget based on use. This report should be run and shared via email with the finace team at accountingops@gitlab.com on the first day of every month by the Community Advocate team.

Advocates should process this report on the first of each new month. The calendar [Monthly Swag Report Reminder](https://calendar.google.com/calendar?cid=Z2l0bGFiLmNvbV9ndW9vdmxnbmk1dDh0ZWtpYjlvOGhwcjFyMEBncm91cC5jYWxlbmRhci5nb29nbGUuY29t) is available to the GitLab team and is integrated with Zapier to generate a new Zendesk ticket on the last day of each month. This ticket includes a link to the monthly swag report Goolge sheet, and serves a notification to the Community Advocate team that the report must be processed.

Teams/Campaigns that most often use Printfection inventory:
- Communtiy Team, for community giveaways, meetup kits, and code contributions
- Swag Store, for purchased items
- Sales Team, for customer orders
- Social Team, for giveaway campaigns

Note: this process is not necessary for all items, and should only be used for bulk orders. Please see the current bulk inventory items in the [monthly bulk swag reporting spreadsheet](https://docs.google.com/spreadsheets/d/1_B1ytcSNadQ0eq89SYo3p3AM6vTfFWmJl5DzxzfKArs/edit#gid=1995944076)

To pull usage data for specific swag items:
1. Create a new month tab in the [monthly bulk swag reporting spreadsheet](https://docs.google.com/spreadsheets/d/1_B1ytcSNadQ0eq89SYo3p3AM6vTfFWmJl5DzxzfKArs/edit#gid=1012369609)
1. Review Printfection for all campaigns and giveaways that are using the bulk swag and add them to the reporting spreadsheet.
1. In Printfection, navigate to Reports -> Run a Report
1. Click the 'Run Items Report' button in the 'Item Usage' section
1. For each campaign listed on the reporting spreadsheet, run an item usage report. Do this by editing the report parameters to include the campaign name and dates to reflect the prior month. Edit the start day to represent the previous calendar month, then click 'Generate Report'.
1. Download this report to your computer and save it as 'Campaign Name - Bulk Swag Use'. Repeat this step for all campaigns using the bulk swag.
1. After all reports are generated, navigate to the [Monthly Bulk Swag Reports Google folder](https://drive.google.com/drive/u/0/folders/1E-FDMYnfy_gNl94TSuO6eiyNucI3rFIj) and create a new folder. Name the folder 'Month Year'. Upload all bulk swag reports into this folder. Confirm that the folder is accessible by accountingops@gitlab.com.
1. Complete the reporting spreadsheet. For each campaign, add a link to the Google folder where the report as been uploaded. Add a campaign finance tag for all campaigns where you know the tag. The Shopify Store orders is always `swag_ownedevents_swagstore`, the Sales Order Kit is always 'swag_ownedevents_saleskit', and community relations campaigns are always `swag_community`.
1. Send the reporting spreadsheet to the finance team via email at accountingops@gitlab.com


## Feedback

Have ideas for new GitLab swag? See a process that needs work? 

Please add your comments to the [GitLab Swag Ideas and Process Improvements](https://gitlab.com/gitlab-com/marketing/community-relations/community-advocacy/general/-/issues/56) issue



