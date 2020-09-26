---
layout: handbook-page-toc
title: "Critical System Tiering Methodology"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# What is a critical system?

A critical system is a system that has at least one of the following characteristics:
Is in-scope for one or more compliance certifications or regulatory requirements
Has a data classification of Orange or higher, per [GitLab’s Data Classification Policy](/handbook/engineering/security/data-classification-standard.html)

Critical systems are called out in the GitLab environment to ensure that the appropriate level of security visibility is provided over these systems given that they impact one or more of GitLab’s compliance and/or regulatory goals and/or the system itself contains sensitive, non-public data. The identification of critical systems at GitLab is a key driver in the prioritization of security related work.

## Critical System Tiers

All critical systems defined by GitLab Security are subject to a critical system tier. Tiering our critical systems allows us to effectively prioritize work based on a specific tier that a system belongs to. Each critical system is tiered based on the definitions in the table below.

|  **Tier Level** | **Definition** | **Examples of Associated Work** |
| ----- | ----- | ----- |
|  **Tier 1** | The system is in-scope for an external security compliance requirement. [Note that systems only in-scope for SOX are not included in this tier(#why-sox-compliance-is-excluded-from-tier-1). | Security Compliance owns Quarterly Access Reviews for these systems and will prioritize control testing activities for these systems first. Additionally, security impacting events and associated work will be prioritized for these systems. Vendor security reviews will always be performed at least annually for Tier 1 systems. |
|  **Tier 2** | The system is in-scope for SOX compliance only. | Quarterly Access Reviews are performed by the respective System Owner and control testing is prioritized following Tier 1 systems. Vendor security reviews will be performed at minimum over specific systems impacting Financial Reporting. |
|  **Tier 3** | The system is not in-scope for any type of external compliance requirement, but stores or processes ORANGE or RED data. | Quarterly Access reviews are performed by the respective System Owner and control testing is prioritized after Tier 2 systems, as applicable. |
| **Tier 4** | All remaining systems not subject to Tiers 1-3. | These systems will be reviewed as part of the [Security Operational Risk Management (STORM)](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html) Annual Risk Assessment and adjustments to system tiering will be made accordingly based on the annual assessment. |

**Important Note:** While Security will prioritize work for Tier 1 systems, note that at GitLab, our highest priority is ensuring that our core service offerings, GitLab hosted and on prem solutions, are secure for our customers. As such, any security related work impacting these offerings will always be prioritized above all other systems, regardless of a system’s tier.

### Why SOX Compliance is excluded from Tier 1

The critical system identification methodology is a tool used by the Security Organization to understand areas of focus and work prioritization due to impacts to security. SOX compliance is not included as part of the Tier 1 considerations because it is a compliance requirement driven by the business. Security compliance requirements considered for Tier 1 include the specific compliance audits that directly impact GitLab Security, such as SOC 2. 

## Current listing of critical systems

Security Compliance maintains a listing of critical systems in our environment that is viewable internally by GitLab Team members [here](https://docs.google.com/spreadsheets/d/1lbynw7uaFhv-uPJ1QETFmxN-SmObiEGkwUZIzqIy9uA/edit#gid=0). Note that this listing is updated ad-hoc as new systems are identified that are being used in GitLab’s environment or as systems are onboarded as part of procurement.

## When are critical systems identified

A critical system risk assessment is performed on an annual cadence in alignment with the [STORM annual risk assessment process](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html) to validate existing systems in GitLab’s environment and make adjustments to system risk ratings as necessary based on the criteria mentioned in the [system risk rating methodology](/handbook/engineering/security/security-assurance/security-compliance/third-party-vendor-security-review.html#inherent-risk-rating-methodology) section.

Ad-hoc system risk ratings will be performed throughout the year, with primary triggers being the procurement, SecOps, and IT processes that identify or incorporate new systems into GitLab’s environment.

The final risk levels assigned to critical systems will also be an input/driver during the STORM annual risk assessment process as the annual assessment activities will be aligned with assessing security risks related to GitLab’s critical systems.
