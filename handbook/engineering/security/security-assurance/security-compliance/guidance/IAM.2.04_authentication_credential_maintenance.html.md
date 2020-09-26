---
layout: markdown_page
title: "IAM.2.04 - Authentication Credential Maintenance"
---
 
## On this page
{:.no_toc}
 
- TOC
{:toc}
 
# IAM.2.04 - Authentication Credential Maintenance
 
## Control Statement
Authorized personnel verify the identity of users before modifying authentication credentials on their behalf.
 
## Context
Verifying the identity of users before making authentication changes prevents attackers from impersonating someone in order to gain access to their credentials.
 
## Scope
This control applies to:
   * GitLab.com
   * System that support the operation of GitLab.com
   * All applications that store or process financial data

## Ownership
*  Control Owners:
    *  IT Ops
*  Process owner:
    * IT Ops
    * SecOps

## Guidance
For the remediation of this control these are the steps that should be followed:
* validate process that support users to verify account ownership and ensure that this is documented
* validate process that IT Helpdesk/IT Ops uses to verify account ownership and ensure that this is documented
* validate process that Tech Stack system owners use to verify account ownership and ensure that this is documented


## Additional control information and project tracking
Non-public information relating to this security control as well as links to the work associated with various phases of project work can be found in the [Authentication Credential Maintenance issue](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/815)  


### Policy Reference
*  /handbook/business-ops/tech-stack-applications/
*  /handbook/support/workflows/account_verification.html

 
## Framework Mapping
* ISO
   * `A.9.2.4` - Management of secret authentication information of users
The allocation of secret authentication information shall be controlled through a formal management process.
   * `A.9.3.1` - Use of secret authentication information: Users shall be required to follow the organization’s practices in the use of secret authentication information.
* PCI
   * `8.2.2` - Verify user identity before modifying any authentication credential—for example, performing password resets, provisioning new tokens, or generating new keys.
