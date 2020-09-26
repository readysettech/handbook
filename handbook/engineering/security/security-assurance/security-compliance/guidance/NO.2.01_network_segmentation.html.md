---
layout: handbook-page-toc
title: "NO.2.01 - Network Segmentation Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# NO.2.01 - Network Segmentation

## Control Statement

Production environments are logically segregated from non-production environments.

## Context

Lesser environments must exist and be segregated, whether logically or physically, from the production counterparts. 

## Scope

This control applies to the GitLab.com and customers.gitlab.com environments. For each, lesser environments in which development and testing occur must be logically segregated from the production environments.

## Ownership

Control Owner: 
* `Infrastructure`

Process Owner:
* Infrastructure 

## Guidance

Pre-production environments should be logically segregated from their production counterparts. This can be accomplished by hosted them on different hosting providers or logically segregating them by project within the same hosting provider. 

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Network Segmentation control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/854).

### Policy Reference

* [Production Architecture](/handbook/engineering/infrastructure/production/architecture/#infra-current-archi-diagram)
* [Infrastructure Environments](/handbook/engineering/infrastructure/environments/)
* [Environment naming conventions](/handbook/engineering/infrastructure/production/architecture/#environments)

## Framework Mapping

* SOC
  * CC8.1
* PCI
  * 6.4.1

