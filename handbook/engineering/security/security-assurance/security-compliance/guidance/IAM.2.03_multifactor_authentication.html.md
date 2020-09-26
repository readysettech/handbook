---
layout: handbook-page-toc
title: "IAM.2.03 - Multi-factor Authentication Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.2.03 - Multi-factor Authentication

## Control Statement

Multi-factor authentication is required for authentication to the production environment.

## Context

Where and only if applicable, appropriate, and technically feasible, and with the understanding GitLab is a cloud-native, multi-factor authentication will be enabled on user accounts accessing prodcution instances of applications used internally.

## Scope

This control is applicable to application layer authentication for production instances of applications used at GitLab. Note that for systems which support Security Assertion Markup Language (SAML), these systems will either be onboarded to Okta (a tool used by GitLab to enforce MFA). In instances where SAML authentication is not available, MFA will be configured locally for an application if available. In instances where MFA has not been setup (either through Okta or locally), an exception request will be open to document an exception to the use of MFA. The exception request will be maintained over a system until it can comply with the MFA requirements specified in GitLab's Information Security Policies.

## Ownership

Control owner:
* IT-Ops (ultimate owner of the rollout/onboarding of systems onto Okta to support MFA as applicable)

Process owner:
* IT-Ops

## Guidance

If MFA cannot be configured, an exception request will be maintained until it can be configured.

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Multifactor Authentication control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/814).

### Policy Reference

## Framework Mapping

N/A - This GCF control has been scoped to SOX only. A separate MFA control exists specific to remote access / SSH. 
