---
layout: handbook-page-toc
title: "SLC.1.01 - Service Lifecycle Workflow Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# SLC.1.01 - Service Lifecycle Workflow

## Control Statement

GitLab software releases are developed using the DevOps Lifecycle (plan, create, verify, package, secure, and release).

## Context

The purpose of this control is to formalize the documentation and approval of software changes before those changes are implemented. This rigid process helps protect GitLab from insecure code being quickly pushed out into production without proper vetting.

## Scope

This control applies to all major software releases to GitLab.com.

## Ownership

* Control Owner(s): `Delivery` and `Development`
* Process owner(s):
    * Delivery
    * Development

## Guidance

This control is inherently performed as of the planning and rollout of new features for the GitLab.com SaaS offering. 

1. **PLAN**: The plan stage is the start of the lifecycle and is documented publicly on the [GitLab Releases handbook page](https://about.gitlab.com/releases/) This page links out to specific issues (which may have linked MRs) for each planned feature of a GitLab.com release. An important note to consider is that GitLab is working towards a continuous deployment model and features released for the GitLab SaaS offering occur on a daily cadence. On the 22nd of each month, all of the features developed and deployed between the 22nd of the last month and the current month are consolidated into a monthly blog post calling out the features that have been released. 

1. **CREATE**: The create stage is the actual development work that occurs to develop features and modify/change the GitLab.com source code. This phase is evidenced through the work that is completed via merge requests using the GitLab flow. Additionally, the development work is subject to change management controls.

1. **VERIFY**: The verify stage is automatic - all changes that will be deployed to the GitLab.com production instance are subject to the continuous integration (CI) pipelines where automated testing occurs to verify the source code changes. All changes navigate through staging and canary environments to ensure that changes in source code won't break GitLab.com prior to the changes being deployed to production. 

1. **PACKAGE**: Changes that will be deployed into production are packaged on a daily cadence and distributed to production as a single deployment. This is accomplished via a series of automated jobs that pick up source code changes and related component (i.e. dependency) versions that are compiled into a single deployment artifact and then packaged/built in preparation for deployment.

1. **SECURE**: The secure stage is engaged within the CI pipelines itself where automated Static Application Security Testing (SAST) and Dynamic Application Security Testing (DAST) testing is performed alongside container scanning to ensure that source code changes are secure in nature. This automated testing is performed at the deployment level.1

1. **RELEASE**: The release stage is engaged when a deployment is ready to be promoted from GitLab's Canary environment into GitLab's production environment. One of GitLab's Release Managers are responsible for engaging the Site Reliability Engineer on call and obtaining an approval to promote a deployment to the production environment.

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Service Lifecycle Workflow control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/888).

Examples of evidence an auditor might request to satisfy this control:

* Most of this evidence will be apparent during an auditor's evaluation of the change management process with the exception of the Plan stage. The plan stage can be evidenced through pointing to the [GitLab Releases page]((https://about.gitlab.com/releases/)

### Policy Reference

N/A

## Framework Mapping

* SOC2 CC
  * CC8.1
