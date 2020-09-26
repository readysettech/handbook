---
layout: markdown_page
title: "Usecase: DevSecOps"
---


## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

#### Who to contact

|     Product Marketing    |    Technical Marketing    |
| ------------------------ | ------------------------- |
| Cindy Blake ( @cblake )  | Fernando Diaz ( @fjdiaz ) |

# The Market Viewpoint

## DevSecOps

The DevSecOps usecase is applicable for customers who are trying to "shift left" to find security vulnerabilities earlier within their DevOps methodology but have not been able to achieve expected results.

Application Security is hard when security is separated from your DevOps flow. Security has traditionally been the final hurdle in the development life cycle. Iterative development workflows can make security a release bottleneck. Customers don't have enough security people to test all of their code, and hiring more security analysts won't automatically reduce the friction between app sec and engineering teams. Only testing major releases, or limiting tests to certain apps, leaves weak spots hackers can exploit. They need a way to balance risk and business agility. Instead of waiting for security at the end of the development process, they want to include it within their DevOps workflow. Often this is referred to as DevSecOps.

DevSecOps integrates security controls and best practices in the DevOps workflow. DevSecOps automates security and compliance workflows to create an adaptable process for your development and security teams.

### Why is DevSecOps needed?

Balancing business velocity with security is possible. With GitLab, DevSecOps architecture is built into the CI/CD process. Every merge request is scanned through its pipeline for security issues and vulnerabilities in the code and its dependencies using automated tests. This enables some magic to happen.

### Benefits of DevSecOps

Every piece of code is tested upon commit for security threats, without incremental cost.
The developer can remediate now, while they are still working in that code, or create an issue with one click.
The dashboard for the security pro is a roll-up of vulnerabilities remaining that the developer did not resolve on their own.
Vulnerabilities can be efficiently captured as a by-product of software development.
A single tool also reduces cost over the approach to buy, integrate and maintain point solutions throughout the DevOps pipeline.

### Personas

#### User Persona

Users include both the developer and the security pro. We pride ourselves on having a united view of the software vulnerabilies and their status toward resolution.

**The Developer** uses GitLab primarily within the MR pipeline report

The developer cares about security but does not want to become a security expert. Their primary driver to write secure code is to protect their personal/professional reputation. They don't want to be the one that brings their company down via vulnerable code that they wrote. At the same time, they are goaled mostly on quickly turning out code that meets their users' requirements. Often they are not measured on security flaws. Security can seem like a necessary nuisance. Tools that fit within their workflow, without context-switching are most acceptable. The clarity GitLab provides by reporting vulnerabilities at code commit is helpful.

**[Sam the Security Analyst](/handbook/marketing/product-marketing/roles-personas/#sam-security-analyst)** uses GitLab primarily in the Security Dashboard

The security pro cares most about managing risk to the enterprise/agency. They take a broad view of process looking for process improvement areas to reduce risk and avoid repeat mistakes. Because they care about risk, they want to identify unresolved vulnerabilities, their severity, and their remediation status. They care about trends over time and aggregate improvements. Often their metrics are mean time to remediation. It is rare that the security person themselves is able to remediate a software security flaw; they depend upon the developer to do this. This goal misalignment is often a reason for contention between the groups. In traditional app sec environments, where testing is done at the end of the SDLC, they may spend alot of their time tracking and reporting vulnerability statuses, vetting findings, and triaging to dev teams. Where development is more automated, they may be able to focus more on setting policies and allowing the tools to enforce them. They often want to avoid moving any new critical/high vulnerabilities into production and favor breaking the build to enforce this.

#### Buyer Personas

**The Security Manager or CISO (Sam's boss) is usually the buyer**

While developers and DevOps teams like to use GitLab for security, the security pro is often skeptical, comparing it to their favorite incumbant scanner. They may have bet their career on justifying a very expensive scanner like Fortify or Veracode and are often reluctant to replace it, even if it can simplify their work as well as that of the developer.

## Industry Analyst Coverage

Examples of comparative research for this use case are listed just below. Additional research relevant to this use case can be found in the [Analyst Reports - Use Cases](https://docs.google.com/spreadsheets/d/1vXpniM08Ql0v0yDd22pcNmXpDrA-NInJOwj25PRuHXA/edit#gid=0) spreadsheet.

It is important to note whether or not we have reprint rights for a piece of content. When we do, there will be two links. One is direct link to the content that you can download and share. The other link is to the gated page. Please use this link for lead generation activities. If we do not have reprint rights, you will get a link to an internal company document that you may use for your education but you may NOT share with customers, prospects or partners.

GitLab has reprint rights to the following document:
- Direct link: [Gartner Magic Quadrant for Application Security Testing, 2020](https://www.gartner.com/reprints/gitlab-inc-flex?id=1-1Z8WKB1C&ct=200615&st=sb)
- Gated link: [Gartner Magic Quadrant for Application Security Testing, 2020](https://about.gitlab.com/resources/report-gartner-mq-ast/)

Please note that GitLab does NOT have reprint rights for these two reports, so please do not share these with customers, prospects, or partners.
- [Gartner - AppSec Testing Hype Cycle 2019](https://drive.google.com/file/d/1UOXO8YisjpBLFfdwQTDnJFhtjZf5LcJR/view?usp=sharing)
- [The Forrester Wave™: Software Composition Analysis, Q2 2019](https://drive.google.com/file/d/1gBJWRLRQv1NK1xXQQxvejo2hK7Y1TGgm/view?usp=sharing)


## Market Requirements (in priority order)

| Market Requirements | Description | Typical capability-enabling features | Value/ROI |
| ------ | ------ | ------ | ------ |
| Scan results for the Developer | For developers to find and fix vulnerabilities while they are coding, vulnerability scan results must be made available to the developer within their native workflow. Findings that can be automatically corrected should use automation to apply a fix and test the results. | Incremental scanning for rapid, iterative scans. Integrate scan results into the CI pipeline. Auto Remediation to automatically create a fix, eliminating developer effort.  | Allows security flaws to be fixed early, when less expensive, removes context-switching, and minimizes risk by preventing vulnerabilities from reaching production. |
| Application Security Testing of code and components | Often referred to as Software Composition Analysis (SCA), it tests all code components (custom code and open source), wherever it resides (e.g. within containers). The GitLab survey shows Dependency scanning is most frequently used scan type. | SAST, Dependency Scanning, Container scanning, Secrets Detection, and (optionally) License Compliance | Reduces security and compliance risks.|
| Application Security Testing of running app | Scans that look for vulnerable code behavior as the code executes.| DAST, IAST, Input Fuzzing, UEBA/Threat modeling, Mobile app sec testing | Reduces security and compliance risks. |
| Security Governance | The solution automatically applies security policies against code to ensure that only appropriate risks are taken. Application vulnerabilities, repesenting risk, are tracked, managed, and reported. The solution enables routine assessments of security practices to evaluate for risk, compliance, audit and process improvement opportunities (usually for education purposes). |  Security policy automation, Risk and compliance reporting, Audit reporting, Variety of security metrics and process reporting, Vulnerability database and management | Efficiently monitor, manage and mitigate risk. Ability to identify exceptions and refine policies over time. |
| Security guardrails (Preventative - Pre CI/CD) | Preventative Application Security uses guardrails to help teams consistently build things that are secure from the start. | Spell-check-like functionality that identifies insecure phrases as the developer types, bill of materials that limit developer choices to pre-approved code libraries, and auto-discovery that catalogs all third party code. | Prevents creating new vulnerabilities. |
|Works with existing and diverse tools| Security scanners must integrate into an existing environment that may use third party CI and/or security scanners. | APIs and Plug-ins | Allows continued use of existing investments and avoids a rip-n-replace scenario. |

More detailed breakdown may be found on output tab of [Use Case Requirements Discussion](https://docs.google.com/spreadsheets/d/1s3O1M5ZsWfVZxRdPyh98FR9pt4z44fpZYV2b6ySN6WI/edit?ts=5ea764e0#gid=1435219921)

# The GitLab Solution

## How GitLab Meets the Market Requirements

GitLab DevSecOps use case overview
<figure class="video_container">
<iframe width="560" height="315" src="https://www.youtube.com/embed/fPLEWnI4k6k" frameborder="0" allow="accelerometer; autoplay;  encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</figure>


| Market Requirements | How GitLab Delivers | GitLab Category | Demos |
| ------ | ------ | ------ | ------ |
| Scan results for the Developer | Incremental scanning for rapid, iterative scans. Integrate scan results into the CI pipeline. Auto Remediation to automatically create a fix. | CI (for [MR pipeline](https://docs.gitlab.com/ee/user/application_security/)), [Auto remediation](https://docs.gitlab.com/ee/user/application_security/#solutions-for-vulnerabilities-auto-remediation) | [![Adding Security to your CICD Pipeline](../../images/youtube_social_icon_red-32x23.png) Adding Security to your CICD Pipeline](https://youtu.be/Fd5DhebtScg) |
| Application Security Testing of code and components | SAST, Dependency Scanning, Container scanning, Secrets Detection, and License Compliance | [SAST](https://docs.gitlab.com/ee/user/application_security/sast/), [Dependency Scanning](https://docs.gitlab.com/ee/user/application_security/dependency_scanning/), [Container scanning](https://docs.gitlab.com/ee/user/application_security/container_scanning/), [Secrets Detection](https://docs.gitlab.com/ee/user/application_security/secret_detection/#:~:text=GitLab%2011.9%20includes%20a%20new,Security%20Dashboard), and [License Compliance](https://docs.gitlab.com/ee/user/compliance/license_compliance/) | [![SAST and Secret Detection](../../images/youtube_social_icon_red-32x23.png) SAST and Secret Detection](https://youtu.be/8sOjvlkl8QY)<BR>[![Dependency scanning](../../images/youtube_social_icon_red-32x23.png) Dependency scanning](https://youtu.be/39RvTMLDszc)<BR>[![Container scanning](../../images/youtube_social_icon_red-32x23.png) Container scanning](https://youtu.be/wIcaSerMfFQ)<BR>[![License compliance](../../images/youtube_social_icon_red-32x23.png) License compliance](https://youtu.be/42f9LiP5J_4) |
| Application Security Testing of running app | GitLab uses its review app, spun up during CI, to run dynamic application security tests. Recent acquisitions will provide multi-dimensional fuzz testing, useful for API scanning. Mobile app sec testing can be performed on any app within our language scanning capabilities | [DAST](https://docs.gitlab.com/ee/user/application_security/dast/), [Input Fuzzing](https://about.gitlab.com/direction/secure/fuzz-testing/fuzz-testing/), Mobile app sec testing (partners needed) | [![DAST](../../images/youtube_social_icon_red-32x23.png) DAST](https://youtu.be/9tIrrByOum4) |
| Security Governance | Security Policy Automation, Compliance Assessment, Security Risk Assessment, Audit Assessment, Security Process Improvement/ Assessment, Vulnerability Management, Vulnerability Database,  | [Security Dashboards](https://docs.gitlab.com/ee/user/application_security/security_dashboard/), [Vulnerability Management](/handbook/engineering/security/vulnerability_management/), [Audit events](https://docs.gitlab.com/ee/administration/audit_events.html) [Compliance Management](https://about.gitlab.com/direction/manage/compliance-management) | [![Managing Vulnerabilities with the Security Dashboard](../../images/youtube_social_icon_red-32x23.png) Managing Vulnerabilities with the Security Dashboard](https://youtu.be/t-3TSlChHy4) |
| Security guardrails (Preventative - Pre CI/CD) | GitLab provides bill of materials showing dependencies. We do not yet use this to limit developers to use only pre-approved dependencies | [bill of materials feature](https://docs.gitlab.com/ee/user/application_security/dependency_list/) | videos coming soon |
| Works with existing and diverse tools | GitLab allows the integration of external CI tools to run alongside GitLab's CI enabling Jenkins users to also use GitLab Secure capabilities. Similarly, users may have invested in third party security scanners or may require another scanner for a language not covered by GitLab. We have made it easier for third party scanners to integrate into the GitLab MR and the security dashboards. | CI (for [MR pipeline](https://docs.gitlab.com/ee/user/application_security/)), [Security Dashboards](https://docs.gitlab.com/ee/user/application_security/security_dashboard/) | [![Using GitLab Application Security Capabilities with Jenkins](../../images/youtube_social_icon_red-32x23.png) Using GitLab Application Security Capabilities with Jenkins](https://youtu.be/8VoxulxxM4Y) |

## Top Differentiators

| Differentiator | Value | Proof Point  | Demos |
|-----------------|-------------|---------------|
| **Scans performed on feature branch before code is merged with the scan results in MR pipeline** | GitLab performs security scans like SAST, license compliance, dependency scanning before the code is merged - giving Developers opportunity to identify and fix security vulnerabilities before they context switch to other activities. This improves cycle time and development costs as the time and cost to resolve defects and vulnerabilities exponentially increase the later it is detected in the development cycle | [Gartner - Integrating Security Into the DevSecOps Toolchain](https://www.gartner.com/doc/3975263) explains how Security should be included in the DevSecOps lifecycle in small actionable steps that developers can take action on quickly & integrating into defect tracking workflow to match the pace of security fixes to the pace of development. | **-** |
| **Apply security policy & gating within the MR pipeline** | Bring Development and Security Teams closer by allowing security teams to apply organizational security policies before hand and review/approve security exceptions before the code is merged | **-**  | **-** |
| **Streamlined Auditing** | GitLab provides a single source of truth for Dev, Sec and Ops through a single data-store. Everything is audited and for every change, there is a single thread that contains the full audit log of every decision and action - making audit compliance a breeze | The auditor for [Glympse](/customers/glympse/) observed that the company had remediated security issues faster than any other company that he had worked with before in his 20-year career. Within one sprint, just 2 weeks, Glympse was able to implement security jobs across all of their repositories using GitLab’s CI templates | **-** |
| **Offline Environments** | GitLab provides a variety of scanners to run in offline or limited connectivity environments. This feature enables security vulnerabilities to be detected in code that lies in offline environments. | **-** | [![Running GitLab Security Scans in Limited Connectivity and Offline Environments](../../images/youtube_social_icon_red-32x23.png) Running GitLab Security Scans in Limited Connectivity and Offline Environments](https://youtu.be/FoLmRvTcOAY) |

### What Are The GitLab Advantages?

**Contextual**. Unlike traditional application security tools primarily intended for use by security pros, GitLab secure code capabilities are built into the CI/CD workflows where the developers live. We empower developers to identify vulnerabilities and remove them early in the development cycles. While at the same time, providing security professionals a dashboard to view items not already resolved by the developer, across projects. This contextual approach helps each role deal with items that are most important and most relevant to their scope of work within the delivery process.

**Congruent with DevOps processes**. GitLab secure capabilities support the decision-makers, within their natural workflow. Reports are interactive, actionable, and iterative and most important immediate and relevant to changes made. Developers immediately see the cause and affect of their own specific changes so they may iteratively address security flaws alongside code flaws.
Integrated with DevOps tools. When triaging vulnerabilities, users can confirm (creating an issue to solve the problem), or dismiss them (in case they are false positives or there are compensating controls). When using GitLab, no additional integration is needed between app sec and ticketing, CI/CD, etc.

**Efficient and automated**. Eliminates mundane work wherever possible. Auto remediation applies patches to vulnerable dependencies and even re-runs the pipeline to evaluate the viability of the patch.

## [Message House](./message-house/)

The message house for the use case provides a structure to describe and discuss the value and differentiators for the use case.

## Competitive Comparison

See how we [compare against other Security tools](https://about.gitlab.com/devops-tools/)

See how we compare against [GitHub's roadmap for Security](https://about.gitlab.com/devops-tools/github/GitLab-vs-GitHub-Security-Roadmap-Comparison.html)

## Key Value by tier

### Free

**Why choose Gitlab free for DevSecOps?** Security matters to everyone, and we're committed to lowering the barriers to a fully secure, compliant SDLC. That's why we've migrated Brakeman SAST scanning to Core, allowing every Rails developer—at every product tier—to scan their source code for known vulnerabilities.

**Key DevSecOps features with Free tier:**
* SAST for Rails.  Static Application Security Testing (SAST) helps prevent security vulnerabilities by allowing developers to easily identify common security issues as code is being contributed, and mitigate them proactively. As part of our community stewardship commitment, we are making our Rails SAST analyzer (Brakeman) available in every GitLab tier. This will allow ALL GitLab users developing in Rails to leverage SAST Security Scans for their projects. We will continue to move other open source (OSS) SAST analyzers to Core. You can follow our SAST to Core epic to see when other analyzers will become available, and contribute to this effort.

### Ultimate/Gold

**Why choose Gitlab Ultimate/Gold for DevSecOps?** Achieve advanced DevOps maturity with enterprise-level application security capabilities.
* [GitLab Secure](https://docs.gitlab.com/ee/user/application_security/) helps you shift left to enable developers to find and fix vulnerabilities early.
* Multi-faceted scanning includes SAST, DAST, Container and Dependency scanning, Secrets Detection, and License Compliance checks, all within the GitLab Merge Request CI Pipeline with results provided to the developer at the point of code commit. Vulnerability findings are actionable and provide remediation advice while the developer is still working on the code.
* Security dashboards at the project, group, and instance level provide visibility into application risks earlier in the SDLC.

In addition, enjoy these benefits of Ultimate/Gold:
* Enterprise-grade priority support, including 24/7 uptime support, a named Technical Account Manager (TAM), and live upgrade assistance are all still included with Gold/Ultimate.
* Embed security and compliance into your CI Pipelines.
* Protect your IP and get access to free guest users.

**Key DevSecOps features with Ultimate/Gold:**

* [Static Application Security Testing](https://docs.gitlab.com/ee/user/application_security/sast/) - check for potential security issues by evaluating static code.
* [Secrets Detection](https://docs.gitlab.com/ee/user/application_security/secret_detection/) - avoid exposing secrets and credentials for potential exploit.
* [Dynamic Application Security Testing](https://docs.gitlab.com/ee/user/application_security/dast/) - analyze review applications to identify potential security issues.
* [Dependency Scanning](https://docs.gitlab.com/ee/user/application_security/dependency_scanning/) - evaluate third-party dependencies to identify potential security issues.
* [Container Scanning](https://docs.gitlab.com/ee/user/application_security/container_scanning/) - analyze Docker images and check for potential security issues.
* [Security Dashboard](https://docs.gitlab.com/ee/user/application_security/security_dashboard/) - visualize security status for projects.
* [Vulnerability Management](/handbook/engineering/security/vulnerability_management/)
* [Security Approvals in Merge Requests](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html#security-approvals-in-merge-requests)(available in Premium)
* [License Compliance](https://docs.gitlab.com/ee/user/compliance/license_compliance/index.html) - identify the presence of new software licenses included in your project and track project dependencies. Approve or deny the inclusion of a specific license.
* [Compliance Dashboard](https://docs.gitlab.com/ee/user/compliance/compliance_dashboard/index.html) - See if merge requests were approved, and by whom.


## Technology Partnerships

We partner with key industry vendors to extend GitLab's ability to address customer needs and fulfil the market requirements.

One of the first partners to [integrate their scan results](https://docs.gitlab.com/ee/development/integrations/secure.html) into the GitLab Security Dashboard and the GitLab CI pipeline is [WhiteSource](www.whitesource.com).

To extend scanning language support to [nearly 200 additonal languages](https://www.whitesourcesoftware.com/whitesource-languages/) and deeper dependency insight, [WhiteSource](https:://www.whitesource.com) integrates with GitLab and provides a seamless experience for developers to improve the secuirty of their code.  Learn more about [how to integrate WhiteSource into GitLab](https://www.whitesourcesoftware.com/gitlab/) and [more](https://about.gitlab.com/blog/2020/01/14/whitesource-gitlab-security-integration/);

You can also watch [![Dependency Scanning with GitLab and WhiteSource](../../images/youtube_social_icon_red-32x23.png) Dependency Scanning with GitLab and WhiteSource](https://www.youtube.com/watch?v=yJpE_ACt9og) to get started.

If you or your customer has a third party they'd like to see integrated into GitLab, send them to the [partner integration page](https://about.gitlab.com/partners/integrate/) for instructions.


# Selling the DevSecOps Solution

## Customer Facing Slides
* [Security customer presentation](https://docs.google.com/presentation/d/1WHTyUDOMuSVK9uK7hhSIQ_JbeUbo7k5AW3D6WwBReOg/edit?usp=sharing)

## Discovery Questions

The suggested discovery questions below are meant to help you uncover opportunities when speaking with prospects or customers who are not currently using GitLab for Secure/Defend. They are grouped by topic or entry point. **Don’t try to use them all, just those most relevant to your customer.**  The deeper you can dig into their processes, the more benefits you are likely to show of using GitLab. Feel free to contribute!

**Initial probe for direction. Where’s the pain?**

Integrating application security testing into Agile DevOps software development is difficult with many potential challenges. Use these 6 questions to probe a bit to see which areas are of most concern, then go deeper on those topics further below.

1. Finding security vulnerabilities -  Can your security scans keep up with your iterative coding velocity? How often are projects stopped waiting for a security scan?
2. Collaboration /visibility - Is there friction between dev and sec? Can you see security risks at any point in the SDLC?
3. Remediation - How much time is wasted translating what was found by sec to what needs to be done by dev and tracking if it was done? Can you quickly see the status of security remediations?
4. Managing Risk in a DevOps environment -  What percentage of code are you currently scanning? Are there holes where an attacker could more easily enter and then traverse laterally? How much more would it cost you to scan all of your code?
5. Policy Automation - Are Security policies automated with security requirements built into the development process? Or are most projects secured a bit differently every time?
6. Tools - Is your organization investing to improve application security in the short term or long term? Is there a clearly defined strategy or timeline? Are you working to integrate app sec tools into the DevOps tool chain?

**1. Finding security vulnerabilities**

* How often do you rely on pen testing as your primary means of finding vulnerabilities? (indicates little automation; our out-of-the-box scanning can get them started quickly)
* Have you automated app sec testing within your DevOps process? Can you tell me more about this?
* What application security scans are most important to you? (SAST, DAST, IAST, dependency scanning, container scanning, secrets detection, license compliance? Mobile app testing? Fuzz testing?) Would you like to be able to run multiple types of scans for defense in depth? If you are not today, what prevents it?
* What steps have you taken to enable developers to find and fix vulnerabilities themselves? Are the scan results in the CI pipeline?
* How valuable would it be if your developers could find and fix more vulnerabilities themselves before the code ever leaves their hands?
* If you are using a security ‘spell-checker’ to aid developers, how effective is it? Are you still finding vulns with static testing after the code is merged? (the point is this alone is not enough)

**2. Collaboration /visibility**

* Are projects delayed due to inefficient handoff between teams, lack of visibility across systems, or lack of planning and consideration?
* Is time lost translating or reconciling between security tool findings, planning/development tools and issue tracking?
* Is there tension between responsibility for security and ability to improve it?
* How might your process be simplified if there were a single source of truth for both security and development to find and manage vulnerabilities?
* Can vulnerabilities be easily tracked by both developers and security to see where they reside in the code, who created them, action taken (issue created, dismissed, unresolved), and their remediation status? How time consuming is it to get this information?

**3. Efficiency of remediation**

* How many steps are required before vulns get to a developer who can remediate? How much time is wasted on these steps between development and security?
* What percentage of vulnerabilities do you think could be remediated by the developer right away if found while they were still working on the code? If it were more, would it save you time and money?

**4. Managing Risk**

* Are you mostly concerned about the OWASP Top 10. What if you could find the OWASP Top 10 for every code change and free your development workflow by decluttering their tasks to focus on vulns they just created and not technical debt from past efforts to avoid creating new technical debt? Would that help you avoid new technical debt and reduce risk?
* Do you focus on remediation of critical and high vulnerabilities? How much of your remediation is for medium and low vulns? Did you know that most exploits are against medium risk vulnerabilities? What if you could help developers find and fix each vuln as they are created?
* What percentage of code are you currently scanning? Are there holes where an attacker could more easily enter and then traverse laterally? How much more would it cost you to scan all of your code?
* If you are using containers, orchestrators, and/or microservices/API’s, how are you scanning them for vulnerabilities and monitoring them during production?
* What percentage of vulns found that require remediation are actually remediated? How quickly? (Mean time to remediation)
* Can you see how developers handled vulnerabilities that were found? Would it be valuable to have visibility into vulnerabilities and their risk earlier in the lifecycle? Would this help you with security audits?
* How much of the security team’s time is spent tracking vulnerabilities, triaging them, and following up to see that they were remediated?

**5. Policy Automation**

* Does automation enforce security standards? Are Security policies automated with security requirements built into the development process? Or are most projects secured a bit differently every time? How much manual intervention is needed?
* How difficult is it to evaluate compliance with policies and drift/exceptions?
* Compliance should be regularly evaluated and exceptions reviewed. Automating overly rigorous policies may prove detrimental to business objectives and may not be realistically achieved, so it is important to find a balance between compliance and efficiency.
   * Do you have Visibility into access control, reporting, and change logs?
   * Do you know how often policy exceptions are granted?

**6. Tools**

* How many different security tools are you using (which ones?)
* Have you integrated your security tools into your CI pipeline so that security scans run automatically or are they kicked off manually? Are the integrations fragile? Complex? Time consuming? How often does that process need to be updated? How much effort is required to set up for a new project? How do you ensure the scans are applied consistently? How often is your planned work interrupted to fix or maintain your security integrations?
* Which of your security scans are able to provide vulnerability findings directly to the developer? Can you scan a feature branch? (before code is merged) Are you able to see the line of code and which developer created the vulnerability? Do vulnerabilities automatically initiate a work ticket/issue creation?
* Have your teams run into roadblocks or hurdles automating security tests within the CI pipelines at scale?
* How predictable is the cost of your app sec tools? If you find more vulnerabilities, or test more apps, does it cost you more?

## Potential Objections

**I have an incumbent tool. How does your scanning compare?**

 GitLab scanners use a combination of proven open source scanners and proprietary scanners.

Finding vulnerabilities is important, but what you do with the results is equally important. Consider:
* Are your developers able to see vulnerabilities he/she created with every code commit or at least before merging their code with others?
* Are the scan findings actionable for the developer, within their native workflow?
* Is plugin management and compatibility an ongoing concern?

Also, how predictable is the cost of these tools? If you find more vulnerabilities, or test more apps, does it cost you more? Are you essentially penalized for more testing? How does that work with DevOps breaking apps into microservices and running more frequent pipelines? In fact, Gartner even called us out in a report on how to set up an AppSec program inexpensively ([7 Tips to Set Up an Application Security Program Without Breaking the Bank](https://www.gartner.com/document/3986206)).

**If using Fortify, Veracode or Synopsys**
* Do your scan times keep up with or inhibit software iteration?
* Are you able to scan every code change?
* Are you overwhelmed by the number of findings? Do they all get remediated? If not, how do you prioritize and how much time/effort is required? What if the developer could prioritize, using the same guidelines as security, and fix vulns as he/she created them?
* Are you able to afford scanning all of your code?

**If using Snyk, WhiteSource or other point solutions**
* How are you scanning API’s and containers? Are you able to monitor them in production?
* Are you scanning all of your code? At every commit? Does the developer have all of the information they need for remediation?

**If using GitHub Actions and/or Azure DevOps**
* How much effort is required to set up your security scans for every project?
* How difficult is it to enforce policies/standards for security scanning in every project/pipeline?
* GitHub offers a free security testing option as part of its development environment. Yes, only for public repositories, and only in a beta form that is invite only

**The Gartner Magic Quadrant for AST placed GitLab as a niche player. Does that mean your security scanners are not as good as the other vendors?**

Our placement has nothing to do with the efficacy of our scanners. [GitLab is a niche player](https://about.gitlab.com/resources/report-gartner-mq-ast/) because our security scanning capabilities are best used by people using GitLab for CI. We have [demonstrated](https://www.youtube.com/watch?v=8VoxulxxM4Y) that people using GitLab for SCM and Jenkins for CI can still use GitLab’s security testing, however if you are not using GitLab for SCM nor for CI, it probably makes little sense for you to use GitLab for AST as a standalone app sec tool.

**I can’t justify the cost difference for Ultimate.**

NIST [demonstrated the cost savings](https://www.nist.gov/document/report02-3pdf) from shifting security left back in 2002. How far left are you currently? Hypothetically, if 50% of your vulnerabilities could have been found by the developer and if half those could hypothetically be fixed before the code ever leaves the developer’s hands, what value would that have for your cost and your risk exposure? Let's consider the potential benefit of:
* 25% less vulns to prioritize, vet, triage, and track
* 25% fewer vulns with their associated risk exposure
* 25% less opportunities to stop business innovation for security flaws
What if even more could be found and fixed by dev?

How predictable is the cost of other app sec tools? If you find more vulnerabilities, or test more apps, does it cost you more? Are you essentially penalized for more testing? How does that work with DevOps breaking apps into microservices and running more frequent pipelines? What is the value of scanning every code change going forward? What is the impact on your technical debt over time? What would it cost you with your other tools to scan every software change?


## Industry Analyst Relations (IAR) Plan
- The IAR Handbook page has been updated to reflect our plans for [incorporating Use Cases into our analyst conversations](/handbook/marketing/product-marketing/analyst-relations/#how-we-incorporate-use-cases-into-our-industry-analyst-interactions).
- For  details specific to each use case, and in respect of our contractual confidentiality agreements with Industry Analyst firms, our engagement plans are available to GitLab team members in the following protected document: [IAR Use Case Profile and Engagement Plan](https://docs.google.com/spreadsheets/d/14UthNcgQNlnNfTUGJadHQRNZ-IrAe6T7_o9zXnbu_bk/edit#gid=1124037301).

For a list of analysts with a current understanding of GitLab's capabilities for this use case, please reach out to Analyst Relations via Slack (#analyst-relations) or by submitting an [issue](https://gitlab.com/gitlab-com/marketing/product-marketing/issues/new) and selecting the "AR-Analyst-Validation" template.

## Proof Points - customers

### Quotes and reviews

GitLab customer, HERE, [shares their experience](https://developer.here.com/blog/shifting-security-left-in-the-here-platform) with using GitLab to Shift Left

GitLab customer, Arctic Engine, [shares their experience](https://about.gitlab.com/blog/2020/08/19/arctic-engine-fuzz-testing-blog/) with using GitLab's fuzz testing to find unknown vulnerabilities.

#### Gartner Peer Insights

*Gartner Peer Insights reviews constitute the subjective opinions of individual end users based on their own experiences, and do not represent the views of Gartner or its affiliates. Obvious typos have been amended.*

"GitLab Application Security Testing helps to analyze our source code for vulnerabilities, listed in GitLab Security Dashboard. It is easily configurable with Docker setup. It shows the complete vulnerabilities report immediately after a new merge request is created within a project. With listing potential risks in code, it also prioritizes vulnerabilities in terms of critical, high, low, medium which helps team to plan and focus on what first."
> * Sr. Software Engineer, [Gartner Peer Insights Review](https://www.gartner.com/reviews/market/application-security-testing/vendor/gitlab/product/gitlab/review/view/1307149)

"The Application testing feature of [GitLab] is very useful in scanning for vulnerabilities in the applications. There are multiple test[s] available. We mostly use the tools to scan the docker containers, dependencies, source code and web application for the vulnerabilities."
> * Native Android Application Developer, [Gartner Peer Insights Review](https://www.gartner.com/reviews/market/application-security-testing/vendor/gitlab/product/gitlab/review/view/1320427)

### Customer Case Studies

* **[Glympse](/customers/glympse/)**
* **Problem** A complex developer tech stack with over 20 distinct tools that was hard to maintain and manage. Teams spent several hours a week keeping tools running rather than shipping innovation to their app.
* **Solution:** GitLab Ultimate (SCM, CI, DevSecOps)
* **Results: ~20 tools consolidated into GitLab and remediated security issues faster than any other company in their Security Auditor's experience.
* **Sales Segment:** SMB

* **[BI Worldwide](https://about.gitlab.com/customers/bi_worldwide/)**
* **Problem:** Had a large legacy codebase that was created years ago. Looking to eliminate (or at least significantly reduce) manual testing and manual deployments to their on-premise infrastructure.
* **Solution:** GitLab Ultimate (SCM, CI, DevSecOps)
* **Results:** **10x daily deployments** Simplified their toolchain and migrated from their previous Git tools to GitLab. Saw an immediate improvement of collaboration and release pace as a result of their move to GitLab.
* **Sales Segment:** Mid-Market

* **[Chorus](https://about.gitlab.com/customers/chorus/)**
* **Problem:** The founders of Chorus built the tool from the beginning using GitLab.
* **Solution:** GitLab Ultimate (SCM, CI, DevSecOps)
* **Results:** **6 week production cycles reduced to 1 week** During a recent audit for SOC2 compliance, the auditors said that Chorus had the fastest auditing process they have seen and most of that is due to the capabilities of GitLab.
* **Sales Segment:** SMB

### References to help you close

[SFDC report of referenceable secure customers](https://gitlab.my.salesforce.com/a6l4M000000kDw2) Note: Sales team members should have access to this report. If you do not have access, reach out to the [customer reference team](/handbook/marketing/product-marketing/customer-reference-program/#which-customer-reference-team-member-should-i-contact) for assistance.

## Adoption Guide

The following section provides resources to help TAMs lead capabilities adoption, but can also be used for prospects or customers interested in adopting GitLab stages and categories.

### Playbook Steps

- Start with the first 6 Discover Questions to identify which area to drill into further.

### Adoption Recommendation

There are multiple pathways to adoptiong GitLab's DevSecOps workflow, depending on the current state of the customers' current state. The following diagram shows the adoption sequence and relationship between scenarios.

![Secure Adoption path](/images/handbook/customer-success/adoption-path-secure.png "Secure Adoption Path")

This table shows the recommended use cases to adopt, links to product documentation, the respective subscription tier for the use case.

| Feature / Scenario                                  |    F/C    |   Basic   |    S/P    | G/U  | Notes                      |
| --------------------------------------------------- | :-------: | :-------: | :-------: | :--: | :------------------------- |
| Adopt GitLab Flow                                   |     X     |     X     |     X     |  X   |                            |
| Try / Utilize Auto DevOps                           | *Partial* | *Partial* | *Partial* |  X   |                            |
| Automated Testing with CI                           |     X     |     X     |     X     |  X   |                            |
| Review app                                          |     X     |     X     |     X     |  X   | Run DAST in CI/CD pipeline |
| Merge Request Approval Flow / Rules                 |           |           |     X     |  X   |                            |
| Protected Environments                              |           |           |     X     |  X   |                            |
| Container Registry / Package Repo (When applicable) |     X     |     X     |     X     |  X   |                            |

The table includes free/community and paid tiers associated with GitLab's self-managed and cloud offering.

- F/C = Free / Core
- Basic = Bronze/Starter
- S/P = Silver / Premium
- G/U = Gold / Ultimate

### Additional Documentation Links

- [From SCM and CI to Security](https://docs.google.com/presentation/d/1Oq8znDkHrgGK5Xe5D23SdiRLt33OIJZ30OWCHNNDV14/edit?usp=sharing) *(GitLab internal only)*
- [GitLab Security Compliance Controls](/handbook/engineering/security/security-assurance/security-compliance/sec-controls.html)
- [GitLab Security Practices](/handbook/security/)
- [Security Planning](/handbook/engineering/security/planning/)

### Enablement and Training

The following will link to enablement and training videos and content.

- [Handling Security Audits](https://www.youtube.com/watch?v=ziIJIec4w0g)
- [Application Security at High Velocity](https://www.youtube.com/watch?v=VN6Z6qtlMjg)
- [Adding Security to your pipelines](https://www.youtube.com/watch?v=Fd5DhebtScg&t=3s)

### Professional Service Offers

GitLab offers a [variety of pre-packaged and custom services](https://about.gitlab.com/services/) for our customers and partners. The following are service offers specific to this solution. For additional services, see the [full service catalog](https://about.gitlab.com/services/catalog/).

- [DevOps Fundamentals Training](https://about.gitlab.com/services/education/devops-fundamentals/) (all stages of the DevOps lifecycle)
- [GitLab CI/CD Training](https://about.gitlab.com/services/education/gitlab-ci/)
- [Integration Services](https://about.gitlab.com/services/integration/	)


## Resources

### White paper
* [A Seismic Shift Left](https://about.gitlab.com/resources/downloads/gitlab-seismic-shift-in-application-security-whitepaper.pdf)

### eBook: Ten Steps Every CISO Should Take to Secure Next-gen Applications
* [Gated](https://lnkd.in/er8tjQg)
* [Ungated](https://drive.google.com/file/d/0B-ZpQfvLs-2AVFI5VmNybTBvWWttRWxENWpGVnlNbVBFODNZ/view?usp=sharing)

### Integration with third party commercial scanners
* [WhiteSource](/handbook/marketing/product-marketing/enablement/security-integrations-whitesource/)

### Blogs
* [How application security engineers can use GitLab to secure their projects](https://about.gitlab.com/blog/2020/07/07/secure-stage-for-appsec/)
* [How to capitalize on GitLab Security tools with external CI](https://about.gitlab.com/blog/2020/07/10/jenkins-migration/)

### Other DevSecOps Videos
* [Deep Dive into a Security demo](https://youtu.be/k4vEJnGYy84)
* See how [integration is the key to successful DevSecOps](https://about.gitlab.com/blog/2018/09/11/what-south-africa-taught-me-about-cybersecurity/)

### Related Videos
* [Container Network Security](https://youtu.be/45Q__T42ZMA)

### Clickthrough & Live Demos
* [All Marketing Click Through Demos](/handbook/marketing/product-marketing/demo/#click-throughs)
* [All Marketing Live Demos](/handbook/marketing/product-marketing/demo/#live-instructions)

### Roadmap
* [Secure and Defend Roadmap](https://docs.google.com/presentation/d/16prp0FY0dcP8eWtCbk1K5Mh7j4180oq1Vi3JnJ46Oqo/edit?usp=sharing) (DevSecOps is highlighted in red)

## Technical Resources for Solution Architects

Sometimes customers and prospects have unique requirements, often around using an preferred scanning tool to integrating with some other part of their tool chain. If you or your customer has a third party they'd like to see integrated into GitLab, send them to the [partner integration page](https://about.gitlab.com/partners/integrate/) for instructions. While GitLab can be a single platform to meet all of their needs, often they need an on-ramp to help them transition or proof of the integration before purchasing GitLab. The resources below may help.
**NOTE:** Please do not use these to put GitLab in the position where users expect us to support a 3rdparty product integration that we do not [officially recognize](https://about.gitlab.com/partners/).
* [Using OSS Review as your default License scanner](https://youtu.be/dNmH_kYJ34g)
* [Integrating GitLab with Sonarqube](https://www.youtube.com/watch?time_continue=1&v=OItsDDzIP8g)

## Buyer's Journey
Inventory of key pages in the buyer's Journey

| **Awareness** <br> learning about the problem  |  **Consideration** <br> looking for solution ideas  |  **Decision** <br> is this the right solution|
| ------ | -------- |-------- |
| [topic page?]()  | [solution page]() | [proof points]() |
| [landing pages?]() | ?comparisons?  | [comparisons]() |
| -etc?            |   |  - [product page x]() <br>  - [product page y]() <br>  - [product page z]() |
