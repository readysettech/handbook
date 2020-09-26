---
layout: handbook-page-toc
title: "Self help and troubleshooting"
---

<link rel="stylesheet" type="text/css" href="/stylesheets/biztech.css" />

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

Please read through this page to find the most common questions GitLab team members encounter. If you cannot find an answer to your question, please find more information on how to contact us at the bottom of the page. If the team has provided you with an answer that isn't listed here, please submit an MR to add it!

## <i class="fas fa-question-circle" id="biz-tech-icons"></i> Frequently asked questions

### 2FA for GitLab and other tools

For 2FA related problems for your GitLab accounts, please use your backup codes or try generating [new ones](https://docs.gitlab.com/ee/user/profile/account/two_factor_authentication.html#generate-new-recovery-codes-using-ssh).

Follow these steps to successfully set up 2FA for your [Google account](https://support.google.com/accounts/answer/185839?co=GENIE.Platform%3DDesktop&hl=en).

When you get a new device, before you get rid of the old one, make sure to set up your authenticator app on the new device.
You will need to log into your accounts with the old device and disable 2FA for your accounts.
Then delete the accounts off the old device and re-enable the 2FA on your accounts on the authenticator app on the new device.
If you still need a 2FA reset, please reach out to #it_help on slack with the system that needs it and the issue you are encountering.

### Forgot my password

We understand sometimes life happens and passwords get forgotten or deleted.
If it is for a system that requires immediate access, please reach out on the slack #it_help channel.
Provide as much information as possible.
Password resets to sensitive systems such as your G Suite account and Okta require a zoom call to verify.

### New to Mac?

A lot of people coming onboard to GitLab have had some sort of exposure to macOS and Apple hardware, if you are one of those people the below link is probably not for you but you still might learn something!

- [Mac tips for Windows switchers](https://support.apple.com/en-us/HT204216)
- [Mac Keyboard Shortcuts](https://support.apple.com/en-us/HT201236) - great to help your productivity!
- [macOS : Catalina New Features](https://www.apple.com/au/macos/catalina/features/) - Apple's newest OS features
- [Got an iPad? - Check out Sidecar!](https://support.apple.com/en-afri/HT210380) - Apple iPad Sidecar
- [How to use mutliple workspaces on Mac](https://support.apple.com/guide/mac-help/work-in-multiple-spaces-mh14112/mac)

### How to Erase a Disk for Mac

If you are keeping your GitLab machine [Laptop Buy Back Policy](/handbook/business-ops/team-member-enablement/onboarding-access-requests/#laptop-buy-back-policy) it is required you wipe the machine and restore to base OS, these instructions will help you accomplish this.

[How to erase a disk](https://support.apple.com/en-us/HT208496)

## Self-Help and Troubleshooting Tips

This section should provide some quick and easy troubleshooting tips anyone can do to possibly remedy an IT issue before reaching out.
This section will be expanding over time so keep an eye out or feel free to contribute if you think something belongs.

### Built-In MacBook Troubleshooting Commands

MacBooks are wonderful laptops, but no laptop is without faults.
You may come across a "wonky" situation with your Mac, so below are some pointers that may help fix common issues.

- Reset your [NVRAM and PRAM](https://support.apple.com/en-us/HT204063) - non-volatile random access memory and parameter RAM stores small amount of information on your Mac, if you experience issues related to what's in the Apple article reseting this might help out.
- Reset the [SMC](https://support.apple.com/en-us/HT201295) - System Management Controller handles some low-level functions like battery management and if you experience issues with fans or internal ports this could help resolve those issues.
    (Note: different models have different reset methods)
- Apple Diagnostics [Hardware Diagnostics](https://support.apple.com/en-us/HT202731)

### Password Reset for Your MacBook

Did you go out for a long well deserved vacation and come back to a completely blank memory on what your laptop password was?
It happens to the best of us!
Apple has you covered.

- Power down the Mac.
- Restart the Mac while also concurrently holding down the Command + R keys (to go to recovery mode); release the keys when Apple logo appears
- Once Mac is restarted select from the menu Utilities > Terminal
- At the window that opens, type `resetpassword`
- Follow onscreen instructions to reset

### Battery Cycle Count

Want to see the health of your battery? Generally the laptops that we use have a maximum battery cycle life of 1000, you can check it below

- Battery Cycle Count [Battery Cycle Count](https://support.apple.com/en-us/HT201585)

### Repair a Disk or Mac Storage Drive

Apple's Disk Utility tool can fix some problems such as applications unexpectedly quitting or crashing, corrupted files, and external drives not working.
You can also format drives with Disk Utility.

This is a quick walkthrough on how to check your MacBook's disk and run First Aid.

- If you don't want to reboot the laptop, open Spotlight and search `disk utility`
- In the Disk Utility App, select your disk (should be named Macintosh HD but you can change that too)
- At the top you will see `First Aid`, click that an hit `run`
- Your MacBook will run First Aid, report any issues, and correct them if it can

### How long is my Macbook in Warranty?

- Review your Apple Warranty Status [Service and Support](https://checkcoverage.apple.com/)

### Want to add different profiles for your different GitLab accounts?

It is recommended that you create different profiles in Chrome so you can manage your different GitLab accounts.
This way you can easily sign in without having to signout out of different accounts each time.
A lot easier if you've got `staging.gitlab.com` and `dev.gitlab.org` accounts.

- On your computer, open Chrome
- At the top right, click the `Profile Profile`
- Click `Add`
- Choose a name and a photo
- Click `Add`.
- A new window will open and ask you to turn on sync

### Is your Chrome browser acting a little weird?

If you are having issues that seemingly can't be explained the below steps might help resolve your issue.
Keep in mind this will reset chrome to default settings but its easy enough to restore and link data back.

- On your desktop, open Chrome
- At the top right, click `More` and then `Settings`
- At the bottom, click `Advanced`
- Linux, and Mac: Under `Reset Settings`, click `Restore settings to their original defaults` and then `Reset Settings`

### Does your Gmail account keep getting suspended?

This usually occurs when the emails you send out get reported for spam. Collect too many reports and Google will automatically suspend your account. Here is some more info on Google's [page](https://support.google.com/a/topic/28609).

**How do I get access to my account after suspension?**

Someone from IT will need to unlock your account. Please submit a [Team Member Enablement request](https://gitlab.com/gitlab-com/business-ops/team-member-enablement/issue-tracker/-/issues/new?issuable_template=General%20HelpDesk%20Request) or reach out to us on the #it-help slack channel.

**How do I prevent this from happening?**

Please look into the following mailing applications which may prevent this from happening in the future due to a different mailing method.

- MailGun: <https://www.mailgun.com/>
- MailChimp: <https://mailchimp.com/>

Both of those applications are listed in GitLab's tech stack meaning they can be used.

### Getting a new phone and want to preemptively reset your MFA?

Great! If you are getting a new phone, and are aware of when you'll receive it.
It's handy to advise us firstly, so we can reset your MFA and your new device can authenticate for accounts straight away.
Please fill out the issue below and we'll reset as soon as we can.

Access request for OKTA MFA [here](https://gitlab.com/gitlab-com/business-ops/team-member-enablement/issue-tracker/-/issues/new?issuable_template=General%20HelpDesk%20Request).

### Questions about Okta?

Want to know how as an organization we leverage Okta as a Single Sign On tool? Please click [here](/handbook/business-ops/okta/)

### Tools and Tips

Check out the GitLab Tools and Tips pages for recommended software and applications - [Tools and Tips](/handbook/tools-and-tips/)

Our security team also did an amazing write-up for Linux installations - [Linux Setup](/handbook/tools-and-tips/linux/)

## Can't find what you are looking for?

Request for support should have an issue open at [IT Help Issues](https://gitlab.com/gitlab-com/business-ops/team-member-enablement/issue-tracker/-/issues/new?issuable_template=General%20HelpDesk%20Request).

### How to Contact Us or Escalate Priority Issues Outside of Standard Hours

We ask that all requests are made through an [IT Help Issue](https://gitlab.com/gitlab-com/business-ops/team-member-enablement/issue-tracker/-/issues/new?issuable_template=General%20HelpDesk%20Request). We will triage and address them as soon as we can. All issues created in the queue are public by default. Privileged or private communications should be sent to [it-help@gitlab.com.](mailto:it-help@gitlab.com.) Screenshots and videos are very helpful when experiencing an issue, especially if there is an error message.

As a distributed team, we have support around the clock with team members in North America, Europe and Australia.
High volumes of issues being triaged can dictate the delay in response within that window. If the issue is extremely time sensitive and warrants escalation, use judgement on whether or not it can wait until ‘business hours’.
Escalated issues should be made through the #it_help slack channel.
All other request should have an issue created.
