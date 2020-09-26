---
layout: handbook-page-toc
title: "Security"
---

### On this page

{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Engaging the Security On-Call

If you identified an urgent security issue, if something feels wrong, or you need immediate assistance from the Security Department, you have two options available:

- Slack: use the `/security Hi security, I have a concern! Please see the following URL ...` command.
- Email: send an email with a brief description of the issue to page-security@gitlab.com.

Please be aware that the Security Department can only be paged internally. If you are an external party, please proceed to [Vulnerability Reports and HackerOne](/handbook/engineering/security/#vulnerability-reports-and-hackerone) section of this page.

Both mechanisms will trigger the very same process, and as a result, the Security responder on-call will engage in the relevant issue within the appropriate SLA. If the SLA is breached, the Security manager on-call will be paged. When paging security a new issue will be created to track the incident being reported. Please provide as much detail as possible in this issue to aid the Security Engineer On Call in their investigation of the incident. The Security Engineer On Call will typically respond to the page within 15 minutes and may have questions which require synchronous communication from the incident reporter. It is important when paging security to please be prepared to be available for this synchronous communication in the initial stage of the incident response.

For lower severity requests or general Q&A, GitLab Security is available in the `#Security` channel in GitLab Slack and the Security Incident Response Team can be alerted by mentioning `@sirt-team`. If you suspect you've received a phishing email, and have not engaged with the sender, please see: [What to do if you suspect an email is a phishing attack](/handbook/security/#what-to-do-if-you-suspect-an-email-is-a-phishing-attack). If you have engaged a phisher by replying to an email, clicking on a link, have sent and received text messages, or have purchased goods requested by the phisher, page security as described above.

> **Note:** The Security Department will never be upset if you page us for something that turns out to be nothing, but we will be sad if you don't page us and it turns out to be something.
> _**IF UNSURE - PAGE US.**_

Further information on GitLab's security response program is described in our [Incident Response](./sec-incident-response.html) guide.

## External Contact Information

The security department can be contacted at `security@gitlab.com`. External researchers or other interested parties should
refer to our [Responsible Disclosure Policy](/security/disclosure/) for more information about reporting vulnerabilities. The `security@gitlab.com`
email address also forwards to a [ZenDesk queue](/handbook/support/channels/#security-disclosures) that is monitored by the Field Security team.

For security team members, the private PGP key is available in the Security 1Password vault. Refer to [PGP process](/handbook/security/pgp_process/)
for usage.

## Security Mission and Vision Statements

Our Mission is to be most Transparent Security Group in the world with a results oriented approach.

By embracing GitLab values and being active in engaging with our customers, our staff and our product, we enhance the security posture of our company, products, and client-facing services. The security department works cross-functionally inside and outside GitLab to meet these goals.

Our Vision is as follows:

1. GitLab Security as a business enabler
with a focus on

- Improving time to market (new features getting into releases faster and prevent slippage)
- Creating Product and competitive differentiation
- Reducing internal roadblocks and delays
- Improving security’s risk based approach to decision making through decentralization and managing appropriate levels of acceptable risk

1. Strengthen GitLab's enterprise grade security
with a focus on

- Achieving industry recognized security certifications
- Reducing the time required to pass customer security reviews
- A Direct impact to increasing contract size and volume
- Closing the gap between customer security requirements and GL’s Security posture

1. Reduce GitLab's threat landscape
with a focus on

- Reducing the likelihood of breach
- Reducing the exposure and severity of vulnerabilities
- Reducing the cost associated with service vulnerabilities

To help achieving the mission of being the most Transparent Security Group in the world the Security Department has nominated a [Security Culture Committee](./security-culture.html).

## Security Hiring

The company-wide mandate is justification for mapping Security headcount to around 5% of total company headcount. Tying Security Department growth headcount to 5% of total company headcount ensures adequate staffing support for the following (below are highlights and not the entire list of responsibilities of the Security Department):

- Security releases. At GitLab, the Security Department is DRI for critical and non-critical security releases.
- Detection/response for security incidents, which will increase as GitLab.com users increase.
- Preparation for upcoming IPO.
- Running the GitLab public bug bounty program.
- Dogfooding and contributing to our product.
- Improving and maintaining the security of GitLab.com and related services.

## Performance Review Pilot in Security Department

Performance reviews are a formal assessment in which managers evaluate a team members' performance, identify strengths and weaknesses, offer feedback, and set goals for future performance and career development. A good performance review is designed to facilitate conversations between team members and their managers. The benefits of performance reviews include:

- Transparency
- Recognition
- Improved communication and focus for 1-1s
- Additional data for Promotions and Compensation reviews
- Team member Development
- Career goals and path

There is a company-wide [360 performance review process](/handbook/people-group/360-feedback/) run by the People Group which focuses on values and gathering feedback from peers, managers and direct reports. Besides the People Group is working on developing a [9-box/Talent assessment](/handbook/people-group/performance-assessments-and-succession-planning/) and facilitating [Career Development Conversations](/handbook/people-group/leadership-toolkit/career-development-conversations/).

The Security Department is aiming to add to those processes, bring them together and deliver additional value to team members and the company. This specific performance review cycle will be run every 6 months and start with a pilot. The specific things looking to achieve with the pilot are:

- Setting expectations with Security leadership and team members based on the updated job family responsibilities and requirements;
- Facilitating a conversation between security leadership and team members and reflect on strengths/weaknesses bringing together 360 feedback on values and Career Development;
- Calibrating how performance is evaluated cross teams;
- Encouraging Security leadership to document expectations and performance going forward.

We will assess whether these goals were achieved three times: after the conversations have taken place with Security Leadership, after 3 months and at the end of the 6 month period with a Security Department member survey. This will be reviewed and discussed with their People Business Partner. Upon success, parts or the whole of this pilot will be integrated into the company-wide review process. Also, we may decide to continue the pilot, or perform a new one.

The framework of the performance review is as follows:

- Overview and Accomplishments
- GitLab Values (aligned with [360 feedback](/handbook/people-group/360-feedback/))
- Role Responsibilities and expectations (aligned with the Job Families)
- Career Path (aligned with [Career Development in Engineering](/handbook/engineering/career-development/#security-engineering))
- Next Steps (short term improvements)
- Team member Feedback

The performance review process is as follows:

- Managers draft reviews of direct reports baed on the above framework
- Each performance review will be reviewed by at least 2 others in security management (manager, director, vp)
- Managers will make final edits of performance review and deliver to direct report
- A 1:1 will be scheduled to faciliate conversation and feedback
- Individuals feedback will be included in the performance review and be documented
- A post-cycle review session will be held with security management and people business partner to review the process, what went well, areas for improvement
- Managers will continue to track progress and maintain conversation through 1:1's

## Security Department

As the Security Department has evolved, so has the area of engagement where Security has been required to provide input. Today, the Security Department provides an essential security service to the Engineering and Development Departments, and is directly engaged in Security Releases. However, the functions that the Security Department provides to the rest of the business are more consultative and advisory in nature - while the Security Department is a key player in the security questions raised throughout the business, it is not directly responsible for all of the administration of execution of functions that are required for the business to function while minimising risk.

This is expected - the security of the business should be a concern of everyone within the company and not just the domain of specialists. In addition, the role of the Security Department has expanded to assure customer, investor and regulator concerns about the security and safety of using GitLab as an enterprise-ready product, both through compliance certifications and through assurance responses directly to customers, and as we continue to encourage enterprise customers to use GitLab.com.

To reflect this, we have structured the Security Department around three key tenets, which drive the structure and the activities of our group. These are :

* Secure the Product  - [Product Security Sub-department](/handbook/engineering/security/application-security)
* Protect the Company - [Security Operations Sub-department](/handbook/engineering/security/operations)
* Assure the Customer - [Security Assurance Sub-department](/handbook/engineering/security/security-assurance/security-assurance.html)

### Secure the Product

This reflects the Security Department’s current efforts to be involved in the Application development and Release cycle for Security Releases, Security Research, our HackerOne bug bounty program, Security Automation and Vulnerability Management.

The term “Product” is interpreted broadly and includes the GitLab application itself and all other integrations and code that is developed internally to support the GitLab application for the multi-tenant SaaS. Our responsibility is to ensure all aspects of GitLab that are exposed to customers or that host customer data are held to the highest security standards, and to be proactive and responsive to ensure world-class security in anything GitLab offers.

### Protect the Company

This encompasses protecting company property as well as to prevent, detect and respond to risks and events targeting the business and GitLab.com. This sub department includes the Security Incident Response Team (SIRT), Trust and Safety team (former Abuse Operations) and Red team.

These functions have the responsibility of shoring up and maintaining the security posture of GitLab.com to ensure enterprise-level security is in place to protect our new and existing customers.

### Assure the Customer

This reflects the need for us to provide resources to our customers to assure them of the security and safety of GitLab as an application to use within their organisation and as a enterprise-level SaaS. This also involves providing appropriate support, services and resources to customers so that they trust GitLab as a Secure Company, as a Secure Product, and Secure SaaS

### Tenets Overlap between all Teams

It’s important to note that the three tenets do not operate independently of each other, and every team within the Security Department provides an important function to perform in order to progress these tenets. For example, Application Security may be strongly focused on Securing the Product, but it still has a strong focus around customer assurance and protecting the company in performing its functions. Similarly, Security Operations functions may be engaged on issues related to Product vulnerabilities, and the resolution path for this deeply involves improving the security of product features, as well as scoping customer impact and assisting in messaging to customers.

## Department Structure

Broadly speaking, teams are aligned under three Sections (Product, Operations and Customer) which reflect the tenets that are their primary focus. The Graph below illustrates how the teams within the Department are managed.

``` mermaid
graph TD;
    VP[VP of Security]---A1[Security Engineering & Research];
    VP[VP of Security]---A2[Security Operations];
    VP[VP of Security]---A3[Security Assurance];
    A1[Security Engineering & Research]---A11[Application Security];
    A11[Application Security]---A12[Security Automation];
    A12[Security Automation]---A13[Security Research];
    A13[Security Research]---A14[Security Communications];
    A2[Security Operations]---A21[SIRT];
    A21[SIRT]---A22[Trust & Safety];
    A22[Trust & Safety]---A23[Red Team];
    A3[Security Assurance]---A31[Security Compliance];
    A31[Security Compliance]---A32[Risk and Field Security];

```

## "Secure the Product" - The Product Security Sub-Department

The teams below are primarily focused on Application Security or other functions related to Securing the Product.

### Application Security

[Application Security](/handbook/engineering/security/application-security/) specialists work closely with development, product security PMs, and third-party groups (including paid bug bounty programs) to ensure pre and post deployment assessments are completed. Initiatives for this specialty also include:

- Pre and post deployment security assessments/tests
- Capture of flaws in software environment configuration
- Malicious code detection
- Patch/upgrade
- IP filtering
- Lock down executables
- Monitoring of programs at runtime to enforce the software use policy
- Developing and implementing a Secure Software Development Lifecycle (S-SDLC)
- Training and coaching developers on current security best practices

### Security Automation

[Security Automation](/handbook/engineering/security/automation/) specialists help us scale by creating tools that perform common tasks automatically. Examples include building automated security issue triage and management, proactive vulnerability scanning, and defining security metrics for executive review. Initiatives for this specialty also include:

- Assist other security specialty teams in their automation efforts
- Assess security tools and integrate tools as needed
- Define and own metrics and KPIs to determine the effectiveness of security programs
- Define, implement, and monitor security measures to protect GitLab.com and company assets
- Design, plan, and build new products or services to aid and improve security of the product and company

### Security Research

[Security research](/handbook/engineering/security/security-research/) specialists conduct internal testing against GitLab assets, against FOSS that is critical to GitLab products and operations, and against vendor products being considered for purchase and integration with GitLab. Initiatives for this specialty also include:

- Conduct vulnerability research against all GitLab and GitLab.com assets
- Research FOSS tools that are integrated with GitLab
- Develop proof-of-concept code to be included in security findings
- Report findings to tool developers and track mitigation process
- Follow [GitLab's responsible disclosure policy](/security/disclosure/#external) for community disclosure
- Author blog posts on vulnerabilities discovered
- Conduct vulnerability research against SaaS apps and other products that are used by GitLab

Security research specialists are subject matter experts (SMEs) with highly specialized security knowledge in specific areas, including reverse engineering, incident response, malware analysis, network protocol analysis, cryptography, and so on. They are often called upon to take on security tasks for other security team members as well as other departments when highly specialized security knowledge is needed. Initiatives for SMEs may include:

- Security testing of electronics being used as swag by Marketing to be handed out at GitLab events
- Network analysis and/or reverse engineering of a closed source application used with a third party SaaS app integration (e.g. iOS/Android app)
- “Test” the guidelines outlined in a detailed step-by-step instructional document used in the configuration of an asset to ensure the asset is properly secured

Security research specialists are often used to promote GitLab thought leadership by engaging as all-around security experts, to let the public know that GitLab doesn’t just understand DevSecOps or application security, but has a deep knowledge of the security landscape. This can include the following:

- Submit security-related technical talks for presentations at security conferences as a GitLab team member
- Handle security-related questions by the Marketing/PR teams in response to questions from the press, or even direct press interviews

### Security External Communications

The External Communications Team leads customer advocacy, engagement and communications in support of GitLab Security Team programs. Initiatives for this specialty include:

* Increase engagement with the hacker community, including our public bug bounty program.
* Build and manage a Security blogging program.
* Develop social media content and campaigns, in collaboration with GitLab social media manager.
* Manage security alert email notifications.
* Collaborate with corporate marketing, PR, Community Advocates, and Developer Evangelism teams to help identify opportunities for the Security Team to increase industry recognition and thought leadership position.


## "Protect the Company" - The Security Operations Sub-department

[Security Operations Sub-department](/handbook/engineering/security/operations) teams are primarily focused on protecting GitLab the business and GitLab.com.

### SIRT - Security Incident Response Team (former "Security Operations")

The [SIRT team](./sec-incident-response.html) is here to manage security incidents across GitLab. These stem from events that originate from outside of our infrastructure, as well as those internal to GitLab. This is often a fast-paced and stressful environment where responding quickly and maintaining ones composure is critical.

More than just being the first to acknowledge issues as they arise, SIRT is responsible for leading, designing, and implementing the strategic initiatives to grow the Detection and Response practices at GitLab. These initiatives include:

- Work with the internal and external partners to ingest logging and alerting into our centralized monitoring solution
- Triage and analysis of alerting to determine validity, how to remediate and/or prevent incidents, then act accordingly
- Coordinate localized or company-wide response to security incidents
- Define and lead vulnerability management for GitLab Team Members and the production/pre-production environments as part of GitLab.com
- Incorporate current security trends, advisories, publications, and academic research into our security practices
- Deploy and maintain security monitoring and analysis solutions for GitLab the business and GitLab.com

SIRT can be contacted on slack via our handle `@sec-ops-team` or in a GitLab issue using `@gitlab-com/gl-security/secops`. If your request requires immediate attention please review the steps for [engaging the security on-call](#engaging-the-security-on-call).

### Trust & Safety (former "Abuse Operations")

[Trust & Safety](/handbook/engineering/security/operations/abuse/) specialists investigate and mitigate the malicious use of our systems, which is defined under Section 3 of the [GitLab Website Terms of Use](/terms/#gitlab_com). This activity primarily originates from inside our infrastructure.

Initiatives for this specialty include:

- Detection and mitigation of abusive activity on GitLab.com.
- DMCA Notice and Counter-Notices processing.
- Escalating potential abuse vectors to stakeholders for mitigation.
- Research and prevention of trending abuse methodologies.

 For more information please see our [Resources Section](/handbook/engineering/security/operations/abuse/#trust--safety-resources)

<i>**Code of Conduct Violations**</i> are [handled](/handbook/marketing/community-relations/community-advocacy/workflows/code-of-conduct-enforcement) by the [Community Advocates](/handbook/marketing/community-relations/community-advocacy/) in the [Community Relations Team](/handbook/marketing/community-relations/). For more information on reporting these violations please see the [GitLab Community Code of Conduct](/community/contribute/code-of-conduct/) page.

### Red Team

GitLab's internal [Red Team](/handbook/engineering/security/red-team) emulates adversary activity to better GitLab’s enterprise and product security. This includes activities such as:

- Performing exercises with SecOps to collaboratively and rapidly iterate on improving GitLab's security posture. These exercises will be referred to as purple team exercises merging blue (secops) and red teams together.
- Performing exercises to reflect simulated adversarial attempts to compromise organizational mission/business functions and provide a comprehensive assessment of the security state of information systems and organizations.
- Simulating adversarial attempts to compromise organizational missions/business functions and the information systems that support those missions/functions may include technology-focused attacks (e.g., interactions with hardware, software, or firmware components and/or mission/business processes) and social engineering-based attacks (e.g., interactions via email, telephone, shoulder surfing, or personal conversations).

## "Assure the Customer" - The Security Assurance Sub-department

The [Security Assurance](/handbook/engineering/security/security-assurance/security-assurance.html) sub-department is comprised of the teams below. They target Customer Assurance projects among their responsibilities.

### Security Compliance

Operating as a second line of defense, Security Compliance's core mission is to implement a best in class governance, risk and compliance program that encompasses SaaS, on-prem, and open source instances. Initiatives for this specialty include:

 * Maintaining a certification [roadmap](https://gitlab.com/groups/gitlab-com/gl-security/compliance/-/roadmap) based on customer needs _e.g._
   * FedRAMP
   * ISO 27001
   * [SOC 2](/handbook/engineering/security/security-assurance/security-compliance/soc2.html)
 * Monitoring the adequacy and effectiveness of [GitLab security common controls](/handbook/engineering/security/security-assurance/security-compliance/sec-controls.html) and timely remediation of observations
 * Facilitating external certification audits to include timely remediation of observations
  * Assisting Security leadership in developing processes and controls to manage risks and issues
 * Proposing compliance features for the GitLab product in order to help our customers more easily achieve their compliance goals

For additional information about the Security Compliance program see the [Security Compliance team handbook page](/handbook/engineering/security/security-assurance/security-compliance/compliance.html) or refer to [GitLab's security controls](/handbook/engineering/security/security-assurance/security-compliance/sec-controls.html) for a detailed list of all compliance controls organized by control family.

### Risk and Field Security
The Risk and Field Security team serves as the public representation of GitLab's internal Security function. We are tasked with providing high levels of security assurance to internal and external customers. This means working with multiple departments to document requests, analyze the risk assocaited with those requests, and provide value-added remediation recommendations. As a member of the Risk and Field Security team, you will support GitLab's growth by effectively and appropriately identifying, tracking, and treating Operational, Third Party and Customer related risks. 

Initiatives for this specialty include:

* Facilitating [Customer Security Assurance activities](/handbook/engineering/security/security-assurance/field-security/customer-security-assessment-process.html) including [The Trust Site](https://about.gitlab.com/security/) and [The Customer Assurance Package](/handbook/engineering/security/security-assurance/field-security/customer-assurance-package.html).
* Maintaining a [Security Operational Risk Management program](/handbook/engineering/security/security-assurance/security-compliance/risk-management.html), executing annual operational security risk assessments, and managing a consolidated security risk register.
* Maintaining a [Vendor Security Risk Management program](/handbook/engineering/security/security-assurance/security-compliance/third-party-vendor-security-review.html)
*  Enabling the Sales organization through security training, collateral development, RFP maintenance and customer support
*  Evangelizing Security Best Practices to customers and internal teams
*  Managing customer security questions and escalating potential security issues to appropriate teams and drive to resolution

For additional information about the Field Security Team see the [Field Security Team handbook page](/handbook/engineering/security/security-assurance/field-security/).

## Security Internship

For information on the security internship, see the [Internship page](/handbook/engineering/security/internship.html).

## Security Department Collaborators

### Secure Team

The Security department will collaborate with development and product management for security-related features in GitLab.
The [Secure team](../ops/secure) must not be mistaken with the Security Teams.

- Develop real-world security use cases
- Ideation of compelling security features and products
- Test and provide product feedback

### External Security Firms

We work closely with bounty programs, as well as security assessment and penetration testing firms to ensure external review of our security posture.

- One security assessment firm is rotated periodically to gain new perspectives
- One security assessment firm is engaged every quarter to build expertise in GitLab
- We maintain a public bug bounty program via [HackerOne](https://hackerone.com/gitlab)

## Resources

### Information Security Policies

Information Security Policies are reviewed annually. Policy changes are approved by the Senior Director of Security and Legal. Changes to the Data Protection Impact Assessment Policy are approved by GitLab's Privacy Officer.

- [GitLab Internal Acceptable Use Policy](/handbook/people-group/acceptable-use-policy/)
- [GitLab Password Policy](/handbook/security/#gitlab-password-policy-guidelines)
- [Access Management Policy](/handbook/engineering/security/access-management-policy.html)
- [Data Classification Policy](/handbook/engineering/security/data-classification-standard.html)
- [Data Protection Impact Assessment Policy](/handbook/engineering/security/dpia-policy/)

- [Penetration Testing Policy](/handbook/engineering/security/penetration-testing-policy.html)

- [Audit Logging Policy](/handbook/engineering/security/audit-logging-policy.html)

### Information Security Policy Exception Management Process

Information security considerations such as regulatory, compliance, confidentiality, integrity and availability requirements are most easily met when companies employ centrally supported or recommended industry standards. Whereas GitLab operates under [the principle of least privilege](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege), we understand that centrally supported or recommended industry technologies are not always feasible for a specific job function or company need. Deviations from the aforementioned standard or recommended technologies is discouraged.  However, it may be considered provided that there is a reasonable, justifiable business and/or research case for an information security policy exception; resources are sufficient to properly implement and maintain the alternative technology; the process outlined in this and other related documents is followed and other policies and standards are upheld.

In the event a team member requires a deviation from the standard course of business or otherwise allowed by policy, the Requestor must submit a [Policy Exception Request](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/new?issue%5Bassignee_id%5D=&issue%5Bmilestone_id%5D=) to IT Security, which contains, at a minimum, the following elements:

- Team member Name and contact
- Time period for the exception (deviations should not exceed 90 days unless the exception is related to a device exception, like using a Windows device)
- The exception being requested, i.e. which policy or procedure is affected by the proposed deviation
- Any alternative, lesser solution can be provided
- The business justification for the proposed deviation
- Compensating controls which will be implemented to ensure proper oversight.

The [Policy Exception Request](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/new?issuable_template=Exception_Request) should be used to request exceptions to information security policies, such as the password policy, or when requesting the use of a non-standard device (laptop).

Exception request approval requirements are documented within the issue template. The requester should tag the appropriate individuals who are required to provide an approval per the approval matrix.

If the business wants to appeal an approval decision, such appeal will be sent to Legal at legal@gitlab.com. Legal will draft an opinion as to the proposed risks to the company if the deviation were to be granted. Legal’s opinion will be forwarded to the CEO and CFO for final disposition.

Any deviation approval must:

- Recommended compensating controls to reduce exposure and/or harm (i.e. admin rights to financially significant system may require audit logs and review of users activity within the system)
- Be captured in writing

### GitLab.com Groups and Projects

Many teams follow a convention of having a GitLab group `team-name-team` with a
primary project used for issue tracking underneath `team-name` or similiar. For example:
`gitlab-com/gl-security/security-assurance/field-security-team/field-security`.

- [@gitlab-com/gl-security](https://gitlab.com/gitlab-com/gl-security/) is the primary group for @'mentioning the entire Security Department.
  - [@gitlab-com/gl-security/security-managers](https://gitlab.com/gitlab-com/gl-security/security-managers) is the primary group for @'mentioning all managers in the Security Department.
  - [public (!) Security Department Meta](https://gitlab.com/gitlab-com/gl-security/security-department-meta/) for Security Department initiatives, `~meta` and backend tasks, and catch all for anything not covered by other projects. For non-Security department team members, use this if unsure which team to contact. For Security Team members, use of this
  project as a catch-all is _deprecated_.
  - [Security Assurance Sub-department (@gitlab-com/gl-security/security-assurance)](https://gitlab.com/gitlab-com/gl-security/security-assurance) Security Assurance Sub-department
    - [@gitlab-com/gl-security/security-assurance/sec-compliance](https://gitlab.com/gitlab-com/gl-security/compliance) is the primary group for @'mentioning the Security Compliance team.
    - [@gitlab-com/gl-security/field-security](https://gitlab.com/gitlab-com/gl-security/security-assurance/field-security-team) is the primary group for @'mentioning the Field Security team.
  - [Engineering and Research Sub-department (@gitlab-com/gl-security/engineering-and-research)](https://gitlab.com/gitlab-com/gl-security/engineering-and-research/engineering-and-research-meta)
    - [gitlab-com/gl-security/engineering-and-research-meta](https://gitlab.com/gitlab-com/gl-security/engineering-and-research-meta) For sub-department wide management and planning issues.
    - [@gitlab-com/gl-security/appsec](https://gitlab.com/gitlab-com/gl-security/appsec) is the primary group for @'mentioning the Application Security team.
    - [@gitlab-com/gl-security/automation](https://gitlab.com/gitlab-com/gl-security/engineering-and-research/automation) is the primary group for @'mentioning the Security Automation team.
      - [gitlab-com/gl-security/engineering-and-research/automation-team/automation](https://gitlab.com/gitlab-com/gl-security/engineering-and-research/automation-team/automation)
  - [Operations](https://gitlab.com/gitlab-com/gl-security/secops) Operations Sub-department
    - [@gitlab-com/gl-security/secops](https://gitlab.com/gitlab-com/gl-security/secops) is the primary group for @'mentioning the Security Operations team.
      - [Security Operations (private)](https://gitlab.com/gitlab-com/gl-security/secops/operations) for SIRT team issues.
    - [@gitlab-com/gl-security/abuse-team](https://gitlab.com/gitlab-com/gl-security/abuse-team) is the primary group for @'mentioning the Trust & Safety team.
- [security runbooks (private)](https://gitlab.com/gitlab-com/gl-security/runbooks) -
**NOTE**: The handbook and [production runbooks](https://gitlab.com/gitlab-com/runbooks) should
be the first locations considered for any process or documentation. `gl-security/runbooks`
should only be used for documenting specifics that would increase risk and/or
have customer impact if publicly disclosed.
- [Incident-Tools (private)](https://gitlab.com/gitlab-com/gl-security/incident-tools)
for working scripts and other code during or while remediating an incident.
If the tool is applicable outside of the `GitLab.com` environment, consider
if it's possible to release when the `~security` issue becomes
non-confidential. This group can also be used for private demonstration projects for
security issues.
- [security-tools (mostly private)](https://gitlab.com/gitlab-com/security-tools/) contains some
operational tools used by the security teams. Contents and/or configurations
require that most of these projects remain private.

### Slack Channels

- [#security](https://gitlab.slack.com/archives/security); Used for general
security questions and posting of external links for the great discussions.
Company wide security relevant announcements are announced in #whats-happening-at-gitlab
and may be copied here.
- [#security-department](https://gitlab.slack.com/archives/security-department) - Daily questions
and discussions focused on work internal to the security department. Can be used for
reporting when unsure of where to go.
- [#abuse](https://gitlab.slack.com/archives/abuse) - Used for reporting suspected abusive activity/content (_GitLab Internal_) as well as general discussions regarding anti-abuse efforts. Use `@trust-and-safety` in the channel to alert the team to anything urgent.
- `#security-department-standup` - Private channel for daily standups.
- `#incident-management` and [other infrastructure department channels](/handbook/engineering/infrastructure/#common-links)
- `#security-alert-manual` - New reports for the security department from various intake sources, including ZenDesk and new HackerOne reports.
- `#hackerone-feed` - Feed of most activity from our HackerOne program.
- Other `#security-alert-*` and `#abuse*` - Multiple channels for different notifications
handled by the Security Department.
- Use the **@sec-ops-team** mention in any Slack channel to tag the members of the Security Operations team.
- Use the **@sec-assurance-team** mention in any Slack channel to tag the members of the Security Compliance and Field Security teams.
- Use the **@field-security** mention in any Slack channel to tag the members of the Field Security team.
- Use the **@appsec-team** mention in any Slack channel to tag the members of the Application Security team.
- Use the **@trust-and-safety** mention in any Slack channel to tag the members of the Trust & Safety team (former Abuse Operations).

### Other Frequently Used GitLab.com Projects

Security crosses many teams in the company, so you will find `~security` labelled
issues across all GitLab projects, especially:

- [gitlab-foss](https://gitlab.com/gitlab-org/gitlab-foss/issues/)
- [gitlab](https://gitlab.com/gitlab-org/gitlab/issues/)
- [infrastructure](https://gitlab.com/gitlab-com/gl-infra/infrastructure/issues/)
- [production](https://gitlab.com/gitlab-com/gl-infra/production/issues/)

When opening issues, please follow the [Creating New Security Issues](#Creating-New-Security-Issues) process for using labels and the confidential flag.

### Other Resources for GitLab Team Members

- [Security Best Practices](/handbook/security/), using
1Password and similar tools, are documented on their own [security best
practices page](/handbook/security/).
- GitLab.com and GitLab Hosted [data breach notification policy](/security/#data-breach-notification-policy).
- GitLab Internal Acceptable Use [Policy](/handbook/people-group/acceptable-use-policy/).
- For GitLab.com, we have developed a [Google Cloud Platform (GCP) Security Guidelines Policy](https://docs.google.com/document/d/1BBTWC5OpIqrva7DqH4nkjYUmNZ3UFbc6erqV89P_N-o/edit?usp=sharing) document, which outlines recommended best practices, and is enforced through
our security automation initiatives.
- GitLab Security Tanuki for use on security release blogs, social media and security related swag as appropriate:
    - [Web-RGB](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/tree/master/design/gitlab-brand-files/gitlab-logo-files/gitlab-security-logo/web-rgb)
    - [Print-CMYK](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/tree/master/design/gitlab-brand-files/gitlab-logo-files/gitlab-security-logo/print-cmyk)
    - and one [exclusively for stickers](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/blob/master/design/gitlab-brand-files/gitlab-logo-files/gitlab-security-logo/print-cmyk/pdf/sticker/gitlab-security-icon-diecut-sticker-3x2_78in.pdf).

### How to track OKR related work scheduled by quarter

The Security Department tracks their OKRs using the boards in the table below.
These boards aggregate work from the many subgroups and projects under `gitlab-com/gl-security`
used by the various subteams to track their work and projects. High level issues
and open issues that map directly to an OKR should be added to the board for the
quarter to provide visibility into the current work of the security department.

When creating an issue that maps to an OKR, apply the following group level labels
so that it appears in the board:

- The label for the assigned (usually the current) quarter. For example: `~FY20Q3`
- The scoped `Security Management::` label for the appropriate team. For example: `~Security Management::Security Automation Team`

These labels can also be applied to MRs related to the work.

| Quarter | Board |
| ------- | ----- |
| `~FY20Q4` | [Board link](https://gitlab.com/groups/gitlab-com/gl-security/-/boards/1367370?label_name%5B%5D=FY20Q4) |
| `~FY20Q3` | [Board link](https://gitlab.com/groups/gitlab-com/gl-security/-/boards/1218177?label_name%5B%5D=FY20Q3) |
| `~FY20Q2` | [Board link](https://gitlab.com/groups/gitlab-com/gl-security/-/boards/1122898?label_name%5B%5D=FY20Q2) |

### How We Plan, Assign, and Execute Work

Any work that is related to an OKR is tracked with an issue in the appropriate
team or project tracker and linked to the OKR issue as related.

Larger initiatives that span the scope of multiple teams or projects may require
a [Planning](./planning) handbook page to further developer requirements.

## Security Releases

The definitions, processes and checklists for security releases are described
in the
[release/docs](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/process.md)
project.

The policies for backporting changes follow [Security Releases](https://docs.gitlab.com/ee/policy/maintenance.html#security-releases)
for GitLab EE.

For critical security releases, refer to [Critical Security Releases](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/process.md#critical-security-releases) in `release/docs`.

## Issue Triage

The Security team needs to be able to communicate the priorities of security related issues to the Product, Development, and Infrastructure teams. Here's how the team can set priorities internally for subsequent communication (inspired in part by how the [support team does this](/handbook/support/workflows/working-with-issues.html)).

### Creating New Security Issues

New security issue should follow these guidelines when being created on `GitLab.com`:

- Create new issues as `confidential` if unsure whether issue a potential
vulnerability or not. It is easier to make an issue that should have been
public open than to remediate an issue that should have been confidential.
Consider adding the `/confidential` quick action to a project issue template.
- Always label as `~security` at a minimum.
- Add any additional labels you know apply. Additional labels will be applied
by the security team and other engineering personnel, but it will help with
the triage process:
    - `~bug` or `~feature` if appropriate
    - Team or devops lifecycle labels
    - `~customer` if issue is a result of a customer report
    - `~internal customer` should be added by team members when the issue
    impacts GitLab operations.
- Issues that contain customer specific data, such as private repository contents,
should be assigned `~keep confidential`. If possible avoid this by linking
resources only available to GitLab team member, for example, the originating
ZenDesk ticket. Label the link with `(GitLab internal)` for clarity.

Occasionally, data that should remain confidential, such as the private
project contents of a user that reported an issue, may get included in an
issue. If necessary, a sanitized issue may need to be created with more
general discussion and examples appropriate for public disclosure prior to
release.

For review by the Application Security team, @ mention `@gitlab-com/gl-security/appsec`.

For more _immediate_ attention, refer to [Engaging security on-call](#engaging-the-security-on-call).

### Severity and Priority Labels on `~security` Issues

If an issue is determined to be a vulnerability, the security engineer will ensure that the issue labelled as a `~bug` and not a [`~feature`](#feature).

The presence of `~security` and `~bug` labels modifies the standard [severity labels](/handbook/engineering/quality/issue-triage/#severity)(`~severity::1`, `~severity::2`, `~severity::3`, `~severity::4`)
by additionally taking into account
likelihood as described [below](#security-severity-labels), as well as any
other mitigating or exacerbating factors. The priority of addressing
`~security` issues is also driven by impact, so in most cases, the priority label
assigned by the security team will match the severity label.
Exceptions must be noted in issue description or comments.

The intent of tying `~S/~P` labels to remediation times is to measure and improve GitLab's
response time to security issues to consistently meet or exceed industry
standard timelines for responsible disclosure. Mean time to remediation (MTTR) is
a external
metric that may be evaluated by users as an indication of GitLab's commitment
to protecting our users and customers. It is also an important measurement that
security researchers use when choosing to engage with the security team, either
directly or through our [HackerOne Bug Bounty Program](#hackerone-process).

| Severity  | Priority  | Time to mitigate    |Time to remediate      |
|-----------|-----------|---------------------|-----------------------|
| `~severity::1` (Critical)     | `~priority::1`     | Within 24 hours     | On or before the [next security release](/blog/categories/releases/)   |
| `~severity::2` (High)    | `~priority::2`     | N/A                 | Within 60 days        |
| `~severity::3` (Medium)    | `~priority::3`     | N/A                 | Within 90 days        |
| `~severity::4` (Low)     | `~priority::4`     | N/A                 | Best effort unless risk accepted |

### Due date on `~security` Issues

For `~severity::2`, `~severity::3`, and `~severity::4` `~security` `~bug`s, the security engineer assigns the `Due date`,
which is the target date of when fixes should be ready for release.
This due date should account for the `Time to remediate` times above, as well as
monthly security releases on the 28th of each month. For example, suppose today is October 1st, and
a new `severity::2` `~security` issue is opened. It must be addressed in a security release within 60 days,
which is November 30th. So therefore, it must catch the November 28th security release.
Furthermore, the [Security Release Process deadlines](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/process.md#release-deadlines)
say that it should the code fix should be ready by November 23rd. So the due date
in this example should be November 23rd.

`~severity::1` `~security` issues do not have a due date since they should be fixed as soon
as possible, and a security release made available as soon as possible to accommodate
it. These issues are worked by a security engineer oncall to mitigate the risk within 24 hours. This means the risks relevant to our customers have been removed or reduced as much as possible within 24 hours. The remediation timeline target is never greater than our next [security release](/blog/categories/releases/) but remediation in this case would not impact customer security risk.

Note that some `~security` issues may not need to be part of a code release, such as
an infrastructure change. In that case, the due date will not need to account for
monthly security release dates.

On occasion, the due date of such an issue may need to be changed if the security team
needs to move up or delay a monthly security release date to accommodate for urgent
problems that arise.

### Reproducibility on `~security` Issues

The issue description should have a `How to reproduce` section to ensure clear replication details are in description. Add additional details, as needed:

- Environment used:
    - Docker Omnibus version x.y.z
    - gitlab.com
    - staging.gitlab.com
- Conditions used such as projects, users, enabled features or files used
- A step by step plan to reproduce the issue
- The url or even better the `curl` command that triggers the issue

#### ~feature

Issues labelled with the `security` and `feature` labels are **not** considered vulnerabilities, but rather security enhancements or defense-in-depth mechanisms. This means the security team is not required to set the `S` and `P` labels or follow the vulnerability triage process as these issues will be triaged by [product](/handbook/product/) or other appropriate team owning the component.

Implementation of security feature issues should be done publicly in line with our [Transparency](/handbook/values/#transparency) value, i.e. not following the [security developer workflow](https://gitlab.com/gitlab-org/release/docs/-/blob/master/general/security/developer.md).

On the contrary, note that issues with the `security`, `bug`, and `severity::4` labels are considered `Low` severity vulnerabilities and will be handled according to the standard vulnerability triage process.

#### ~"security request"

The security team may also apply `~internal customer` and [~`security request`](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name%5B%5D=security%20request) to issue as an
indication that the feature is being requested by the security team to meet
additional customer requirements, compliance or operational needs in
support of GitLab.com.

#### Transferring from Security to Engineering

The security engineer must:

- Add [group label](https://gitlab.com/gitlab-org/gitlab-foss/blob/master/doc/development/contributing/issue_workflow.md#group-labels) (`~group::editor`, `~group::package`, etc.)
- Add [stage label](https://gitlab.com/gitlab-org/gitlab-foss/blob/master/doc/development/contributing/issue_workflow.md#stage-labels)
- Any additional labels, such as `~merge request`.
- Mention the product manager for scheduling, such as `@pm for scheduling`.
- The engineering team lead should be @ mentioned and followed up with when necessary as
noted below for different severity levels.

The product manager will assign a `Milestone` that has been assigned a due
date to communicate when work will be assigned to engineers. The `Due date`
field, severity label, and priority label on the issue should not be changed
by PMs, as these labels are intended to provide accurate metrics on
`~security` issues, and are assigned by the security team. Any blockers,
technical or organizational, that prevents `~security` issues from being
addressed as [our top priority](/handbook/engineering/workflow/#security-is-everyones-responsibility)
should be escalated up the appropriate management chains.

**Note that issues are not scheduled for a particular release unless the team leads add them to a release milestone _and_ they are assigned to a developer.**

Issues with an `severity::1` or `severity::2` rating should be immediately brought to the
attention of the relevant engineering team leads and product managers by
tagging them in the issue and/or escalating via chat and email if they are
unresponsive.

Issues with an `severity::1` rating have priority over all other issues and should be
considered for a critical security release.

Issues with an `severity::2` rating should be scheduled for the next scheduled
security release, which may be days or weeks ahead depending on severity and
other issues that are waiting for patches. An `severity::2` rating is not a guarantee
that a patch will be ready prior to the next security release, but that
should be the goal.

Issues with an `severity::3` rating have a lower sense of urgency and are assigned a
target of the next minor version.  If a low-risk or low-impact vulnerability
is reported that would normally be rated `severity::3` but the reporter has
provided a 30 day time window (or less) for disclosure the issue may be
escalated to ensure that it is patched before disclosure.

#### Security issue becoming irrelevant due to unrelated code changes

It is possible that a ~security issue becomes irrelevant after it was initially triaged,
but before a patch was implemented. For example, the vulnerable functionality was removed
or significantly changed resulting in the vulnerability not being present anymore.

If an engineer notices that an issue has become irrelevant, he should @-mention the person
that triaged the issue to confirm that the vulnerability is not present anymore. <b>Note that it might still be necessary to backport a patch to previous releases according to our [maintenance policy](https://docs.gitlab.com/ee/policy/maintenance.html#security-releases)</b>.
In case no backports are necessary, the issue can be closed.

## Secure Coding Training

For information on secure coding initiatives, please see the [Secure Coding Training](./secure-coding-training.html) page.

## Security Gearing Ratios

Gearing ratios are used as [Business Drivers](/handbook/finance/financial-planning-and-analysis/#business-drivers-also-known-as-gearing-ratios) to forecast long term financial goals by function. The primary gearing ratios for Security is Bug Bounty expenditure:

- Bug Bounty budget is determined as 1% of the cost of a compromise which is estimated at 1% of company worth
- Bug Bounty top reward is determined as 1% of budget

An illustration:
GitLab is worth 2.5 billion and a significant compromise can cost GitLab $250 million.
1% ratio = $2.5 millon budget. Likewise, 1% of budget = $25,000 top reward

Approximate monthly budget should be set at total budget divided by 12. It should be understood that our bug bounty payouts are largely unpredictable and fluctuate based on the following:

- Number and severity of bugs produced by GitLab and pushed to production
- Participation of research community
- Reward ranges

## Internal Application Security Reviews

For systems built (or significantly modified) by Departments that house customer and other sensitive data, the Security Team should perform applicable application security reviews to ensure the systems are hardened. Security reviews aim to help reduce vulnerabilities and to create a more secure product.

### When to request a security review?

1. If your changes are processing, storing, or transferring any kind of [RED or ORANGE data](https://docs.google.com/document/d/15eNKGA3zyZazsJMldqTBFbYMnVUSQSpU14lo22JMZQY/edit), it _should_ be reviewed by the [application security team](https://gitlab.com/gitlab-com/gl-security/appsec).
1. If your changes involve implementing, utilizing, or is otherwise related to any type of **authentication**, **authorization**, or **session handling** mechanism, it _should_ be reviewed by the [application security team](https://gitlab.com/gitlab-com/gl-security/appsec).
1. If your changes have a goal which requires a **cryptographic function** such as: confidentiality, integrity, authentication, or non-repudiation, it _should_ be reviewed by the [application security team](https://gitlab.com/gitlab-com/gl-security/appsec).

### How to request a security review?

There are two ways to request a security review depending on how significant the changes are. It is divided between individual merge requests and larger scale initiatives.

#### Individual merge requests or issues

Loop in the application security team by `/cc @gitlab\-com/gl\-security/appsec` in your merge request or issue.

These reviews are intended to be faster, more lightweight, and have a lower barrier of entry.

#### Larger scale initiatives

To get started, create an issue in the [security tracker](https://gitlab.com/gitlab-com/gl-security/security-department-meta/issues), add the `app sec review` label, and submit a [triage questionnaire form](https://docs.google.com/forms/d/e/1FAIpQLScIpq-vmfRTN3ClvETGP1B68C91FDXoiYhkSSzIpN7IFiGlWQ/viewform?usp=sf_link). The complete process can be found at [here](https://gitlab.com/gitlab-com/gl-security/security-department-meta/issues/16).

Some use cases of this are for epics, milestones, reviewing for a common security weakness in the entire codebase, or larger features.

### Is security approval required to progress?

No, code changes do _not_ require security approval to progress. Non-blocking reviews enables the freedom for our code to [keep shipping](/handbook/ceo/#how-do-we-keep-shipping) fast, and it closer aligns with our values of [iteration and efficiency](/handbook/values/#iteration). They operate more as guardrails instead of a gate.

### What should I provide when requesting a security review?

To help speed up a review, it's recommended to provide any or all of the following:

- The background and context of the changes being made.
- Any documentation or diagrams which help provide a clear understanding it's purpose and use cases.
- The type of data it's processing or storing.
- The security requirements for the data.
- Your security concerns and a worst case scenario that could happen.
- A test environment.

### What does the security process look like?

The current process for larger scale internal application security reviews be found [here](https://gitlab.com/gitlab-com/gl-security/security-department-meta/issues/16)

### My changes have been reviewed by security, so is my project now secure?

Security reviews are not proof or certification that the code changes are secure. They are best effort, and additional vulnerabilities may exist after a review.

It's important to note here that application security reviews are not a one-and-done, but can be ongoing as the application under review evolves.

## Vulnerability Reports and HackerOne

GitLab receives vulnerability reports by various pathways, including:

- HackerOne bug bounty program
- `security@gitlab.com`
- Reports or questions come in from customers through Zendesk.
- Issues opened on the public issue trackers. The security team can not review
all new issues and relies on everyone in the company to identify and label
issues as `~security` and @-mention `@gitlab-com/gl-security/appsec` on issues.
- Issues reported by automated security scanning tools

For **any** reported vulnerability:

- Open a confidential issue in the appropriate issue tracker as soon as a report
is verified. If the vulnerability was reported via a public issue, make the issue confidential.
If triage is delayed due to team availability, the delay should be communicated.
- An initial determination should be made as to severity and impact. Never **dismiss** a security report outright. Instead, follow up with the reporter, asking clarifying questions.
- For next steps, see the process as it is detailed below for HackerOne reports, and adhere to the guidelines there for vulnerabilities reported in other ways as well in terms of frequency of communication and so forth.
- Remember to prepare patches, blog posts, email templates, etc. on `dev` or in other non-public ways even if there is a reason to believe that the vulnerability is already out in the public domain (e.g. the original report was made in a public issue that was later made confidential).

### Triage Rotation

Application Security team members may assign themselves as the directly
responsible individual (DRI) for incoming requests to the Application
Security team for a given calendar week in the [Triage Rotation](https://docs.google.com/spreadsheets/d/18vz84dgTfetTaBjbOCXaLKNfzLYMiy_tBW6RfEUYYHk/edit?ts=5ce48702#gid=0)
Google Sheet in the Security Team Drive.

The following rotations are defined:

- (Weekly Assignment) HackerOne and ZenDesk
    - Two application security engineers are assigned this task each week and can be found at [Triage Rotation](https://docs.google.com/spreadsheets/d/18vz84dgTfetTaBjbOCXaLKNfzLYMiy_tBW6RfEUYYHk/edit?ts=5ce48702#gid=0).
    - Point of contact for "New" HackerOne reports during that week.
    - At least once daily, review and initial triage and assignment if necessary
    of tickets reported to `security@gitlab.com`, which creates tickets in ZenDesk,
    following the [AppSec ZenDesk process](/handbook/support/workflows/working_with_security.html#appsec-and-vulnerability-reports)
    - Responsible to escalating to other team members and management if the size of
    the either queue spikes.
- (Weekly Assignment) Mentions and issues
    - First responder to mentions of the following group aliases:
        - @gitlab-com/gl-security/appsec on GitLab.com
        - @appsec-team in Slack
    - First responder to automated messages posted in the `#public_merge_requests_referencing_confidential_issues` Slack channel
    - Issues created needing triage: [~security-triage-appsec issue search](https://gitlab.com/groups/gitlab-org/-/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name%5B%5D=security-triage-appsec)
    - [Security Dashboards](#security-dashboard-review)
        - [GitLab](https://gitlab.com/gitlab-org/gitlab/-/security/dashboard)
        - [GitLab Workhorse](https://gitlab.com/gitlab-org/gitlab-workhorse/-/security/dashboard)
        - [Gitaly](https://gitlab.com/gitlab-org/gitaly/security/dashboard)
        - [GitLab Pages](https://gitlab.com/gitlab-org/gitlab-pages/-/security/dashboard)
        - [GitLab Shell](https://gitlab.com/gitlab-org/gitlab-shell/-/security/dashboard)
        - [Gitter Webapp](https://gitlab.com/gitlab-org/gitter/webapp/security/dashboard)
        - [Gitter Android](https://gitlab.com/gitlab-org/gitter/gitter-android-app/-/security/dashboard)
        - [License](https://gitlab.com/gitlab-org/license-gitlab-com/-/security/dashboard)
        - [k8s-workloads](https://gitlab.com/groups/gitlab-com/gl-infra/k8s-workloads/-/security/dashboard)
        - [Version](https://gitlab.com/gitlab-services/version-gitlab-com/-/security/dashboard)
        - [UBI images](https://gitlab.com/gitlab-com/gl-security/appsec/container-scanners/-/security/dashboard/)
        - [release-cli](https://gitlab.com/gitlab-org/release-cli/-/security/dashboard/)
        - [vscode-extension](https://gitlab.com/gitlab-org/gitlab-vscode-extension/-/security/dashboard)
        - [Customers](https://gitlab.com/gitlab-org/customers-gitlab-com/-/security/dashboard)
        - [elastic-search-indexer](https://gitlab.com/gitlab-org/gitlab-elasticsearch-indexer/-/security/dashboard)
        - [GitLab DAST](https://gitlab.com/gitlab-org/security-products/dast/-/security/dashboard/)
- (Monthly Assignment) Security Engineer for Security Releases
- (Quarterly Assignment) Bug Bounty/AppSec Blog Post

Team members should not assign themselves on weeks they are responsible for the
scheduled security release.

Team members not assigned as the DRI for the week should continue to triage
reports when possible, especially to close duplicates or handle related reports
to those they have already triaged.

Team members remain responsible for their own assigned reports.

### HackerOne Process

GitLab utilizes [HackerOne](https://hackerone.com/gitlab) for its bug bounty program. Security researchers can report vulnerabilities in GitLab applications or the GitLab infrastructure via the HackerOne website. Team members authorized to respond to HackerOne reports use procedures outlined here.
The `#hackerone-feed` Slack channel receives notifications of report status changes and comments via HackerOne's Slack integration.

For information or questions about the GitLab HackerOne program, please contact

- [James Ritchey](https://gitlab.com/jritchey) - Primary Program Manager, or
- [Ethan Strike](https://gitlab.com/estrike) - Secondary Program Manager

#### Working the Queue

- When beginning work on a report, the security team member should assign the
report to themselves immediately.
- It is OK to take a report that you will not work on immediately, especially
if it is a duplicate or related to another report you are familiar with, just
be sure to get it reassigned if you won't be able to meet the estimated triage time.
- When starting a triage work cycle, team members should prioritize as follows:
  1. Identify, triage, and [escalate any severity::1/priority::1](./application-security/handling-s1p1.html) issues first.
  1. Close duplicate and invalid reports.
  1. Triage further using Sort by "Oldest" reports.

  If a reporter has questions about the order of report responses, `06 - Duplicates/Invalid Reports Triaged First` common response may be used.
- Conduct initial communication with the reporter and investigation, using the
following guidelines as necessary:
    - [Request clarification](#if-a-report-is-unclear)
    - Attempt to verify the report and triage the vulnerability.
- Potential, non-bounty outcomes:
    - Report is out-of-scope. If actionable, issues may still be created, but
    further process may not be followed see [violating the rules](#if-a-report-violates-the-rules).
    - Report is a `~feature` as defined above and would not need to be
    made confidential or scheduled for remediation. An issue can be created, or
    requested that the reporter creates one if desired, but the report can be
    closed as "Informative".
    - Report is otherwise [Informative, Not Applicable, or Spam](#closing-reports-as-informative-not-applicable-or-spam).
    For example, we've gotten a number of reports for [inline HTML in markdown](https://docs.gitlab.com/ee/user/markdown.html#inline-html)
    that do not exceed the capabilities of markdown itself.
    - Report is a duplicate. Verify that the issue was not previously reported in HackerOne, or
    that an issue does not already exist in GitLab. If it is a duplicate:
        - Change the state of the report to "Duplicate".
        - If the issue was previously reported in H1, include the report id, as it can
        impact the reporter's reputation
        - Fill in the `01 - Duplicate` common response. Include the link to the GitLab issue.
        - The team member may use their discretion if the reporter asks to be added as a contributor to the original H1 report;
        however, the default is to not add because the corresponding GitLab issue will
        be made public 30 days after the patch is released. If it is decided to add the
        duplicate reporter, ensure that the report does not have reporter sensitive information before allowing access.
        `05 - Duplicate Follow Up, No Adding Contributors/Future Public Release` common response
        can be used when denying the request to add as a contributor.
- If the report is valid, in-scope, original, and requires action, security-related documentation change, or further investigation by
the responsible engineering team:
    - Verify and/or set the appropriate Severity in H1
    - Verify and/or set the appropriate Weakness in H1
    - If the report is [permissions related](https://gitlab.com/gitlab-com/gl-security/security-guidelines/blob/master/permissions.md), check for similar issues in the API, GraphQL, and Elasticsearch, as appropriate. Also check with alternate authentication mechanisms like Deploy Tokens, Deploy Keys, Trigger Tokens, etc.
    - Add your initial [suggested bounty](https://docs.hackerone.com/programs/bounties.html#suggesting-bounties) in H1
        - If the severity is Medium or higher, award a bounty of $1000 when the report is triaged. See [GitLab's H1 Policy](https://hackerone.com/gitlab), under `Rewards`
        - If the report is a security-related documentation change, the bounty will be $100
    - Import the report into a GitLab issue using `/h1import <report> [project]` in Slack
        - Verify the Severity/Priority assigned by `h1import` ([Severity and Priority](#severity-and-priority-labels-on-security-issues))
        - On the imported issue:
            - Assign the appropriate [Due Date](#due-date-on-security-issues)
            - Have a proper [`How to reproduce`](#reproducibility-on-security-issues) section
        - If the report is a security-related documentation change, add the `~documentation` label
    - @-mention product manager of appropriate teams for scheduling and/or the engineering managers if additional engineering feedback is required to complete the triage, based on the [product categories page](../handbook/product/product-categories/)
        - add labels (`/label ~` command) corresponding to the [DevOps stage](/handbook/product/product-categories/#devops-stages) and source group (consult the [Hierarchy](/handbook/product/product-categories/#hierarchy) for an overview on categories forming the hierarchy)
        - As applicable, notify relevant team members via the issue, chat, and email, depending on the chosen security level.
    - Change the state of the report to "Triaged" in HackerOne and include a link to the issue as the reference.
        - Fill in the comment using the `00 - Triaged` Common response as a template.
        - In the comment, include link to the confidential issue
    - If full impact is needed to be assessed against GitLab infrastructure, instead of testing in https://gitlab.com, use https://staging.gitlab.com/help to sign in with your GitLab email account
        - If multiple users are needed, use credentials for users gitlab-qa-user* stored in 1password Team Vault to access the staging environment
- Discussion and remediation of vulnerabilities can sometimes take longer than we would prefer. Even so, frequent communication with reporters is far better than leaving reporters in the dark, even if our progress is slow. Therefore:
    - Once the corresponding GitLab issue has been assigned a milestone, an
    automated process will add a comment to the H1 report with the planned
    fix date. If the issue has not been assigned to a milestone within **1 week**
    of the product manager being @ mentioned on the issue, follow up with
    the product management team.
    - In the case where fixes are not as clear or discussion is still
    on-going as to whether a patch will be created at all, reporters should
    be notified of updates at least **monthly**.
    - Awards may be paid in advance of a confirmed fix by the following review
      process to insure 1) the report is not duplicated by other active reports and
      2) consistency in award amounts:
      - Post a note on the current [~"bug bounty council"](https://gitlab.com/gitlab-com/gl-security/security-department-meta/issues?scope=all&utf8=%E2%9C%93&state=opened&label_name[]=Bug%20Bounty%20Council) issue, following the
        format in the template, which includes a brief description and suggested
        bounty amount.
        - Wait for at least two thumbs up from other members of the team.
        - The `04 - Bounty Award / Reviewed and Awarded Prior to Fix` can be used
        as the template for the bounty award if approved.
    - In any case, no report should go "stale" where updates are not provided within the last month.

#### Application Security Engineer Procedures for severity::1/priority::1 Issues

Please see [Handling severity::1/priority::1 Issues](./application-security/handling-s1p1.html)

#### If a Report is Unclear

If a report is unclear, or the reviewer has any questions about the validity of the finding or how it can be exploited, now is the time to ask. Move the report to the "Needs More Info" state until the researcher has provided all the information necessary to determine the validity and impact of the finding. Use your best judgement to determine whether it makes sense to open a confidential issue anyway, noting in it that you are seeking more information from the reporter. When in doubt, err on the side of opening the issue.

One the report has been clarified, follow the "regular flow" described above.

#### If a Report Violates the Rules of Engagement

If a report violates the rules of GitLab's bug bounty program use good judgement in deciding how to proceed. For instance, if a researcher has tested a vulnerability against GitLab production systems (a violation), but the vulnerability has not placed GitLab user data at risk, notify them that they have violated the terms of the bounty program but you are still taking the report seriously and will treat it normally. If the researcher has acted in a dangerous or malicious way, inform them that they have violated the terms of the bug bounty program and will not receive credit. Then continue with the "regular flow" as you normally would.

#### Closing reports as Informative, Not Applicable, or Spam

If the report does not pose a security risk to GitLab or GitLab users it can be closed without opening an issue on GitLab.com.

When this happens inform the researcher why it is not a vulnerability. It is up to the discretion of the Security Engineer whether to close the report as "Informative", "Not Applicable", or "Spam". HackerOne offers the following guidelines on each of these statuses:

- Informative: Report contained useful information but did not warrant an immediate action.
- Not Applicable: Report was invalid, ineligible, or irrelevant.
- Spam: Report is not a legitimate attempt to describe a security issue.

We mostly use the "Informative" status for reports with little to no security impact to GitLab and "Not Applicable" for reports that show a poor understanding of security concepts or reports that are clearly out of scope. "Spam" results in the maximum penalty to the researcher's reputation and should only be used in obvious cases of abuse.

#### Breakdown of Effective Communication

Sometimes there will be a breakdown in effective communication with a reporter. While this could happen for multiple reasons, it is important that further communication follows [GitLab's Guidelines for Effective and Responsible Communication](/handbook/communication/#effective--responsible-communication-guidelines). If communication with a reporter has gotten to this point, the following steps should be taken to help meet this goal.

- Take a step back from the situation. Do not respond immediately.
- Seek advice from the H1 triage engineer or, if you are more comfortable, a manager on how best to move forward.
- Consider writing the response multiple times, and have the response reviewed by the person you consulted.
- Once diffused, if the general situation is not currently documented, open an MR to the handbook on how it can be handled in the future.

#### Reports potentially affecting third parties

When GitLab receives reports, via HackerOne or other means, which might affect third parties the reporter will be encouraged to report the vulnerabilities upstream. On a case-by-case basis, e.g. for urgent or critical issues, GitLab might proactively report security issues upstream while being transparent to the reporter and making sure the original reporter will be credited. GitLab team members however will not attempt to re-apply unique techniques observed from bug bounty related submissions towards unrelated third parties which might be affected.

#### Awarding Ultimate Licenses

GitLab reporters with 3 or more valid reports are eligible for a 1-year Ultimate license for up to 5 users. As per the [H1 policy](https://gitlab.com/gitlab-com/gl-security/hackerone/configuration/-/blob/master/program-policy.md#gitlab-ultimate-license), reporters will request the license through a comment on one of their issues. When a reporter has requested a license, the following steps should be taken:

1. Validate that the three reports were valid. That means they are `Triaged` or `Resolved`.
1. Validate that the three reports have not been used to obtain a previous license.
1. If the reports are not valid, respond to the reporter on H1 explaining the reason the license is not being issued.
1. If the reports are valid, create the license on `https://license.gitlab.com`,
    - For `Name` use the reporters fullname if available, otherwise their H1 handle
    - For `Company` use `H1 Reporter Award`
    - For `Email` use the reporter's `[username]@wearehackerone.com` email address
    - `User Count` is up to 5
    - `GitLab Plan` is `Ultimate`
    - The license should start the day of issue and expire in 1 year
1. Enter the associated license information in the [H1 License Award sheet](https://docs.google.com/spreadsheets/d/1qJZ9jfIvQuSU5u4odj4Db_CRKJ_GHegtSZQvJx36FUE/edit)
1. Reply to the report on H1 use the `20 - Ultimate License Creation` template.

The license will be sent to the reporter by the License app. If the reporter claims that the license has not arrived, the app can be used to resend the license.
When that happens, the creation of a new license should be avoided.

### Security Dashboard Review

**Frequency:** Daily

AppSec engineers are responsible for triaging the findings of the GitLab security tools. This role has two primary functions.

1. Validate the findings and handoff to engineering for correction
1. Provide feedback to the Secure team

For the dashboards to review, please see [triage rotation](#triage-rotation) above.

#### Validation

For each finding:

- Using the information provided and any additional information, determine if the finding is valid
- For a valid report:
    - Change the status to `Confirmed`
    - Click `Create Issue`
    - Assign [Priority and Severity labels](#severity-and-priority-labels-on-security-issues) based on the finding rating and the impact on GitLab
    - Assign a [Due Date](#due-date-on-security-issues)
    - add labels (`/label ~` command) corresponding to the [DevOps stage](/handbook/product/product-categories/#devops-stages) and source group (consult the [Hierarchy](/handbook/product/product-categories/#hierarchy) for an overview on categories forming the hierarchy)
    - @-mention product manager of appropriate teams for scheduling and/or the engineering managers if additional engineering feedback is required to complete the triage, based on the [product categories page](../handbook/product/product-categories/)
        - If an appropriate engineering team is not immediately apparent, ping an Appsec manager for help identifying the owner
- For an invalid report:
    - Change the status to `Dismissed`
    - Leave a comment providing feedback on why the vulnerability is being dismissed. This information can be used by Secure engineers in tuning the findings of the tool and is also useful if we ever wonder why it was dismissed at some point in the future.

#### Dependency Updates

If a vulnerability is identified in a product dependency, the appsec engineer should follow the [security development workflow](https://gitlab.com/gitlab-org/release/docs/blob/master/general/security/developer.md) to create a merge request to update the dependency in all supported versions. The merge request should be opened in the [GitLab Security repo](https://gitlab.com/gitlab-org/security/gitlab) so that the dependency gets updated in supported backports as well. Vulnerabilities determined to be `Critical` or `High` should have merge requests created when identified. `Medium` and `Low` vulnerabilities will be addressed by best effort, but always within the 90-day SLA.

The goal of this process is to update dependencies as quickly as possible, and reduce the impact on development teams for minor updates. In the future, this step could be replaced by [auto remediation](https://gitlab.com/gitlab-org/gitlab/issues/37452).

**If an upgrade to a new major version is required**, it might be necessary for the update to be handled directly by the responsible development team.

- Complete the [Validation](#validation) process above.
- Create an issue in the [GitLab Security repo](https://gitlab.com/gitlab-org/security/gitlab/issues) issue tracker using the `Security developer workflow` template.
- Follow the template to create a merge request targeting the `master` branch.
- If the resulting pipeline is clean, continue with the developer checklist in preparation for merging. This must include reviews by a reviewer and maintainer.
- If the pipeline fails, work with the responsible engineering team to remediate. Depending on the cause, it may be necessary for a developer with advanced knowledge of the dependency functionality to review the change. If a developer is not immediately available, continue to track the issue/MR to ensure remediation within the defined SLA.

### When a Patch is Ready

When a patch has been developed, tested, approved, merged into the security branch, and a new security release is being prepared it is time to inform the researcher via HackerOne. Post a comment on the HackerOne issue to all parties informing them that a patch is ready and will be included with the next security release. Provide release dates, if available, but try not to promise a release on a specific date if you are unsure.

This is also a good time to ask if they would like public credit in our release blog post and on our vulnerability acknowledgements page for the finding. We will link their name or alias to their HackerOne profile, Twitter handle, Facebook profile, company website, or URL of their choosing. Also ask if they would like the HackerOne report to be made public upon release. It is always preferable to publicly disclose reports unless the researcher has an objection.

#### CVE IDs

We use CVE IDs to uniquely identify and publicly define vulnerabilities in our products. Since we publicly disclose all security vulnerabilities 30 days after a patch is released, CVE IDs must be obtained for each vulnerability to be fixed. The earlier obtained the better, and it should be requested either during or immediately after a fix is prepared.

We currently request CVEs either through the HackerOne team or directly through MITRE's [webform](https://cveform.mitre.org/). Keep in mind that some of our security releases contain _security related_ enhancements which may not have an associated [CWE](https://cwe.mitre.org/) or vulnerability. These particular issues are not required to obtain a CVE since there's no associated vulnerability.

### On Release Day

On the day of the security release several things happen in order:

- The new GitLab packages are published.
- All security patches are pushed to the public repository.
- The public is notified via the GitLab blog release post, security alerts email, and Twitter.
- The vulnerability acknowledgements page is updated with appropriate credits to the reporting researchers.

Once all of these things have happened notify the HackerOne researcher that the vulnerability and patch are now public. The GitLab issue should be closed and the HackerOne report should be closed as "Resolved". Public disclosure should be requested if they have not objected to doing so. Any sensitive information contained in the HackerOne report should be sanitized before disclosure.

### Swag for Reports

GitLab awards swag codes for free GitLab swag to any reports that result in a security patch. Limit: 1 per reporter. When a report is closed, ask the reporter if they would like a swag code for free GitLab clothing or accessories. Swag codes are available by request from the marketing team.

### Handling Disruptive Researcher Activity

Even though many of our 3rd-party dependencies, hosted services, and the static
`about.gitlab.com` site are listed explicitly as out of scope, they are sometimes
targeted by researchers. This results in disruption to normal GitLab operations.
In these cases, if a valid email can be associated with the activity, a warning
such as the following should be sent to the researcher using an official channel
of communication such as ZenDesk.

```
Dear Security Researcher,

The system that you are accessing is currently out-of-scope for our bounty
program or has resulted in activity that is disruptive to normal GitLab
operations. Reports resulting from this activity may be disqualified from
receiving a paid bounty. Continued access to this system causing disruption to
GitLab operations, as described in policy under "Rules of Engagement,
Testing, and Proof-of-concepts", may result in additional restrictions on
participation in our program:

  Activity that is disruptive to GitLab operations will result in account bans and disqualification of the report.

Further details and some examples are available in the full policy available at:

https://hackerone.com/gitlab

Please contact us at security@gitlab.com with any questions.

Best Regards,

Security Department | GitLab
security@gitlab.com
/handbook/engineering/security/
```

## External Code Contributions

We have a process in place to conduct security reviews for externally contributed code, especially if the code functionality includes any of the following:

- Processing credentials/tokens
- Storing credentials/tokens
- Logic for privilege escalation
- Authorization logic
- User/account access controls
- Authentication mechanisms

The Security Team works with our Community Outreach Team to ensure that security reviews are conducted where relevant. For more information about contributing, please reference the [Contribute to GitLab](/community/contribute/) page.

## Vulnerability Management

Vulnerability Management is the recurring process of identifying, classifying, prioritizing, mitigating, and remediating vulnerabilities. This overview will focus on infrastructure vulnerabilities and the operational vulnerability management process. This process is designed to provide insight into our environments, leverage GitLab for vulnerability workflows, promote healthy patch management among other preventative best-practices, and remediate risk; all with the end goal to better secure our environments.

To achieve these goals, we’ve partnered with Tenable and have deployed their software-as-a-service (SaaS) solution, [Tenable.io](https://www.tenable.com/products/tenable-io/faq), as our vulnerability scanner. Tenable.io allows us to focus on what is important; scanning for vulnerabilities, analyzing, and ingesting vulnerability data into GitLab as the starting point for our vulnerability management process. For more information, please visit the [vulnerability management overview](/handbook/engineering/security/vulnerability_management/#the-vulnerability-management-process).

## Package Signing

{: #package-signing}

The packages we ship are signed with GPG keys, as described in the [omnibus documentation](https://gitlab.com/gitlab-org/omnibus-gitlab/blob/master/doc/package-information/signed_packages.md). The process around how to make and store the key pair in a secure manner is described in [the runbooks](https://gitlab.com/gitlab-com/runbooks/-/blob/master/docs/packaging/manage-package-signing-keys.md). The Distribution team is responsible for updating the package signing key. For more details that are specific to key locations and access at GitLab, find the internal google doc titled "Package Signing Keys at GitLab" on Google Drive.

## Annual 3rd-Party Security Testing

Along with the internal security testing done by the [Application Security](#application-security), [Security Research](#security-research), and [Red](/handbook/engineering/security/red-team/) teams, GitLab annually contracts a 3rd-party penetration test of our infrastructure. For more information on the goals of these exercises, please see our [Penetration Testing Policy](/handbook/engineering/security/penetration-testing-policy.html).

The following process is followed for these annual tests:

1. The Application Security team will partner with the [Security Operations](#security-operations) and other releveant teams to define the scope of the test.
1. The Infrastructure team will be notified in accordance with their [procedures](/handbook/engineering/infrastructure/production/#penetration-testing)
1. The Application Security team will manage the relationship with the 3rd-party vendor. Included in this role will be communicating the chosen scope and soliticing feedback.
1. Based on feedback from all parties, testing dates will be defined and communicated to teams for appropriate actions.
1. Testing will be done by the 3rd-party vendor and the results communicated to GitLab.
1. The Application Security team will triage the findings and create issues in accordance with the [Issue Triage](#issue-triage) process.

### Obtaining the Report

GitLab customers can request a redacted copy of the report. For steps on how to do so, please see our [External Testing page](https://about.gitlab.com/security/#external-testing).
