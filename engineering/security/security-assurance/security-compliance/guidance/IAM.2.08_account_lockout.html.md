---
layout: handbook-page-toc
title: "IAM.2.08 - Account Lockout Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.2.08 - Account Lockout

## Control Statement

Users are locked out of information systems after multiple, consecutive invalid attempts within a defined period; Accounts remain locked for a defined period. 

## Context

Where and only if applicable, appropriate, and technically feasible, users are locked out of information systems after 6 consecutive invalid attempts within a defined period. Where not feasible, multifactor authentication will serve as a mitigating control. 

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

Control owners: 
* Engineering
* Finance

Process owner: 
* Engineering
* Finance
* Infrastructure

## Guidance

TBD

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Account Lockout control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/819).

### Policy Reference

## Framework Mapping

* ISO

* SOC2 CC

* PCI
