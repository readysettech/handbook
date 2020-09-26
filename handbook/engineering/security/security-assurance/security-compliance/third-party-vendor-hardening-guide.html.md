---
layout: markdown_page
title: "Third Party Vendor Hardening Guide"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Third Party Vendor Hardening Guide Overview
Data at GitLab is [classified](/handbook/engineering/security/data-classification-standard.html) 
based on its sensitivity, which is the level of confidentiality that information
requires to protect against unauthorized use. Customer data uploaded into the service, personally identifiable
information of users and team members, and internal information are some examples 
of the more sensitive (i.e. Orange and Red) and thus engagements involving 
these types undergo risk-based assessments and vendor security reviews to identify and
manage risks. This guide should be referenced any time non-public data will be 
handled, managed, stored, accessed or transmitted to third parties or fourth parties.

## Best Practices

Data should be kept on GitLab systems whenever possible and professional service
contractors should only access public data and communication channels. For all 
else the following are steps that business owners can work with their vendors 
processing or storing sensitive data uphold GitLab's security standards:
 
 <br>

### All Vendors (general guidance)

<br>

✅ when sharing information externally is absolutely necessary utilize the granular permissions provided by Google Drive 

✅ sensitive data should be erased immediately upon our request or when a specific need for that data no longer exists (whichever comes first)

✅ protect from unauthorized access by following the [least privilege principle](/handbook/engineering/security/Access-Management-Policy.html#principle-of-least-privilege). For GitLab team members this means to minimize access to only those people who have 
        been previously authorized to access that data and have a legitimate need for that access. As with regular team members, access granted to third parties should be at the lowest level possible to accomplish the specific need

✅ for a list of compensating controls we are beginning to compile, please see the [Vendor Observations and Treatment Catalog](https://docs.google.com/spreadsheets/d/1llZkgIQMwky91YQBH40qfvs_BQR5z7Np81tczCJg0Bo)


<br>

### Vendors Providing Services and Tools

<br>

✅ vendor should participate in independent third party technical assessments

✅ vendor ensures all risks are addressed within a timely fashion, prioritizing critical and high risks

✅ if the system is hosted on AWS, S3 bucket configurations need to keep the hosted data from being visible to the public

✅ the system(s) use the minimum encryption standards for data in transit and at rest as defined in our [security controls](handbook/engineering/security/sec-controls.html#data-management)

✅ the system(s) supports logging and monitoring that can be ingested into our internal security tooling, such as a SIEM

✅ the system(s) use the minimum encryption standards for data in transit and at rest as defined in our [security controls](hhandbook/engineering/security/sec-controls.html#data-management)

✅ enable 2-Factor authentication when possible


<br>

### Vendors Providing Physical Services (Field Marketing) 

<br>

✅ when sending gifts to individuals, consider if the individual is knowingly providing their address for the shipment (consent). If not, request for a vendor review to be performed on the engagement to ensure GitLab is not introducing the risk of mishandling of personal data 

✅ shippers should only receive personal data by secure means such as by sharing through a document controlled by GitLab where access can be revoked once completed 

✅ also ask for the shipper to securely dispose of any of information that may exist outside of the document, such as physical lists and labels


<br>

### Vendors providing Temporary Contract Services (working as GitLab team-members)

<br>

✅ if vendor is providing contractor services that includes access to sensitive data via email or Slack, and/or access to GitLab systems that houses sensitive data, 
   the vendor must undergo equivalent onboarding activities as a regular GitLab team member. This includes completing a Non-Disclosure Agreement, background checks, security awareness training and review the [code of conduct](/handbook/people-group/code-of-conduct/). Please reference the [recruiting process](/handbook/hiring/recruiting-framework/ces-contract-processes/) and onboarding process for [U.S. based consultants](/handbook/people-group/general-onboarding/onboarding-processes/#onboarding-for-us-based-consultants)
 
 <br>
 
### Free Apps

<br>

✅ review the user terms to understand if the app will integrate with any of our systems (e.g. Chrome extension, bots, Calendar tools) and the information it will access. If it is non-public data, strongly consider reqeusting a security review to verify we are not introducing risk to GitLab by using the tool. Please review the [instructions](/handbook/engineering/security/security-assurance/security-compliance/third-party-vendor-security-review.html#free-apps) on this in the Third Party Vendor Security Review process
