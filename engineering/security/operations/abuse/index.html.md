---
layout: handbook-page-toc
title: Trust & Safety Team (former Abuse Operations)
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Vision

Making the internet safer by reducing malicious activity originating from GitLab.com.
 
## Mission

The Trust & Safety team investigates and mitigates the malicious use of GitLab.com and it’s associated features and tools with the goal of making the internet a safer place. In order to achieve this we must ensure that we are good internet citizens. 
 
### Initiatives for this specialty include:

* Detection and mitigation of [abusive activity](#what-is-abuse) on GitLab.com.
* [DMCA Notice and Counter-Notices](#dmca-requests) processing.
* Escalating potential abuse vectors to stakeholders for mitigation.
* Research and prevention trending abuse methodologies.
 
***Code of Conduct Violations*** are handled by the [Community Advocates](/handbook/marketing/community-relations/community-advocacy/) in the [Community Relations Team](/handbook/marketing/community-relations/). For more information on reporting these violations please see the [GitLab Community Code of Conduct](https://about.gitlab.com/community/contribute/code-of-conduct/) page.

## Team Members

The following people are permanent members of the Trust & Safety Team

<table>
<thead>
<tr>
<th>Person</th>
<th>Role</th>
</tr>
</thead>
<tbody>
<tr>
<td>Roger Ostrander</td>
<td><a href="/job-families/engineering/security-engineer">Security Engineer, Trust & Safety</a></td>
</tr>
<tr>
<td>Shawn Sichak</td>
<td><a href="/job-families/engineering/security-engineer">Security Engineer, Trust & Safety</a></td>
</tr>
<tr>
<td>Westley van den Berg</td>
<td><a href="/job-families/engineering/security-analyst">Security Analyst, Trust & Safety</a></td>
</tr>
<tr>
<td>Charl de Wit</td>
<td><a href="/job-families/engineering/security-management">Security Manager, Trust & Safety</a></td>
</tr>
</tbody>
</table>
 
## Work

To bring an issue to our attention please tag `@gitlab-com/gl-security/abuse-team`, or create an issue in the [Trust & Safety](https://gitlab.com/gitlab-com/gl-security/abuse-team/abuse/-/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=). If it is an urgent issue, please reach out on Slack in the `#abuse` channel or by using `@trust-and-safety`. 

## Metrics

**[Trust & Safety Mitigation Dashboards](https://app.periscopedata.com/app/gitlab/642878/WIP:-Abuse-Mitigation-Dashboard)** *(GitLab internal)*

Total accounts mitigated per week
  - Defined as all accounts mitigated for abusive activity or content in a given week (weeks run from Mon to Sun).

Automatic vs Manual
  - Defined as the volume of accounts detected and mitigated via automation vs manual detection (via abuse reports/investigations/monitoring) and mitigation. 

Average Time to Mitigation
  - Time to Mitigation is defined as the date/time between the creation of an abusive account and the date/time of taking administrative action on the account.  

Accounts mitigated per category
  - This is a breakdown of the total accounts mitigated per abuse category.
 
# Trust & Safety Resources
 
## What is Abuse?
Abuse is the intentional misuse of GitLab products/services to cause harm or for personal gain. (Abuse is covered under Section 3 of the GitLab Website [Terms of Use](/terms/#gitlab_com))

### Examples of common forms of Abuse include, but are not limited to:
 
**1. Malware:** Defined as software that is designed and distributed with the intention of causing damage to a computer, server, client, or computer network.

Making use of GitLab.com services to deliver malicious executables or as attack infrastructure is prohibited under the [GitLab Website Terms of Use](/terms/#gitlab_com) (**Section 3, “Acceptable Use of Your Account and the Website”**).
We do however understand that making such technical details available for research purposes can benefit the wider community and as such it will be allowed if the content meets the following criteria:
  - The Group and Project descriptions must clearly describe the purpose and author of the content.
  - Further details about specific project content that can be independently verified by the **GitLab Security** department must be present in the project `README.md` file; for example, links to supporting materials such as a blog post describing the project.
  - All malicious binaries/files are stored in password protected archive files, with the passwords clearly documented; for example, placed in the repository’s `README.md`.
     * Example: https://github.com/ytisf/theZoo
     * `git-lfs` is available for use for binary files on GitLab.com.
  - Non-profit open source projects may meet the requirements to qualify for our [GitLab for Open Source](/solutions/open-source/program/) program.

**2. Commercial Spam:** An account that's been created for the purpose of advertising a product or service.

**3. Malicious Spam:** An account that’s been created for the purpose of distribution of fraudulent, illegal, pirated or deceptive content.

**4. CI Abuse:** Making use of CI Runners for any other purpose than what it is intended for. Examples include, but are not limited to:
  - Cryptocurrency Mining
  - Network Abuse (Denial of Service, Scraping, etc.)


**5. Prohibited Content:** Distributing harmful or offensive content that is defamatory, obscene, abusive, an invasion of privacy or harassing.
  - For any reports of Child Sexual Abuse Material (CSAM) please notify [INHOPE](https://www.inhope.org/EN) via the [`Report Content`](https://www.inhope.org/EN#hotlineReferral) button.

**6. GitLab Pages**: Pages Abuse: Include, but are not limited to:
  - Web Spam,
  - Phishing Pages
  - Pages that contain Obscene or Harmful content
 
## How to Report Abuse
You can report abuse on GitLab.com via the `Report Abuse` [button](https://docs.gitlab.com/ee/user/abuse_reports.html) while logged in.
	* Please ensure to include any relevant details pertaining to your report in the text field.
Alternatively you can eMail abuse report to `abuse@gitlab.com`
For DMCA Notices please email `dmca@gitlab.com`
 
## DMCA Requests
 
The Trust & Safety team are responsible for processing Digital Millennium Copyright Act (DMCA) notices. All DMCA requests need to be vetted by Legal first before we proceed with the take down of the reported content. 
 
### For DMCA requests the Abuse Team will follow the below process
 
* Confirm that the content is still live.
* Temporarily remove the content to allow the parties to commence litigation.
* Return the content to the original state if no litigation was commenced.
 
Trust & Safety works in conjunction with Legal referencing the [DMCA Removal Workflow](/handbook/engineering/security/operations/abuse/dmca-removal-requests.html)
 
## Our Mission statement

Be good internet citizens.
 
### How do we achieve this? 

* Be honest and trustworthy
* Follow the rules and laws
* Be informed about the world around you
* Respect the property of others
* Be active in the community
* Be compassionate
* Be a good neighbour
* Protect the GitLab environment
* Respect the rights of others
* Take responsibility for your actions
 
