---
layout: handbook-page-toc
title: "Security Compliance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Security Compliance Mission

It is the goal of the GitLab Security Compliance team to:

1. Enable GitLab sales by providing customers information and assurance about our information security program and remove security as a barrier to adoption by our customers.
1. Enable security to scale through the definition of security controls and determining the boundaries and applicability of the information security management system to establish its scope.
1. Work across industries and verticals to support GitLab customers in their own compliance journey.
1. Identify and mitigate GitLab information security risk through continuous control monitoring and automation.

## Security Compliance Core Competencies
A member of the [Security Assurance](https://about.gitlab.com/handbook/engineering/security/security-assurance/security-assurance.html) organization, these are the primary functions of the Security Compliance team:

1. Goveranance
   * GCF Control Maintenance
   * Security Compliance Handbook Pages
   * Security Policies and Standards
   * Security Compliance Training
   * Regulatory and Compliance Landscape Monitoring
   * Security Compliance Metrics
   * GRC Application Administration
1. Internal Compliance Audit
   * GCF Continuous Control Monitoring
1. Security Certifications
   * External Audits (e.g. [SOC](/handbook/engineering/security/security-assurance/security-compliance/soc2.html), FedRAMP, ISO, etc.)
   * Readiness Planning
   * Gap Assessments
1. Remediation
   * Control Test [Observations](/handbook/engineering/security/security-assurance/security-compliance/observation-management.html)
   * External Audit [Observations](/handbook/engineering/security/security-assurance/security-compliance/observation-management.html)
   * Gap Analysis [Observations](/handbook/engineering/security/security-assurance/security-compliance/observation-management.html)

## Security Compliance Work Inputs

1. GCF Continuous Control Testing
   * Controls are tested based on Security Certification requirements, GitLab Internal Audit team needs, and security risk.
1. External Audit requirements
   * When an external security audit is kicked off, work is performed as required within that audit.
1. Goveranance requirements
   * Work supporting the Security Compliance governance core competency is based on industry best practices, security certification requirements, and GitLab business need.
1. Customer Support
   * The Security Compliance team is engaged as subject matter experts to support specific security compliance customer requests. 
   * The Security Compliance team triages findings produced by external scanning services when responses are required according to the GitLab Risk and Field Security team.
1. Ad-hoc work streams
   * If you have a request for the GitLab Security Compliance team please [open an ad-hoc issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/new?issuable_template=ad_hoc_work.md) and we will review and prioritize that work weekly.

## Security Compliance Work Outputs
1. Governance documentation
   * The Security Compliance team manages security policies and standards.
   * The Security Compliance team evaluates GitLab handbook documentation through the course of continuous control testing and proposes updates as required.
1. Security Certifications (e.g. [SOC](/handbook/engineering/security/security-assurance/security-compliance/soc2.html), FedRAMP, ISO, etc.)
1. Remediation documentation
   * Control Test [Observations](/handbook/engineering/security/security-assurance/security-compliance/observation-management.html)
   * External Audit [Observations](/handbook/engineering/security/security-assurance/security-compliance/observation-management.html)
   * Gap Analysis [Observations](/handbook/engineering/security/security-assurance/security-compliance/observation-management.html)
1. Metrics/Reporting
   * The Security Compliance team provides the data relating to the health of the above [core competencies](#security_compliance_core_competencies).

## GitLab's Control Framework (GCF)

GitLab uses a common control framework that maps to a variety of industry compliance requirements and best practices. For information about how we developed this framework and a list of all of our security controls, please see the [security controls handbook page](/handbook/engineering/security/security-assurance/security-compliance/sec-controls.html).

## Ownership/DRI's

### Security Compliance Program DRI's
1. [SOC](/handbook/engineering/security/security-assurance/security-compliance/soc2.html) - [Liz Coleman](https://gitlab.com/lcoleman)
1. FedRAMP - [Nik Sarosy](https://gitlab.com/nsarosy)
1. GitLab IT General Controls (ITGC) - [Jeff Burrows](https://gitlab.com/jburrows001)
1. Governance - [Jeff Burrows](https://gitlab.com/jburrows001)
1. Internal Compliance Audit - [Jeff Burrows](https://gitlab.com/jburrows001)
1. Remediation - [Jeff Burrows](https://gitlab.com/jburrows001)

### GitLab system DRI's
The Security Compliance team uses an application-based ownership model for control testing. The information below represents the current ownership for systems that have already been tested or scheduled to being testing. This list will expand as our continuous control testing expands to include new systems.

1. GitLab.com - [Liz Coleman](https://gitlab.com/lcoleman)
1. customers.gitlab.com - [Nik Sarosy](https://gitlab.com/nsarosy)
1. Snowflake - [Nik Sarosy](https://gitlab.com/nsarosy)
1. Sisense - [Nik Sarosy](https://gitlab.com/nsarosy)

## Contact the Compliance Team

* Email
   * `security-compliance@gitlab.com`
* Tag us in GitLab
   * `@gitlab-com/gl-security/security-assurance/sec-compliance`
* Slack
   * Feel free to tag is with `@sec-compliance-team`
   * The #sec-assurance slack channel is the best place for questions relating to our team (please add the above tag)
* [GitLab compliance project](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance)

**Note: If you have an urgent request and you're not getting a response from the above team tags, the security compliance manager (@jburrows001) has their cell phone number in their slack profile. **
