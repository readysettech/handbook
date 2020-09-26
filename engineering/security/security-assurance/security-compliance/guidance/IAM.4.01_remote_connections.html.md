---
layout: handbook-page-toc
title: "IAM.4.01 - Remote Connections Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.4.01 - Remote Connections

## Control Statement

Remote connections to production systems are controlled with either two factor authentication or an SSH connection.

## Context

Where and only if applicable, appropriate, and technically feasible, and with the understanding GitLab is a cloud-native, fully-remote and international organization favoring a Zero Trust network without a traditional corporate network infrastructure, access will be managed with a combination of [ssh](https://nvlpubs.nist.gov/nistpubs/ir/2015/NIST.IR.7966.pdf) and [Two Factor Authentication](https://csrc.nist.gov/glossary/term/Multi_Factor_Authentication) technologies.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

Control owner: 
* `Security Management`

Process owner: 
* Security Operations
* IT-Ops

## Guidance

Identity access management systems should enforce SSH or 2FA for connections to production systems and networks. 

Evidence an auditor may request:
* Policy defining our SSH or Two Factor Authentication requirements
* Configuration showing SSH or 2FA is required in order to connect to production systems.


## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Remote Connections control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/826).

### Policy Reference

* [Handbook>Engineering>Infrastructure>Team>Reliability Engineering>SRE Onboarding>Credentials](/handbook/engineering/infrastructure/team/reliability/sre-onboarding/#credentials)
* [Infrastructure readme.me file with instructions on setting up access](https://ops.gitlab.net/gitlab-com/gitlab-com-infrastructure#getting-started)
* [Infrastructure project>onboarding>SSH config](https://gitlab.com/gitlab-com/gl-infra/infrastructure/blob/3f30380f30faece696304922353c10c1e72011fd/onboarding/ssh-config)
* [Infrastructure instructions on setting up access using key-based SSH](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/gstg-bastions.md)
* [Cookbook for future Okta ASA solution for SSH Access Control](https://gitlab.com/gitlab-cookbooks/gitlab_okta_asa)
* [Two Factor Authentication](/handbook/security/#two-factor-authentication)

## Framework Mapping

* SOC2 CC
  * CC6.6
  * CC6.7
* PCI
  * 8.1.1
  * 8.6
