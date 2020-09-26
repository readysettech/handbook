---
layout: handbook-page-toc
title: "IR.2.02 - Incident Reporting Contact Information Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Control Statement
GitLab provides a contact method for external parties to:

* Submit complaints and inquiries
* Report incidents

## Context
Having an easily accessible and public channel for external parties to contact GitLab in the event of a security incident provides a way for the community to help GitLab keep its systems safe and to faster identify and respond to security incidents internally. This control can be tested by means of citing sufficient documentation with respect to emergency contacts and on-call engineers to support when an incident occurs, and to see if this documentation is easily available.  

## Scope
This control applies to all systems within our production environment. The production environment includes all endpoints and cloud assets used in hosting GitLab.com and its subdomains. This may include third-party systems that support the business of GitLab.com.

## Ownership
* Control Owner: `Corporate Compliance`
* Process owner(s):
    * Security Operations
    * Infrastructure
    * Legal

## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Incident Reporting Contact Information control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/843).

Examples of evidence an auditor might request to satisfy this control:
* Handbook pages that provide external parties a contact method

### Policy Reference
GitLab provides a contact method for external parties to:

1. Submit complaints and inquiries
*  [Incident Management](/handbook/engineering/infrastructure/incident-management/)
*  [Security Operations Oncall Guide](/handbook/engineering/security/secops-oncall.html)

*  [Support Team function in the handbook](/handbook/support/) 
*  [Support page](https://about.gitlab.com/support/) contains information to contact the Support team

*  [Security Incident Comms Plan](/handbook/engineering/security/security-incident-communication-plan.html#communicating-internally)

2. Report incidents
*  [Process for engaging security on-call](/handbook/engineering/security/#engaging-the-security-on-call)
*  [Security operations on-call guide](/handbook/engineering/security/secops-oncall.html#gitlab-security-operations-on-call-guide)
*  [Security Incident Comms Plan](https://gitlab.com/gitlab-com/gl-security/secops/operations/issues/205)

3. GitLab IR Contact information in the Handbook
*  [Information on how to contact the GitLab legal team](/handbook/legal/)
*  [Information on how to submit DMCA takedown requests to GitLab](/handbook/engineering/security/dmca-removal-requests.html)
*  [GitLab maintains current contact information for external parties to report Security incidents](/handbook/engineering/security/#external-contact-information)
*  [GitLab maintains an active bug bounty program](/handbook/engineering/security/#vulnerability-reports-and-hackerone) on HackerOne as another way for external parties to report security vulnerabilities
*  [All other inquiries and reports can be made on the `gitlab-ce` issue tracker](https://gitlab.com/gitlab-org/gitlab-ce/issues)

4. [Red Team Rules of Engagement](/handbook/engineering/security/red-team/red-team-roe.html)
5. [Incident Management for Self-Managed Customers](/handbook/support/incident-management/)


## Framework Mapping
* SOC2 CC
  * CC2.3
* PCI
  * 12.10.1
