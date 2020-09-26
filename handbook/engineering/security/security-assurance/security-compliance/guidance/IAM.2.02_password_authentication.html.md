---
layout: handbook-page-toc
title: "IAM.2.02 - Password Authentication Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.2.02 - Password Authentication

## Control
User and device authentication to information systems is protected by passwords that meet GitLab's [password policy guidelines](/handbook/security/#gitlab-password-policy-guidelines) as outlined in the Employee Handbook.

## Context

By ensuring passwords are implemented when and where appropriate, sensitive and valuable data is protected from unauthorized access and use. Enforcing GitLab's password complexity requirements further protects that data by reducing the risk of brute force and dictionary attacks that aim to guess user passwords.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

* Control Owner: `IT Ops`
* Process owner(s): 
    * IT Ops

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Password Authentication control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/813).

Examples of evidence an auditor might request to satisfy this control:

* Copy of GitLab's password policy and the Okta/1Password handbook entries
* Samples of service minimum password requirements, especially for Okta, which manages identify for many SaaS services used by GitLab

### Policy Reference

[Password Policy Guidelines](/handbook/security/#gitlab-password-policy-guidelines)

## Framework Mapping

* SOC2 CC
  * CC.5.2
  * CC6.1
  * CC6.6
  * CC6.7
* PCI
  * 8.2
  * 8.2.3
  * 8.2.4
  * 8.2.5
  * 8.2.6
  * 8.6
