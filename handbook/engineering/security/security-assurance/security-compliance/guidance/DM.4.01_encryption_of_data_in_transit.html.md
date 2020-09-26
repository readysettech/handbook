---
layout: handbook-page-toc
title: "DM.4.01 - Encryption of Data in Transit Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# DM.4.01 - Encryption of Data in Transit

## Control Statement
Data in transit is encrypted over public networks according to GitLab policy.

## Context
Encrypting data transmitted over public networks helps ensure the confidentiality and integrity of that data. Without encryption, data in transit over public networks can easily be intercepted using automated, open source tools and viewed and maliciously modified by malicious actors.

## Scope
This control applies to red, orange, and yellow data in the production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com

## Ownership
* Control Owner: `Infrastructure`
* Process owner(s): `Infrastructure`

## Guidance
*  TLS 1.2 or higher should be used to encrypt data in transit [Deprecate support for TLS 1.0 and TLS 1.1](https://gitlab.com/gitlab-com/gl-security/security-department-meta/issues/202).
*  Biannual validation of this control may be done by performing a scan with [Qualys SSL Labs](https://www.ssllabs.com/ssltest/) and/or scanning with [tls-scanner](https://gitlab.com/gitlab-com/security-tools/tls-scanner).
*  Such scans are sufficient for testing this control as the results show whether infrastructure transmitting red, organge, and yellow data over public networks uses TLS.

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Encryption of Data in Transit control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/796).

Examples of evidence an auditor might request to satisfy this control:
* Architecture and design documentation showing the use and high-level implementation details of TLS for production
* Random sampling of connections to/from production

### Policy Reference
* [GitLab Production Architecture](/handbook/engineering/infrastructure/production/architecture/)
* [Encryption in Transit in Google Cloud](https://cloud.google.com/security/encryption-in-transit/)
* [Deprecate support for TLS 1.0 and TLS 1.1](https://gitlab.com/gitlab-com/gl-security/security-department-meta/issues/202)

## Framework Mapping
* ISO
  * A.13.2.3
  * A.14.1.2
  * A.14.1.3
  * A.18.1.4
  * A.18.1.5
* SOC2 CC
  * CC6.7
* PCI
  * 2.3
  * 4.1
  * 4.1.1
  * 8.2.1
