---
layout: handbook-page-toc
title: "GitLab.com DMCA Removal Requests"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

----

## Overview

This worklow stipulates the steps that need to be taken when receiving DMCA take down requests for users who host copyrighted content belonging to others. Follow the guide below on how to handle incoming requests for GitLab.com.

**DMCA complaints have a 24 hour Service Level Agreement.**

## Workflow

### First 24 hours

 **Note:** If the DMCA is originating from Google, refer to [Abuse-DMCA-Google](https://gitlab.com/gitlab-com/gl-security/Abuse-DMCA/Abuse-DMCA-Google) for further guidance.

1. Review the notice and confirm that the content is still live.
2. Create a `confidential` issue in [Abuse-DMCA-Zendesk](https://gitlab.com/gitlab-com/gl-security/Abuse-DMCA/Abuse-DMCA/issues) using [GitLab_DMCA_Issue](https://gitlab.com/gitlab-com/gl-security/Abuse-DMCA/Abuse-DMCA/blob/master/.gitlab/issue_templates/gitlab_issue_templates_dmca_gitlab_issue_templates_dmca_servicedesk.md)
3. Assign the issue to Legal and comment on the issue for Legal to review. Legal will leave a comment on the issue once the notice has been reviewed. 

#### Valid Notice

1. Forward the notice to the defendant in a new Zendesk ticket using the `DMCA::Notice to Content 'Owner'::First Touch` macro. Set the requester and Cc email to the email address(es) belonging to the GitLab.com user and paste the content of the forwarded notice into the space provided. The macro should set the ticket on-hold and re-open in 24 hours.
1. Remove any `Personal Identifiable Information (PII)`
1. In the content owner ticket, also add an internal note referencing the DMCA Meta Issue.
1. In the GitLab_DMCA_Issue, paste the contents of `DMCA::Notice to Legal::First Touch` into a note and add the link to the owner contact ticket.

### Next 24 hours

1. Confirm whether the content is still live. If the content has been removed, add an internal note and resolve the ticket.
1. Respond to the original requester using the `DMCA::Requestor reply takedown complete` macro.  
1. If the content is still live and the user has not responded, proceed to send a follow up notice to them using the `DMCA::Notice to Content 'Owner'::Second Touch` macro.
1. In the GitLab_DMCA_Issue, add a note with the contents of the `DMCA::Notice to Legal::Second Touch` macro.

### Taking Action

If the content still remains active and the user has not responded to the notice:

1. Pull up the projects in question and make them private, then block the user.
1. Ensure that your internal note indicates the original state of the projects in question (i.e., `Were the projects already private and which users had access?`).
1. Send another follow-up to the defendant, this time informing them that action has been taken, using the macro `DMCA::Notice to Content 'Owner'::Final Touch (takedown)`.
1. In the GitLab_DMCA_Issue Issue, add a note with the contents of the `DMCA::Notice to Legal::Final Touch` macro and add any additional relevant information.

### Service Desk Requests - dmca@gitlab.com

1. For `Service Desk` DMCA requests, post a public comment to the original issue [Service-Desk](https://gitlab.com/gitlab-com/gl-security/Abuse-DMCA/SD/issues)

> Note:  The `Service Desk` issue is public and any correspondence on the issue will be sent to the requestor.  Make sure any URL(s) in the response have been sanitized.

## User disputes a takedown notice
If the user disputes the takedown request, the user should have submitted a valid counter-notice.

1. Use the `DMCA::Acknowledge Counter Receipt` macro.
1. Paste the contents of the counter-notice in a note in the GitLab_DMCA_Issue and @-mention Legal for review.
1. If the counter-notice is determined to be valid, Legal will add an internal note whether it is a valid notice.

### Valid Counter-Notice

1. If the counter-notice is valid and vetted by Legal, forward the notice on to the plaintiff (original requester).
1. Still follow the steps in the [Taking Action](#taking-action) section above even though the owner has responded.

### Invalid Counter Notice

1. If the counter-notice is invalid after being vetted by Legal, proceed with steps stipulated in [Taking Action](#taking-action).

### Content No Longer Available

1. If the content is no longer available, respond to the requestor with the [Content no longer available](https://gitlab.com/gitlab-com/gl-security/abuse/blob/master/Blurbs/Abuse_Reporter_Blurbs.md#content-no-longer-available-dmca)

### Reactivating the content
If there was a valid counter-notice and no response has been received from the plaintiff within 10 days of the counter-notice being forwarded, proceed with the following steps:

1. Pull up the projects in question returning them to the original state and account. Refer to notes made in step 2 under [Taking Action](#taking-action).
1. Add an internal note to the defendant and plaintiff tickets leaving it resolved.

## Macros

### `DMCA::Notice to Legal::First Touch`

```
I have forwarded the notice to the user and marked it on-hold for 24 hours before the next follow up.

Ticket #
```

### `DMCA::Notice to Legal::Second Touch`

```
- No response from user.
- Content is still live.
- Follow up sent. 
- On-hold for 24 hours before taking action. 
```

### `DMCA::Notice to Legal::Final Touch`

```
- No response from user.
- Content made private.
- Account blocked.
- Notice sent to user.
```

