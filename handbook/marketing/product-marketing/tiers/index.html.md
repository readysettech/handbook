---
layout: handbook-page-toc
title: "GitLab tiers"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Tiers

### Overview

| Tier      | Delivery                  | License                   | Fee            |
| --------- | ------------------------- | ------------------------- | -------------- |
| Core      | self-managed              | open source               | unpaid         |
| Starter   | self-managed              | source-available          | paid           |
| Premium   | self-managed              | source-available          | paid           |
| Ultimate  | self-managed              | source-available          | paid           |
| Free      | GitLab.com                | open source               | unpaid         |
| Bronze    | GitLab.com                | source-available          | paid           |
| Silver    | GitLab.com                | source-available          | paid           |
| Gold      | GitLab.com                | source-available          | paid           |

### Definitions

1. Tier: a GitLab offering that provides a set of features at a particular price point.
1. Users: anyone who uses GitLab regardless of tier.
1. Customers: users on a paid tier.
1. Plans: the paid tiers only.
1. License: open source vs. source-available, for example moving a feature from a source-available tier to an open-source tier.
1. [Distribution](#distributions-ce-and-ee): self-managed CE vs. EE, for example you can have a EE distribution but in the Core tier.
1. Version: the [release of GitLab](/releases/), for example asking what version a user is on.

### Delivery

In general each of the four self-managed tiers match the features in the GitLab.com tiers. They have different names for two reasons:

1. There is not complete feature parity between self-managed and GitLab.com plans. For example, Starter, Premium, and Ultimate include [LDAP Group Sync](https://docs.gitlab.com/ee/administration/auth/ldap-ee.html#group-sync) but Bronze, Silver and Gold do not.
1. We want to know if a user is using self-managed or GitLab.com based on a just the tier name to prevent internal and external confusion.

When we need to specify which tier includes a particular feature using only one word (for example on our issue tracker), we reference the self-managed tiers by default because they tend to contain a superset of the GitLab.com tier features.
Where we can, we highlight both the self-managed and the GitLab.com tiers (like in [a release post](/blog/2018/02/22/gitlab-10-5-released/#instant-ssl-with-lets-encrypt-for-gitlab)).

### Libre, gratis, and free
Libre, gratis, and free are terms used in the open source community. "free" is an ambiguous term that can means either free as in "no cost" (e.g. $0 "free as in beer"), free as in "with few or no restrictions" (e.g. "free as in free speech"), or both. "gratis" is an unambiguous term to mean "no cost" while "Libre" is an unambiguous term to mean "with few no restrictions." Open source software is "libre" in that it is free to inspect, modify, and redistribute. Open source software may or may not be "gratis." Features that are part of our Free and Core tiers refer to open source software that is both [free as in speech and as in beer](http://www.howtogeek.com/howto/31717/what-do-the-phrases-free-speech-vs.-free-beer-really-mean/). For more info see the [wikipedia article](https://en.wikipedia.org/wiki/Gratis_versus_libre).

### GitLab.com

We call the multitenant SaaS GitLab.com (with the G and L capitalized) since it is unambiguous and common.
We don't call it GitLab Cloud since most self-managed instances of GitLab are hosted in the cloud as well, and if we introduce single tenant instances it will be even more confusing.
We don't call it GitLab SaaS since GitLab.com is shorter and more popular.

### Personal vs group subscriptions
GitLab.com subscriptions are added to either a personal namespace or a group namespace. Personal subscriptions apply to a single user while Group subscriptions apply to all users in the Group.

### History of CE and EE distributions

Historically, GitLab was provided as two different software distributions, each with their own separate source code repository and documentation: [Community Edition (CE)](https://gitlab.com/gitlab-org/gitlab-ce/) and [Enterprise Edition (EE)](https://gitlab.com/gitlab-org/gitlab-ce/). As of GitLab version 12.3, released on 2020-09-22, [GitLab moved to a single code base](/blog/2019/08/23/a-single-codebase-for-gitlab-community-and-enterprise-edition/).

The "CE" and "EE" names referred to the actual software packages that were [downloaded and installed](/install/). Today, the single distribution is referred to as the "Official Linux package". 

For a period of time, GitLab pricing tiers also used "CE" and "EE". When the [free, self-managed tier was changed from "CE" to "Core"](/blog/2018/04/20/gitlab-tiers/) it led this this dynamic: 

**Core users** could use either one of two distributions: Community Edition (CE) and Enterprise Edition (EE). Enterprise Edition can be downloaded, installed, and run without a commercial subscription. In this case it runs using the open source license and only has access to the open source features. In effect, EE without a subscription, and CE have the exact same functionality.

**Starter, Premium, and Ultimate users** could only use Enterprise Edition.

If a Core user was running CE and wanted to upgrade to a paid tier, they had to re-install and migrate to EE. The advantage of using EE as a Core user is that it is much easier to upgrade to a commercial subscription later on. All that's needed is to install a license key to access more features vs needing to re-install a different distribution. Today, GitLab's single distribution maintains these advantages. 

See the [messaging dos and don'ts](#messaging-dos-and-donts) section for how to talk about GitLab, distributions, versions, tiers, pricing, and licneses. 

### GitLab trials
We offer a [free trial for self-managed GitLab](/free-trial/self-managed?glm_source=about.gitlab.com&glm_content=tiers) as well as a [free trial for GitLab.com Gold](https://gitlab.com/-/trial_registrations/new?glm_source=about.gitlab.com&glm_content=tiers).

#### Why offer a free trial when we already have free tiers?

The trial allows users to have access to all of the features of GitLab Ultimate or Gold. Users on the Core (self-managed) and Free (GitLab.com) plans get access to a limited set of features for an unlimited amount of time. Trial users get access to a full set of features for a limited amount of time (30-days).

| License type | Features | Time Period |
| ------------ | -------- | ----------- |
| Core & Free  | Limited (Open source features only) | unlimited |
| Trial        | Unlimited (access to all Ultimate or Gold features) | limited (30 days) |

### Open source projects on GitLab.com get all Gold features.
The GitLab.com Free plan offers unlimited public and private repos and unlimited contributors but has limited features for private repos. Private repos only get access to the open source features. Public projects get access to all the features of Gold free of charge. This is to show our appreciation for [Open Source projects hosted on GitLab.com](/solutions/open-source/).

### Open-source vs. source-available

GitLab is an open-core product that contains both open-source and source-available code.
The source-available code is proprietary (so not open-source) but you can view the source code.
Please don't use CE, EE, or Core to refer to the type of license since:

1. While most open source code is in GitLab CE some code in EE is additional open source code since all our [javascript code is MIT licensed](https://about.gitlab.com/blog/2015/05/20/gitlab-gitorious-free-software/#free-javascript).
1. The majority of the code in EE is open source.
1. We might ship source-available code in Core that is free as in beer but not as in freedom (open source).

### Messaging dos and don'ts

1. Do always present Ultimate as _the_ product.  Every customer and prospect would benefit greatly from the Ultimate product and it's the correct frame of reference to explain our complete vision.
1. Don't introduce lower tiers unnecessarily. We are consultative sellers with a high-value product.  If a customer asks about pricing, the answer is "We have end-to-end DevOps in a single application ranging from our free offering up to ultimate at $1,188 per user per year."  Only go into detail on the lower tiers when appropriate based on your assessment of the customer's needs and progression in the product.  Focus on the value sale as long as possible and only discuss tiers once there is a clear path forward to purchase.
1. Do focus only on Premium and Ultimate when negotiating pricing. The typical conversation should simply be the tradeoff between Premium and Ultimate (no need to introduce, discuss or quote on Core or Starter).  Starter is a specific use case for small accounts getting started.  The majority of our customers are simply deciding whether Premium or Ultimate is the right step for the next 12 months as Ultimate still provides the most value for customers.
1. Don't use the word "`GitLab`" alone unless you are referring to the company or an attribute that applies to both `GitLab Self-managed` and `GitLab.com`. If talking about an attribute that only applies to one delivery method but not the other, then specify. I.e. "GitLab.com does X" or "GitLab Self-managed does X".
1. Do specify `GitLab Self-managed` or GitLab.com when you are refrencing something that is unique to that delivery method. (e.g. a security bug that only affects GitLab.com)
1. Do use the word `GitLab` alone to refer to Ultimate/Gold. "GitLab does X" means, "GitLab Ultimate/Gold does X".
1. Don't use `GitLab` by itself when you really mean a specific, e.g. specify `GitLab Core` if you are referring to the free self-managed tier.
1. Don't use the terms `Enterprise Edition Starter`, `Enterprise Edition Premium`, `Enterprise Edition Ultimate`, `EES`, `EEP`, or `EEU`. These have all been deprecated.
1. Don't use `Community Edition`, `CE`, `Enterprise Edition`, or `EE` to refer to tiers.
1. Don't use `Community Edition`, `CE`, `Enterprise Edition`, or `EE` to refer to where a feature goes. e.g. "This is a CE feature" or "this is an EE feature."
1. Don't use "edition" to refer to plans like `Starter Edition` or `Premium Edition` - Starter, Premium, and Ultimate are tiers, not "editions" of the software.
1. Don't use "enterprise" as a modifier for tiers such as `Enterprise Starter`, `Enterprise Premium`, or `Enterprise Ultimate`.
1. Do refer to plans by their stand-alone name: Core, Starter, Premium, Ultimate, Free, Silver, Bronze, and Gold.
1. Do optionally use "GitLab" as a modifier for plan names: GitLab Core, GitLab Starter, GitLab Premium, GitLab Ultimate, GitLab Free, GitLab Silver, GitLab Bronze, and GitLab Gold.
1. Do use Core, Starter, Premium, Ultimate, Free, Silver, Bronze, and Gold to refer to where a feature goes. e.g. "This is a Premium feature" or "We are moving this feature from Premium & Silver to Core & Free"
1. Do use "enterprise" to describe a market segment. e.g. good phrases to use are: "GitLab provides DevOps for the enterprise", "GitLab is enterprise-ready", "GitLab has many enterprise customers", and "GitLab provides enterprise software for the entire DevOps lifecycle."
1. Do use `Community Edition`, `CE`, `Enterprise Edition` and `EE` to refer to our software distributions. Encourage customers to use the EE distribution since it provides the least painful upgrade path if/when users discover they need commercial features.
1. Do use the terms "open source" and "source-available" to talk about our different license models.
1. When talking to customers, do use language that they are familiar with. They will likely know what "open source" is, but will probably be unfamiliar with "source-available". Similarly, they'll know what "paid" means, but will not know what "gratis" means. If you want to distinguish our $0 tiers from our paid tiers feel free to talk about our "open source" offerings and our "commercial" offerings. For example, "I see that today you are using GitLab Core, I'd love to set up a call to discuss the value your business can get by upgrading from our open source offering to a commercial tier." (You could write the same sentence and use "paid" instead of "commercial" but that puts the focus on what they have to do, i.e. pay, instead of what they get, i.e. business-grade, commercial software.)

## GitLab FOSS

[GitLab FOSS](https://gitlab.com/gitlab-org/gitlab-foss/) is neither a tier, nor a distribution. It is a repository.
