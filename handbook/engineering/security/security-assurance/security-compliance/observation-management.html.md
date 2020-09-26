---
layout: handbook-page-toc
title: "Security Compliance Observation Management"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Security Compliance Observation Management

## Observation Management Overview

Observations in the context of security compliance refers to any Tier 3 operational risks which are more granular than [Tier 2 operational risks](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html#scope). These observations are risks identified at the Information System level. The volume and granularity of these Tier 3 risks make it inappropriate to track via the [GitLab Risk Register](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html#risk-tracking-and-reporting) and so this observation management process will guide team-members on how to track these Tier 3 risks.

## Observation Management Process

The following phases walk through the lifecycle of operational risk observations.

### Identifying observations

Observations can be identified in the following ways:
1. Security control testing
1. Vendor security reviews
1. User access reviews
1. Ad-hoc issues

### Recording observations

Each observation has a GitLab issue associated with it in the [Observation Management project](https://gitlab.com/gitlab-com/gl-security/compliance/observation-management). The GitLab security compliance team will [create all observation issues](https://gitlab.com/gitlab-com/gl-security/compliance/observation-management/-/issues/new) to ensure uniformity in the process. If you have a Tier 3 operational risk that you have identified, please [reach out to the GitLab security compliance team](/handbook/engineering/security/security-assurance/security-compliance/compliance.html#contact-the-compliance-team) and we can help get this observation record created.

If a template does not exist for the related source of the identified observation, please create an MR for the proposed new observation issue template and share with the Security Compliance team.

### Observation Risk Ratings

Tier 3 operational risk ratings are based off the [STORM risk rating methodology](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#risk-factors-and-risk-scoring).

#### Determining the likelihood

"Likelihood" refers to the likelihood that the observation will impact the results of an internal or external audit:

|Qualitative Score | Risk Level	| Scoring Guidelines |
| :---: | :---: | :---: |
|5 to 6	| HIGH	| 6 = This observation will **certainly** change internal or external audit results 5 = This observation will **almost certainly** change internal or external audit results |
|3 to 4	| MODERATE	| 4 = This observation will **likely** change internal or external audit results 3 = This observation **could** change internal or external audit results |
|1 to 2	| LOW	| 2 = This observation **is unlikely to** change internal or external audit results 1 = This observation **won't** change internal or external audit results |

#### Determining the impact

"Impact" refers to the impact this observation would have on the results of an internal or external audit if such an impact were to occur:

| Impact Score | SOC Audit Impact Guidelines |
| :---: | :---: |
| Very Low (1) | This observation **will not** result in an audit exception or a qualified report |
| Low (2) | This observation **could** result in a low-risk audit exception |
| Moderate (3) | This observation on its own **will** result in a low-risk audit exception |
| High (4) | This observation on its own **will** result in either a moderate-risk audit exception or **could** result in a qualified report |
| Very High (5) | This observation on its own **will** result in either a high-risk audit exception or **will** result in a qualified report |

#### Determining the overall risk rating

Inherent risk of the observation is calculated by multiplying the qualitative score of the likelihood by the qualitative score of the impact and using that product in the [STORM risk level table](/handbook/engineering/security/security-assurance/security-compliance/operational-risk-management-methodology.html#determining-inherent-risk-vs-residual-risk).

### Tracking observations

Current observations can be tracked in a number of different ways:
1. [Observations grouped by the source of how they were identified](https://gitlab.com/gitlab-com/gl-security/compliance/observation-management/-/boards/1741813)
1. [Observations grouped by the Risk Rating of the observation](https://gitlab.com/gitlab-com/gl-security/compliance/observation-management/-/boards/1741814)
1. [Observations grouped by the current status of the observation](https://gitlab.com/gitlab-com/gl-security/compliance/observation-management/-/boards/1741815)

If multiple observation issues relate to the same root cause or are blocked by the same component of work, these issues will be connected together into an Epic in order to more clearly see how multiple observations issues are connected. A list of these Epics can be found [here](https://gitlab.com/groups/gitlab-com/gl-security/compliance/-/epics?label_name%5B%5D=Observation+Epics).

### Remediating observations

Once observations are identified and recorded by the security compliance team, that observation will first be validated by the observation owner. Once validated, it will be up to the observation owner to identify the milestones/phases of work involved in the remediation, tracking progress towards remediation, and completing remediation. Once remediation has been completed, the observation owner will notify the security compliance team who will validate that remediation has been completed and re-test the observation as appropriate before closing the observation issue.

## Remediation SLA

Observation remediation SLA's are determined by the risk rating of the individual observation. The following table shows the SLA for each risk rating:

| Risk Rating | Remeditation SLA |
| :---: | :---: |
| Low | Best effort |
| Moderate | 90 days |
| High | 30 days |

## Contact

If you have any questions or feedback about the security compliance observation management process please [contact the GitLab security compliance team](/handbook/engineering/security/security-assurance/security-compliance/compliance.html#contact-the-compliance-team).
