---
layout: handbook-page-toc
title: "BC.1.04 - Business Impact Analysis Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# BC.1.04 - Business Impact Analysis

## Control Statement
GitLab identifies the business impact of relevant threats to assets, infrastructure, and resources that support critical business functions. Recovery objectives are established for critical business functions.

## Context
The Business impact analysis (BIA) is a systematic process to determine and evaluate the potential effects of an interruption to critical business operations as a result of a disaster, accident or emergency.
* The Business impact analysis (BIA) report is a component of both business continuity planning and risk management.
* In the context of business continuity, BIAs help establish a priority for teams and services.
* Additionally, BIAs help document the risks associated with those teams and functions.
* BIAs help document the role of a team or service within the organization. They are not meant to be comprehensive or perfectly reflect the impact that the team or service has on GitLab. They are simply a way to illustrate the threats and the related impact to the business operations.

## Scope
This control is a subset of the Business Continuity control. Business Impact Analysis should exist for all services and teams that have a business continuity plan. 
## Ownership
* Business Operations owns this control.
* Infrastructure will provide implementation support for .com (GitLab.com, customer.com, licences.com) 

## Guidance
- BIA is a part of the BC plan. The first step is to come up with a comprehensive GitLab Business Continuity Plan, that includes the business approved RTO (recovery time objectives) and RPO (recovery point objectives). 
- The BIA report has to be reviewd and approved by Senior management. 

### Main points that a high-level BIA should include, are listed below:
* The business process criticality ranking:  Identify all critical business functions and processes. All business processes, systems and functions that are considered critical are those, if the failure to perform them result in an unacceptable damage to the company. Also include the interdependent processes that are deemed essential and business fails to function normally, if they are impacted by a disaster. 

* Additional findings: Any other finding or system vulnerability that might impact GitLab are noted here. The risk rating of these findings are to be calculated and a strategy to mitigate these risks are to be accordingly documented. Tools such as organizational charts, interviews, data flow diagrams and questionnaires, to gather data necessary to analyze the potential impact of a disaster on the business, can be utilized. 

* Delegation and defining the process:  Designate each process as critical or non-critical based on the business priority. Compile a list of personnel who must be in place to perform these functions. For the critical functions, come up with a detailed step-by-step approach about how each is performed, who performs it, and the operational and financial impact of interruption to each. 

* Adherence to GitLab's agreed upon RTO/ RPO: Determine a target recovery date for each process, each business system and each business-critical function. Identify internal and external business dependencies. Finally, decide upon a safe place for all the Business Impact Analysis data to be stored for future reference in the event of a disaster.

* Supporting information: This can include names of participants, tables summarizing business processes, etc.

* Conclusion: The most important part of the Business Impact Analysis is to weigh the exactness of all findings. Communicate the findings to the respective department managers or key personnel, to ensure that the assumptions made are in fact accurate and realistic. Once they review and agree to what has been determined and documented is accurate, present these BIA findings to the Senior management to gain approval. Now use these findings to develop the business recovery strategies.

* Protect the plan from unauthorized disclosure and modification.

* Update the BIA report at least annually and based on changes to the organization, information system, or environment of operation and problems encountered during the implementation, execution, or testing. 


## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Business Impact Analysis control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/777).


### Policy Reference
*  [Business Impact Analysis in the handbook](/handbook/business-ops/gitlab-business-continuity-plan.html#business-impact-analysis)
*  [Data Protection Impact Assessment (DPIA) Policy](/handbook/engineering/security/dpia-policy/)
*  [Data Protection Impact Assessments or DPIAs](/handbook/legal/privacy/#data-protection-impact-assessments-dpias)
*  [Data Protection Office and the Privacy Office](https://about.gitlab.com/privacy/#data-protection)	
*  [NIST BCP with reference to BIA](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-34r1.pdf)
*  [Handbook listing for DR](/handbook/engineering/infrastructure/design/disaster-recovery/)
*  [Project Plan related to the BC test tabletop exercise](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1721)
*  [Business Continuity Testing Procedure](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1818)
*  [Retrospective of the exercise documented](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1838)
