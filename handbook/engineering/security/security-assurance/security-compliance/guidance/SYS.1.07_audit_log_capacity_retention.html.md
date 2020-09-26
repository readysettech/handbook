---
layout: handbook-page-toc
title: "SYS.1.07 - Audit Log Capacity and Retention"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# SYS.1.07 - Audit Log Capacity and Retention

## Control Statement

GitLab allocates audit record storage capacity in accordance with logging storage and retention requirements; Audit logs are retained one year with 90 days of data immediately available for analysis.

## Context

While GitLab already maintains a record retention policy, the purpose of this control is to establish required minimum storage and retention requirements for in-scope financial systems to ensure the requirements within the record retention policy align with compliance requirements.

## Scope

This control applies to SOX and PCI in-scope financial systems.

## Ownership

*  Control Owner:
    *  `Infrastructure`

*  Process Owners:
    * `Infrastructure`
    * `Security Operations`
    * `Security Compliance`

## Guidance

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/910).

### Policy Reference

*  [SOX IT General Controls Scoping](https://docs.google.com/spreadsheets/d/143pUC61YVS1VC-GWsRZb5wdiUCeu-PEwAc751sOPsdE/edit?ts=5d323bbf#gid=214635064)
*  [Record Retention Policy](/handbook/legal/record-retention-policy/)

## Framework Mapping

PCI DSS V3.2.1:
    * 10.7
