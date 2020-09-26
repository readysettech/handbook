---
layout: handbook-page-toc
title: "NO.1.01 - Network Policy Enforcement Points Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# NO.1.01 - Network Policy Enforcement Points

## Control Statement

Network traffic to and from untrusted networks passes through a policy enforcement point; firewall rules are configured to prevent unauthorized access.

## Context

Effective network traffic policies help minimize the risk of network-based attacks, including denial of service attacks and malicious data exfiltration. By inforcing ingress and egress rules, we can limit the number of unnecessary open ports to protect customer, GitLab team-member, and partner data and prevent unauthorized access.

## Scope

This control applies to all systems within the production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

Control Owner: 
* `Security Operations`

Process Owner:
* Infrastructure Team

## Guidance

Control should be designed to ensure we don't default to "allow all" traffic and instead put in place reasonable barriers for access to our production network.

## Additional control information and project tracking

Infrastructure manages the configuration for GCP using chef and terraform which includes firewall rules. Configurations are version controlled and require approval prior to changing.
The Infrastructure team engages with Security Operations to review new firewall rules that fall outside of the baseline. Security manages the monitoring for the service and can validate the correct rules are still in tact.

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Network Policy Enforcement Points control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/847).

### Policy Reference

* [Internal Networking Scheme](/handbook/engineering/infrastructure/production/architecture/#internal-networking-scheme) in the handbook links to the production mirror terraform [`gitlab-com-infrastructure` project](https://gitlab.com/gitlab-com/gitlab-com-infrastructure).
* Terraform configurations provided for the [production environment](https://gitlab.com/gitlab-com/gitlab-com-infrastructure/blob/master/environments/gprd/main.tf) 'gprd' project within GCP and [VPC](https://gitlab.com/gitlab-com/gl-infra/terraform-modules/google/vpc) configurations for each module.
* Infrastructure [production testbed template](https://gitlab.com/gitlab-com/gl-infra/infrastructure/blob/master/.gitlab/issue_templates/production_testbed.md) with process to prompt Security review of firewall rules for access to production data.

## Framework Mapping

* SOC2 CC
  * CC4.1
  * CC5.2
* PCI
  * 1.1.4
  * 1.2
  * 1.2.1
  * 1.2.3
  * 1.3
  * 1.3.1
  * 1.3.2
  * 1.3.3
  * 1.3.4
