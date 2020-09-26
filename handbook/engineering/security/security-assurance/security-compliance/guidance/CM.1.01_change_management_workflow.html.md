---
layout: handbook-page-toc
title: "CM.1.01 - Change Management Workflow Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# CM.1.01 - Change Management Workflow

## Control Statement

The standard change management process is documented in a change control workflow. 

## Context

Having a structured workflow and guidance on change management helps reduce the risk of GitLab experiencing platform or application instability by increasing the predictability and reproducibility of the change management process.

## Scope

This control applies to all systems within our GitLab.com production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This doesn't include third-party systems that support the business of GitLab.com, which can be found in CM.3.01.

## Ownership

* Control Owner: `Infrastructure`
* Process owner(s):
    * Infrastructure

## Guidance

Change management encapulates multiple types of changes within our business environment. 

The two primary production changes are **infrastructure** changes and **source code** changes to gitlab service itself. 
* Infrastructure changes are done in accordance with the [Change Management](/handbook/engineering/infrastructure/change-management/) process.
* Code changes are made in accordance to our contribution, review, and approval processes, which is described as part of the [Service Lifecycle Workflow](/handbook/engineering/security/security-assurance/security-compliance/guidance/SLC.1.01_service_lifecycle_workflow.html) control.

**Third-party systems**, the **data warehouse**, and **financial** changes are related to the [Business Technology Change Management Workflow](/handbook/business-ops/business-technology-change-management/).

Additionally, any changes to the GitLab [handbook](about.gitlab.com) utilizes [gitlab.com](gitlab.com) version control system.

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Change Management Workflow control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/781).

Examples of evidence an auditor might request to satisfy this control:

* Copy of the GitLab change management workflow
* Sample of issues or other documentation showing the change management workflow is followed

### Policy Reference

* [Change Management](/handbook/engineering/infrastructure/change-management/) 
* [Service Lifecycle Workflow](/handbook/engineering/security/security-assurance/security-compliance/guidance/SLC.1.01_service_lifecycle_workflow.html)
* [Business Technology Change Management Workflow](/handbook/business-ops/business-technology-change-management/)

## Framework Mapping

* ISO
  * A.12.1.2
  * A.12.6.2
  * A.14.2.1
  * A.14.2.2
  * A.14.2.4
* SOC2 CC
  * CC2.3
  * CC8.1
* PCI
  * 1.1.1
  * 10.4.2
  * 6.4
  * 6.4.5
  * 6.4.5.1
  * 6.4.5.2
  * 6.4.5.3
  * 6.4.5.4
  * 6.4.6
