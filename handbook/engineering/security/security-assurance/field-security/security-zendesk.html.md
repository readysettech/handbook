---
layout: handbook-page-toc
title: "Security ZenDesk Process"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Security ZenDesk Process

The Field Security team triages and responds to ZenDesk tickets that come from emails sent to `security@gitlab.com`. Users email with questions and concerns about their accounts and the security of GitLab as a SaaS platform. These emails open tickets in ZenDesk which is monitored by the Field Security team for triage.

Tickets are handled in one of the four ways described below.

## Reply
Field Security has a 1 business-day SLA to handle the ticket. When Field Security has all the required information a friendly, concise, and complete answer to the requestor's concern is provided and the ticket is closed as "Solved". The ticket requestor may reopen the ticket at any time should they require further assistance.

## Engage a subject matter expert (or team)
When additional information is required, an issue is opened for the appropriate team (e.g. Security Operations, Application Security, Abuse, Security Compliance, etc.) and the requestor is notified that additional research on our part is required. These issues are monitored and once the required information has been collected, that information is provided to the ticket requestor and the ticket is closed. Periodic updates are given to the requestor as appropriate.

## Redirect
There are 3 classes of tickets that Field Security cannot handle directly, and these are either forwarded and/or replied with referral information for the requestor:
*  **Support requests.** When account access is lost users often email `security@gitlab.com`. Our Support team has established workflows for lost passwords, 2FA lockouts, blocked accounts, and other issues related to authentication. These tickets can be forwarded within ZenDesk where they are promptly handled by a member of that team.
* **Exploit/vulnerability reports.** GitLab uses our bug bounty program HackerOne.com to track and manage vulnerabilities whereever possible. Reports are triaged there, and bounties paid when applicable. We reply to the ticket with information on the program and a link should they decide to try for the bounty. Vulnerability reports are subject to the terms of our [Resonsible Disclosure Policy](/security/disclosure/). A reporter can always report directly via `security@gitlab.com` if they prefer not to go through HackerOne.
* **Copyright violations.** Under the terms of the Digital Millenium Copyright Act (DMCA) we may not store or distribute material that doesn't belong to the individual(s) responsible for uploading it. As with support requests, we refer the requestor to `dmca@gitlab.com`. Our DMCA policy is publicly available [here](/handbook/dmca).

## Compliance Report Requests
Our [Customer Assurance Package](/handbook/engineering/security/security-assurance/field-security/customer-assurance-package.html) details the process for existing customers to request our SOC 2 Type 1 report and/or pen test reports directly by emailing `security@gitlab.com`. Once we verify their status the request is queued and we respond to confirm receipt. GitLab employees may also request reports through this process, but they must be on behalf of a customer for the SOC 2 report. 

Reports are distributed on Mondays & Thursdays with adjustments for US holidays.

Details about our SOC 2 Security Compliance are available [here](/handbook/engineering/security/security-assurance/security-compliance/soc2.html).

## Additional information

Additional detail about our workflows is available in our [Runbook](https://gitlab.com/gitlab-com/gl-security/field-security/-/blob/master/Projects/SecurityQueue-v2/ZenDesk_Runbook.md). (Internal link.) You can find more information on the Field Security program and our offerings [in our Field Security handbook page](/handbook/engineering/security/security-assurance/field-security).
