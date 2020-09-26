---
layout: handbook-page-toc
title: "Customer Use Cases"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Customer Use Case Definition

A customer use case is:
* A customer problem or initiative that needs a solution and attracts budget
* Defined In customer terms
* Often aligned to industry analyst market coverage (i.e. Gartner, Forrester, etc. write reports on the topic)
* Relatively stable over time.
* These are discrete problems that we believe GitLab solves and are reasons customers choose GitLab (hence which we should seek out in prospects)


## Specific Use Cases

#### [1. Version Control and Collaboration (VC&C)](/handbook/marketing/product-marketing/usecase-gtm/version-control-collaboration)
**Create, manage and protect my intellectual property (i.e. source code, design, images, etc)** - in simple terms [Version Control](https://about.gitlab.com/solutions/version-control/) and Collaboration (VC&C), but more inclusively, *product configuration management* or *product asset management*.
I need a better way to manage changes to documents, software, images, large web sites, and other collections of code, configuration, and metadata among disparate teams. (Examples in GitLab include Git, branches, merge requests, code review, InnerSourcing, WebIDE, and files.)  
  
   **Analyst Coverage**: IDC, to some extent, forecasts this market. No spot on, recent reports, though Gartner may be considering a future report.
    
   **Value Drivers:**
   1. *Increase Operational Efficiencies:* Share and reuse code, prevent rework, and make reviews more efficient.
   1. *Deliver Better Products Faster:* Streamline reviews and collaboration around code changes.
   1. *Reduce Security and Compliance Risk:* Easier compliance through approvals of code changes.

#### [2. Continuous Integration (CI)](/handbook/marketing/product-marketing/usecase-gtm/ci/)
**Increase the quality of my code while decreasing time to delivery** - Continuous Integration (**CI**)
I need to automate the build and testing processes to consistently integrate code and continuously test. I want to run the unit and integration tests, measure performance and automate manual QA processes. I may use GitLab SCM or another. (Examples in GitLab include Pipeline, CI Runner, Jobs, Scheduled Jobs, Testing, Security Scanning (SAST), and Code Quality).

   **Analyst Coverage**: Forrester CI and Forrester Cloud CI

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* Single source of truth between SCM and CI; consistent and efficient dev experience.
   1. *Deliver Better Products Faster:* Automation to speed the process.
   1. *Reduce Security and Compliance Risk:* test my code automatically and early to reduce risks

#### [3. Continuous Delivery (CD)](/handbook/marketing/product-marketing/usecase-gtm/cd/)
**Want to speed up my build and release process and empower my developers to automatically deploy code** - (CI/**CD**)
I want to automate the build, test and packaging, configuration and deployment of applications to a target environment. (Examples in GitLab include: Pipeline, CI Runner, Jobs, Scheduled Jobs, Testing, Security Scanning (SAST), and Code Quality. CI Runner, Container Repository, Deploy Boards, Canary Deploys, Partial Deploys, Manual Deploys, Environments.)  

   **Analyst Coverage**: Gartner ARO, Forrester CDRA

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* Scalable, self-service, reusable deployment template. Deploy anywhere.
   1. *Deliver Better Products Faster:* Automatically deploy and test application with early feedback.
   1. *Reduce Security and Compliance Risk:* Enforce common controls and scan for vulnerabilities at the point of code change.

#### [4. DevSecOps (Shift Left Security)](/handbook/marketing/product-marketing/usecase-gtm/devsecops/)
**Test for application security vulnerabilities early in my app dev lifecycle** - (Shift-left security or **DevSecOps**)
I need to identify vulnerabilities during development with actionable information to empower dev to remediate vulnerabilities earlier in the life cycle. (In GitLab, SAST, DAST, Dependency Scanning, and Container Scanning.)

   **Analyst Coverage**: Forrester SCA Wave, Gartner Application Security MQ

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* Fix vulnerabilities at point of code change to reduce rework
   1. *Deliver Better Products Faster:* Ability to start testing early in dev process to eliminate vulnerabilities at the source
   1. *Reduce Security and Compliance Risk:* Fix vulnerabilities with actionable feedback to the developer at point of code change. Auto remediate when possible.

#### [5. Agile Management](/handbook/marketing/product-marketing/usecase-gtm/agile/)
**Need a better way to manage projects, programs, and portfolios using Agile methodology** - (**Agile** Management)
I need a better way of planning, initiating, monitoring, controlling, closing, and measuring the value created by Agile teams and projects. (Examples in GitLab include Roadmaps, Epics, Issues, Issue Boards, Issue Weights, Labels, Milestones, and burndown charts.)  

   **Analyst Coverage**: Gartner EAPT, Forrester PPM

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* Scalable, self-service, templated CI/CD, consistent and efficient dev experience, complete visibility to business.
   1. *Deliver Better Products Faster:* Ability to work in parallel and collaborate. Single source of truth between dev, sec and the business.
   1. *Reduce Security and Compliance Risk:* Single source of truth between dev and sec.

#### [6. GitOps](/handbook/marketing/product-marketing/usecase-gtm/gitops/)
**Want to automatically provision, administer and maintain infrastructure as code** - (CI/CD Infrastructure-as-code or **GitOps**)
I manually stage and test environments for infrastructure making it hard to track and error-prone. I want to stage all components and test them to be sure it works to automate my release pipelines, provide consistency, reduce cost, and  eliminate errors. I may frequently leverage integration with Terraform, Kubernetes, Ansible, OpenStack and others.

   **Analyst Coverage**: TBD

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* consistent dev experience, reusable scripts for operations.
   1. *Deliver Better Products Faster:* developer self-service, reusable CI/CD templates.
   1. *Reduce Security and Compliance Risk:* Enforces common controls

#### [7. Simplify DevOps](/handbook/marketing/product-marketing/usecase-gtm/simplify-devops/)
**Want to achieve expected results of DevOps given siloed teams, lack of visibility and collaboration which inhibits my speed of delivery** - (Simplify **DevOps**)
I want to manage my entire DevOps lifecycle more efficiently with better outcomes. The number of tools and maintenance of integrations is overwhelming and costly and security is challenging to integrate. My processes may include planning to production or may be a segment of the SDLC. (GitLab examples: Epics, Issue Boards, Source Code Management, CI, CD, Security Scans and Monitoring from GitLab. Value Stream Management: (VSM) helps you visualize and manage the flow of new innovation from ideas to customers. In GitLab, cycle analytics is a key element of managing the value stream.)

   **Analyst Coverage**: TBD

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* consistent and efficient dev experience with single source of truth and simplify tool chain
   1. *Deliver Better Products Faster:* More collaboration, working in parallel
   1. *Reduce Security and Compliance Risk:* Testing early, and enforcing common controls like single sign on, and shared view for collaboration, reporting and visibility.

#### [8. Cloud Native](/handbook/marketing/product-marketing/usecase-gtm/cloud-native/)
**Want to use more modern, cloud-native approaches to application development** (**cloud native**)
I want to use things like containers, K8s, and/or serverless for new development or containerize legacy applications. Help me lift and shift to cloud. Minimize my learning curve to set up, maintain and use clusters.

   **Analyst Coverage**: TBD

   **Value Drivers:**
   1. *Increase Operational Efficiencies:* consistent dev experience, streamline cloud native deployment, simplified tool chain
   1. *Deliver Better Products Faster:* developer self-service, application scalability, resiliency
   1. *Reduce Security and Compliance Risk:* Reduce technical and operational risk of migrating to the cloud. Enforce common controls.

## Other Use cases to consider

#### Data Science
I want to collaborate both inside and outside my team and/or organization. I need to plan and manage projects and sprints, with tools flexible enough to support scrum, kanban, and more. I want to be able to version control everything (e.g. manage and track different versions of files, models, test cases, data sets) and automate key workflow steps to improve efficiencies and mitigate manual errors. Speed is key, so I also want to streamline testing and validation of work. In addition to all of the above, I'd like to simplify infrastructure management (often across multiple cloud providers).

#### Repository Management
I want a package repository so that I can manage my organization's dependencies and control how they are built, published and shared throughout my organization. I need a local repository to store, version and access dependencies, that allows me to cache, proxy and audit all of my external dependencies in one place. I want all of the above to work securely and seamlessly with my pipelines so that I never have to worry about external dependencies causing problems during the software development lifecycle.

#### Application Monitoring (APM)
Monitoring application performance and feedback is a most critical step in the DevOps lifecycle. Product teams need to understand how their changes impact the business value of their applications. Examples in GitLab include Application Performance monitoring, server monitoring, Kubernetes Cluster Monitoring, and Kubernetes pod log review.

#### Portfolio Management
The goal of portfolio management is to determine the optimal resource mix for delivery and to schedule activities to best achieve an organization’s operational and financial goals, while honoring constraints imposed by customers, strategic objectives, or external real-world factors. Examples in GitLab include epics, roadmaps, and milestones. Analyst Coverage: Gartner EAPT, Forrester. GitLab does Agile project mgmt, not Portfolio Mgmt at this time.

#### Incident Management
I need a platform that consumes alerts from my monitoring stack and provides me with tools to take action on the critical ones by creating incidents. This tooling would allow us to triage, troubleshoot, remediate, and optimize to reduce risk of future incidents.


## Non-Use Cases

#### Integration - Planning
Integrations with Project Planning tools like: VersionOne, Rally, Jira, Trello, Monday, Workfront, and Basecamp.  Or integrations with Portfolio Planning tools like Clarity, MicroFocus PPM, or others.

#### Integration - SCM(GitHub)
The most common SCM integration is with GitHub

#### Integration - CI
Integrations with Jenkins, CircleCI, Bamboo or other CI servers.

#### Integration - CD
Integrations with common CD tools such as Puppet, Chef, Ansible, Jenkins and others.
