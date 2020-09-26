---
layout: handbook-page-toc
title: "Application Security Review Process"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Appsec Engineer Process for Application Security Reviews

This page details the application security review process for appsec engineers. 
The purpose of application security reviews are to proactively discover and 
mitigate vulnerabilities in GitLab developed or deployed applications in order 
to reduce risk and ultimately help make the company's mission successful.

An application security review may include any or all of the following stages:
- Threat modeling
- In-depth code review
- Dynamic testing

The results of each stage will inform the review done in the next stage. 
Ideally, all new features would receive some threat modeling, with 
the latter two stages being performed based on the risk profile. Features
already in development or production can receive an appsec review as 
well. The testing done is dependent on the circumstances.

## Stable Counterparts

One of the goals of the [stable counterpart][3] is to help identify features that 
need security review in the area to which they are assigned. This process 
is intended for such features, even if the stable counterpart will be 
performing the review.

## Building the Queue

The application security review queue is a priority queue of application 
features for security review. The priority can range from `priority::1` (Critical)
to `priority::4` (Low/Backlog).

Some guidelines for which features should be added to the queue are: 
- All new major features
- Features that have had repeat vulnerabilities
- Features related to authorization or authentication
- Features that handle [Red or Orange data][1]
- Features that work with cryptography or other data protection solutions

The idea is to capture features determined to be higher risk for 
vulnerabilities. It is quite probable that all features, especially `priority::4`
issues, will not get a full review, but by capturing those that are at higher 
risk, we can track additional statistics. For example, how many related 
vulnerabilities were reported in the bug bounty program. This data can help us 
to help iterate on priority.

Single Issue/MR pings that can be completed by the engineer on triage rotation
do not need a separate issue. This process is primarily for tracking features
over time. With that in mind, if a ping will need additional review, an issue 
should be created.

### Adding Features to the Queue

Separate issues will be used to track the appsec review process, as this
process could outlive the original issue/merge request.

1. Create an issue in the [Appsec Reviews issue tracker][2] using the [Appsec Review template](https://gitlab.com/gitlab-com/gl-security/appsec/appsec-reviews/-/issues/new?issueable_tempalte=AppSec%20Review)
    1. Set the title to a unique name for the feature
1. Follow the description in the template

### Assigning Priority

Every issue should have a priority assigned to help team members plan
testing. It is up to the application security engineer creating the issue to 
determine priority based on the data available to them. If you are not sure 
of the appropriate priority, be conservative and assign a higher priority. 
It can always be adjusted given feedback from other team members.

Guidelines for Priority (Not comprehensive, please build upon)

| Priority | Criteria |
|----------|----------|
| priority::1       | Red data, AuthN/AuthZ, Crypto, Single severity::1, Repeat severity::2 vulns |
| priority::2       | Orange data, Single severity::2 vulns |
| priority::3       | Yellow data |
| priority::4       | Only standard secure practices necessary |

### Quantifying interactions

The engineering team has created multiple labels with the purpose of quantifying
interactions done by stable counterparts and tracking the status of these interactions. 
Stable counterparts should add the right label depending on the status of the interaction
following the conditions below:
- `~sec-planning::in-progress`: The issue or MR is under review.
- `~sec-planning::pending-followup`: Stable counterpart expects to follow up on the review.
- `~sec-planning::complete`: Review finished with comments.
- `~sec-planning::no-action`: Review completed and no action required.

[1]: https://docs.google.com/document/d/15eNKGA3zyZazsJMldqTBFbYMnVUSQSpU14lo22JMZQY/edit
[2]: https://gitlab.com/gitlab-com/gl-security/appsec/appsec-reviews/issues
[3]: /handbook/engineering/security/application-security/#stable-counterparts
