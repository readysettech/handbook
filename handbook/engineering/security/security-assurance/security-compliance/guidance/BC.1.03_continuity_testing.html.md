---
layout: handbook-page-toc
title: "BC.1.03 - Continuity Testing Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# BC.1.03 - Continuity Testing

## Control Statement
GitLab performs business continuity and disaster recovery tests annually and ensures the following:

* Tests are executed with relevant contingency teams.
* Test results are documented.
* Corrective actions are taken for exceptions noted.
* Plans are updated based on results.

## Context
The business continuity plan is only useful if it is both maintained and validated. The testing part of this process is meant to be that validation and determines the efficacy of the plan. The purpose of this control is to determine if the business continuity plan would work in the event of a disruption to normal GitLab operations.  The business continuity test must have these three main categories:

* Recovery Planning:  Ensuring that Recovery processes and procedures are executed and maintained to timely restoration of systems or assets affected by any disruptive event.
* Improvements:  Recovery planning and processes are improved by incorporating lessons learned into future activities.
* Communications:  Restoration activities are coordinated with internal and external parties: such as coordinating centers, Internet Service Providers, system owners, victims and vendors.

## Scope
This control is a subset of the Business Continuity control. It defines that, a Business Continuity Plan (BCP) must be tested and updated on a regular basis to ensure its effectiveness in the event of a disaster and its continuing relevance to the Business. The process should include the testing of data recovery, information asset management, leadership response and recovery procedures. A process to do a full simulation of these, at least once each year with different, realistic scenarios that test the effectiveness of GitLab's Business Continuity plan should be the goal.

All parts of the business continuity plan should be tested. All teams and services that have a documented business continuity plan should have a corresponding documented test.

## Ownership
* Business Operations owns this control.
* Infrastructure will provide implementation support for .com

## Guidance
* BCP tests should be performed annually either via tabletop exercises or live simulations of business-disrupting events and the related resolution
    - To enhance organizational resilience by building upon the extensive coordination between GitLab teams to mature internal BCP processes.
    - To support best practice methodology and satisfy regulatory control requirements.

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Continuity Testing control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/776).

### Policy Reference
- [Business Continuity Test handbook link](/handbook/business-ops/gitlab-business-continuity-plan.html#business-continuity-testing)
- [Project Plan for GitLab's Business Continuity Test - Q1 2020](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1721)
- [Business Continuity Test Plan - Apr 30, 2020](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1818
- [Business Continuity Exercise Runbook Template](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/new?issuable_template=Business_Continuity_Exercise_Runbook)
- [Business Continuity Plan for Malicious Software Attack(s)](https://gitlab.com/gitlab-com/business-ops/Business-Operations/-/issues/264)
- [Business Continuity Test - April 30th, 2020 - Retrospective](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1838)

## Framework Mapping
* SOC2 CC
  * CC7.5
* SOC2 Availability
  * A1.3
