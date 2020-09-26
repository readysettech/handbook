---
layout: handbook-page-toc
title: "SLC.2.01 - Source Code Management"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# SLC.2.01 - Source Code Management

## Control Statement
GitLab source code is managed using automated version control mechanisms.
 
## Context

GitLab-approved version control mechanisms should be enforced over all source code that is maintained by GitLab to ensure tracability and auditability between source code changes. Processes in place to enforce version control demonstrate strong security and SDLC maturity.

GitLab source code version is managed via the use of an automated job that prepares a build for deployment into production. At GitLab, an automated deployment model is used to increase efficiency and minimize the level of human interaction when consolidating source code changes into a build/package to be deployed into production. This is accomplished using GitLab's Release Tools project. One of the deployment jobs that is executed daily consolidates all changes into an auto-deploy branch for eventual deployment into production (i.e. the gprd environment). There is specific logic that is executed by this job which names the auto-deploy branch with a date and timestamp at the point of branch creation, creating a unique source code deployment version. 
 
## Scope

The scope of this control applies to the GitLab product, where the source code is owned and managed by GitLab. Note that this control does not extend to other systems where GitLab does not maintain source code.

## Ownership
Delivery Team (maintains the logic for the auto-deployment jobs)
 
## Guidance

The auto-deploy job logic responsible for applying a date and timestamp to an auto-deploy branch is housed within the `auto_deploy.rake` file in the gitlab-org/release-tools/ project. There is a specific line item in the logic that is used to define the auto-deploy branch version. The logic appends a date and timestamp to the auto-deploy branch that is created as part of the automated deployment process. The logic is:

> version = "#{branch.version.to_minor}.#{branch.tag_timestamp}"

Changes to this logic are subject to GitLab's change flow, where a merge request is opened suggesting a chagne to the file. Changes are subject to review and approval and cannot be merged by the merge request author.
 
## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Source Code Management control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/889).
 
## Framework Mapping
* SOC2 CC
   * CC2.1
