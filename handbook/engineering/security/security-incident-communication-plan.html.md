---
layout: handbook-page-toc
title: "Security incident communications plan"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

GitLab takes the security of our clients’ information extremely seriously, regardless of whether it’s on GitLab.com or in a self-managed instance. In keeping with GitLab’s [value of transparency](/handbook/values/#transparency) we believe in communicating about security incidents clearly and promptly. 

This communication response plan aims to map out the who, what, when, and how of GitLab in notifying and engaging with internal stakeholders and external customers on security incidents. This plan of action covers the strategy and approach for security events which have a ‘high’ or greater impact as outlined in [GitLab’s risk scoring matrix](https://gitlab.com/gitlab-com/gl-security/security-assurance/field-security-team/risk-assessments/blob/master/Risk%20Scoring%20Matrix.md#overall-impact).

Security incident communications runbooks are located [here](https://gitlab.com/gitlab-com/gl-security/runbooks/-/tree/master/communications) (internal only).

### What is an incident?
The GitLab Security team identifies security incidents as any violation, or threat of violation, of GitLab security, acceptable use or other relevant policies.  You can learn more about how we identify incidents in the [GitLab security incident response guide](/handbook/engineering/security/sec-incident-response.html#incident-identification).

### Defining the scope/severity of an incident 
The Security Engineer On-Call will determine the scope, severity and [potential impact](https://gitlab.com/gitlab-com/gl-security/security-assurance/field-security-team/risk-assessments/blob/master/Risk%20Scoring%20Matrix.md#overall-impact) of the security incident.   Once the potential impact has been determined, implementation of the appropriate internal and external communications strategy should begin.

## Security incident roles and responsibilities

### Security team roles and responsibilities
**Security Engineer on Call (SEOC):** This is the on-call Security Operations Engineer. The individual is the first to act, validate, and begin the process of determining severity and scope.

**Security Incident Manager on Call (SIMOC):** This is a Security Engineering Manager who is engaged when incident resolution requires coordination across multiple parties. The SIMOC is the tactical leader of the incident response team, typically not engaged to perform technical work. The SIMOC assembles the incident team by engaging individuals with the skills, access, and information required to resolve the incident. The primary focus of the SIMOC is to keep the incident moving towards resolution.

**Communications Manager on Call (CMOC):** This individual will coordinate external communications efforts according to this security incident response plan and liaise across the extended GitLab teams to ensure all parties are activated, updated and aligned.

### Extended team roles, responsibilities and points of contact
**Marketing Programs:** Responsible for sending incident-related email to impacted parties of a security incident. Marketing programs can send these emails through Mail Chimp (users, but not customers) or Marketo (customers and prospects). This group is engaged by creating an issue using the `Email-Request-mpm template` and [pinging team members in `@marketing-programs` in Slack](/handbook/marketing/revenue-marketing/digital-marketing-programs/marketing-programs/emails-nurture/#holiday-coverage-for-s1-security-vulnerabilities-email-communication).

**Marketing Ops:** If a new, custom distribution list needs to be created, Marketing Ops will work closely with Marketing Programs and generate the distribution list for the incident-related email. Contact this group via: `@mktg-ops` in slack. For urgent issues, like a security incident, page the on-call marketing ops via entering `/pd trigger` command in any slack channel and select `Marketing Ops Ext. Comms - Emergency`.

**Support Team:** Using background information and prepared responses provided by the Security Engineer On Call and Communications Manager On Call, our Support Team will triage and respond to customer communications stemming from the security incident. [Contact the on-call manager via `#support_managers` in Slack](/handbook/support/internal-support/#on-slack). If it's urgent [page the Support Manager On-call](/handbook/support/on-call/#paging-the-on-call-manager) using `/pd-support-manager` command in slack.

**Community Advocates:** May need to respond to customers and the general public via social channels, as such should be engaged before public-facing materials are released. Any prepared responses or FAQs should be provided to assist with their interactions. [Contact this group in `#community-advocates` or any Slack channel by pinging `@advocates`](/handbook/marketing/community-relations/community-advocacy/#emergency-contact).

## Communicating internally
Security incidents can be high-pressure, high-stress situations.  Everyone is anxious to understand the details around the investigation, scope, mitigation and more. Ensuring that stakeholders across security, infrastructure, engineering and operations teams are informed and engaged is one of the chief responsibilities of the Security Incident Manager On Call. The Security Incident Manager should focus on providing high-level status updates without delving too deeply into the technical details of the incident, including:
* Current Risk
* Users Impacted (some, many, all?)
* Services Impacted (production, enterprise apps, other)
* Timeline of events
* Mitigation steps that have been taken
* Current status of the incident
* Next steps


### Communicating with GitLab team members
Any time there is a service disruption for team members, the CMOC should post details regarding the disruption and related issue(s) in #whats-happening-at-gitlab, and cross-post in any related channels. It is important to identify if this is a production incident affecting gitlab.com or a service used by the organization.
 
### Incident response channel on Slack
Setting up a public to GitLab incident response Slack channel will be one of the first actions taken by the Security Engineer on Call. This Slack channel will allow for continuous engagement and updates. All security incident team members and extended POCs should be invited.  The link to this channel should also be shared in `#security-department` to increase visibility within Security.

### Key internal stakeholders and when/how to engage

| Group & Contacts | When to Engage | DRI to Engage | At what Cadence | In what Channel |
| ------ | ------ | ------ | ------ | ------ |
| Director of Security, Operations | For high-severity (or higher) incidents | Security Incident Manager on Call | Continuous | In incident response Slack channel |
| VP of Security | For high-severity (or higher) incidents | Security Incident Manager on Call | 30 minute intervals (unless otherwise requested) | Slack direct message |
| Broader e-group | Immediately in cases of a data breach or an RCE with evidence of exploitation | VP of Security | 30 minute intervals (unless otherwise requested) | `#e-group` Slack channel |
| Sr. Director of Corporate Marketing and Director of Corporate Communications | Immediately, if the incident has been publicly reported or if there is a regulatory requirement to make an announcement. In other cases, once the full impact and associated risk has been determined. | Communications Manager on Call | Continuous | In incident response Slack channel |
| Legal | If GitLab EE customers are impacted, or if the security incident includes a data breach including but not limited to: <br> Exposure of PII / Personal Data <br> Private Projects <br> Financial Information | VP of Security | Continuous | incident response Slack channel |

## Communicating externally

External communications should happen as soon as possible after the scope and impact of the security incident is determined, using concise and clear language. The first external communications should always be directed to customers. 

The chart below illustrates the process flow between incident and impact investigation and the communications decisions and actions needed:
```mermaid 
graph TD; 
A[Incident Declared]-->B{Investigate: Scope & Impact}; 
B-->C(Decision: Comms Scope & Frequency); 
C-->D(Decision: Comms Medium);
D-->E(Engage Extended Teams);
E-->F(Investigate: collect contact data);
E-->G(Produce: Comms Content);
G-->H[Send Comms];
H-->G(Produce: Comms Content);
H-->I[All Clear: Final Comms];
```

## Customer messaging

Once it has been determined that a customer alert is needed, the CMOC will identify the appropriate customer alert channel (email, blog, `@gitlabstatus` twitter alert) and begin tracking message development and approvals using the ['Security event communications template'](https://gitlab.com/gitlab-com/gl-security/security-communications/communications/-/blob/master/.gitlab/issue_templates/Security%20event%20communications%20template.md). This template also identifies key stakeholders for contribution, review and approval of the customer communications and should be identified by the CMOC, SEOC and support team.

The Security Engineer on Call (SEOC) is responsible for providing the initial key information summary points around the security event or concern, what action may have already been taken and what may be required on behalf of the customer as well as where to get more information, if needed, as outlined in the linked google doc template within the 'Security event communications template'. The CMOC reviews and edits the customer communication and moves through the review and approvals stages.

### Turnaround on Customer Messaging

Once security communications has been engaged and key stakeholders for contribution, review and approval have been identified, the team should develop, gain approval on a final customer communication and distribute and/or publish within 24 hours. 

### Sync meetings to develop and review customer communications

Key stakeholders for contribution, review and approval will meet synchronously in a Zoom session to create and fine-tune customer communications (emails, FAQs, blog post, etc). Meeting synchronously in this case allows us to expedite the development of communications with key inputs from stakeholders in security, customer support and beyond and quickly move into the review stage.  These zoom sessions are recorded and will be linked into the related security event communications issue.

### On-going, live incidents on GitLab.com

For on-going, live site incidents on GitLab.com, updates are provided by the Communications Manager on Call through status.io to [https://status.gitlab.com/](https://status.gitlab.com/) and the [@GitLabStatus](https://twitter.com/GitLabStatus) twitter handle. 

### Channels and responses for use in a security incident

| Communications Channels | Purpose/Message | Additional Details |
| ------ | ------ | ------ |
| Incident Response Customer Email | Provides incident background, response, potential, impact, follow-up actions, and who to contact with questions. | Drafted by Security Incident Manager on Call and reviewed by Director of Security, Operations and/or VP of Security. Sent by Marketing Program Manager. Sent from [security@gitlab.com](mailto:security@gitlab.com) with reply to [security@gitlab.com](mailto:security@gitlab.com). Should be in **plain text** with **no link tracking**. |
| Mitigation and response blog post | Details the background, GitLab response and any action required by our customers. | If it is determined that a longer, more-in-depth response is needed (i.e. a blog post), the team will follow the Marketing [rapid response process](/marketing/#-marketing-rapid-response-process) in which the Sr. Director of Corporate Marketing is engaged immediately (via slack or text) and proposes the path forward. This includes determining the appropriate channel, response and timing and engaging the appropriate resources across marketing and corporate to collaborate, review and/or be advised of the response (corporate communications, content, community and legal teams). Content for the blog post is provided by the Security Engineer on Call, the content team performs copyedits and the corporate communications and legal teams review and approve message. Once the message is approved, the Security Manager on Call will merge the blog post. **Note: collaboration and work on the response blog post should happen in the related incident response channel on slack.** |
| GitLab Security Release Alert/Email | Indicates required action for customers and links to related mitigation and response blog. | Email sent to opt-in security notices distribution list. Prepared and sent by Communications Manager on Call, Sent to Security Notices distro through Marketo. Users can sign up for this distribution list through our [Communication Preference Center](/company/preference-center/). |
| Customer Frequently Asked Questions (FAQs) | List of early customer questions and responses, or probable questions and responses. | Created by Communications Manager on Call and SecOps Team. Provided to appropriate [Support group](/handbook/support/#channels). |
| Social media post | For distribution of related blog post, details our response to X issue. | Communications Manager on Call engages `@advocates` in the incident response Slack channel. Provides advocates with tweet text and blog link. GitLab social media team should also be alerted for ongoing awareness and monitoring, using `@social` in slack. |

### External statements and other public-facing official communications

Depending on scope, impact or risk associated with the incident, our Corporate Communications and Marketing team may determine that additional outreach is necessary. Any official statements about the security incident would be made by GitLab’s Director of Corporate Communications, Sr. Director of Corporate Marketing, CMO or VP of Security.  
