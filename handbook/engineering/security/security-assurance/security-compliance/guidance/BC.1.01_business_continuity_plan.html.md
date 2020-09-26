---
layout: handbook-page-toc
title: "BC.1.01 - Business Continuity Plan Control Guidance"
---
 
## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}
 
# BC.1.01 - Business Continuity Plan
 
## Control Statement
GitLab's business continuity plan is reviewed, approved by management and communicated to relevant team members biannually.
 
## Context
A business continuity plan is an overall organizational program for achieving continuity of operations for business functions. Continuity planning addresses both information system restoration and implementation of alternative business processes when systems are compromised. The business continuity plan is a comprehensive runbook that can walk all GitLab team-members through exactly what their individual responsibilities are, in the event of a disruption to GitLab operations. This triggering event can be anything from a malicious breach of our systems to a global datacenter disruption. A business continuity plan is only effective if users can trust the accuracy of the information in the plan. The review cycle for a business continuity plan is designed to ensure all information in the plan is as up-to-date as possible.
 
## Scope
The business continuity plan is comprehensive by nature and will impact all GitLab stakeholders. The scope of GitLab Business Continuity Plan will cover:
* BC plan for gitlab.com
* BC plan for customers.gitlab.com (Azure)
* BC plan for license.gitlab.com (AWS)
* Processes and procedures that support business operations and above environments


## Ownership
* Business Operations owns this control.
* Infrastructure will provide implementation support for all of the above mentioned sites. (.com, customers, license)
 
## Guidance
A comprehensive business continuity plan for GitLab, can be categorized into the following seven steps:
* Identify GitLab's critical business functions
* Identify GitLab's critical systems & its dependencies
* Identify the risks to the business
* Specify and confirm GitLab data backup and recovery are working efficiently
* Document the functions, procedures and key personnel, who should lead the effort during the disaster
* Prepare a detailed communication plan with all key players involved
* Test, assess, learn and improve the plan on an annual basis

Based on the above, GitLab business continuity plan will have team and departmental pieces that roll up into one comprehensive plan. Each team knows best, as to what steps are needed in the event of a disruption to operations. Hence this overall plan is really more of a collection of individual plans and the packaging of these individual plans together. The plan should include the following: 

* The RTO (recovery time objective) and RPO (recovery point objective) decided and approved by GitLab management 
* Documentation on critical business requirements, including backup plans, business contingency and other related needs and logistics 
* Procedure documentation detailing the high-level steps that addresses how to respond in the event of the most likely disaster scenarios 
* Ensure backups are running and include an additional full local backup on all servers and data as part of the BCDR plan and test this annually
* Line of Communication and role assignments at each step. Document this list and make it readily available in times of need
* Vendor communication and service restoration plan of action 
* Once we have a high-level plan we can push this out to teams and have them create team-level plans
* The consolidated plan to be reviewed, approved and signed off by senior management
* DR test to be run annually, to ensure that the plan is working efficiently. 
 
## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Business Continuity Plan issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/774) . 
 
### Policy Reference
* [GitLab Business Continuity Plan in Handbook](/handbook/business-ops/gitlab-business-continuity-plan.html)
* [GitLab Disaster Recovery](https://gitlab.com/gitlab-com/gl-infra/readiness/-/blob/master/library/disaster-recovery/index.md)
* [GitLab Reference Architectures](https://about.gitlab.com/solutions/reference-architectures/)
* [GitLab Infra Epic for Geo](https://gitlab.com/groups/gitlab-com/gl-infra/-/epics/1)
* [GitLab Handbook listing of DR for Databases](/handbook/engineering/infrastructure/database/disaster_recovery.html)
* [NIST Guidance on Business Continuity](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-34r1.pdf)
* [PCI DSS v3.2.1 - Business Continuity Plan](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-2-1.pdf?agreement=true&time=1551196697261#page=113)
* [Geo and Disaster Recovery](/handbook/engineering/development/enablement/geo/)
* [GitLab DR Design](https://gitlab.com/gitlab-com/gl-infra/readiness/-/blob/master/library/disaster-recovery/index.md#design)
* [GitLab DR for Databases](/handbook/engineering/infrastructure/database/disaster_recovery.html)

## Framework Mapping
* ISO
  * A.17.1.1
  * A.17.1.2
* SOC2 CC
  * CC7.5
  * CC9.1
* SOC2 Availability
  * A1.2
* PCI
  * 12.10.1


 