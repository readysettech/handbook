---
layout: handbook-page-toc
title: "Choosing between GitLab.com and self-managed subscriptions"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Why you probably want GitLab.com
If you don't want to worry about downloading, installing, and managing GitLab yourself, then you'll want to use **GitLab.com**, where there is no technical setup required. If you want full control of your GitLab environment, then you can choose to download and install **GitLab self-managed**, on your own infrastructure or in the public cloud environment.

Choose the version of GitLab that is best for you — let us host it for you, or host GitLab on your servers:

*  **GitLab.com**: GitLab's SaaS offering. You don't need to install anything to use GitLab.com, you only need to [sign up](https://gitlab.com/users/sign_in) and use GitLab straight away.
*  **GitLab self-managed**: Install, administer, and maintain your own GitLab instance.

**GitLab.com** is hosted, managed, and administered by GitLab, Inc., with free and paid options for individuals and teams: **Free**, **Bronze**, **Silver**, and **Gold**.

To support the open source community and encourage the development of open source projects, GitLab grants access to **Gold** features for all GitLab.com public projects, regardless of the subscription.

With **GitLab self-managed**, you deploy your own GitLab instance on-premises or in the cloud. From bare metal to Kubernetes, you can [run GitLab almost anywhere](/install/), with free and paid options: **Core**, **Starter**, **Premium**, and **Ultimate**.

## Six of one, half a dozen of the other
Feature by feature, GitLab.com and self-managed are mostly the same.

Features that are not available to .com customers are primarily configuration or administration tasks that GitLab, Inc. necessarily manages for GitLab.com, with a few exceptions as detailed below.

Your subscription determines which tier of features you can access. There are some differences in how a subscription applies, between use of GitLab.com or a self-managed instance.

On GitLab.com, you can apply a subscription to either a group or a personal namespace. On a self-managed instance, a GitLab subscription provides the same set of features for all users.

## Key differences between GitLab.com & self-managed
While there are several dozen minor functional differences, they amount to a few key considerations:

{::options parse_block_html="true" /}

<div class="panel panel-info">

**Key differences between GitLab.com & self-managed**
{: .panel-heading}

<div class="panel-body">

| type of difference | **GitLab.com**  | **GitLab self-managed** |
|:---------------||:---------------|:-------------|
| **Infrastructure** | GitLab manages HA Architecture, and instance-level backups, recovery, and upgrades  | manage your own, anywhere |
| **Instance wide settings** | same for all users  | custom |
| **Access controls** | customer is group owner  | customer is admin |
| **Features availability, such as:** | [SAML SSO](https://docs.gitlab.com/ee/user/group/saml_sso/) is Silver | [SAML](https://docs.gitlab.com/ee/integration/saml.html) or [LDAP](https://docs.gitlab.com/ee/administration/auth/ldap.html) is Core |
| **Log information and auditing**<code>&ast;</code> | no access, but Support or Security can answer questions | unrestricted access |
{: .custom-class #custom-id}

*<code>&ast;</code> On GitLab.com, each user agrees to our TOS and privacy policy as an individual, regardless of what email domain they use. Thus, we cannot provide their employer with personally identifiable information such as an email address, log info, etc., as that would be a violation of our user agreement.*

</div>
</div>

We should work on removing as many difference between GitLab.com and self-managed as possible. Please contribute relevant issues to [this epic](https://gitlab.com/groups/gitlab-org/-/epics/3182) for the Product team to consider and prioritize.

## All differences between GitLab.com and self-managed
The [GitLab Pricing page](/pricing/) includes a "Frequently asked questions" section which answers "What features do not apply to GitLab.com?" _Some of the bullets below require clarification, here and on the web site._ That list includes:

*  24/7 uptime support
*  Access to the server
*  Runs on metal
*  Highly Available setups
*  Run your own software on your instance
*  Use your configuration management software
*  Use standard Unix tools for maintenance and monitoring
*  Single package installation
*  Single configuration file
*  Basic backup and restore mechanism without additional software
*  IPv6 ready
*  AD / LDAP integration
*  Multiple LDAP / AD server support
*  Access to and ability to modify source code
*  Advanced Global Search
*  Advanced Syntax Search
*  Create and remove admins based on an LDAP group
*  Kerberos user authentication
*  Integrate with Atlassian Crowd
*  Multiple LDAP server support (compatible with AD)
*  PostgreSQL HA
*  Import from GitLab.com
*  Email all users of a project, group, or entire server
*  Limit project size at a global, group, and project level
*  Omnibus package supports log forwarding
*  Admin Control
*  Restrict SSH Keys
*  LDAP group sync
*  LDAP group sync filters
*  Live upgrade assistance
*  Audit Logs
*  Auditor users
*  Disaster Recovery
*  DevOps Score
*  Database load balancing for PostgreSQL
*  Mattermost integration
*  Object storage for artifacts
*  Object storage for LFS
*  Globally distributed cloning with GitLab Geo
*  Support for High Availability
*  Containment
*  Control
*  Retrieval
*  Configurable issue closing pattern
*  Custom Git Hooks
*  Various authentication mechanisms
*  Fast SSH Authorization
*  Instant SSL with Let’s Encrypt for Omnibus GitLab
*  Plugins
*  Supports geolocation-aware DNS
*  Instance file templates
*  Instance-level Kubernetes cluster configuration
*  Smart card support
*  Instance-level kubernetes clusters
*  Show most affected projects in Group Security Dashboard
*  New configuration screen for Secure
*  Credentials Management
