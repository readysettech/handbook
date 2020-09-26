---
layout: handbook-page-toc
title: "TPM.1.02 - Vendor Risk Management Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# TPM.1.02 - Vendor Risk Management

## Control Statement

GitLab performs a vendor security risk assessment to determine the data types that can be shared with a third party vendor.

## Context

The purpose of this control is for GitLab to be very intentional about the data shared with any third parties. Every time we share GitLab data (including customer data) with a third party we increase the attack surface of that data. Since we rely on a number of third party services, we will need to share certain data; performing the risk assessment referenced in this control ensures that we are following a formal process of evaluating the information security program of any third parties and only sharing appropriate data when there is a legitimate need.

## Scope

This control applies to all information shared with third parties that interact with the GitLab production environment.

## Ownership

Control Owner:

* `Security Compliance`

Process Owner:

* Security Compliance
* Legal

## Guidance

The GitLab Data Classification Policy defines the categories of data. This risk assessment process is most easily achieved by reviewing the SOC2 Type 2 audit report for any managed service providers if available, or through a privacy review at minimum. When a SOC2 Type 2 report is not available, a GitLab security questionnaire would serve as a good substitute.

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Vendor Risk Management control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/923).

### Policy Reference

## Framework Mapping

* SOC2 CC
  * CC9.2
* PCI
  * 12.8
  * 12.8.2
  * 12.8.3
  * 12.8.5
  * 2.6
