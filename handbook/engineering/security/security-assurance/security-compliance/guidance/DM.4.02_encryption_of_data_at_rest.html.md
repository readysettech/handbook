---
layout: handbook-page-toc
title: "DM.4.02 - Encryption of Data at Rest Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# DM.4.02 - Encryption of Data at Rest

## Control Statement

Data at rest is encrypted according to GitLab policy.

## Context

Encryption is a process in which data is encoded so that it remains hidden from or inaccessible to unauthorized users. It helps securely protect data that you don't want anyone to have access to. By encrypting our data at rest, we can better protect private, proprietary and sensitive data and can enhance the security of communication between client applications and servers. Encrypting sensitive data at rest also adds another roadblock and layer of complexity for the adversary and helps protect customer, employee, and partner data.

## Scope

This control is applicable to the production environment and any end user devices that store such data. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may also include third-party systems that support the business of GitLab.com

## Ownership

* Control Owner: `Infrastructure`
* Process owner(s):
    * Infrastructure `100%`

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Encryption of Data at Rest control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/797).

Examples of evidence an auditor might request to satisfy this control:

* Reference to production architecture in the handbook
* Resource export from Google Cloud showing implementation of production architecture practices and state of encryption.
* GitLab Encryption Policy

## Guidance

This control can be tested by verifying the at-rest encryption status for any production resources. For compute instances, this can be done by verifying the compute resource's drive encryption status. For other resources such as managed databased (e.g., RDS and CloudSQL), this can be done by verifying the at rest encryption status through the resource's dashboard or other summary. For vendors such as GCP who encrypt data at rest by default, consider providing vendor's [documentation](https://cloud.google.com/security/encryption-at-rest/) showing the default at rest encryption.

### Policy Reference

[Encryption Policy](/handbook/engineering/security/vulnerability_management/encryption-policy.html)

## Framework Mapping

* SOC
  * 3.2
  * 6.5
* PCI
  * 3.4
  * 3.5
  * 3.5.3
  * 3.6
  * 3.6.3
  * 8.2.1
