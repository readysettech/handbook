---
layout: handbook-page-toc
title: "BU.1.01 - Backup Configuration Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# BU.1.01 - Backup Configuration

## Control Statement
GitLab configures redundant systems and performs data backups routinely as specificied by management to resume system operations in the event of a system failure.

## Context
We need to demonstrate that GitLab can be restored to a prior point in time in the event the data is corrupted, service interruption or other event that disrupts normal service. This helps ensure we have redundancy/backups enabled.

## Scope
Regular Backups help ensure secure and clean data to keep the business running in case of data loss, or a natural disaster. Scope is to make sure, at GitLab there is a regular backup process in place which is efficient and operational. 

* At GitLab, two components of infrastructure are backed up regularly: git repository data and the database. 
* The cadence of backup cycle at GitLab: Disk snapshots are taken every 24 hours. In addition to snapshots, the database is continually streaming transaction data to a fleet of standby replicas.
* All data is stored on the Google Cloud Platform on disk snapshots and in storage buckets and remains available indefinitely.
* Also, GitLab runs daily verification of the full database backup, ie a daily restore of the latest backup plus replay of writes from the archive. Thus being able to test the quality of the backup.


## Ownership
* GitLab Infra team owns the backup configuration to 100%. They are responsible to run both app snapshots and database backups.  


## Guidance
Assess and apply a clear backup and restore standard for all GitLab systems
* Prioritize systems according to data sensitivity
* Define the backup and recovery standards per data prioritization
* Prevent loss of data in case of an accidental deletion or corruption of data, system failure, or disaster
* Permit timely restoration of information and business processes, should such events occur.
* Manage and secure backup and restoration processes and the media employed in the process
* Ability to provide a point-in-time snapshot of information, whenever business requires. 
* Follow backup retention periods and data retention periods as defined by the [retention policy](/handbook/legal/record-retention-policy/), and if applicable, where defined contractually per business requirements.

The Backup configuration Documentation should include:

* Configuration of redundant systems showing how a failover occurs
* Configuration of backup settings of each system
   * If centrally managed, the runbook that controls backup configurations

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Backup Configuration control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/778).

### Policy Reference
* [PCI DSS v3.2.1 - 12.10.1 - Backup Configuration](https://www.pcisecuritystandards.org/documents/PCI_DSS_v3-2-1.pdf?agreement=true&time=1550838512120#page=113)
* [Backup & Restore at GitLab](https://docs.gitlab.com/ee/raketasks/backup_restore.html)
* [Backup & Recovery at GitLab](/handbook/engineering/infrastructure/database/#backup-and-recovery)
* [GitLab Production Backups](/handbook/engineering/infrastructure/production/#backups)
* [Handbook listing of DR for Databases](/handbook/engineering/infrastructure/database/disaster_recovery.html)
* [GitLab Development Guides](https://docs.gitlab.com/ee/development/README.html#databases)

## Framework Mapping
* ISO
  * A.18.1.3
* SOC
  * A1.2
* PCI
  * 12.10.1
