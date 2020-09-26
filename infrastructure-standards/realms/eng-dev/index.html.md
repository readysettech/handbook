---
layout: handbook-page-toc
title: "Engineering Development Realm"
---

## On this page
{:.no_toc}

- TOC
{:toc}

### Quick links

* [Global infrastructure standards](/handbook/infrastructure-standards)
* [Global labels and tags](/handbook/infrastructure-standards/labels-tags)
* [Infrastructure policies](/handbook/infrastructure-standards/policies)
* [Infrastructure helpdesk](/handbook/infrastructure-standards/helpdesk)

## Overview

This infrastructure realm is for product stages and functional groups across the engineering and product departments to share testing and tool infrastructure that aren't appropriate for the `sandbox` realm. Any production resources should be created in the `saas` or `eng-infra` realm.

<div class="panel panel-info">
<div class="panel-heading">
Future Iteration with Engineering Infrastructure Handbook Pages
</div>
<div class="panel-body">
The <a href="/handbook/engineering/infrastructure/environments">Engineering Infrastructure Environments handbook page</a> is the current SSOT for environments. As the WIP initiative to iterate on our company-wide infrastructure standards evolves, the Engineering Infrastructure pages will be refactored incrementally as the standards are documented, implemented, and changes to environments take place.
</div>
</div>

### Access requests

To request access to a group, please see [group access request tutorial](/handbook/infrastructure-standards/tutorials/groups/access-request).

> For email authenticity security reasons, only GitLab issues or Slack messages to owners or counterparts are allowed for infrastructure requests.

### Realm Owners

| Name                 | GitLab.com Handle       | Group Role       | Job Title                                       |
|----------------------|-------------------------|------------------|-------------------------------------------------|
| Dave Smith           | `dawsmith`              | Owner            | Engineering Manager, Reliability Engineering    |
| Anthony Sandoval     | `AnthonySandoval`       | Counterpart      | Engineering Manager, Reliability Engineering    |
| Gerardo (Gerir) Lopez Fernandez | `glopezfernandez` | Counterpart | Engineering Fellow, Infrastructure              |
| Alberto Ramos        | `albertoramos`          | Counterpart      | Engineering Manager, Reliability Engineering    |
| Brent Newton         | `brentnewton`           | Counterpart      | Director of Infrastructure, Reliability         |

## Realm labels and tags

The [global labels/tags](/handbook/infrastructure-standards/labels-tags) and [realm labels/tags](/handbook/infrastructure-standards/realms/eng-dev/labels-tags) should be applied to each resource.

## Realm Groups

Each infrastructure group has a shared GCP project and/or AWS account for group members.

If a group has not been implemented yet, please contact the realm owner for assistance. After a group is implemented, a separate handbook page is created with usage documentation.

We have separate realms for [eng-infra-*](/handbook/infrastructure-standards/realms/eng-infra), [eng-security-*](/handbook/infrastructure-standards/realms/eng-security), and [eng-support-*](/handbook/infrastructure-standards/realms/eng-support). 

| Stage                | Group Name (AWS Account/GCP Project Name) | Usage Documentation (Empty cells are not implemented yet)                                                                |
|----------------------|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| `eng-dev-manage`     | `eng-dev-manage-shared-infra`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-manage-shared-infra)-->                |
| `eng-dev-manage`     | `eng-dev-manage-access`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-manage-access)-->                      |
| `eng-dev-manage`     | `eng-dev-manage-compliance`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-manage-compliance)-->                  |
| `eng-dev-manage`     | `eng-dev-manage-import`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-manage-import)-->                      |
| `eng-dev-manage`     | `eng-dev-manage-analytics`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-manage-analytics)-->                   |
| `eng-dev-plan`       | `eng-dev-plan-shared-infra`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-plan-shared-infra)-->                  |
| `eng-dev-plan`       | `eng-dev-plan-project-mgmt`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-plan-project-mgmt)-->                  |
| `eng-dev-plan`       | `eng-dev-plan-portfolio-mgmt`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-plan-portfolio-mgmt)-->                |
| `eng-dev-plan`       | `eng-dev-plan-certify`                    | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-plan-certify)-->                       |
| `eng-dev-create`     | `eng-dev-create-shared-infra`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-shared-infra)-->                |
| `eng-dev-create`     | `eng-dev-create-source-code`              | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-source-code)-->                 |
| `eng-dev-create`     | `eng-dev-create-knowledge`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-knowledge)-->                   |
| `eng-dev-create`     | `eng-dev-create-static-site-editor`       | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-static-site-editor)-->          |
| `eng-dev-create`     | `eng-dev-create-editor`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-editor)-->                      |
| `eng-dev-create`     | `eng-dev-create-gitaly`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-gitaly)-->                      |
| `eng-dev-create`     | `eng-dev-create-gitter`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-gitter)-->                      |
| `eng-dev-create`     | `eng-dev-create-ecosystem`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-create-ecosystem)-->                   |
| `eng-dev-verify`     | `eng-dev-verify-shared-infra`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-verify-shared-infra)-->                |
| `eng-dev-verify`     | `eng-dev-verify-ci`                       | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-verify-ci)-->                          |
| `eng-dev-verify`     | `eng-dev-verify-runner`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-verify-runner)-->                      |
| `eng-dev-verify`     | `eng-dev-verify-testing`                  | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-verify-testing)-->                     |
| `eng-dev-package`    | `eng-dev-package-shared-infra`            | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-package-shared-infra)-->               |
| `eng-dev-package`    | `eng-dev-package-package`                 | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-package-package)-->                    |
| `eng-dev-release`    | `eng-dev-release-shared-infra`            | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-release-shared-infra)-->               |
| `eng-dev-release`    | `eng-dev-release-progressive-delivery`    | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-release-progressive-delivery)-->       |
| `eng-dev-release`    | `eng-dev-release-release-mgmt`            | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-release-release-mgmt)-->               |
| `eng-dev-configure`  | `eng-dev-configure-shared-infra`          | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-configure-shared-infra)-->             |
| `eng-dev-configure`  | `eng-dev-configure-configure`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-configure-configure)-->                |
| `eng-dev-monitor`    | `eng-dev-monitor-shared-infra`            | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-monitor-shared-infra)-->               |
| `eng-dev-monitor`    | `eng-dev-monitor-apm`                     | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-monitor-apm)-->                        |
| `eng-dev-monitor`    | `eng-dev-monitor-health`                  | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-monitor-health)-->                     |
| `eng-dev-secure`     | `eng-dev-secure-shared-infra`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-shared-infra)-->                |
| `eng-dev-secure`     | `eng-dev-secure-static-analysis`          | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-static-analysis)-->             |
| `eng-dev-secure`     | `eng-dev-secure-dynamic-analysis`         | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-dynamic-analysis)-->            |
| `eng-dev-secure`     | `eng-dev-secure-composition-analysis`     | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-composition-analysis)-->        |
| `eng-dev-secure`     | `eng-dev-secure-fuzz-testing`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-fuzz-testing)-->                |
| `eng-dev-secure`     | `eng-dev-secure-threat-insights`          | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-threat-insights)-->             |
| `eng-dev-secure`     | `eng-dev-secure-research`                 | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-secure-research)-->                    |
| `eng-dev-defend`     | `eng-dev-defend-shared-infra`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-defend-shared-infra)-->                |
| `eng-dev-defend`     | `eng-dev-defend-container-security`       | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-defend-container-security)-->          |
| `eng-dev-defend`     | `eng-dev-defend-insider-threats`          | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-defend-insider-threats)-->             |
| `eng-dev-growth`     | `eng-dev-growth-shared-infra`             | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-shared-infra)-->                |
| `eng-dev-growth`     | `eng-dev-growth-acquisition`              | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-acquisition)-->                 |
| `eng-dev-growth`     | `eng-dev-growth-conversion`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-conversion)-->                  |
| `eng-dev-growth`     | `eng-dev-growth-expansion`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-expansion)-->                   |
| `eng-dev-growth`     | `eng-dev-growth-retention`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-retention)-->                   |
| `eng-dev-growth`     | `eng-dev-growth-fulfillment`              | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-fulfillment)-->                 |
| `eng-dev-growth`     | `eng-dev-growth-telemetry`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-growth-telemetry)-->                   |
| `eng-dev-enablement` | `eng-dev-enablement-shared-infra`         | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-enablement-shared-infra)-->            |
| `eng-dev-enablement` | `eng-dev-enablement-distribution`         | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-enablement-distribution)-->            |
| `eng-dev-enablement` | `eng-dev-enablement-geo`                  | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-enablement-geo)-->                     |
| `eng-dev-enablement` | `eng-dev-enablement-memory`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-enablement-memory)-->                  |
| `eng-dev-enablement` | `eng-dev-enablement-search`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-dev-enablement-search)-->                  |
|                      | `eng-quality-shared-infra`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-quality-shared-infra)-->                   |
|                      | `eng-quality-ops-ci-cd`                   | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-quality-ops-ci-cd)-->                      |
|                      | `eng-quality-secure-enablement`           | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-quality-secure-enablement)-->              |
|                      | `eng-quality-productivity`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-quality-productivity)-->                   |
|                      | `eng-quality-growth-defend`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-quality-growth-defend)-->                  |
|                      | `eng-ux-shared-infra`                     | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-ux-shared-infra)-->                        |
|                      | `eng-ux-technical-writing`                | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-ux-technical-writing)-->                   |
|                      | `eng-ux-research`                         | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-ux-research)-->                            |
|                      | `eng-ux-pajamas`                          | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/eng-ux-pajamas)-->                             |
|                      | `product-mgmt-shared-infra`               | <!--[Group Docs](/handbook/infrastructure-standards/realms/eng-dev/groups/product-mgmt-shared-infra)-->                  |

## Usage guidelines

This is a placeholder for the realm owner to provide instructions on best practices and usage guidelines for this infrastructure.
