---
layout: handbook-page-toc
title: "VUL.3.01 - Infrastructure Patch Management Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# VUL.3.01 - Infrastructure Patch Management

## Control Statement

GitLab installs security-relevant patches, including software or firmware updates monthly.

## Context

This control details security best practices in relation to infrastructure patching. This control is trying to ensure that all GitLab productions systems are up to date according to our own patching standards. We need to prove that patching is prioritized and we consistently apply all possible patches and decommission systems as appropriate.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

Control Owner:

* Infrastructure (.com)

* SIRT Team (everything else)

Process Owner:

* Infrastructure (.com)

* SIRT TEAM (everything else)

## Guidance

* This control is related to control VUL.1.01.
* The implementation of this control will depend on the use of idempotent or immutable infrastructure. This patching can be done manually but can also be satisfied by tearing down and deploying new systems as updates are made available.

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Infrastructure Patch Management control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/941).

### Policy Reference

## Framework Mapping

* SOC2 CC
  * CC7.1
* PCI
  * 6.2
