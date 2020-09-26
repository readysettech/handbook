---
layout: handbook-page-toc
title: "BU.1.02 - Resilience Testing Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# BU.1.02 - Resilience Testing

## Control Statement

GitLab performs backup restoration and/or failover tests quarterly to confirm the reliability and integrity of system backups and/or recovery operations.

## Context

By validating system backups/recovery operations in the event of an actual disaster or other disruption to service; we will have greater proficiency in restoring service to customers.

## Scope

This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership

* Control Owner: Infrastructure Team
* Process owner: Infrastructure Team

## Guidance

This guidance is a two-parter, provide evidence demonstrating:
* Documentation of incident response plan, including:
   * Roles and responsibilities
   * Specific procedures
   * Business recovery and continuity procedures
   * Backup processes
   * Legal requirements for reporting compromises
   * Coverage and responses for all critical systems
   * Reference/inclusion of incident response procedures from the payment brands
* Sample of previously reported incidents documentation

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Resilience Testing control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/779).

Examples of evidence an auditor might request to satisfy this control:

* A copy of GitLab's backup, disaster recovery, and incident response processes
* Documentation showing the testing of backup and disaster recovery procedures
* Testing the efficiency of GitLab backup and recovery process (at a minimum) on a quarterly basis.

### Policy Reference

*  A summary of our backup strategy is maintained [here](/handbook/engineering/infrastructure/production/#backups).
*  Database disaster recovery is documented in the [GitLab Handbook](/handbook/engineering/infrastructure/database/disaster_recovery.html).
*  Database backup recovery testing is [implemented](https://gitlab.com/gitlab-com/gl-infra/gitlab-restore/postgres-gprd/blob/master/README.md) in the form of an automated pipeline.
*  Snapshot restoration has been [manually verified](https://gitlab.com/gitlab-com/migration/issues/560) and handbook updates reflecting such testing and verification merged.
*  GCP snapshot procedures can be found [here](https://gitlab.com/gitlab-com/runbooks/blob/master/howto/gcp-snapshots.md). A manual verification of this process was done [here](https://gitlab.com/gitlab-com/migration/issues/560).
*  Incident management is documented in the [GitLab Handbook](/handbook/engineering/infrastructure/incident-management/). The documentation contains the following components:
*  [Incident runbooks](https://gitlab.com/gitlab-com/runbooks/tree/master/incidents) are available and maintained in the `runbooks` project.
*  Database-specific runbooks are located [here](https://gitlab.com/gitlab-com/runbooks/blob/master/incidents/database.md).
*  [Additional runbooks](https://gitlab.com/gitlab-com/runbooks) not specific to incident management are also available.


## Framework Mapping

* ISO
  * A.12.3.1
* SOC
  * A1.2
* PCI
  * 12.10.1
