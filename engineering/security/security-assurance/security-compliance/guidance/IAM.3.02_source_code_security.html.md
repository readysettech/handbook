---
layout: handbook-page-toc
title: "IAM.3.02 - Source Code Security Control Guidance"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# IAM.3.02 - Source Code Security

## Control Statement

Access to modify source code is restricted to authorized personnel.

## Context

As GitLab is open source and we have contributors outside of the company from across the world, anybody can view and submit edits to the codebase to fix issues, add features, and so on. The spirit of this control is to ensure there's a process in place so that all additions, including from the GitLab community, are appropriately reviewed and approved before being merged into the codebase.

## Scope

This control applies to any system or process where source code can be modified.

## Ownership

Control owner:
* `Engineering`

Process owner:
* Engineering
* IT-Ops

## Guidance

As the GitLab system supports the ability to restrict modification without the `Owner` approval, this should be able to demonstrate how access reviews are achieved of the `Maintainer`, `Developer`, and `Owner` roles within GitLab.com.

Possible evidence an auditor would request:
* Policy on authorized roles that can make changes to source code
* Policy on how source code changes are approved
* List of authorized team members with permissions to change source code
* Evidence of an MR approved by an eligible approver

## Additional control information and project tracking

Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Source Code Security control issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/823).

### Policy Reference

* [Handbook section on Code Review](https://docs.gitlab.com/ee/development/code_review.html)
* [Handbook section on Maintainers](https://docs.gitlab.com/ee/development/code_review.html)
* [GitLab Enterprise Edition Docs - Permissions](https://docs.gitlab.com/ee/user/permissions.html)
* [GitLab Enterprise Edition Docs - Merge request approvals](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html)
* [GitLab Enterprise Edition Docs - Code owners as eligible approvers](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html#code-owners-as-eligible-approvers)
* [Member list for `gitlab-org`](https://gitlab.com/gitlab-org/gitlab/-/project_members?sort=access_level_asc)
* [Pre-production environment](https://pre.gitlab.com/users/sign_in)

## Framework Mapping

* SOC2 CC
  * CC8.1
