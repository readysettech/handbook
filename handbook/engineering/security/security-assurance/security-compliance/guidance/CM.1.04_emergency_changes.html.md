---
layout: handbook-page-toc
title: "CM.1.04 - Emergency Changes"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# CM.1.04 - Emergency Changes

## Control Statement

Emergency changes to the production environment follow the same change control workflow as standard changes. Approval can be retroactively applied depending on the urgency of the change.

## Context

Under certain conditions, like a zero-day vulnerability or out-of-band software patch, a change needs to escalated and applied outside of normal change management workflow and can potentially obtain approval after a change has been made.  This is done in the event a disruption or introduction of risk to business will occur.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

* Control Owners: 
  * Infrastructure
* Process owner(s):
  * Infrastructure

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Emergency Changes control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1692).

Examples of evidence an auditor might request to satisfy this control:



### Policy Reference

## Framework Mapping

* SOC2 CC
  * CC8.1
