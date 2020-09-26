---
layout: handbook-page-toc
title: "Okta"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## What is Okta?

From the Okta website

> Okta is the foundation for secure connections between people and technology.
> It’s a service that gives employees, customers, and partners secure access to the tools they need to do their most important work.

In practice - Okta is an Identity and Single Sign On solution for applications and Cloud entities.
It allows GitLab to consolidate authentication and authorisation to applications we use daily through a single dashboard and ensure a consistent, secure and auditable login experience for all our GitLab team members.

### How is GitLab using Okta?

GitLab is using Okta for a few key goals :

- We can use Okta to enable Zero-Trust based authentication controls upon our assets, so that we can allow authorised connections to key assets with a greater degree of certainty.
- We can better manage the login process to the 80+ and growing cloud applications that we use within our tech stack.
- We can better manage the provisioning and deprovisioning process for our users to access these application, by use of automation and integration into our HRIS system.
- We can make trust and risk based decisions on authentication requirements to key assets, and adapt these to ensure a consistent user experience.

### What are the benefits to me using Okta as a user?

- A single Dashboard that is provided to all users, with all the applications you need in a single place.
- Managed SSO and Multi-Factor Authentication that learns and adapts to your login patterns, making life simpler to access the assets you need.
- Transparent Security controls with a friendly user experience.

### What are the benefits to me as an application administrator to using Okta?

- Automated provisioning and group management
- Ability to transparently manage shared credentials to web applications without disclosing the credentials to users
- Centralised access for users, making it easy to add, remove and change the application profile without the need to update all users.

## How do I get my Okta account set up?

All GitLab team-members will have an Okta account set up as part of their onboarding process. You should already have an activation email in both your Gmail adn Personal Accounts.  For efficiency, please follow the onboarding process for setting up Okta and set up 1Password first and follow that up with Okta.  Please also set up Okta from your computer rather than your mobile or the mobile app, as you will be guided to set up the mobile app as part of the onboarding process.

Follow the GitLab Okta [Getting Started Guide](https://docs.google.com/document/d/1x2NJan0job5nM5tT8HF6yofg-Y2aAsSVKc6qNnCuoxo/) and [FAQs](/handbook/business-ops/okta/okta-enduser-faq/).

We have also prepared Introductory Videos on [Okta Setup](https://youtu.be/upJ4p3lKYKw), [Setting up MFA/Yubikeys](https://youtu.be/9UyKml_aO3s), [Configuring Applications](https://youtu.be/xS2CarGUPLc) and [Dashboard Tips](https://youtu.be/xQQwa_pbe2U).

We recommend particularly that once your account is set up, you set up an additional MFA factor (either YubiKey or Google Authenticator/TOTP) in case there's an issue with one of your MFA factors.

### Setting up my Okta Account requires me to use the app Okta Verify on my phone, and I don't like that.

Our Okta implementation defaults to using Okta Verify as the Required MFA factor.
Okta Verify is a safe and secure application that allows push notifications and one-time tokencodes on your phone to validate your login.
It is supported on iPhone, Android and Windows Phones.

For some people, there are issues with installing a verification app on their phone.
If there is some reason that this is not appropriate for your geography or other reasons, please submit an issue to [Opt Out](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/new?issuable_template=okta_verify_optout) and we can add you to an authentication group that will make Okta Verify optional.
Please note that we still recommend that you set up at least two MFA factors, in case something happens to one of your factors.

## I forgot my password/my login doesn't work, what do I do?

There is a "need help signing in?" button on the login screen.
If you expand this there is a link to an automated password reset process via email.
You will need to know the answers to your security question(s) to use this.

We recommend that you store your Okta password in 1Password as well as your Security Questions there.
Please review the [1Password Guidelines](/handbook/security/#1password-guidelines) for best ways to use Okta and 1Password together.

### I forgot my Security Questions, how do I reset my password?

Firstly, review the [1Password Guidelines](/handbook/security/#1password-guidelines).
Then head to `#it_help` in Slack and ask for a temporary password to be issued.
You will be issued a temporary password at which point you can reset your access.

### I changed my phone and now can't do MFA, what do I do?

No worries! You can easily reset your own MFA code for Okta if you did not wipe/return your old phone yet. 

Firstly, sign into your Okta webpage by going to [gitlab.okta.com](https://gitlab.okta.com) use your email, password, and the MFA code on your old phone. 

Once you're on the Okta webpage click on your name and then click settings. 

<div style="text-align:center;">
  <img src="/handbook/business-ops/Okta-settings.png" alt="Okta Settings" width="500"/>
</div>
<br>

While on the Okta settings page, click the green "Edit Profile" button to edit the page contents.

<div style="text-align:center;">
  <img src="/handbook/business-ops/Okta-EditProile.png" alt="Okta Edit Profile" width="500"/>
</div>
<br>

Scroll down until you see "Extra Verification", once you're there click "remove" to disable that specific MFA and then click setup to configure the new MFA code on your new phone. 

<div style="text-align:center;">
  <img src="/handbook/business-ops/Okta-2FA.png" alt="Okta 2FA" width="700"/>
</div>
<br>


If you wiped and returned your old mobile device you could use a [Yubikey](https://www.yubico.com/products/) as another form of authentication (if you have one set one up). Use that to access your settings page and follow the steps above to reset your Okta MFA.

Lost all your MFA Factors?
Head to `#it_help` in Slack and ask for a MFA Reset.
Once your Factors have been reset, please set up at least two MFA factors (Yubikey or Google Authenticator, see [this video](https://youtu.be/9UyKml_aO3s)).


### My Okta account has been locked out because of failed attempts, what do I do?

Head to `#it_help` and ask to have your account unlocked.
As a precaution, you will also need to change your Okta Password.

## Why isn't an application I need available in Okta?

Create a [new application setup issue](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/new?issuable_template=okta_add_application) and fill in as much information as you can.

Okta is currently configured with assigned groups/roles based on a team member's role/group.
Refer to the [Access Removal Request](/handbook/business-ops/team-member-enablement/onboarding-access-requests/access-requests/#access-change-request) section of the handbook for additional information on why an application may not be available in Okta.

### How do I get my application set up within Okta?

If you are an application owner please submit a [new application setup issue](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/new?issuable_template=okta_add_application) on the Okta project page for your application.
We will work with you to verify details and provide setup instructions.

### I have an application that uses a shared password for my team, can I move this to Okta?

Yes you can!
Submit a [new application setup issue](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/new?issuable_template=okta_add_application) on the Okta project page for your application.
We will work with you to verify details and provide setup instructions.

## I'm getting asked to MFA authenticate a lot, is that normal?

The way we have Okta setup should require you to authenticate once with MFA when you start your working day, and that session should last for the rest of your work day.
It's recommended that you login via the [Okta Dashboard](https://gitlab.okta.com/) at the beginning of your day, and then use either the dashbaord or the Okta plugin for applications during your work day.

For some applications, we enforce an additional MFA step periodically because of the sensitivity of the data in them.
We are also trialling a risk-based authentication algorithm that may ask you to re-authenticate if anomolous behaviour is detected on your account or Okta detects an unusual login pattern.
At this stage, BambooHR and Greenhouse require an additional authentication step.

If you are having problems with being asked for multiple MFA authentications during the day, please [log an issue](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues) and we can look into it.

### Why does GitLab.com ask for an additional MFA when I login via Okta?

Your gitlab.com account will have 2FA installed as required by our policy.
Note that the 2FA for GitLab.com is different to the MFA you use to log into Okta.
[This issue](https://gitlab.com/gitlab-com/gl-infra/infrastructure/issues/7397) has been opened to propose a solution.

## Where do I go if I have any questions?

- For Okta  help, setup and integration questions: `#it_help` slack channel

## Who are the Okta Super Admins?

- Paul Harrison, Security Manager, Security Operations
- Peter Kaldis, IT Manager
- Robert Mitchell, Security Manager, Strategic Security
- Jan Urbanc, Director of Security Operations
