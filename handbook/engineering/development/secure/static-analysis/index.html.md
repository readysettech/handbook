---
layout: handbook-page-toc
title: "Static Analysis Group"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Static Analysis

The Static Analysis group at GitLab is charged with developing solutions which perform [Static Analysis Software Testing (SAST)](/direction/secure/static-analysis/sast/),

[Secrect Detection](/direction/secure/static-analysis/secret-detection/), and [Malware Detection](/direction/secure/#malware-scanning) for customer software repositories.

## Common Links

* Slack channel: #g_secure-static-analysis
* Slack alias: @secure_static_analysis_be
* Google groups: static-analysis-be@gitlab.com

## How We Work

The Static Analysis group largely follows GitLab's [Product Development Flow](/handbook/product-development-flow/) as well as
[Secure's interpretation of this workflow](/handbook/engineering/development/secure/workflow/).

### Product Prioritization Labels

We also use additional labels to categorize different types of requests. These labels represent the top areas of product impact we are currently focused on within the Static Analysis team.

[Issue board](https://gitlab.com/gitlab-org/gitlab/-/boards/1578273?label_name[]=group%3A%3Astatic%20analysis).

#### `~SAST: Common Need`

Features we expect everyone to need and use

*Goal:* How do we protect from the most common security issues

*Measure:* Opportunity for impact

##### Types of issues

* Scanner updates
* Language coverage
* OWASP Top 10
* Better Vunl Metadata
* Documentation

#### `~SAST: Advanced Config`

Features we don’t expect everyone to use

*Goal:* Enable customization in configuration and enable advanced capabilities advanced users

*Measure:* Power and flexibility

##### Types of issues

* Customize rulesets
* Monorepo support
* Security scan customization

#### `~SAST: Enforce & Control`

Use least disruptive settings by default and allow customizations

*Goal:* Provide robust policies and controls to enforce security compliance

*Measure:* Policy & Compliance

##### Types of issues

* New scanners
* Policy ideas
* Compliance features

#### `~SAST: Workflow`

*Goal:* Enable workflows to ensure the appropriate attention on issues and allowing them to be tracked overtime.

*Measure:* Trust Scanner Issues & Track over time

##### Types of issues

* Speedy Scanners
* Usage ping data

#### `~SAST: Integrate`

Strongly defined integration harness to make internal/external integrations easier and more conformant

*Goal:* Provide defined integration point, enabling easier integrations

*Measure:* Be an ecosystem player

##### Types of issues

* Integration related ideas

### Community Contributions

The Static Analysis group is actively reserving capacity each iteration to be responsive to MRs
from the community. Each backend engineer in the group will serve as the [Community Merge Request Coach](https://about.gitlab.com/job-families/expert/merge-request-coach/) on a rotating basis. The Community Merge Request Coach has the following responsibilities, in priority order:

1. Triage and work with community contributors to help drive their MRs to completion.
1. Release feature(s) to core.
1. Triage and resolve ~priority::1 bugs.
1. Work an issue in the backlog that's of great interest to you.

## Issue Boards

* [Static Analysis Planning Workflow Board](https://gitlab.com/groups/gitlab-org/-/boards/1590105?label_name[]=group%3A%3Astatic%20analysis)
* [Static Analysis Delivery Workflow Board](https://gitlab.com/groups/gitlab-org/-/boards/1590112?label_name[]=group%3A%3Astatic%20analysis)
* [Static Analysis Planning Board](https://gitlab.com/groups/gitlab-org/-/boards/1229162?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=group%3A%3Astatic%20analysis)
* [Static Analysis Next X-Y Release Board](https://gitlab.com/groups/gitlab-org/-/boards/1702880?label_name[]=group%3A%3Astatic%20analysis)
* [Static Analysis EM Board](https://gitlab.com/groups/gitlab-org/-/boards/1655697)
