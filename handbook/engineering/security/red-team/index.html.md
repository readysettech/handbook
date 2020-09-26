---
layout: handbook-page-toc
title: "Red Team"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Red Team Overview

GitLab's internal red team extends the objectives of penetration testing by examining the security posture of the organization and their ability to implement effective cyber defenses.

Penetration testing is a specialized type of assessment conducted on information systems or individual system components to identify vulnerabilities that could be exploited by adversaries. Such testing can be used to either validate vulnerabilities or determine the degree of resistance organizational information systems have to adversaries within a set of specified constraints (e.g., time, resources, and/or skills).

Red team exercises provide more comprehensive assessments that reflect real-world conditions over penetration testing. The exercises can further be used to improve security awareness and training and to assess levels of security control effectiveness. GitLab utilizes NIST 800-53 Revision 4 security control CA-8 to define the Red Team and their mission. The control can be found on [NIST.gov](https://nvd.nist.gov/800-53/Rev4/control/CA-8).

The Red Team operates under a pre-defined set of [rules of engagement](./red-team-roe.html). The rules of engagement exist to inform GitLab's team members on how the team operates during engagements. It provides guidelines for determining scope, the ethics we employ during our engagements, how we collaborate as a security team, and how we escalate vulnerabilities and exploits we discover during those engagements.

Further details can be found in the [job family description](/job-families/engineering/security-engineer/#red-team).



## Red Team Operations

Most Red Team operations are planned and approved before any actions are conducted (see [Red Team Open Scope](#red-team-open-scope) for exceptions). Each operations consists of the following steps:

- [Threat modeling](#threat-modeling)
- [Proposing an operation](#proposing-an-operation)
- [Documenting an operation](#documenting-an-operation)
- [Completing an operation](#completing-an-operation)
- [Delivering a report](#delivering-a-report)
- [Completing a restrospective](#completing-a-restrospective)
- [Iterating an operation](#iterating-an-operation)

### Threat Modeling

GitLab maintains a document titled "Data Classification Policy" (team members can find this by searching Google Docs) that categorizes digital assets based on levels of sensitivity.

The Red Team maintains a [secure project](https://gitlab.com/gitlab-red-team/threat-modeling) that builds threat models on top of these classification policies.

While planning a new operation, the first step is to ensure there is alignment with an existing threat model. If not, the existing model should be updated or a new model created.

### Proposing an Operation

Operations should have a clear goal, generally in alignment with one of the following:

- Test a specific detection and/or response capability
- Test a hypothesis that a specific asset in a threat model could be compromised
- Identify a specific security gap in order to justify a new project, policy, or procedure

Any GitLab team member can participate in the proposal or discussion of an upcoming operation. To do so, [open an issue](https://gitlab.com/gitlab-com/gl-security/gl-redteam/proposed-red-team-operations/-/issues/new) in [Red Team Proposed Operations](https://gitlab.com/gitlab-com/gl-security/gl-redteam/proposed-red-team-operations) and choose the issue template called `red_team_operation`.

The issue template will guide you through the process of planning an operation.

### Documenting an Operation

Ongoing operations are documented in a GitLab-manged instance of [Vectr](https://vectr.io). This tool allows us to track at a very granular level the specific Tactics, Techniques, and Procedures (TTP) used in an operation. Each TTP (known as a "Test Case" inside Vectr) can be can be analyzed to determine what was detected, blocked, and/or logged after the operation is complete.

New operations can be documented as follows:

- Create a new "assessment" inside Vectr based on the operation name.
- Create a new "campaign" inside the assessment. Based on the "Red Team Methodology" section inside the issue that proposed the operation, try to plan out as much of the attack as possible prior to actually beginning the operation.
- As the operation progresses, make sure to enter any test case into Vectr *first* before conducting the activity. This will ensure we can properly track the activity start and finish time.

Attempting to plan out test cases in Vectr ahead of time helps us understand the offensive strategies that will be used. This, in turn, helps us understand the specific security controls we expect to encounter in terms of detection, response, and logging. It also encourages a broader usage of techniques from the [MITRE ATT&CK](https://attack.mitre.org/) framework, which we use to ensure our security team has a broad exposure to realistic attack scenarios.

Logging every action in a single campaign inside Vectr may produce a complex attack path, particularly for a chain of events that cycles through a traditional killchain multiple times. That's ok. It's best to get everything logged as you go. Once an operation is complete, it may make sense to use the "clone" functionality to split some actions out into separate, logical attack paths.

### Completing an Operation

Once the Red Team has completed the planned offensive operations, the assigned members of the Blue Team will work through each test case in Vectr to fill in the following:

- Outcome (Blocked, Detected, Not Detected [logged / not logged])
- Expected detection layers
- Actual detection layers
- Notes and evidence as required, such as links to resulting issues

If a test case is marked as "Not Detected", it needs to be considered for remediation - especially if there was a specific "Expected detection layer" marked inside Vectr. Some test cases may also expose a specific vulnerability in a product or configuration - these should also result in an issue being opened.

These issues will generally be opened in the [Security Operations issue tracker](https://gitlab.com/gitlab-com/gl-security/secops/operations/-/issues) and labeled with the following:

- Red Team :: Issue
- Red Team :: {operation name}
- Goal :: Tactical *or* Goal :: Strategic

### Delivering a Report

Vectr provides a wide range of reports to provide insight on detection and response capabilities. These can be exported and shared on request.

After project completion, the Red Team will create a report as a GitLab issue in the [Reports](https://gitlab.com/gitlab-com/gl-security/security-operations/gl-redteam/reports) project. An issue template is provided that includes the following sections:

- Executive Summary:
  - Operation Goals: A short summary of what the operation was meant to accomplish.
  - Outcomes: A short summary of what was actually accomplished.
  - Highlights: Noteworthy observations from the operation, such as best practices that were encountered or security controls that were working well.
- Operation Detail:
  - Attack Paths: A graphical workflow exported from Vectr.
  - Attack Narrative: A written explanation of the attack paths, in narrative format.
  - Technique Detail: Detailed outcome table of every technique performed, exported from the Vectr report called "Campaign Detailed".

Most of these reports will be classified [YELLOW](/handbook/engineering/security/data-classification-standard.html#yellow), meaning they will not be made publicly available. The Red Team does support GitLab's [core value](/handbook/values/) of transparency but must ensure not to introduce risk to GitLab, GitLab customers, or GitLab business partners. When possible, we will share techniques and tooling via our [Tech Notes](https://gitlab.com/gitlab-com/gl-security/gl-redteam/red-team-tech-notes).


### Completing a Restrospective

The Red Team follows GitLab engineering's recommendation to perform regular [retrospectives](/handbook/engineering/management/team-retrospectives/). These may be performed on a regular cadence or, at minimum, just prior to completing an individual operation depending on need. The objective is to improve the performance of the team by taking an honest look at what went well, what went poorly, and specific, actionable takeaways to iteratively improve the team in terms of our technical and collaborative skills.

The steps are all outlined in the link above. A new issue should be opened on the operation's project to ensure the retrospective is completed.

### Iterating an Operation

There are multiple reasons to iterate over past/completed operations - the GitLab environment is changing, new attack techniques are discovered, the Blue Team has improved detection capabilities and want to re-assess those regarding past scenarios/operations, etc.

In those situations, the Red Team can simply clone either a full assessment or an individual campaign inside Vectr. This way, it is possible to iterate over past operations, make appropriate changes to the new versions and continue the cycle described above. Operations may therefore have multiple versions, and Vectr reporting will automatically gather the metrics to show progress over time.

## Red Team Open Scope
Some activities are considered open-scope, meaning that they can be conducted at any time, from any source IP address, and against any GitLab-managed asset without prior approval or notification. The output may or may not be included in the reporting for planned operations, depending on the results and whether or not it is helpful to the Blue Team.

This includes:

- Port scanning.
- Web crawling and scraping.
- Manually and programmatically querying the GitLab API.
- Accessing and cloning any public projects, issues, snippets, etc. on www.gitlab.com.
- Accessing other data intended to be open to the public, such as logging platforms.
- Attempting to log in to any publicly-exposed administrative interface with common and default credentials.
- Attempting to validate credential data such as GCP service accounts, SSH keys, and API keys found in public locations.

If these activities are detected by SecOps, they should be treated as potentially malicious and acted upon appropriately. Unless part of a planned operation, there should never be an assumption that suspicious behaviour is a Red Team activity.

Conducting open-source intelligence (OSINT) gathering against non-GitLab managed assets, such as social media sites, is also considered open-scope and may be conducted outside of planned operations.

If an open-scope activity uncovers a vulnerability that puts GitLab at immediate risk of compromise, SecOps will be notified via the official paging procedures.

## Red Team Office Hours
Every two weeks the Red Team will host Red Team Office Hours. This meeting will be open to the entire company and will alternate between EMEA and APAC friendly times. For the most part these will be an open discussion with members of the Red Team but we will also use this time to perform "read outs" of recently completed Red Team Operations. Note that in some cases, depending on the content these will not be recorded or made public. 
