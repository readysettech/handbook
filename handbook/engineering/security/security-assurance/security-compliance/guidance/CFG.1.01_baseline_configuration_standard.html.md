---
layout: handbook-page-toc
title: "CFG.1.01 - Baseline Configuration Standard Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# CFG.1.01 - Baseline Configuration Standard

## Control Statement

A configuration management tool is utilized for security hardening and baseline configuration standards have been established on production servers.

## Context

Baseline configuration standards make it clear how systems should be hardened and configured.  To ensure these standards are always relevant, we need to regularly review these documents and update them as needed.  The goal of this control is to remove as much subjectivity as possible from the process of configuring systems.  If we create a standard for each system type within GitLab, it will be easier to automate system configuration and ensure that all systems are configured the same. This consistent configuration becomes critical when critical vulnerabilities are discovered and need to be rapidly deployed to all applicable systems.
This control should be tested to ensure the configuration management tool that GitLab has established is utilized 100% of the time for security hardening and baseline configuration standards on produciton servers.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

* Control Owner: `Security`
* Process owner(s):
    * Infrastructure
    * IT Ops
    * Security
    
## Guidance

*  The related pages in the handbook listed below in the Policy reference section, can be more comprehensive, covering all details including all OS hardening guidelines, For ex:Linux hardening guide, etc
*  We don't have to reinvent the wheel with these. Whenever possible we should be referencing industry standards for system configurations (e.g., NIST guidelines).


## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Baseline Configuration Standard control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/784).

Examples of evidence an auditor might request to satisfy this control:

* Configuration standards, guides, Chef cookbooks, and Terraform configs.
* Documentations showing the configuration standards are consistently applied.

### Policy Reference
* [Laptop or Desktop System configuration](/handbook/security/#laptop-or-desktop-system-configuration)
* [Configuring New Laptops](/handbook/business-ops/team-member-enablement/onboarding-access-requests/#configuring-new-laptops--apple-ids)
* [Security Best Practices](/handbook/security/#best-practices)

## Framework Mapping

* SOC2 CC
  * CC7.1
  * CC7.2
* PCI
  * 1.1
  * 1.1.4
  * 1.1.6
  * 1.2
  * 1.2.2
  * 2.1
  * 2.1.1
  * 2.2
  * 2.2.2
  * 2.2.3
  * 2.2.4
  * 2.2.5
  * 5.3
