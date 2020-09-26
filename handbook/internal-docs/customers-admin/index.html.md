---
layout: handbook-page-toc
title: Customers Portal Admin Panel Documentation
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Introduction

The target audience is the internal GitLab team, and covers the [admin panel](https://customers.gitlab.com/admin/) of the [Customers Portal](https://customers.gitlab.com). Customers or subscription managers should refer to the [Customers](https://docs.gitlab.com/ee/subscriptions/index.html) section of GitLab's user documentation for help in using the portal, or the [licensing FAQ](https://about.gitlab.com/pricing/licensing-faq/) for questions on subscriptions such as how users are counted.

## Searching

When using the admin panel search, be aware that results will be based on searching only one field at a time. For example, entering a person's full name will likely provide no results because the system will not search first and last name at the same time, only one or the other.

We recommend searching by email address, partial email address (e.g. company domain), or company name. When searching by name, enter only first *or* last name.

## Account

### Adding another account to manage subscription

1. Find existing customer and click on `Edit`.
1. Copy the Zuora and SFDC IDs.
1. Paste the IDs into the same fields for the requesting customer.

### GitLab Groups

If an account has a connected GitLab.com user account, then a list of namespaces will show with relevant information including current plan.

The list of namespaces are:

- personal namespace
- top level group namespaces where user is `Owner`

## Trials

### Check, change, or extend trial expiry date

> **Note:** Until [customers #973](https://gitlab.com/gitlab-org/customers-gitlab-com/-/issues/973) and [customers #1643](https://gitlab.com/gitlab-org/customers-gitlab-com/-/issues/1643) are resolved, this is unlikely to be available.

1. Find the customer who initiated the trial.
1. Click on the `GitLab Groups`.
1. If the trial is expired and needs to be extended, click on the `Renew Trial` button.
1. Change the trial date as necessary and click on `Update`. **Warning:** Do not change the date to a date prior to today's date in UTC timezone.
