---
layout: handbook-page-toc
title: "BU.1.03 - Backup Management: Alternate Site Control Guidance"
---
 
## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}
 

# BU.1.03 - Backup Management: Alternate Storage
 

## Control Statement
GitLab backups are securely stored in an alternate location from source data.
 

## Context
GitLab backup copies of information, software and system images need to be stored in an alternate site in the event of a disruption to the primary storage location. This supports system availability and redundancy. The main take-aways are listed below: 

* GitLab establishes an alternate storage site including necessary agreements to permit the storage and retrieval of information system backup information;
* GitLab ensures that the alternate storage site provides information security safeguards equivalent to that of the primary site.
* Alternate storage sites must be geographically distinct from primary storage sites.
* An alternate storage site should maintain duplicate copies of information and data in the event that the primary storage site is not available.
* The alternate storage site should include agreements, such as: environmental conditions at alternate sites, access rules, physical and environmental protection requirements, and coordination of delivery/retrieval of backup media.
* The Alternate storage site's requirements must be reflected in the corresponding contingency plan, so that GitLab can maintain essential missions/business functions despite disruption, compromise, or failure in GitLab's information systems.
 

## Scope
Alternate storage controls should cover:
* gitlab.com
* customers.gitlab.com (Azure)
* licenses.gitlab.com (AWS)


## Ownership
* Control owner:  `Infrastructure`
* Process owner:  `Infrastructure`
 

## Guidance
Backup copies of GitLab information, software and system images need to be stored in an alternate site in the event of a disruption to the primary storage location. This supports system availability and redundancy. Before choosing an alternate site, the following points should be considered:

* Identify an alternate storage site that is separated from the primary storage site to reduce susceptibility to the same threats.
* Threats that affect alternate storage sites are to be defined in GitLab Risk assessments and must include, the following such as: natural disasters, structural failures, hostile cyber attacks, and errors of omission/commission.
* Based on the types of threat that are of concern, GitLab can determine what is considered a sufficient degree of separation between primary and alternate storage sites; but for the hostile cyber attack threat, the degree of separation between sites is less relevant.
* RTO/RPO for Alternate storage sites - The alternate storage site should be configured so as to facilitate recovery operations in accordance with GitLab's recovery time and recovery point objectives.
* The alternate processing site agreements must contain priority-of-service provisions, in accordance with GitLab's availability requirements (including recovery time objectives).
* Identify any potential accessibility problems to the alternate storage site, in the event of an area-wide disruption or disaster and outline explicit mitigation actions. 
* Area-wide disruptions refer to those types of disruptions that are broad in geographic scope (such as, hurricane, regional power outage etc). These determinations are based on GitLab's risk assessment policy.
* Duplicating backup information at other alternate storage sites if access problems occur at originally designated alternate sites
* Comprehensive plan & procedure documentation on GitLab alternate site information needs to be in the handbook   


## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Backup Management: Alternate Storage issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/780) . 
 
### Policy Reference
*  [GitLab Geo](https://docs.gitlab.com/ee/administration/geo/)
*  [Geo Enablement](/handbook/engineering/development/enablement/#geo)
*  [Enablement Team: Jobs to Be Done for Geo](/handbook/engineering/ux/stage-group-ux-strategy/enablement/#ux-scorecards)
*  [Geo Planning](/handbook/engineering/development/enablement/geo/process.html)

## Framework Mapping
* ISO
  * A.12.3.1
* SOC2 CC
* SOC2 Availability
* PCI
    *  9.5.1
* NIST
    *  CP-6 
 
