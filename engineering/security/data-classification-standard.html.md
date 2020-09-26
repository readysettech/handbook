---
layout: handbook-page-toc
title: "GitLab Data Classification Standard"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

# Data Classification Standard

## Purpose
The Data Classification Standard defines data categories and provides a matrix of security and privacy controls for the purposes of determining the level of protection to be applied to GitLab data throughout its lifecycle.

## Scope 
The Data Classification Standard applies to all GitLab team members, contractors, consultants, vendors and other service providers that handle, manage, store or transmit GitLab data.

## Roles and Responsibilities

### GitLab Responsibilities
* GitLab team members, contractors, consultants, vendors and other service providers are required to review and understand this policy, and to handle data according to the classification levels below unless otherwise noted.  

* Data Owners shall determine the classification of data in accordance with this standard. The Data Classification Index (internal only) provides a list of various types of data and their classification level. If you cannot identify the data element or are uncertain of the risk associated with the data and how it should be classified and handled, please contact The Security Compliance Team.				

### Customer Responsibilities
* GitLab customers are responsible for managing their own data, to include identification and classification according to their own internal requirements. GitLab handles Customer Data internally according to our non-disclosure obligations written in our Mutual Non Disclosure Agreement and the controls identified in this standard. 

## Definitions

* Personal Data: As defined by [General Data Protection Regulation(GDPR)](https://gdpr.eu/article-4-definitions/): ‘personal data’ means any information relating to an identified or identifiable natural person (‘data subject’); an identifiable natural person is one who can be identified, directly or indirectly, in particular by reference to an identifier such as a name, an identification number, location data, an online identifier or to one or more factors specific to the physical, physiological, genetic, mental, economic, cultural or social identity of that natural person.

* Customer Data: Refers to the electronic data uploaded or created by GitLab customers and processed in the GitLab application labeled as Private by the customer and subject to legal or contractual obligations. 

## Data Classification Levels

Examples of each data type: [See Data Classification Index](https://docs.google.com/spreadsheets/d/1eNuSLuBcZWQe13SV1TfEjtNdCOZw7G7ofY9A42Y0sPA/edit#gid=797822036)

### RED
Restricted and must remain confidential. This is GitLab’s most sensitive data and access to it should be considered privileged and must be explicitly approved. Exposure of this data to unauthorized parties could cause extreme loss to GitLab and/or its customers. In the gravest scenario, exposure of this data could trigger or cause a business extinction event. 

Examples include:
* Customer Data

### ORANGE
Data subject to laws and regulation that should not be made generally available. Unauthorized access or disclosure could cause significant or financial material loss, risk of harm to GitLab if exposed to unauthorized parties, break contractual obligations, and/or adversely impact GitLab, its partners, employees, contractors, and customers. 

Examples include:
* Personal Data
     * Any vendor who is in possession of any form of Personal Data must have appropriate contractual terms that address GitLab data protection requirements (e.g. a Data Processing Agreement).
* GitLab Intellectual property
* Customer metadata
* Audit logs
* Open security incidents, vulnerabilities and risks

### YELLOW
Data and information that should not be made publicly available that is created and used in the normal course of business. Unauthorized access or disclosure could cause minimal risk or harm and/or adversely impact GitLab, its partners, employees, contractors, and customers. 

Examples include:
* Asset registers
* General internal company communications
* Vendor contracts
* GitLab runbooks/work instructions/manuals/policies/procedures containing data NOT appropriate for [public consumption](https://about.gitlab.com/handbook/communication/#not-public)

### GREEN
Data that is publicly shareable, and does not expose GitLab or its customers to any harm or material impact. 

Examples include:
* [GitLab handbook](https://about.gitlab.com/)
     * Including most GitLab runbooks/work instructions/manuals/policies/procedures
* Public announcements
* [Public product information](https://docs.gitlab.com/ee/README.html)

## Data Classification Standards:
#### Credentials and access tokens are classified at the same level as the data they protect:
Credentials such as passwords, personal access tokens, encryption keys, and session cookies derive their importance from the data they protect. 

#### Combinations of data types may result in a higher system classification level:
If there is more than one data type residing in a system, the system should be classified at the highest data classification level of the data being stored, transmitted or processed on that system. 

#### Labeling:
There is currently no internal requirement to label data according to this standard, however labels are encouraged. By labeling data according to classification level, individuals can quickly refer to this policy for proper handing.
Issues that are confidential must be marked accordingly per our [Communication Handbook Page](https://about.gitlab.com/handbook/communication/). It is up to the data owner to ensure that security and privacy settings are applied as per their own requirements.

### Security and Privacy Controls: 

|  | Access: | Reproduction: | Distribution/ Disclosure: | Storage/Disposal: |
|-|-|-|-|-|
| **Red:** | Business need to know required for approved business functions | All copies of Red data outside of approved system(s) must be pre-approved by both Legal and Security | Do not share publicly | Data must be encrypted at rest |
|  | Manager and data owner approval required | Systems must have security controls equal to or greater than the approved system(s) | Data sharing with internal GitLab team members is authorized by the Data Owner and management after establishing “need-to-know” | Stored or processed on approved GitLab managed systems only unless otherwise approved |
|  | Logging and monitoring of access required |  | Data sharing with non GitLab team members is not allowed unless explicitly approved by Legal and Security | Electronic storage media must be irretrievably erased, degaussed and/or disposed of in a secure fashion |
|  | Quarterly access reviews required |  | API/Integrations must be approved by Security |  |
|  | NDA required (if disclosed to a 3rd party) |  | Data must be encrypted in transit | When information is no longer valid or necessary, it should be completely and permanently destroyed in accordance with the Record Retention Policy. |
|  | Background check required |  |  |  |
| **Orange:** | Business need to know required | May be reproduced for Internal Use only | Do not share publicly | Stored or processed on approved GitLab managed systems only unless otherwise approved |
|  | Data owner approval required | Systems must have security controls equal to or greater than the approved system(s) | May be shared internally on a need to know basis |  |
|  | NDA required |  | Data sharing with non GitLab team members is not allowed unless explicitly approved by data owner and management. Any vendor who is in possession of any form of Personal Data must have appropriate contractual terms that address GitLab data protection requirements (e.g. a Data Processing Agreement) | Data must be encrypted at rest  if stored on third party system |
|  |  |  | Encrypted or otherwise electronically protected when sent to a recipient outside the company |  |
|  |  |  | Email must be marked as confidential | Electronic storage media must be irretrievably erased, degaussed and/or disposed of in a secure fashion |  |
|  |  |  | When information is no longer valid or necessary, it should be completely and permanently destroyed in accordance with the Record Retention Policy. |
| **Yellow:** | Business need to know required | May be reproduced for Internal Use only | Do not share publicly | Normal deletion commands or utilities with operating systems are sufficient for online files. |
|  | NDA required |  | Can be shared internally and externally in alignment with the Acceptable Use Policy | When information is no longer valid or necessary, it should be completely and permanently destroyed in accordance with the Record Retention Policy. |
|  |  |  | Share externally via a secure mechanism (ie password protected zip file, access controlled Google Drive file, etc) |  |
| **Green:**| Public | Public Information requires no special handling | Public Information requires no special handling | When information is no longer valid or necessary, it should be completely and permanently destroyed in accordance with the Record Retention Policy. |