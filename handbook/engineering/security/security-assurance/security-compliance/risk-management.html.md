---
layout: handbook-page-toc
title: "SecuriTy Operational Risk Management (STORM) Program"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Security Operational Risk Management Program

## Purpose

The purpose of the Security Operational Risk Management (“STORM”) program at GitLab is to identify, track, and treat security operational risks. Ultimately, the management of operational risks helps support the broader organization wide objectives by ensuring that security risks that may impact GitLab's ability to achieve its customer commitments and operational objectives are effectively identified and treated in order to sustain and maintain the operational stability of GitLab's offerings.

## Scope

The scope of the STORM program is limited to operational (also referred to as Tier 2) risks as called out in the [NIST SP 800-30 Rev. 1](https://csrc.nist.gov/publications/detail/sp/800-30/rev-1/final) risk management hierarchy. That being said, there may be operational risks identified by departments outside of Security, such as GDPR or privacy related risks that are considered by the Legal Team which directly impact how GitLab chooses to operationally manage sensitive data. Refer to the risk diagram below for details of the risk management hierarchy as determined by NIST SP 800-30 Rev. 1.

Note that third party vendor and Information Systems deficiencies (also referred to as Tier 3 "risks") are not included as part of the operational risk management program as these deficiencies are typically addressed through the formalization of internal controls. However, deficiencies noted at the Tier 3 level have the potential to escalate to a Tier 2 Risk based on a [control effectiveness rating](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#determining-control-effectiveness-rating-cer).

Ad-hoc risks identified as part of day-to-day operating procedures (i.e. identified outside of the annual security operational risk assessment cadence) are subject to the formal STORM process where risks are scored in accordance with the defined STORM scoring methodologies. 

![Risk Management Hierarchy](/handbook/engineering/security/security-assurance/images/nist-rm-hierarchy.png)

## Risk Governance

A risk governance structure has been put in place to outline the overall roles and responsibilities of individuals as it relates to STORM. The current governance structure is:

|  **Group/Individual** | **Responsibilities** |
| :--- | :--- |
|  VP of Security | Executive sponsor of STORM program, performs a final review and approval of the annual risk assessment report |
|  Director of Security Compliance & Risk | Provides oversight of the STORM program, including a review and approval of the annual risk assessment report |
|  Security Compliance Team | Coordinates and executes the annual risk assessment, including the creation of the annual risk assessment report, maintains the risk register, and tracks risks through treatment. |
|  Risk Owners | Individuals that have the appropriate level of authority to make decisions for their specific organizations, but are not too far removed from the day-to-day operational procedures executed by their org. Responsible for driving risk acceptance and/or remediation activities over the risks in which they own |
|  Senior Leadership | Sets the tone of the risk appetite across the organization. Drive direct reports in their respective business units to comply with the STORM program to foster a culture where security operational risks can be proactively identified, managed, and treated. |
|  Employees and Contractors | Comply with the STORM program policies and procedures |

## Operational Risk Management Process

In order to effectively identify, manage, and treat operational risks, GitLab has defined a set of threat source categories alongside specific risk factors and risk scoring definitions that are considered as part of the security risk assessment process. Based on these threat sources, various stakeholders across the organization will be identified to participate in the annual risk assessment process. For details on the identified threat sources and example threat events, refer to the [STORM Methodology](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#identifying-threat-sources-and-events) page.

## Annual Risk Assessment

### Tone at the Top: Risk Appetite and Tolerance

GitLab's STORM methodology uses a defined Risk Appetite and Risk Tolerance as the primary drivers to determine **what risks we are willing to accept** versus **what risks we are not willing to accept and will need to treat**. These thresholds are defined by Senior Leadership across the organization to ensure that considerations over security operational risks are taking into account the broader Risk Appetite and Tolerance of GitLab in aggregate. In order to determine GitLab's risk appetite and risk tolerance, a risk appetite survey is distributed to individuals operating in a Senior Leadership capacity with direct relations to Security Operations. The responses to each survey question are scored and then averaged to arrive at an overall risk appetite and tolerance that includes perspective from management across the organization. The guiding questions have been prepared based on the [ISO 31000 Risk Management Methodology](https://www.iso.org/iso-31000-risk-management.html). For additional information on how Risk Appetite and Tolerance is determined, refer to the [STORM Methodology](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#risk-appetite-and-tolerance-scoring) page. Risk Appetite and Tolerance are reassessed year-to-year during the annual security operational risk assessment process.

### Risk Identification

Security Compliance conducts security operational risk assessment interviews with individuals operating at the Director and Manager levels at GitLab in order to identify security operational risks within their respective departments. Risks identified will always be framed in terms of threat sources and threat events, and then assessed against the likelihood of occurrence and the impact to GitLab if the risk event occurs. Additionally, these risks will be assessed against the current internal controls in place to determine the overall residual risk remaining. 

For details of the scoring methodology used, refer to the [STORM Methodology](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#risk-factors-and-risk-scoring) page.

### Risk Tracking and Reporting

Risks identified through the operational risk assessment process are formally tracked via an internal risk register. Given the nature of the sensitivity of this information in aggregate, the risk register is [not made public](/handbook/communication/#not-public) or distributed externally (or internally) or outside of the Security Compliance team and senior level management groups. However, Security Compliance will work towards _eventual transparency_ where we publish information about remediated risks within our risk register so that the broader GitLab community can have insight into how GitLab has choosen to remediate various risks. Note that as part of the risk treatment procedures, GitLab will make a determination on whether or not to accept a risk or pursue remediation based on our Risk Appetite and Tolerances.

A publicly viewable GitLab Risk Register Template is available [here](https://docs.google.com/spreadsheets/d/1wvGDdpi_Z0dyVe5mupNIkOlt1mUz64eF7a8fgfLuQuY/edit?usp=sharing) for those interested in getting some more insight into the type of information tracked in GitLab's risk register. 

### Risk Treatment

For each risk identified as part of the operational risk assessment process, a formal risk treatment decision is made to determine how GitLab will handle the risk. For details of the risk treatment options available, refer to the [STORM Methodology](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#risk-treatment-options) page.

### Annual STORM Reports

Once the annual security operational risk assessment is completed, an executive and detailed report is prepared:
* **Executive Report**: The executive report is a summary report that is used to share internally and upon request from external parties as applicable. This report is a high level summary that does not expose specific details about risks identified and individuals involved during the annual assessment.
* **Detailed Report**: The detailed report contains information about the specific high risks identified as part of the annual assessment in additiion to the specific indviduals that contributed to the annual assessment process.

## Ad-hoc Risk Identification

There may be times that risks are identified outside of the annual STORM process - such as risks that arise from a security incident, risk identified through regular day-to-day business operations, etc. All security operational risks identified ad-hoc should be discussed with the Security Compliance Team so that the appropriate level of risk evaluation is applied to the risk to determine if the risk should be escalated to GitLab's Risk Register to determine if a risk treatment plan should be pursued. If there a risk that needs to be discussed with Security Compliance, please reach out via the #sec-assurance Slack channel and tag @sec-compliance-team.

If the nature of the risk is highly sensitive and warrants a more discretionary discussion, please reach out directly to the Security Operational Risk Management program owner.

## Policy Review

The STORM policy is reviewed on at least an annual cadence by the Director of Security Compliance & Risk as part of [GCF Control SG.1.01 - Policy and standards review](/handbook/engineering/security/security-assurance/security-compliance/guidance/SG.1.01_policy_and_standard_review.html).
