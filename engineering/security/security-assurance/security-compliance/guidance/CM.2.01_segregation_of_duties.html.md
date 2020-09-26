---
layout: handbook-page-toc
title: "CM.2.01 - Segregation of Duties Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# CM.2.01 - Segregation of Duties

## Control Statement

Changes to the production environment are implemented by authorized personnel.

## Context

Proper segregation of duties allows GitLab to reduce risk to the integrity and availability of the production GitLab environment and third party systems by ensuring that only those with the proper authorization can make production-level changes. Conflicting duties and areas of responsibility are segregated to reduce opportunities for unauthorized or unintentional modification or misue of GitLab's assets.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

* Control Owners: 
  * Infrastructure
  * Finance
  
* Process owner(s):
    * Infrastructure
    * Finance


## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Segregation of Duties control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/783).

Examples of evidence an auditor might request to satisfy this control:

* Evidence that PostgreSQL database access above data reader is limited to [Database Reliability Engineers](/job-families/engineering/database-reliability-engineer/)