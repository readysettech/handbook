---
layout: handbook-page-toc
title: "Stage Adoption Metrics"
---

## On this page

{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

View the [TAM Handbook homepage](/handbook/customer-success/tam/) for additional TAM-related handbook pages.

- - -

As part of the TAM's mandate to drive stage adoption and expansion with customers, we need to define exactly what it means to adopt a stage at GitLab. [For more information on how stage expansion is recorded and reported on, please visit this page](/handbook/customer-success/tam/success-plans/#open-and-categorize-a-stage-adoption-objective)
The detail below is a guide to defining what it takes to say a customer has adopted that stage within GitLab. We define stage adoption as >25% of the account using a stage as defined below. Less than 25% (roughly) is presumed to be a pilot or work in progress toward a significant foothold of a stage providing value within the company.

## Manage

Using 2 of the following:

- Making use of [Audit Events](https://docs.gitlab.com/ee/administration/audit_events.html) at the instance level as part of managing GitLab.
- Using [Code Analytics](https://about.gitlab.com/direction/manage/code-analytics/) and [Insights](https://docs.gitlab.com/ee/user/group/insights/) within GitLab.
- Using [Compliance Management](https://about.gitlab.com/direction/manage/compliance-management/) within GitLab.
- Using [Value Stream Management](https://about.gitlab.com/solutions/value-stream-management/) within GitLab.

Usage Discovery Questions:

1. How do your admins monitor changes to user permission levels?
1. How do you keep track of which users have access to certain groups within GitLab?
1. How are you measuring developer cycle time?
1. How do you measure efficiencies within a group or project?

## Plan

- Using Issue Tracking and/or Epics across 50% of teams.

Usage Discovery Questions:

1. What tools do you use to organize, plan and track project work?
1. Describe your issue and epic workflow.

## Create

- Using GitLab for git repo storage and code review (MR's).

Usage Discovery Questions:

1. Where do you manage you code base?
1. What processes do you follow for code reviews?

## Verify

- Have made instance level shared Runner(s) available.
- More than 25% of teams or projects are using GitLab CI/CD.
- When 75+% of pipelines are using GitLab CI/CD.

Usage Discovery Questions:

1. What types of Runners are you using today? (shared, group, specific)
1. What tools are you using for continuous integration?

## Package

- Using one or more of our registries (Package Registry, Container Registry, Helm Registry).

Usage Discovery Questions:

1. What tools do you use for package management?
1. What do you use to maintain Docker images?
1. Do you use the GitLab Container Registry to manage Helm Charts?

## Secure

- Using one of more of our security testing tools (SAST, DAST, Container Scanning, Dependency Scanning).

Usage Discovery Questions:

1. What do you use to scan your application source code and binaries?
1. Do you analyze your running web application for known runtime vulnerabilities?
1. What do you use to check your Docker images for known vulnerabilities?
1. Do you look for known vulnerabilities in you external dependencies?

## Release

- Using GitLab CI/CD to deploy their product (either the customer tells us this or we can see a high number of `deployments` and/or `environments` in the Usage Ping data).
- From a feature standpoint, if they are using 2 of the following features...
    - [Pages](https://about.gitlab.com/stages-devops-lifecycle/pages/)
    - [Review Apps](https://about.gitlab.com/stages-devops-lifecycle/review-apps/)
    - [Feature Flags](https://docs.gitlab.com/ee/user/project/operations/feature_flags.html)
    - [Release Orchestration](https://docs.gitlab.com/ee/user/project/releases/)

Usage Discovery Questions:

1. Are you using GitLab to deploy your applications?
1. Do you use GitLab pages to create, manage and deploy static sites?
1. Are you making use of review apps to get a full production like enviornment in every merge request?
1. How do you currently manage your releases? (i.e. versioning, release notes, etc.)

## Configure

- Using AutoDevOps, Kubernetes or Infrastructure As Code with 25% of teams or projects.

Usage Discovery Questions:

1. Are you using AutoDevOps to provide your users a pre-defined CI/CD configuration?
1. Are you using Kubernetes for any of the following scenarios?
1. Deploying software from GitLab CI/CD pipelines to Kubernetes
1. Using Kubernetes to manage runners attached to your GitLab instance
1. Running the GitLab application and services on a Kubernetes cluster

## Monitor

- Using Prometheus & Grafana to monitor their GitLab server.
- Or using Prometheus to monitor 25% of their project deployments.

Usage Discovery Questions:

1. How are you monitoring the stability and perfromance of your GitLab instance?
1. What do you use to monitor your deployed applications?

## Defend

- Using the [Web Application Firewall](https://docs.gitlab.com/ee/user/clusters/applications.html#web-application-firewall-modsecurity) within GitLab.

Usage Discovery Questions:

1. How do you manage HTTP traffic to your deployed application?
1. What do you use to block malicious traffic before it reaches your application?