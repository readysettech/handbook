---
layout: handbook-page-toc
title: "SYS.1.02 - Secure Audit Logging"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# SYS.1.02 - Secure Audit Logging

## Control Statement

GitLab logs critical information system activity to a secure repository. GitLab disables administrators ability to delete or modify enterprise audit logs; the number of administrators with access to audit logs is limited.

## Context

Logging is the foundation for a variety of other security controls including monitoring, incident response, and configuration management. Without comprehensive and reliable logs, large parts of our security compliance program wouldn't be possible.  This control focuses on the integrity of audit logs by securely safeguarding the logs from modification or deletion by privileged GitLab team members.

An auditor will look to validate the in-scope system repositories containing audit logs are unable to be modified or deleted, administrator access is limited to minimum number of team members based on job-related need, and the systems utilized for storage have proper security hardening.

To validate the control is working properly, the auditor should require additional pieces of information to demonstrate audit logging is functioning properly.  Those information items include:

* Handbook entry identifying all audit log repositories
* Handbook entry documenting how audit log modification or deletion is disabled for GitLab administrators
* Handbook entry documenting how we limit log repositories based on job-related need
* Handbook entry documenting how we monitor for log modification or deletion

## Scope

This control applies to all audit log repositories within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

Control Owner: 

* Security Operations

Process Owners:

* Security Operations
* Infrastructure

## Guidance

Audit log repositories should be secure (hardening best practices) and include the inability for GitLab adminstrators to modify or delete logs and for GitLab administrator access to be limited in number of GitLab team members. Any logs stored in Stackdriver cannot be deleted or modified by any person, per Stackdriver's own [documentation](https://cloud.google.com/logging/docs/audit/#audit_log_retention); logs from Stackdriver are only deleted after the retention period has passed.

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Audit Logging control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/905).

### Policy Reference

## Framework Mapping

* PCI
  * 10.5
  * 10.5.1
  * 10.5.2
  * 10.5.3
  * 10.5.4
