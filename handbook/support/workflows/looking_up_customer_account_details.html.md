---
layout: handbook-page-toc
title: Looking up customer account details
category: Handling tickets
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Looking up customer account details

While working on tickets, you may need to look up customer information. Common
use cases include [associating tickets with the appropriate organization](/handbook/support/workflows/associating_needs_org_tickets_with_orgs.html),
checking a customer's subscription plan and looking up the customer's technical
account manager.

In general, you should look for customer details in this order:

1. Within Zendesk
2. Within Salesforce
3. Within customers.gitlab.com

For an overview and runthrough of all three platforms, watch Amanda Rueda's
[How to use Salesforce from a support perspective](https://drive.google.com/file/d/1HLMRvom0REVbP6-vmsgfdNOfBLqs2fEc/view)
video.

### Within Zendesk

The following information is generally available through the Salesforce app in
Zendesk:

- Number of licenses (seats)
- Next renewal date
- Support level
- Technical account manager

To access the Salesforce app:

1. Click on "Apps" in the top right of the Zendesk UI.

   ![Zendesk Apps button](/handbook/support/workflows/assets/zendesk-apps-button.png)

2. Look for the Salesforce app

### Within Salesforce

If you can't find the information you want through the Zendesk app, or if you
are trying to find the ticket requester's organization, you'll have to look it
up directly in Salesforce.

To access Salesforce, use the Salesforce tech support account credentials in
the 1Password Support vault. Notes:

- If prompted for a one-time password, this is available in 1Password.
- If prompted to provide a verification code sent by email, the email account
  credentials are available in 1Password.

#### Finding the customer's organization

1. Search for the customer's domain (e.g. `customer.com`) or full email address
   (e.g. `flastname@customer.com`) in the search bar at the top of the
   Salesforce UI.

   ![Search bar, in repose](/images/handbook/support/zendesk_needs_org-sfdc-search.png)

2. Look for results in the **Accounts** section. You should also be able to see
   if they have a support level if they have one.

   ![Account Name and Support Level in Salesforce search results](/handbook/support/workflows/assets/salesforce-search-results-accounts.png)

3. Click the **Account Name** to view the customer's organization page.

#### Finding the customer's GitLab subscription information

In the customer's organization page, look for the **GitLab Subscription Information**
section. The most relevant pieces of information to support in this section are:

- **Support Level**: Whether they are on starter or premium tier support
- **GitLab Plan (TEST)**: Which subscription plan they are on
- **Number of Licenses**: The number of license seats which the customer is paying for
- **CARR**: The total annual recurring revenue this customer brings

You can also confirm if the organization is a paying customer by look for the
`Type` field under the **Account Detail** section. It should say `Customer`.

#### Finding the customer's account owner

In the customer's organization page, look for the **Account Detail** section.
There should be an `Account Owner` field. This is the person responsible for
the customer account.

Alternatively, look for the list of links just above the **Account Detail**
section. Note: You may have to wait awhile as the list only loads after the
rest of the page is loaded.

![List of links above account details](/handbook/support/workflows/assets/salesforce-account-detail-links.png)

Hover over the "Account Team" link to see a list of people who have handled the
customer account.

![List of account team members](/handbook/support/workflows/assets/salesforce-account-team-list.png)

#### Finding the customer's renewal opportunity owner

In the customer's organization page, look for the **Opportunities** table. Look
for a row with a `Close Date` in the future and a stage that is not `Closed Won`
or `10-Duplicate`. This should generally be the first row.

![List of account opportunities](/handbook/support/workflows/assets/salesforce-account-team-list.png)

The person responsible for the customer's license renewal is listed under 
`Owner Full Name`.

### Within customers.gitlab.com

1. Log in to [customers.gitlab.com](https://customers.gitlab.com/admin) admin area
   (sign in with Okta).

2. In the **Customers** section, search for a domain or full email address.

   ![Search box in customers.gitlab.com customers section](/handbook/support/workflows/assets/customers-gitlab-com-search.png)

3. In the search results, click on the `i` icon to view the customer's details.

   ![Search results in customers.gitlab.com customers section](/handbook/support/workflows/assets/customers-gitlab-com-search-results.png)

4. You can *impersonate* an account to find out if they have a current 
   subscription through the customer's detail page or by clicking on the `home`
   icon in the search results.
