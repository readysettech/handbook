---
layout: handbook-page-toc
title: "GitLab.com Subscriptions"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## How GitLab.com subscriptions work

GitLab.com subscriptions work slightly differently to Self-managed licenses. 
Unlike Self-managed licenses which grant equal access to features across an installation, GitLab.com subscriptions are applied to *[namespaces](https://docs.gitlab.com/ee/user/group/#namespaces)* on GitLab.com (typically groups). Members of groups that have subscriptions applied to them will enjoy those features anywhere within the licensed namespace. For example, if `BigCorp` has a Gold license, the sub-groups `BigCorp/Frontend`, `BigCorp/Backend` will each have access to Gold features and share a common pool of Shared Runner minutes.


### Common Misconceptions
1. **Misconception**: If I'm in a Gold group, my GitLab.com profile should say "Gold"
   - **Reality**: GitLab.com subscriptions are scoped to a namespace, and individual users could participate in many groups with different subscription types. For example, they might have personal projects on a Free subscription type, particpate in an open-source project that has Gold features (because it's public) while their company has a Silver subscription.
1. **Misconception**: Subscriptions grant "the midas touch" and any group or project a subscription-bearing user creates will get the features of their subscription level. i.e. a Gold user will be able to create Gold groups in which all members will have Gold features.
   - **Reality**: Subscriptions can be applied to any *namespace* all items created within said namespace will receive the features of the subscription level.
   - **Reality**: Applying a subscription to a personal namespace will mean that group-level features will **not** be present in any groups that user creates.
1. **Misconception**: A license key will be emailed out and applied somewhere in the UI of GitLab.com
   - **Reality**: Subscriptions are managed, and applied, through https://customers.gitlab.com on a linked GitLab.com account
1. **Misconception**: Someone in accounting made the purchase and can pass along the subscription to the team using it.
   - **Reality**: Subscriptions are managed by a GitLab.com account who has `Owner` in the group.
1. **Misconception**: I should purchase my subscription first before setting up accounts on GitLab.com
    - **Reality**: You can do this in any order, most will find it easier to set things up on .com before they purchase, with the exception of those who want to set up SAML.
1. **Misconception**: I can apply different subscription levels to subgroups.
    - **Reality**: Subscriptions are applied to top level groups; sub-groups inherit their license (and Shared Runner minutes) from the top-level group.
1. **Misconception**: Minutes are deducted from my group for any jobs that are run, even on my personal runners.
    - **Reality**: Runner minutes are deducted only from jobs run on GitLab.com Shared Runners, you can set up your own runners per project or group without affecting your shared minutes.

### Trials
1. Trials should be initiated by users by going to the Settings page of the group that they want to apply the trial to.
1. At writing (2019-06-05) Silver and Bronze trials are not generally available. [Support can manually downgrade a trial by request](/handbook/support/internal-support/#common-requests)
1. At writing (2019-06-05) [Trials must be manually downgraded before a purchase can be made.](https://gitlab.com/gitlab-org/customers-gitlab-com/issues/482) 
1. [Support is **not** included with trials](/support/#trials-support) Please participate in [this issue](https://gitlab.com/gitlab-com/sales/issues/302)

## Common issues the Support Team encounters with sales-assisted purchases

1. New Customers
  - The support team sometimes receives tickets in Zendesk from sales-assisted clients with basic questions like how to set up groups, how to add additional users, why subscriptions are applied to groups vs users, permission questions, etc. Support will direct them to corresponding documentation to address their questions. 
  - Customers are typically not aware that creating an account in the customer portal does not create an account on GitLab.com or how to link a customer portal account to their GitLab.com account.
1. Upgrades/Downgrades
  - There is presently not a self-service way for customers to upgrade/downgrade subscriptions so any of these requests must go through the sales team via a queue in Zendesk. 
  - Requests can sometimes be delayed by the volume or lack of information provided when the ticket is sent to Sales.

## How we can set the customer up for success

The best way to assist a user or system admin on any new platform is to arm them with the resources they will need when questions arise. During the onboarding process after the sale, the user/admin will receive an email from GitLab with pertinent information about their subscription. Highlight this and encourage them to save it somewhere easily accessible.
While many of the links below are included in the email, it would be helpful to review each of the following resources personally with the user/admin.

1. [GitLab Documentation](https://docs.gitlab.com/ee/README.html)
1. [Administrator Documentation](https://docs.gitlab.com/ee/administration/index.html) (self-managed only)
1. [Subscription setup and management](https://docs.gitlab.com/ee/subscriptions/index.html)
1. [Licensing and subscription FAQ](/pricing/licensing-faq/)
1. [Uploading your license](https://docs.gitlab.com/ee/user/admin_area/license.html#uploading-your-license) (self-managed only)
1. Features available by plan: [GitLab.com](/pricing/gitlab-com/feature-comparison/) & [Self-Managed](/pricing/self-managed/feature-comparison/)
1. [Support portal](https://support.gitlab.com/hc/en-us) 
1. [Statement of Support](/support/statement-of-support.html)

**A few more best practices to ensure a smooth start**

1. On this page, you'll read about differences between GitLab.com and Self-Managed functionality. Whenever in doubt, don't hesitate to ask us about a particular feature/functionality which is important to your prospect prior to promissing it is available. For a question like this, contact us on Slack in the [#support_gitlab_com](https://gitlab.slack.com/messages/C4XFU81LG) or [#support_self-managed](https://gitlab.slack.com/messages/C4Y5DRKLK) channel.
1. Be sure to stress to the new user/admin to submit their support issues directly to us via the [Support Portal](https://support.gitlab.com/hc/en-us) instead of using  you as a go-between. This will provide the most timely and comprehensive support we can offer.
1. If you find yourself having to submit something on behalf of the user/admin, do not submit a ticket via the Support Portal/Zendesk. Instead, create an issue in [internal-requests](https://gitlab.com/gitlab-com/support/internal-requests/issues).
1. For GitLab.com, make sure the user understands how to link their GitLab.com account to the [customers portal](https://customers.gitlab.com/customers/sign_in) and how to associate their group with their subscription. See [managing subscriptions page](https://docs.gitlab.com/ee/subscriptions/index.html) for instructions.

## Important differences between GitLab.com and Self-Managed subscriptions

The [Pricing page](/pricing/) includes a "Frequently asked questions for GitLab.com" section that answers "What features do not apply to GitLab.com?" in detail. Here are some highlights:

1. Features availability including [SAML](https://docs.gitlab.com/ee/integration/saml.html)/[LDAP](https://docs.gitlab.com/ee/administration/auth/ldap.html) is Core vs. [SAML SSO](https://docs.gitlab.com/ee/user/group/saml_sso/) is Silver.
1. Access controls: customer is admin on GitLab instance vs. group owner on GitLab.com
1. Log information and auditing: unrestricted access vs. no access on GitLab.com (can work with Support/Security to answer questions)
  - On GitLab.com, each user is "signing a contract" (TOS, privacy policy, etc) as individuals, regardless of what email domain they use. Because of that,  we cannot provide their employer with any personally identifiable information (like email address, log info, etc.) as it would be a violation of the user's contract.
1. Instance wide settings: custom vs. same for all GitLab.com users
1. Infrastructure: manage your own, anywhere vs. GitLab manages HA Architecture, instance level backups/recovery, upgrades, based in US
