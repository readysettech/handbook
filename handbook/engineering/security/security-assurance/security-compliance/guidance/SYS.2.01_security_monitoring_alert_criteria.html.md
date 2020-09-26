---
layout: handbook-page-toc
title: "SYS.2.01 - Security Monitoring Alert Criteria"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

#  SYS.2.01 - Security Monitoring Alert Criteria

## Control Statement

GitLab deploys security monitoring mechanisms over GitLab.com production systems. Alerts generated from these mechanisms are triaged and tracked through to remediation by Security Operations.

## Context

Defined security monitoring alert criteria and a documented mechanism to handle security alerts helps ensure the security of customer, GitLab team member, and partner data. This control can be tested by reviewing the Incident Response and Security Incident Response processes, as well as the DELKE alerting criteria and notification mechanisms. 

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

* Control Owner: `Security Operations`
* Process owner(s):
    * Security Operations
    * Infrastructure

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Security Monitoring Alert Criteria control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/912).

Examples of evidence an auditor might request to satisfy this control:

* Sample security monitoring alert criteria
* Handbook documentation describing security monitoring alert criteria
* Monitoring tool configurations or documentation showing the security alert criteria are loaded
* Sample security monitoring alerts
* Documentation showing security alerts are made to authorized [GitLab Team Members](/handbook/communication/top-misused-terms)
* A list of authorized [GitLab Team Members](/handbook/communication/top-misused-terms)/teams to receive the alerts

### Policy Reference

* [Incident Management](/handbook/engineering/infrastructure/incident-management/)
* [Security Incident Response Guide](/handbook/engineering/security/sec-incident-response.html)
* [DELKE](https://gitlab.com/gitlab-com/gl-security/secops/detection/delke)

## Framework Mapping

* ISO
  * A.9.4.4
  * A.12.4.3
* SOC2 CC
  * CC3.2
  * CC3.3
  * CC3.4
  * CC5.1
  * CC5.2
  * CC7.2
* PCI
  * 10.8
  * 10.9
  * 12.10.5
  * 12.5
  * 12.5.2
