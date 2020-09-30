---
layout: handbook-page-toc
title: "Defend UX"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### Overview
The Defend stage includes all features that help you defend your applications and cloud infrastructure by giving you the ability to identify, catalogue, manage, and remediate threats, vulnerabilities, and risks. For more information about our principles and upcoming features, see our [Product Vision](/direction/defend/) page.

While the [Secure UX](/handbook/engineering/ux/stage-group-ux-strategy/secure/) team’s goal is to provide the best experience in taking pre-emptive security measures before deploying your code, the Defend UX team’s goal is to provide the best experience in keeping your application safe after your code is in production. See the [Defend and Secure UX](/handbook/engineering/ux/stage-group-ux-strategy/secure-and-defend/) page for more about our team and how our two teams work together.

### User

The Defend user is responsible for maintaining the security of their company’s environments and/or applications, through both proactive and reactive measures. They prefer to be proactive by abstracting away from manual, repetitive tasks and moving towards automation. 

The Defend user is responsible for risk mitigation, remediation, documenting their processes in timelines and runbooks, collaborating with other teams, meeting compliance standards, and performing root cause analyses. 

Typically, these user roles are: 

- [Security Analyst](/handbook/marketing/product-marketing/roles-personas/#sam-security-analyst) 
- SecOps Engineer

### UX scorecards 

Primary Jobs To Be Done (JTBD): 
- When I make sure my company’s applications aren’t vulnerable to bad actors, I want to monitor the traffic coming to my application and detect the possibility of an attack (SQL injection attempts, XSS attempts, vulnerability scanners, etc) so I can know what parts of the application I need to protect better. 
- When a bad actor successfully attacks my system, I want to look at the WAF logs to determine the attack vector (how they got in) so I can secure the weak points in my application.  
- When I want to make sure I’m being successful in my role, I want to be able to confirm if a data breach happened, if any systems went down as a result of an attack, to what extent our security controls negatively impact uptime or throughput, and how much maintenance did the security controls require this quarter, so I can track and meet my OKRs.
- When I want to avoid putting out constant fires, I want to be proactive by creating tooling to understand events occurring in my application so I can catch security risks before they can be compromised.
- When our proactive security measures fail, I want to prioritize incident response so I can keep our environments (and our customer data) safe.
- When I’m optimizing my company’s processes, I want to make sure everyone is updating the runbooks so I can make sure the team is being efficient and following the same validated procedures.
- When I want to demonstrate that a procedure is in place, I want to invest time in compliance so I can help our Security Compliance team provide information and assurance about our information security program to customers and remove security as a barrier to adoption by them.
- When I’m conducting incident management, I need to communicate well with other teams and know when to involve them so I can put fixes in place quickly and efficiently.

## Team
* [Justin Mandell](https://gitlab.com/jmandell) - Product Design Manager
* [Kyle Mann](https://gitlab.com/kmann) - Sr. Product Designer
* [Tali Lavi](https://gitlab.com/tlavi) - UX Researcher
### Team Structure
We've divided the Defend stage into dedicated experience groups to align with a similar split undertaken by our engineering and PM counterparts.

| Group        | Features                                               | Designer(s)                         |
| ----------------------- | ------------------------------------------------------ | ----------------------------------- |
| Insider Threat    | UEBA                                              | Kyle Mann             
| Container Security Group | WAF, Container Network Security | Kyle Mann                          |


### Secure & Defend UX
For more information about the Defend team and how we overlap and collaborate with the Secure team, see the [Defend and Secure UX](/handbook/engineering/ux/stage-group-ux-strategy/secure-and-defend/) page.
