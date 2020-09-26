---
layout: markdown_page
title: "Tech Stack Applications"
extra_js:
  - libs/vue.min.js
  - bundles/tech-stack.js
---

## Tech Stack Support Hierarchy

1. Business and technical owners
1. IT Team

Business and technical owners will remain the point of contact for provisioning and issues involving administration of the systems they manage. The IT team empowers business and technical owners to maintain accountability for tech systems through efforts involving automation, monitoring, and visibility.

## Tech Stack Documentation

- [Tech Stack Google Sheet:](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit?usp=sharing) contains information about who the business owners, technical owners, provisioners, data gathered, etc
    - Tech Stack definitions: 
        - Business Owner: The Business Owner is the individual(s) responsible for all budget and decision making around the tool. They should define how the tool is used and by whom. This person(s) usually has login access to the tool as `Owner` but login access isn't necessary in all cases. Please make sure you list individual people in this field, rather than teams. 
        - Technical Owner: The Technical Owner(s) are all of the `administrators` of a tool. This includes everyone with the administrative clearence to provision and deprovision access of a tool and/or as the technical expertise needed to manage it. 
        - Provisioner/Deprovisioner: People in charge of granting and removing team member access to a tool. At least two provisioners/deprovisioners should be named for every tool in the handbook. Provisioners can be contacted as a group in Slack using the `@provisioners` handle and in GitLab using the `@tech-stack-provisioner` handle.
- [Tech Stack Overview:](/handbook/business-ops/tech-stack/) provides an overview of how GitLab uses the tool.

## Tech Stack Updates

#### [**Add new system to the tech stack**](https://gitlab.com/gitlab-com/business-ops/Business-Operations/-/issues/new?issuable_template=Add%20New%20System%20to%20Tech%20Stack%20Application%20List)

This template is necessary for: 
- Adding a new tool to the Tech Stack Google sheet


#### [**Update Tech Stack Information**](https://gitlab.com/gitlab-com/business-ops/Business-Operations/-/issues/new?issuable_template=Update%20Tech%20Stack%20Information) (including offboarding of systems)

This template is necessary for: 
- Updating information around a system/application listed in our Tech Stack Google sheet including Business Owner, Technical Owner, who should have access, group owner, business purpose, etc.
- Removing a system/application from the Tech Stack.

#### [**Update Tech Stack Provisioner**](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Update_Tech_Stack_Provisioner)

This template is necessary for:
- Adding/removing Tech Stack provisioners from the Tech Stack Google Sheet. Please keep in mind we recommend to have more than 1 provisioner listed in the tech stack so that there is coverage for access requests in case of paid time off. 

## Tech Stack offboarding

Occasionally systems listed in our tech stack will be deprecated. If a system is being offboarded (no longer being used and/or being replaced) an issue will need to be submitted to have the system removed from our tech stack. [Submit and issue.](https://gitlab.com/gitlab-com/business-ops/Business-Operations/issues/new?issuable_template=Update%20Tech%20Stack%20Information) Once the issue has been submitted, the Business Owner will need to work with Legal and IT Compliance to ensure that the data deletion process is being completed as outlined in the vendor contract regarding their process and responsibilities. 

## Other related processes

### Access Requests

Please review our [Access Requests handbook page](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/) to find more information on how to request access to systems. Choose the right template for your use case and follow the instructions. 

### Support
Are you experiencing issues with an application/system? Visit our [Tech Stack Google sheet](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit#gid=0) and under `Group Owner/Slack Channel`, you can find out what Slack channel you need to reach out to request support. 

### Procurement
Do you want to procure a new application/system? Visit the [Procurement handbook page](/handbook/finance/procurement/) to find out more information on how to get started. Only applications which go through this process can be added to the tech stack.

<div id="js-tech-stack-overview"></div>
