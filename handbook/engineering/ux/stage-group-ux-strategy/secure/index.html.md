---
layout: handbook-page-toc
title: "Secure UX"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### Overview
Secure tools help your team follow and enforce security best practices effortlessly as part of the DevOps cycle. The Secure UX team’s goal is to provide the best experience in taking pre-emptive security measures before deploying your code, while the [Defend UX](/handbook/engineering/ux/stage-group-ux-strategy/defend/) team’s goal is to provide the best experience in keeping your application safe after your code is in production. See the [Defend and Secure UX](/handbook/engineering/ux/stage-group-ux-strategy/secure-and-defend/) page for more about our team and how our two teams work together.

### User
We have different user types we consider in our experience design effort. Even when a user has the same title, their responsibilities may vary by organization size, department, org structure, and role. Here are some of the people we are serving:

* [Software Developer](/handbook/marketing/product-marketing/roles-personas/#sasha-software-developer)
* [Development Tech Lead](/handbook/marketing/product-marketing/roles-personas/#delaney-development-team-lead)
* [DevOps Engineer](/handbook/marketing/product-marketing/roles-personas/#devon-devops-engineer)
* [Security Analyst](/handbook/marketing/product-marketing/roles-personas/#sam-security-analyst)
* Compliance Associate
* Security Engineer
* Chief Information Security Officer

Generally, developers are the users of the vulnerability reports in the MR/pipeline while security professionals are the users of the Security Dashboards.

### UX scorecards
##### Primary jobs to be done (JTBD)

**Static Analysis**

| Product Category | JTBD                                                         | Walkthrough                                                  | Recommendations                                              | Score | Rescore |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ----- | ------- |
| SAST             | When committing changes to my project, I want to be made aware if I am adding risk through vulnerable code, so that I know my changes can be merged without increasing the risk of my project. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/400) | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/479) | D     |         |

**Composition Analysis**

| Product Category    | JTBD                                                         | Walkthrough                                                  | Recommendations                                              | Score | Rescore |
| ------------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ----- | ------- |
| License Compliance  | When new licenses are added to a project I want to be aware so I can commit work that is compliant with my organization's rules. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/478) | [view epic](https://gitlab.com/groups/gitlab-org/-/epics/1618) | D     |         |
| License Compliance  | When my organization has license compliance rules to follow I want to be able to apply policies so that I can ensure any new code merged in a project is in compliance. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/402) | [view issue](https://gitlab.com/groups/gitlab-org/-/epics/1618) | F     |         |
| License Compliance  | When a merge request is disallowed, I want to know why, so I can resolve the issue and proceed with the MR. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/534) |                                                              | C     |         |
| License Compliance  | When new vulnerabilities are detected in a merge request, I want to disallow the merge request, so the team can review the vulnerabilities to resolve or decide on the next steps. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/533) |                                                              | D     |         |
| Dependency Scanning | When my dependencies have reported vulnerabilities, I want to learn more about the vulnerability cause and implications, so I can make an informed decision on taking action on how to proceed. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/806) |                                                              |       |         |
| Dependency Scanning | When my organization has a compliance policy with dependencies, I want to be aware if I’m breaking a company policy, so I can make sure my project dependencies are in compliance with my org compliance. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/584) |                                                              |       |         |
| Dependency Scanning | When dependencies are out-of-date, I want to be made aware so I can update them to reduce potential security vulnerabilities and avoid the potentially high cost of larger updates. | [view epic](https://gitlab.com/groups/gitlab-org/-/epics/2396) |                                                              |       |         |
| Dependency Scanning | When I need to audit 3rd party licenses and dependencies, I want to be able to provide inventory of licenses and dependencies for the auditor, so I can have them on record for auditing purposes and be able to share them with auditors and customers. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/583) |                                                              |       |         |
| Dependency Scanning | When I want to see how dependencies are related, I want to view them grouped by file, so I can access the information faster. | ... |                                                              |       |         |

**Shared**

| Product Category | JTBD                                                         | Walkthrough                                                  | Recommendations                                              | Score | Rescore |
| ---------------- | ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | ----- | ------- |
| Shared           | When I use the GitLab security feature for the first time, I want to configure all necessary features, so that the security team can start using them for GitLab projects. | [view issue](https://gitlab.com/gitlab-org/gitlab/issues/34368) | [view issue](https://gitlab.com/gitlab-org/gitlab/issues/34369) | C     |         |
| Shared           | When reviewing vulnerabilities for multiple projects, I want to see them all in one location, so that I can prioritize my efforts to resolve or tirage them while seeing the larger picture. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/401) | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/460) | D     |         |
| Shared           | When I want to configure my security tools, I want to be able to configure them to address my own business risk policies, so that I can be assured my company is monitoring risk based on our business risk policies. | [view issue](https://gitlab.com/gitlab-org/gitlab-design/issues/592) |                                                              |       |         |



### Team
* [Justin Mandell](https://gitlab.com/jmandell) - Product Design Manager
* [Tali Lavi](https://gitlab.com/tlavi) - UX Researcher
* [Kyle Mann](https://gitlab.com/kmann) - Sr. Product Designer
* [Andy Vople](https://gitlab.com/andyvolpe) - Sr. Product Designer
* [Camellia Yang](https://gitlab.com/cam.x) - Sr. Product Designer
* [Annabel Dunstone Gray](https://gitlab.com/annabeldunstone) - Product Designer
* [Becka Lippert](https://gitlab.com/beckalippert) - Product Designer

#### Team structure
We've divided the Secure stage into dedicated experience groups to align with a similar [split](/handbook/product/product-categories/#secure--defend-section) undertaken by our engineering and PM counterparts.

**Security Testing**

| Group | Features                                                     | Designer(s)           |
| ---------------- | ------------------------------------------------------------ | --------------------- |
| Static Analysis | SAST, Secret Detection | Becka Lippert         |
| Dynamic Analysis | DAST | Annabel Dunstone Gray         |
| Fuzz Testing | Fuzz Testing | Camellia Yang         |


**Compliance & Auditing**

| Group            | Features                                                     | Designer(s)         |
| --------------------------- | ------------------------------------------------------------ | ------------------- |
| Composition Analysis       | Dependency Scanning, Container Scanning, License Compliance | Kyle Mann           |

**Threat Insights**

| Group            | Features                                                     | Designer(s)         |
| --------------------------- | ------------------------------------------------------------ | ------------------- |
| Vulnerability Management       | Vulnerability Management | Andy Volpe           |

The Secure & Defend UX teams work closely together and have shared coverage in the following areas:

- Security Dashboard
- Control Center
- Status, Metrics and Reporting
- Security Configuration

This segmentation gives us a better opportunity to:
- Grow our expertise and knowledge within our subgroup while sharing relevant information with the rest of the team.
- Evolve and maintain relationships with our dedicated engineering team and PMs.
- Serve as the known main point of contact.
- Deeply understand our users' needs by initiating and/or leading research activities specific to our experience group.
- Focus on iterating and progressing our experiences from MVC to Lovable.

Read more about how we've created these dedicated experience groups [here.](https://gitlab.com/gitlab-org/gitlab-design/issues/458)


### Follow our work
Our [Secure and Defend UX YouTube channel](https://www.youtube.com/playlist?list=PL05JrBw4t0KrFCe5BgUkzFrZifjforQOz) includes UX Scorecard walkthroughs, UX reviews, group feedback sessions, team meetings, and more.
