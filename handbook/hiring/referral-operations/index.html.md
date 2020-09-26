---
layout: handbook-page-toc
title: "Referral Operations"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Referral Operations

This page is for information regarding the “backend” of the [Referral Process](/handbook/hiring/referral-process/).

#### Adding a Referral to BambooHR (People Experience)

During the onboarding process, a People Experience Associate will complete the following steps if a new team member was referred by current team member.

1. Ensure that the current team member is eligible for a referral based upon the [requirements](/handbook/hiring/referral-process/#referral-bonus-eligibility).
2. Review when the referral was submitted in Greenhouse
    * `Job` > `Application Review` > `Applied On YYYY-MMM-DD`
    * If the referral was submitted **on or before 2020-04-09**, then the following referral amounts apply:
        * $1,000 base referral bonus for a new hire.
        * $500 supplemental referral bonus for a hire from a Location factor less than 0.65.
        * $1,000 supplemental referral bonus for a hire from an underrepresented group.
    * If the referral was submitted **after 2020-04-10**, then refer to the bonus amounts listed [here](/handbook/incentives/#referral-bonuses).
3. Add a note in the new team member's BambooHR profile with the name of their referrer.
4. Open the Current Team Members BHR profile
    * `Job` tab > `Bonus` table > `Add Bonus`
    * Add the `Bonus Date` = `90 day + Hire Date`
    * `Bonus Amount`: Review above
    * `Bonus Type`: Referral Bonus
    * `Bonus Comment`: "Referred (New Team Members) - submitted on (submit date) and add if location factor or underrepresented group"

#### Transferring Referral Submissions to Greenhouse

Per the current [Referral Submission Process](/handbook/hiring/referral-process/#submitting-a-referral), Team Members will submit their referrals via Issues. When a new Issue appears, please do the following:

1. Assign the Issue to yourself (upper right corner).
1. Open Greenhouse and click `+` > `Add a Referral`.
1. Reference the Issue to see what should be entered in the following fields:
    * **Job**
        * If a specific requisition is **not** specified, follow-up with the referring Team Member to determine the appropriate role as "general" referrals are **not** accepted.
    * **First Name** - `Required`
    * **Last Name** - `Required`
    * **Email** - `Required`
    * **Social Media** - `Required`
        * e.g. LinkedIn
    * **Resume** - *Optional*
    * **Relationship** - `Required`
    * **Location** - `Required`
    * **Referral's Email** - `Required`
    * **Work History** - *Optional*
    * **When We Reach Out** - *Optional*
    * **Referral Notes** - *Optional*
1. Click `Add this referral` to submit them.
1. Go to the candidate's profile, click the `Details` tab, and scroll down to the **Source & Responsibility** section.
1. Hover over **Source** and click the `Pencil` icon, then edit `Who Gets Credit` with the name of the *Referrer* and click `Update Source`.
1. In the **Make a Note** box, write something similar to the following:
    * *"Submitting referral on behalf of `REFERRER_NAME` for Req # `XXXX`."*
    * Please be sure to `@-mention` the requisition's *Recruiter*.
1. Send a email to the referred candidate. Select `Email REFERRAL_NAME` in the right column and select the **Default Referral Confirmation Receipt** email template.
    * Make sure that the email is sent from the `no-reply@gitlab` alias.
    * Add the referring Team Member to the `CC` field.
    * Click `Send Email`.
1. Follow-up in the Issue and confirm that the referral has been submitted and please mention that the Team Member will be able to follow their referral in the **My Referrals** section of their Greenhouse dashboard.
1. **Close** the Issue.    

#### How to Respond to Referral Update Requests

The Recruiting Team uses the [GitLab Service Desk](/product/service-desk/) to track incoming emails to the `referral@gitlab` email. These emails will, in turn, show up as `Issues`.

To set-up notifications for the [Referral Service Desk Project](https://gitlab.com/gl-recruiting/referrals), please do the following:

1. Click on the `Bell` icon in the upper right corner (next to `Star` and `Clone`).
1. Go to `Custom Settings`.
1. Click `New Issue`.
1. Close the window.

To take action on Issues in that project:

1. Click `Issues` in the left menu bar.
    * This is where incoming `referral@` emails will be; any open Issues here will need to be addressed.
1. Click on the new `Issue`.
1. Assign it to yourself (upper right corner).
1. Read the Issue.
1. Add the appropriate label(s).
1. Look-up the candidate in Greenhouse, if applicable.
1. Respond to the Issue by commenting and please be sure to do so just as you would with any other GitLab communication.
    * e.g. *"Hi, NAME. Thank you for reaching out about the status of your referral. Per our [SLA](/handbook/hiring/referral-process/#referral-statuses), please allow us 10-days to review the submission. `@RECRUITER` is responsible for this role and they’ll provide the candidate with an update soon."*
   * e.g. *"Thank you for the referral. `@RECRUITER` is responsible for this role and will provide you with an update soon."*
1. Please be sure to `@-mention` the responsible Recruiter so that they’re aware an update is being requested.
1. If one comment addresses the entirety of the message, comment and **close** the Issue. If further information is needed, comment and leave the Issue open.
1. The Recruiter will reassign the Issue to themselves once they pickup the communication. They may also add any applicable labels.
1. The Assignee will **close** the Issue when communication is complete.

#### Referral Roundup Sessions

Our Recruiting Team occasionally organizes *Referral Roundup Sessions*.

The objective of theses sessions are to gather referrals, region-specific information about where you're based, and teach you skills related to sourcing and Greenhouse.

We'll invite Team Members who are based in areas with a location factor *less than or equal to* `.58` to theses sessions.

Each session will have a corresponding Issue linked and in that, we ask that you please add information regarding appropriate companies to source from, local meet-up groups, conferences, job boards to advertise on, and any other information you believe will be beneficial to our recruiting efforts in your area.

A Recruiting Team Member will attend these sessions, so they be able to address any questions that arise on sourcing, LinkedIn, or Greenhouse.

#### Referral Rejection Notifications

In the event that a *Referral* is rejected based on their location factor the following steps will need to be taken by the requisition's **Recruiter**:

1. Send the rejection email to the candidate via Greenhouse using the `Referral Declined - Not ELF` template.
1. Search for the **closed** referral submission Issue for the respective candidate and add the following comment:

> Thank you again for submitting `CANDIDATE_FIRST_NAME` to the `REQUISITION_TITLE` role. 
>
> Unfortunately, we’re unable to move forward with `CANDIDATE_FIRST_NAME`’s candidacy right now because they are located in a higher location factor area. With our [outbound hiring model](https://about.gitlab.com/jobs/faq/#gitlabs-outbound-recruiting-model), the > Recruiting team is focused on building a more diverse team in the most efficient way. This allows us to support our all-remote vision: to spread opportunity to underserved locales, and to influence the increase of wages for remote work outside of metro areas.
>
> `CANDIDATE_FIRST_NAME` has received an email from our team explaining this. We’ve also added some clarity about this in the [Referral Submission Issue Template](https://about.gitlab.com/handbook/hiring/referral-process/#submitting-a-referral) now to be sure team members consider this before they submit their referral. 
>
> We appreciate your understanding and hope you’ll continue to refer talented people to GitLab!

#### Ensuring Referral Confidentiality

Once a week, a Recruiting Operations & Insights Team Member will check to make sure that all submitted referral Issues are marked as `Confidential`. 

To do that, please take the following steps:

1. Navigate to the [Issues](https://gitlab.com/gl-recruiting/referrals/-/issues) section of the Referrals Project.
1. Clicked on `Closed` Issues.
1. Set the following filter: `Confidential = No` and run the search.
1. If any Issues appear, please edit the `Confidentiality` section in the right column.
