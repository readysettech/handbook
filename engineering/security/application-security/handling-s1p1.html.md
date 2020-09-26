---
layout: handbook-page-toc
title: "Application Security Engineer Handling priority::1/severity::1 Issues"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Appsec Engineer Procedure for Handling severity::1/priority::1 Issues

The following process is a supplement to the first few steps of the [critical release process](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/process.md#critical-security-releases)

Once a potential severity::1/priority::1 issue is made known. The appsec engineer steps are as follows:

## Triage

1. Triage and verify the issue as you normally would [triage a report](/handbook/engineering/security/#hackerone-process).
1. To help SecOps quickly determine impact and log analysis, comment in the security issue with the summarized reproduction steps (HTTP Requests, generated log messages, images, etc).

## Escalate

1. [Engage the security oncall](/handbook/engineering/security/#engaging-the-security-on-call) with a link to the issue.
1. Engage the appropriate [engineering manager and product manager of the affected component](/handbook/product/categories/) in both the issue **and** in the appropriate Slack channels.
1. Inform the Appsec team in the team Slack channel with a link to the issue. This will help other engineers get up to speed, in case they need to step in.

## Mitigate

Sometimes the fix is very simple, sometimes it's not. If the impact to users is greater than the time it takes to apply the long-term fix, you will need to consider a [short term solution](#short-term) as well as the [long term](#long-term) one. Otherwise, if you and the development team are confident the fix is straightforward and simple, then you only need to do the long term fix and roll it out in a critical security release.

### Short term

1. Collaborate with the development, security, and SRE/infrastructure teams to brainstorm short term solutions until a long term patch can be released.
1. Analyze the impact for each option.
  - How effective is it at solving the problem?
  - How many customers are affected by this decision?
  - How exactly are they affected?
  - What's the magnitude?
  - What other positive and negative consequences are there?
1. Choose the solution that best balances the concerns above with the concerns of participating teams.
1. Approval is not required, but clear communication of decision is necessary. Notify the Director of Security, Directory of Infrastructure, and any other parties involved with the proposals and decision.
1. Once the short term solution has been delivered, validate that the fix was effective.

Some past short term options have been:
* HA proxy to block certain endpoints.
* Disable a specific feature using feature flags or application configuration.
* Deploy a [hotpatch](https://gitlab.com/gitlab-org/release/docs/blob/master/general/deploy/post-deployment-patches.md).

### Long term

1. Handle it like you normally would for a [critical security release](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/security-engineer.md#critical).

## Additional

### Handoff
Appsec engineers are not on-call. That means when the assigned appsec engineer end of day arrives, they are responsible for handing it off to a next appsec engineer in a subsequent timezone. If no appsec engineer is available, handoff to the secops engineer on-call.
