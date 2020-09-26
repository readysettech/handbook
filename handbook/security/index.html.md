---
layout: handbook-page-toc
title: Security Practices
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

Information security encompasses a variety of different working groups. These security best practices support the functions of business operations, infrastructure, and product development, to name a few. Everybody is responsible for maintaining a level of security to [support compliance (available internal-only)](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/), while raising the bar of our security posture.

## Zero Trust

As part of raising that bar, GitLab is implementing Zero Trust, or the practice of  shifting access control from the perimeter of the org to the individuals, the assets and the endpoints. You can learn more about this strategy from the [Google BeyondCorp whitepaper: A New Approach to Enterprise Security](https://ai.google/research/pubs/pub43231).

In our case, Zero Trust means that all devices trying to access an endpoint or asset within our GitLab environment will need to authenticate and be authorized. Because Zero Trust relies on dynamic, risk-based decisions, this also means that users must be authorized and validated: what department are they in, what role do they have, how sensitive is the data and the host that they are trying to access?  We’re at the beginning stages in our Zero Trust roadmap, but as we move along in the journey, we’ll document our lessons learned, process and progress in our [Security blog](/blog/categories/security/).

To learn more about the concept of Zero Trust and our roadmap for implementation, see this GitLab presentation from GoogleNext19: <https://www.youtube.com/watch?v=DrPiCBtaydM>

You can also check out our [Zero Trust Networking (ZTN) blog series](/blog/tags.html#zero-trust) where we detail the ZTN implementation challenges we foresee ahead, some we've already managed to work through, and where we'll go from here:
* Part one: [The evolution of Zero Trust](/blog/2019/04/01/evolution-of-zero-trust/)
* Part two: [Zero Trust at GitLab: Problems, goals, and coming challenges](/blog/2019/08/09/zero-trust-at-gitlab-problems-goals-challenges)
* Part three: [Zero Trust at GitLab: The data classification and infrastructure challenge](/blog/2019/08/21/zero-trust-at-gitlab-the-data-classification-and-infrastructure-challenge/)
* Part four: [Zero Trust at GitLab: Mitigating challenges with data zones and authentication scoring](/blog/2019/09/06/zero-trust-at-gitlab-data-zones-and-authentication-scoring/)
* Part five: [Zero Trust at GitLab: Implementation challenges](/blog/2019/10/02/zero-trust-at-gitlab-implementation-challenges/)
* Part six: [Zero Trust at GitLab: Where do we go from here?](/blog/2019/10/15/zero-trust-at-gitlab-where-do-we-go-from-here/)

Head over to the /r/netsec subreddit to see our [October 29, 2019 Reddit AMA](https://www.reddit.com/r/netsec/comments/d71p1d/were_a_100_remote_cloudnative_company_and_were/) on Zero Trust where we fielded questions around our ZTN implementation, roadmap, strategy and more.

Identity is a critical element of the implementation of a ZTN framework. GitLab is moving forward with an implementation of Okta to allow us to standardise authentication for Cloud Application access and implement user-friendly SSO. See our [Okta](/handbook/business-ops/okta/) page for more details.

### Why We Don't Have a Corporate VPN

In many enterprise environments, virtual private networks (VPN) are used to
allow access to less secured resources, typically also protected by an
enterprise firewall. Adding corporate VPN connectivity only marginally improves
the security of using those systems and assumes a network perimeter is in place.
At GitLab, as an all remote company, we do most of our work using other
Software-as-a-Service (SaaS) providers that we rely on to maintain
confidentiality of communication and data.

In relation to [Zero Trust](#zero-trust), a corporate VPN is a perimeter, which
ZTN architecture deemphasizes as a basis for making authorization decisions.
Current access to critical systems is managed through alternative controls.

While a corporate VPN is not implemented at this time, there are other valid
use cases for which individual team members may still wish to use a _personal_
VPN, such as privacy or preventing traffic aggregation. Team members that
wish to use a personal VPN service for any reason may still [expense one](/handbook/finance/expenses/).

For the use case of laptop usage in untrusted environments, such as coffee
shops and coworking spaces, team members should prioritize a baseline of always-on host protections,
such as up-to-date security patching, host firewalls, and antivirus, by following the
[system configuration guidelines](#laptop-or-desktop-system-configuration)
at a minimum. That said, a personal VPN may provide additional protections in these situations.
For more on personal VPNs see the [tips for Wi-Fi usage](/handbook/tools-and-tips/#wi-fi-usage).

## Contact GitLab Security

The GitLab Security Teams are available 24/7/365 and are ready to assist with questions, concerns, or issues you may have.

There are some common scenarios faced by GitLab team members:

 * [CEO & Executive Fraud](#ceo--executive-fraud)
 * [Phishing](#what-to-do-if-you-suspect-an-email-is-a-phishing-attack)

To contact for any other reason, see [Engaging the Security On-Call](/handbook/engineering/security/#engaging-the-security-on-call)

### External Engagement

The Security Teams can be contacted at `security@gitlab.com`. External researchers or other interested parties should
refer to our [Responsible Disclosure Policy](/security/disclosure/) for more information about reporting vulnerabilities.  The `security@gitlab.com`
email address also forwards to a [ZenDesk queue](/handbook/support/channels/#security-disclosures) that is monitored by the security team.

For Security Team members, the private PGP key is available in the Security 1Password vault.  Refer to [PGP process](/handbook/security/pgp_process) for usage.

### CEO & Executive Fraud

The CEO will not send you an [email to wire cash](http://blog.centrify.com/ceo-fraud-business-email-compromise/), the CFO won't send you a text message to ask for gift cards, or anything else that feels like [CEO fraud or CEO scam](https://www.knowbe4.com/ceo-fraud).  These types of [spear fishing](https://nakedsecurity.sophos.com/2019/09/05/scammers-deepfake-ceos-voice-to-talk-underling-into-243000-transfer/) events will be more common as we grow. Feel free to verify any unusual requests with a video call.

What should you do if you receive a potential phishing email or text from GitLab's CEO?

1.  If you are unsure whether the text or email is legitimate, confirm the request via Video Call or contact [Security](/handbook/engineering/security/) to review.
1.  If the email is determined to be fake, follow the instructions for [phishing attacks](/handbook/security/#what-to-do-if-you-suspect-an-email-is-a-phishing-attack) below.
1.  If the text is determined to be fake: block the number, notify [Security](/handbook/engineering/security/), and delete the text.

## Security Process and Procedures for Team Members

### Accounts and Passwords

1. Read and follow the requirements for handling passwords and other credentials in
  the [GitLab Password Policy Guidelines](#gitlab-password-policy-guidelines) below
  for all accounts used to conduct GitLab related work.
  Using 1Password to [generate and store] the passwords is strongly recommended.
1. Set up your [Okta](/handbook/business-ops/okta/) account at https://gitlab.okta.com,
  and use this as
  your primary means for accessing Applications supported in Okta. As part of
  setting up Okta, you'll need to establish a [strong
  password](https://gitlab.com/gitlab-com/www-gitlab-com/edit/master/source/handbook/security/index.html.md#gitlab-password-policy-guidelines)
  and set up at least one additional form of authentication.
1. For your Okta password and other passwords that you won't store in Okta, set up [1Password] as your password manager and set a **strong and unique**
  master password.
   - Keep your Master Password a secret. No other team members
   should know it, including admins. If the Master Password is known or
   disclosed to someone else, it should be changed immediately.
   - Post a message in #it-ops if you forget your Master Password.
   - Consider using a generated Master Password. Most human-created passwords
   are easy to guess. Let 1Password create a strong Master Password. But: you _will_
   need to memorize this Master Password.
   - Do not let your password manager store the **master password**. It is okay to
     store the username.
   - For more information, review [1Password's Getting Started guide](https://support.1password.com/explore/team-member/)
    and view [this video](https://youtu.be/2cFWk0sBgyM) that guides you through the sign-up process.
   - For account administrators, review [1Password's admin guide](https://support.1password.com/explore/teams-admin/).
1. Enable two-factor authentication (2FA) with an authenticator, such as
  [Google authenticator] or [1Password TOTP] for on every account that supports
  it. This is required for
  [Google](https://myaccount.google.com/signinoptions/two-step-verification/enroll-welcome),
  [Slack](https://get.slack.help/hc/en-us/articles/204509068-Set-up-two-factor-authentication),
  [GitLab.com](https://docs.gitlab.com/ee/user/profile/account/two_factor_authentication.html#enabling-2fa),
  and dev.gitlab.org accounts. `Users without 2FA enabled that are stale for
  over 30 days will be blocked/suspended until resolved. This improves the
  security posture for both the user and GitLab.`
  If any systems provide an option to use SMS text as a second factor, this is highly discouraged.
  Phone company security can be easily subverted by attackers allowing them to take over a phone account.
  _(Ref: [6 Ways Attackers Are Still Bypassing SMS 2-Factor Authentication](https://www.securityweek.com/6-ways-attackers-are-still-bypassing-sms-2-factor-authentication) / [2 minute Youtube social engineering attack with a phone call and crying baby](https://www.youtube.com/watch?v=lc7scxvKQOo))_
1. A Universal 2nd Factor or [U2F](https://en.wikipedia.org/wiki/Universal_2nd_Factor) hardware token can be used as a secure and convenient 2-factor authentication method for Okta, G Suite, GitLab instances, and many other sites. If you do not have one, you may consider [purchasing one](/handbook/spending-company-money/). Popular choices include Yubico's YubiKey and Solokeys' Solo Security Key. For more information on U2F and choices, visit the [Tools and Tips page](/handbook/tools-and-tips/#u2f).
1. When signing up for a new service on behalf of GitLab:
   - Request a [Security Review](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/new?issuable_template=SOC%20Report%20Review) by opening an issue in the Compliance project.
   - If shared access is required by multiple team members to a single account,
     for example, a social media account, an [Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new) should be opened. The credentials will be
     stored and shared via Okta.
1. If you find an existing shared account in 1Password, [create an issue](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/new?issuable_template=okta_add_application)
   to get it migrated to Okta.

[1Password]: https://1password.com
[1Password TOTP]: #two-factor-authentication-and-time-based-one-time-passwords
[Google Authenticator]: https://support.google.com/accounts/answer/1066447?hl=en
[generate and store]: https://support.1password.com/guides/mac/generate-a-strong-password.html

### Laptop or Desktop System Configuration

**The following instructions are for Apple (MacBook Pro or Air) users. Linux users please go to the [Linux Tools](/handbook/tools-and-tips/linux/) section of the handbook.**

1. Set up **full disk encryption** with [FileVault] (for details, refer to [Apple Support](https://support.apple.com/en-in/HT204837)). GitLab is currently utilizing [JAMF](/handbook/business-ops/team-member-enablement/onboarding-access-requests/endpoint-management/) for endpoint management and can assist with this step.
1. Set up a screen saver with **password lock** on your laptop with a timeout of 5 minutes or less. GitLab is currently utilizing [JAMF](/handbook/business-ops/team-member-enablement/onboarding-access-requests/endpoint-management/) for endpoint management and can assist with this step.
1. Never leave your unlocked computer **unattended**. Activate the screensaver,
  lock the desktop, or close the lid.
1. For backups on macOS follow this tutorial: [How to use Time Machine](https://support.apple.com/en-us/HT201250)
  1. If you backup your computer make sure the backup drive is encrypted and use a strong password.
1. [Purchase](/handbook/spending-company-money) (if necessary) and install
  security related software.
  1. Little Snitch is an excellent personal firewall solution for macOS. Recommended to monitor application network communications.
  1. An anti-virus/antimalware program such as Malwarebytes, ESET, or Norton.
  1. Refer to [Why We Don't Have A Corporate VPN](#why-we-dont-have-a-corporate-vpn) for
     more information about personal VPN usage at GitLab
1. Do not allow your web browser (e.g. Chrome, Safari, Firefox) to store passwords when
  prompted. This presents an unnecessary risk and is redundant.
1. Do not install software with many known security vulnerabilities. At this point GitLab's [vendor security review](/handbook/engineering/security/security-assurance/security-compliance/third-party-vendor-security-review.html) scope does not include services individually deployed on endpoint devices. After a decision regarding deployment of an endpoint management solution is made the process will be redesigned accordingly and services, where applicable, will be retroactively reviewed. Please ensure you continue to follow the requirements defined in the [acceptable use policy](/handbook/people-group/acceptable-use-policy/).
1. Enable automatic software updates for security patches. On macOS, this is
  found under "System Preferences" -> "Software Update", "Automatically keep
  my Mac up to date". GitLab is currently utilizing [JAMF](/handbook/business-ops/team-member-enablement/onboarding-access-requests/endpoint-management/) for endpoint management and can assist with this step.
1. Enable your system's built in firewall. In macOS, this can be found in
   `System Settings` -> `Security & Privacy` under the `Firewall` tab. It is
   recommended to select "Block all incoming connections"; however, if choosing
   not to block all incoming traffic, apply the following configuration (see screenshot):
    * Deselect "Automatically allow downloaded signed software to receive incoming messages"
    * Select "Enable stealth mode"
    * GitLab is currently utilizing [JAMF](/handbook/business-ops/team-member-enablement/onboarding-access-requests/endpoint-management/) for endpoint management and can assist with this step.

<div style="text-align:center;">
  <img src="/handbook/security/macos_firewall_settings.png" alt="macOS Firewall Settings" width="560px"/>
</div>

[FileVault]: https://support.apple.com/en-us/HT204837

### WiFi configuration

Refer to this [guide](network-isolation/index.html) for setting up a dedicated WiFi so that your work notebook is isolated from other personal devices in your home network.

### Mobile Applications

Many services that team members use such as Slack and Zoom have mobile applications that can be loaded onto iOS or Android devices, allowing for use of those resources from a mobile phone. Refer to the [acceptable use policy](/handbook/people-group/acceptable-use-policy/#personal-mobile-phone-and-tablet-usage) for more information on using a mobile device.

Most major applications (Slack, Zoom, Okta Verify) have been examined and vetted by the Security Team, but there are some applications such as BambooHR's mobile app which are not only of limited scope in the data they can access, but also have security issues. In such cases, use the mobile device's web browser for access to the resource. If you have a question about the security of a mobile app and want to know if you should be using it to access GitLab data, contact the Security Team via Slack in the #security channel.

### Other Services/Devices

1. Do not configure email **forwarding** of company emails (@gitlab.com) to a
  non-company email address. Follow the [Unacceptable Email and Communications Activities](/handbook/people-group/acceptable-use-policy/#unacceptable-email-and-communications-activities) policy.
1. There are security implications involved in the use of "smart home devices" such as Amazon Echo or Google Home. In rare instances these devices can record conversations you might not have intended them to record. Many smart home devices will provide a visual and/or auditory indicator to let you know they're activated; for many such devices, when they're activated, they're recording you and save a transcript of what you say while it's active. If a smart home device is activated while you're verbalizing sensitive information, wait for it to turn off or manually turn it off. If you think a smart device may have been activated while verbalizing sensitive information, most smart home devices allow you to delete transcripts and recordings. Please use your best judgement about the placement of these devices and whether or not to deactivate the microphone during sensitive discussions related to GitLab. If you ever have any questions or concerns, you can always contact the Security team.

### Security Awareness

1. Follow the guidelines for identifying phishing emails provided in the [training](#training-delivery) and [How to identify a basic phishing attack].
  * During the onboarding process you may receive account
   registration emails for your baseline entitlements. Before clicking these
   links feel free to confirm with #it-ops that they initialized the process.
   Clicking itself is a problem even when you don't enter a password, because a
   visit can already be used to execute a [0-day attack]. Security Team will, from time to time,
   simulate phishing attacks to our company email addresses to ensure everyone is aware of the threat.
2. If you get strange emails personally or other things related to security feel
  free to ask the security team for help,
  [they might be aiming for the company](https://medium.com/starting-up-security/learning-from-a-year-of-security-breaches-ed036ea05d9b).
3. If you receive a security report of any kind (issue, customer ticket, etc.)
  never **dismiss** it as invalid. Please bring it to the attention of the
  [Security Team](/handbook/engineering/security), and follow the steps outlined on
  that team's handbook page.
4. **Report** suspect situations to an officer of the company or use the [engage the Security Oncall](#gitlab-team-members).
5. If you have security **suggestion**, create an issue on the
  [security issue tracker](https://gitlab.com/gitlab-com/security/issues/)
  and ping the security team. New security best practices and processes should be
  added to the `#whats-happening-at-gitlab` slack channel
6. Do not sign in to any GitLab related account using public computers, such as
  library or hotel kiosks.

[How to identify a basic phishing attack]: #how-to-identify-a-basic-phishing-attack

[0-day attack]: https://en.wikipedia.org/wiki/Zero-day_(computing)
[email to wire cash]: http://blog.centrify.com/ceo-fraud-business-email-compromise/

## GitLab Password Policy Guidelines

Passwords are one of the primary mechanisms that protect GitLab information systems and other resources from unauthorized use. Constructing secure passwords and ensuring proper password management is essential. GitLab's password guidelines are based, in part, on the recommendations by [NIST 800-63B](https://pages.nist.gov/800-63-3/sp800-63b.html). To learn what makes a password truly secure, read this [article](https://medium.com/peerio/how-to-build-a-billion-dollar-password-3d92568d9277) or watch this [conference presentation](https://www.youtube.com/watch?v=vudZnjp5Uq0&t=19183) on password strength.

### GitLab team-members Password Requirements
* At GitLab, we enforce a strong password requirement, which consists of minimum length of 12 characters.
* To make a secure password you can remember, consider using a [combination of 5 or more random words](https://medium.com/peerio/how-to-build-a-billion-dollar-password-3d92568d9277#67c2)
* The use of special characters is not required or even recommended.
* Avoid creating predictable passwords.
* Passwords cannot be reused.
* Passwords should not be the same as username.
* Passwords should be unique from the previous passwords used.

### Password Management
* Password "hints" are not to be used. If a password is forgotten, a mechanism must be in place to replace a password/passphrase with sufficient controls to verify the identity of the requester of the password reset.
* Passwords must be stored in a way that is resistant to offline attacks and must be salted and hashed using a suitable one-way key derivation function.
* If a password is required to be stored, it must be stored within an approved password manager application and may be pasted from this using a master password function (e.g. 1Password).
* Passwords are to be kept private and secured.
* If an account or password is suspected to have been compromised, report the incident to Security and promptly follow their instructions.
* Passwords are not to be shared or be in clear text or be written down.

### System Password Requirements
* For systems where a password can be configured the minimum password length needs to be set to 12 characters.
* To make a secure password you can remember, consider using a [combination of 5 or more random words](https://medium.com/peerio/how-to-build-a-billion-dollar-password-3d92568d9277#67c2)
* The use of special characters is not required or even recommended.
* If a particular system will not support 12 character passwords, then the maximum number of characters allowed by that system shall be used.
* If a particular system requires a password history, configuration should be set for 25 remembered passwords.
* Passwords are not acceptable if they match the subsequent patterns, and must be checked against commonly used or expected patterns, including known breached password lists, dictionary words, repetitive or sequential characters, or context specific words, such as the name of the service, username, or derivatives thereof.
* System administrators of applications and or devices must change default passwords.
* System administrators need to enable password strength on third party applications and or tools, where applicable.
* For applications where a password is the only source of authentication a password must be expired within a maximum of 90 calendar days.
* Systems should monitor and log failed login attempts.
* Authentication failed login attempts information needs to be recorded within the application logs such as: name, date, number of failed attempts, unique log identifier.
* Repeated failed login attempts must trigger a temporary account lockout after 10 failed attempts. The lockout may end after a designated period of time, or require a manual unlock, depending on the profile of the application.

### Two Factor Authentication

All GitLab team members should use [Two Factor Authentication](https://en.wikipedia.org/wiki/Multi-factor_authentication) (2FA) whenever possible. Usage of 2FA by GitLab team members is **required** for access to the production environment. It should be noted that references to MFA (Multi-Factor Authentication) are often included in language associated with third party products and certain Compliance references (e.g. [IAM.2.03 - Multi-factor Authentication](/handbook/engineering/security/security-assurance/security-compliance/guidance/IAM.2.03_multifactor_authentication.html) ), but the general concept is still covered by the term "2FA". There are different 2FA methods that can be used by GitLab team members. These are ranked by security strength:

- [U2F](https://en.wikipedia.org/wiki/Universal_2nd_Factor). U2F (Universal 2nd Factor) uses a hardware token and is considered the most secure method, assuming the hardware token itself is physically secured.
- [Push Authentication](https://en.wikipedia.org/wiki/Authenticator#Mobile_Push). For Push Authentication to work, the authentication service and a complementary mobile app typically use RSA keys and OOB (Out Of Band) communications to perform the secondary authentication. GitLab uses Okta, and by using the [Okta Verify](https://help.okta.com/en/prod/Content/Topics/Mobile/okta-verify-overview.htm) mobile app, you can perform Push Authentication. From a pure cryptographic perspective this is _slightly_ less secure than U2F as U2F uses secure hardware storage, otherwise they are pretty much equal.
- [TOTP](https://en.wikipedia.org/wiki/Time-based_One-time_Password_algorithm). TOTP (Time-based One Time Password) is a popular method for a second factor. This can be done via a mobile app (Google Authenticator, Duo Security, etc) although there are some software implementations as well. While not as secure as U2F or Push as TOTP could be [phished](https://en.wikipedia.org/wiki/Phishing) (although the attack window would be extremely short), it is still a very secure method of authentication. As 1Password is used by GitLab team members, this could be used for TOTP after proper configuration ([see below](/handbook/security/#two-factor-authentication-and-time-based-one-time-passwords)).
- [SMS](https://en.wikipedia.org/wiki/SMS). SMS (Short Message Service) is a method of using text messaging to provide out-of-band (OOB) authentication. As the messages can be spoofed or intercepted more easily than other methods, SMS is not recommended for 2FA. As of this writing the Security Department is unaware of GitLab assets or third party applications that team members are using that _only_ support SMS 2FA, but if you need to use something that only offers SMS as a second factor for GitLab, contact the [Security Department](/handbook/engineering/security/#slack-channels).

There is a reason that multiple 2FA methods are supported (e.g. Okta supports U2F, Push, and TOTP). Situations are different for different team members. For team members that travel a lot, they might feel more comfortable using Push instead of U2F if they are concerned about losing the hardware token during their travels. Many team members us 1Password and TOTP for the convenience. Many services support configuring multiple methods, which can be used for different situations or as a backup if a factor is lost. The idea is that we give team members a choice so that they can adapt a 2FA solution that best suits their needs. Again, contact the [Security Department](/handbook/engineering/security/#slack-channels) if you have questions.

For a better understanding of how 2FA fits into GitLab, refer to the [Accounts and Passwords](/handbook/security/#accounts-and-passwords) section, which includes pointers to setting up passwords, acquiring U2F tokens, and links to further resources.

### Application Authentication Requirements
* Authentication to an application should contain Multi-Factor authentication (Token, OTP Generator, SSO, YubiKey/Titan or equivalent) and or a SAML Assertion after logging into an authentication portal is recommended (e.g., Okta).
* Authentication to an application should support individual users, not groups.
* Acceptable secondary authentication factors include Google Authenticator or similar software implementing a One-time Password algorithm. The use of biometrics is acceptable.

### Exceptions to Password Policy

Any application that can not meet MFA and or Password requirements needs to [submit an exception](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/issues/new?issuable_template=Exception%20Request) for the Compliance team to review.  A duration of an exception is valid for 90 days followed by a proper remediation plan. After 90 days the exception will be reevaluated.

## 1Password Guide

1Password is a password manager. Ideally you memorize one strong password -
hence the name - and let 1Password generate and manage strong, unique passwords
for every site for which you have a login.

### Terminology

Following this guide, it will be helpful to understand a few terms we'll be
using throughout.

- **App:** A native 1Password application (macOS, iOS, Windows, Android).
- **Extension:** A web browser extension/plugin that communicates with the
  **App** to provide access to your passwords securely without leaving the
  browser.
- **Vault:** What 1Password calls any grouping of secure data, such as logins or
  secure notes. Sometimes called a "keychain".

### 1Password

1Password can be used in two different ways - as a standalone application
(by purchasing a standalone license) or as a hosted service (by subscribing).
GitLab uses 1Password for Teams which is a hosted service.

GitLab is transitioning to use [Okta](/handbook/business-ops/okta/) as a primary entry and access point for SaaS and other company applications. This does not mean that 1Password will be deprecated completely, but it is preferred that, where possible, you use Okta as your primary entry point into applications. GitLab will be using Okta for SAML/SSO and passwordless authentication for many applications, so the need to store passwords in a password manager will diminish over time.

If you want to use 1Password for your private passwords not related to your work
at GitLab, [there are a few options](#1password-for-your-private-passwords).

### 1Password Guidelines

1. If you install the macOS application, install 1Password via the
[Mac App Store](https://apps.apple.com/us/app/1password-7-password-manager/id1333542190)
to ensure a more secure update process.
1. If you have a YubiKey or other hardware token, it can be added as a 2-factor
method to your 1Password account for convenience.
1. When traveling, consider using 1Password in "Travel Mode", see more on that [below](#travel-mode).
1. Do not share credentials via email, issue comments, chat etc. This includes
   email addresses to login and API keys. Use 1Password vaults for this.
1. If you do not have access to a vault that is part of the baseline entitlements
  for your role and team, mention `gitlab-com/business-ops/itops` in your onboarding
  issue or in #it-ops on slack. For all other access, create an
  [access request issue](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new).
1. Use Watchtower to find passwords that need to be changed. Watchtower tells
users about password breaches and other security problems on the websites they
have saved in 1Password Teams, so users can take action. This is not something
account administrators can review for team members, so it is up to you to enable!
Enable Watchtower by going to your 1Password app and then to **Preferences > Watchtower**.
1. Use the ["Security Audit"](https://i.agilebits.com/dt/Blank_Skitch_Document_18FB0234.png)
functionality of 1Password meet the [password policy](#gitlab-password-policy-guidelines).
It will report reused passwords, weak passwords, accounts that
are missing 2-factor authorization, and so forth that can then be fixed.
1. Do not copy passwords from inside a 1Password vault to a personal password
vault or other password store. 1Password should be the only password
vault used for teams. Team passwords should not be duplicated or placed in
personal password vaults where they can potentially be exposed to compromise.
1. When asked security questions (what is your favorite pet, etc.) do not answer
truthfully since that is easy to research. Make up an answer and write both the
question and answer in 1Password. Consider using the Password Generator function
in 1Password for this.
1. During offboarding, your 1Password account is deleted, which includes the
**Private** vault in the GitLab team account. If you want to keep your personal
passwords, please copy/move them to your **Primary** vault which you will have
if you signed up for an [individual account](#1password-for-your-private-passwords) before
joining the GitLab Team account.
1. **Deprecated** When documenting the location of shared credentials in the handboook refer to the items with NAME_OF_SITE credentials in VAULT_NAME. For example:
   "for access please see the AOL credentials in the Luddite vault".
   * Deprecation note: This is for existing accounts only. New accounts should
     be created by [creating an issue](https://gitlab.com/gitlab-com/gl-security/zero-trust/okta/issues/new?issuable_template=okta_add_application)
     to add it to Okta.


### 1Password for Teams

1Password for Teams stores all **Vaults** on the 1Password servers and allows
for sharing between multiple people on the same team. Every GitLab Team Member who needs access to a shared vault should consult their departments for any shared vault information.

Each member of the team has a vault called **Private** which *only you can see*, and allows you to store personal credentials *within the GitLab team's account*. 

To really get the full benefit of 1Password, you'll need to hook our Teams
account up to one of the native apps.

### Adding the GitLab Team to a 1Password app

This guide will cover setting up the [macOS app]. It's their lead platform and is
the most up-to-date. These instructions may or may not work for the Windows
version. If you use 1Password 6 without a 1Password.com account, make note of
[this](#adding-the-gitlab-team-to-a-1password-account-less-installation).

1. Download and install the 1Password [macOS app].
1. Launch the app.
1. Click "Sign in to your 1Password account" button. If there is no such button
please follow the instructions for [updating 1Password](#1password-update).

Now you'll need the **Emergency Kit** PDF that 1Password told you to save when
you registered your **Teams** account. Note: Store the Emergency Kit safely.
Store a copy of the Emergency Kit on a USB flash drive or print a copy and store
it in a vault at home or safe deposit box — somewhere not online or accessible
by anyone other than yourself.

If you saved it as a digital PDF file:

1. Open the PDF file
1. Click **Scan QR Code**
1. Drag the scanner window over the QR code on the PDF sheet

If you printed the PDF:

1. Click **Sign In Manually**
1. For **Team URL** enter **gitlab.1password.com**
1. For **Account Key** enter the Account Key from your Emergency Kit
1. For **Email Address** enter your `@gitlab.com` email
1. For **Master Password** enter the password to your **Teams** account (*not*
   the password you created above when you chose "I'm a new user")

After the Team is added, you should see some notifications about vaults being
added to 1Password. By default you'll have the **Private** vault, but
may have access to others. It should be part of your onboarding process to be granted access to the **Team** vault, so it might not appear straight away. If in doubt, get in touch with the person responsible for onboarding you to make sure you're granted access.

### Adding the GitLab Team to a 1Password account-less installation

If you already have a non-account based license for 1Password, you can still add the
GitLab Team to your current account, but there are a few peculiarities:
1. The Master Password you create for your new GitLab Team account is distinct from
   your current local vault Master Password, but you will still be able to access
   all vaults in the macOS app, local and Gitlab, with your existing local vault password.
1. You will *not* be able to log into 1Password.com using your local Master Password.
   If you choose to set up 1Password this way, please do print out your GitLab account
   recovery sheet with your new Master Password and store it somewhere secure, because
   you'll need it to access your team account online or recover the account, even if
   you use your local Master Password in day-to-day usage. GitLab cannot recover your
   account if your account-specific Master Password is lost.
1. It is possible to set up your GitLab account with any of your email aliases, but each
   can only be used one time. People Ops Specialists and security will need to set it up as an
   additional account, so coordinate with them.

### Updating 1Password to support the Teams feature
{: #1password-update}

*Read this section only if you could not follow the instructions in "Adding
the GitLab Team to a 1Password app" section.*

1. At the prompt, choose "I'm a new user". *Note:* This is one source of
   confusion. "I created my Teams account, I'm not new!" Just go with it.
1. Enter a master password, confirmation, and hint. This can (and should) be
   different from the password you used for our **Teams** account. This password
   gates access to your **local, private** Vault on your computer and/or phone.
1. Skip over the remaining dialogs (syncing, newsletter, etc.)
1. You should now have an empty vault called **Primary**.

Because the Teams feature is not available in your current version of 1Password,
we need to update the app to the latest version:

1. Go to **Preferences**
1. Go to **Updates**
1. Click **Check Now**
1. Install the update and relaunch
1. After relaunch, go to **Preferences** again
1. Go to **Accounts**
1. Click the **+** icon

### Vaults

Click the **Vault Selector** in the upper-left corner of the window:


<div style="text-align:center;">
  <img src="/handbook/security/1password-vault-selector.png" alt="Vault Selector" width="700"/>
</div>
<br>

GitLab team members have access to a **Private** vault by default, which is your *hosted, private* vault that is part of the GitLab 1Password for Teams account. Since the Private vault is part of the
GitLab Teams account, it should be thought of as company property (like the
@gitlab.com email account), however the vault *can not* be viewed by anyone
else on the team, including admins. If you choose to store truly personal
information in the Private vault, it opens up the possibility that you would
be separated from this information if you offboard. Such truly personal
information is therefore better to store in your **Primary** vault, which is
associated with you instead of with the GitLab Teams account, assuming that you
added an [individual account](#1password-for-your-private-passwords).

People may request access to other vaults such as shared vaults that their teams/departments have created.

### Browser Extension

Go to [Browser extensions](https://agilebits.com/onepassword/extensions) and
install the extension for whatever browser you're using. You *should not* need a
beta version here.

With the extension installed, you should be able to go to a site that you have
credentials stored for in 1Password and log in:

<div style="text-align:center;">
  <img src="/handbook/security/1password-login.gif" alt="Mailchimp Login" width="450"/>
</div>

If you don't see the site listed in the results window, make sure you're using
the correct vault:

<div style="text-align:center;">
  <img src="/handbook/security/1password-vault-change.gif" alt="Vault switching" width="450"/>
</div>


### Saving Logins

When 1Password detects a login form submission, it may ask if you want to save
the login with a dialog like this:

<div style="text-align:center;">
  <img src="/handbook/security/1password-save-login.png" alt="Save login" width="600"/>
</div>

If you do want to save it, make sure the appropriate **Vault** is selected
first.

### Several accounts and unlocking the app

Please refer to [1Password FAQ](https://support.1password.com/faq/#i-have-several-accounts-and-vaults-which-password-do-i-use-to-unlock-1password).

If you are planning to use both the GitLab team account and a separate
individual account you should first add your separate individual account to the
app first (Preferences > Accounts). By doing this you will be able to unlock
the 1Password app using the Master Password of the individual account.

If you were using 1Password before joining GitLab, and you receive a prompt
titled **Migrate To Account**, choose **I'll move later**. There is no harm in
doing this, and it is easy to move items between vaults.

### 1Password for your private passwords
{: #1password-private-use}

You are encouraged to use 1Password for your private passwords, not related to
your work at GitLab.
This makes it less likely for a security breach to occur. You can purchase a
standalone license or start an individual subscription. While under the GitLab
team subscription, it is also possible to create and use a 'Private' vault
(same features of a standalone license, without the cost, but you will lose
access if you go through offboarding).

Please bear in mind that if you decide to purchase a standalone license or
create a personal local vault, your data is stored only in a local folder on
your computer. You can optionally sync this folder to Dropbox or iCloud (if you
are using a Mac/iOS) to make it available on your phone's 1Password app, or on
another computer.

Signing up for a subscription seems to be the solution now recommended by
AgileBits (the company behind 1Password).

To create a personal local vault:

1. Go to **Preferences**
1. Go to **Advanced**
1. Under **Local Vaults**, check **Allow creation of vaults outside of 1Password accounts**
1. Enter your Master Password
1. A new local vault (**Primary**) is created outside the GitLab team account
1. If you want to set up sync for your new local vault, go to **Preferences > Sync**

### Two Factor Authentication and Time-based One Time Passwords

As stated in the [GitLab Password Policy Guidelines](/handbook/security/#gitlab-password-policy-guidelines), all GitLab team-members should use two factor authentication (2FA) whenever possible.

1Password provides an alternative solution that does not
require using your smartphone: 1Password Time-based One Time Passwords
(TOTP). 2FA codes are displayed directly in the 1Password app running on your
laptop (Note: this can not be set up via 1Password browser extension or 1Password web app).

1Password TOTP is compatible with Okta, as it uses the same algorithm as Google Authenticator.

To enable TOTP for a saved account:

1. Open 1Password app
1. Go to the item for which you want to set up TOTP
1. Click **Edit** in the bottom right corner
1. Add a new field by clicking on the field type dropdown (it offers a "Text field" by default)
1. Select **One-Time Password** 

<div style="text-align:center;">
  <img src="/handbook/security/1password-otp.png" alt="One-time password field type" width="600"/>
</div>

1. Click QR code icon that appeared 

<div style="text-align:center;">
  <img src="/handbook/security/1password-qrcode.png" alt="1password QR Code" width="600"/>
</div>


1. Scan QR code using the transparent window
1. Click **Save**
1. 2FA code should be displayed now

Please refer to demo video [1password TOPT setup](https://support.1password.com/one-time-passwords/)

Please refer to the [1Password blog] for more information on how TOTP works.

[1Password blog]: https://blog.agilebits.com/2015/01/26/totp-for-1password-users/

If scanning the QR code using the "transparent window" with the 1Password Mac
app fails on a recent macOS, please consider using the 1Password iOS app instead.
This mechanism works the same way, and supports Touch ID to login.

While the above 1Password default recommendation applies to all GitLab team-members, there are alternative,
although more complex solutions that can also be used. Google Authentication is a TOTP solution
that can be used to store tokens, for those who want to have separate application for password storage
and token storage. However, be aware that using two applications is more complex, and not necessary. If
unsure which mechanism to use, we recommend using 1Password as a TOTP for 2FA.

Follow this [guideline](https://gizmodo.com/how-to-easily-switch-your-two-factor-security-to-a-new-1821808681) when getting a new mobile device, if you are using Google Authenticator as a TOTP mechanism.

#### Setting Up 1Password TOTP for Your GitLab Google Account

1. Navigate to <a href="https://myaccount.google.com">myaccount.google.com</a>.
1. In the left-side menu, select "Security".
1. Under "Signing into Google", click on the option for 2-Factor Authentication.
1. Click "Get Started"
1. Enter your password to log in to your account. If you are unable to do this and Google says it is because the account requires 2FA, contact the security team and ask them to make an exception for your account.
1. Once successfully logged in, on the following page select "Choose another option" and then select "text message or voice call" from the dropdown menu.
1. Enter your mobile phone number and select your preferred method (text or call), and then click "Next".
1. Enter the code that you receive and click "Next".
1. On the following page, click "Turn On". Now 2FA is enabled for your Google account.
1. On the following page, scroll down to the section titled, "Set up alternative second step". From this list, select "Authenticator app" setup.
1. This will present a QR code. Open the 1Password desktop or mobile app, and navigate to your GitLab email/Google login. Select edit.
1. On the edit page, select "Add new section" and title it One-time password (or something else of your choosing), and then select "Add new field", and choose "One-Time Password" from the dropdown menu.
1. Tap or click the small QR code that appears next to your newly created field. A QR scanner will open up. Use the scanner to read the QR code that Google is presenting (from step 11).
1. Tap or click Done within 1Password to save the edits. Keep 1Password open.
1. Within your Google settings, click "Next". Now enter the six-digit code that has appeared in the One-time password field that you have just sent up in 1Password. Once the code is entered, click "Verify".
Google should present a "Done!" message. You have now set up TOPT for your Google account! Nice work.

### Example Usage
{: #1password-example-usage}

This is an example of how <a href="https://gitlab.com/rspeicher">Robert</a>,
one of our developers, uses 1Password:

> Once you fully commit to using 1Password to manage all of your security
> information, it really does make life easier.
>
> I memorize one strong password and let the app generate
> everything else. Every site I use has a unique password that I can't
> compromise because I don't even know it, and a hacked site can't compromise
> it because the password is never re-used on another site.
>
> I store my shipping and credit card info in 1Password and use the browser
> extension to quickly fill out shipping and billing information on shopping
> sites.
>
> I store my passport data, along with a digital scan, in 1Password; driver's
> license info and scan; insurance info; software license keys; any important
> information that needs to be secure but still easily accessible when I need it,
> from anywhere. I sync my personal vault to my personal iCloud so it's
> available on my phone, tablet, laptop, and desktop.
>
> Even my 1Password for Teams account information is stored in my personal
> **Primary** vault, with the Emergency Kit PDF as a secure attachment. 
> I have no idea what the password is. I've never actually typed it. And that's
> the idea:

  <div style="text-align:center;">
    <img src="/handbook/security/1password-teams-login.png" alt="Teams Login" width="560px"/>
  </div>

### Traveling with 1Password
{: #travel-mode}

When traveling with a device that has access to the GitLab 1Password vaults, be
sure to [enable Travel Mode](https://support.1password.com/travel-mode/) in 1Password. Travel Mode removes copies of any
1Password vaults that are not tagged as "safe for travel" from your mobile devices.
None of the GitLab shared vaults are marked as safe for travel so you will need
to either create a dedicated travel vault or mark your Private vault as safe for
travel.

Once you have enabled Travel Mode open 1Password on each device you will be taking
with you so that it can sync with 1Password.com and remove any vaults that cannot
be used while traveling.

For more information on Travel Mode and how it works, see the [AgileBits blog].

[agilebits blog]: https://blog.agilebits.com/2017/05/18/introducing-travel-mode-protect-your-data-when-crossing-borders/
[1Password for Teams]: https://blog.agilebits.com/2015/11/03/introducing-1password-for-teams/
[Teams account]: https://gitlab.1password.com/
[macOS app]: https://agilebits.com/downloads

## Security Awareness Training

The GitLab Security Training is GitLab's security awareness presentation for new hires and annual training requirements beginning in 2020. The purpose of the annual training is to mature our internal posture through regular training while satisfying external regulatory requirements. The New Hire training is part of the onboarding process, and needs to be completed by every new hire. We are trying to make it fun, engaging and not time-consuming.

The future in-house training is being actively developed by [GitLab Security](/handbook/engineering/security/)'s [Security Incident Response Team](/handbook/engineering/security/#sirt---security-incident-response-team-former-security-operations). The goal of the training is to:

1. Make all GitLab team-members aware of the GitLab Security team, and familiarize them with our efforts, team structure, and people.
1. Make all GitLab team-members aware of the importance of their role in securing GitLab on a daily basis, and to empower them to make the right decisions with security best-practices.
1. Familiarize all new GitLab team-members with security-related situations that they might encounter during their tenure with the company.
1. Help all GitLab team-members internalize and reinforce the idea that paging the Security On-Call is an encouraged practice.

### Training Delivery

#### New Hire Security Training
The New Hire Security Training is delivered through a pre-recorded presentation that is presented by a member of the [Security Incident Response Team](/handbook/engineering/security/#sirt---security-incident-response-team-former-security-operations) team. The following materials are made available for your consumption:
* [The video](https://www.youtube.com/watch?v=kNc9f-LH6pU) - the actual training.
* [The slides](https://docs.google.com/presentation/d/1Yts7RixM9Eb7wt9x9TqS2lAHjmHzKcEI_-j_yZaztlc/) - the slides used in the training video.
* [Security Practices](/handbook/security/#security-process-and-procedures-for-team-members) - a list of security process and procedures that you can consult at any time.

#### 2020 GitLab Security Awareness Training
The 2020 Security Training is delivered through the KnowBe4 platform that includes a GitLab-specific introduction module followed by a training conducted by the vendor. The introduction and training materials are included:
* [The video](https://youtu.be/1nAUjrO_b2Q) - the introduction module.
* [The slides](https://docs.google.com/presentation/d/1VqOiGJDZ1vDiVVMgrw3ILxx1ot1-nM8jGzDcWylLTpM) - the slides used in the introduction video.
* Special topics covered:
  * [Suspected phishing](/handbook/security/#phishing-tests)
  * [Acceptable Use](/handbook/people-group/acceptable-use-policy/)
  * [Device Lost or Stolen?!](#panic-email)
    * email: `panic@gitlab.com`
  * [Data Classification](/handbook/engineering/security/data-classification-standard.html)
  * [No Red Data on Unapproved Locations](/handbook/people-group/acceptable-use-policy/#security-and-proprietary-information)

### Training Feedback
You are strongly encouraged to engage the team behind the training and provide feedback, or ask any questions related to the content of the training. You can do that through:
1. Monthly office hours held by the SecOps team on third Friday of each month. There are two sessions for both EMEA and APAC-friendly timeslots. Please see the **GitLab Team Meetings** calendar for current times.
1. A quarterly-reviewed GitLab issue for New Hire training - [FY21-Q1](https://gitlab.com/gitlab-com/gl-security/secops/operations/-/issues/736).
1. Annual security awareness training feedback issue: [2020 GitLab Security Awareness Training](https://gitlab.com/gitlab-com/gl-security/security-assurance/sec-compliance/compliance/-/issues/1924)
1. Email by sending an email to security-training@gitlab.com.

### Phishing Tests

GitLab conducts routine phishing tests at a minimum of once per quarter. All
team members may occasionally receive emails that are designed to look like
legitimate business-related communications but will in actuality be simulated
phishing attacks. Real phishing attacks are designed to steal credentials or
trick the recipient into downloading or executing dangerous attachments. No
actual attempts will be made by GitLab to steal credentials or execute malicious code.

The goal of these campaigns is not to catch people clicking on dangerous links
or punish those who do, but rather to get people thinking about security and the
techniques used by attackers via email to trick you into running malicious
software or disclosing web passwords. If you fall victim to one of these
simulated attacks feel free to take the training courses again or to ask the
security team for more information on what could've been done to recognize the
attack. What you shouldn't do is feel any shame for having clicked on the link
or entered any data, nor should you feel like you need to _cop_ to the security
team and let them know you made a mistake. Making a mistake online is
practically the reason the Internet was invented.

### How to identify a basic phishing attack

When you receive an email with a link, hover your mouse over the link or view
the source of the email to determine the link's true destination.

If you hover your mouse cursor over a link in Google Chrome it will show you
the link destination in the status bar at the bottom left corner of your browser
window.

![Hover Example](/images/phishing/hover-status-bar-example-chrome.png)

In Safari the status bar must be enabled to view the true link destination
(View -> Show Status Bar).

Some examples or methods used to trick users into entering sensitive data into
phishing forms include:

* Using HTTP(S) with a hostname that begins with the name of a trusted
site but ends with a malicious site.

![Malicious Domain](/images/phishing/malicious-domain.png)

* Using a username or password inside the request that corresponds to the name
of a trusted domain and assuming the viewer won't view the whole URL.

![Trick Username](/images/phishing/username-password.png)

* Using a data URI scheme instead of HTTP(S) is a particularly devious means of
tricking users. Data schemes allow the embedding of an entire web page inside
the URI itself. Data schemes will not show the typical green lock in the address
bar of a browser that is customarily associated with a verified SSL connection.

![Data Scheme](/images/phishing/data-scheme.png)

When viewing the source of an HTML email it is important to remember that the
text inside the "HREF" field is the actual link destination/target and the text
before the `</A>` tag is the text that will be displayed to the user.

`<a href="http://evilsite.example.org">Google Login!</a>`

In this case, "Google Login!" will be displayed to the user but the
actual target of the link is "evilsite.example.org".

After clicking on a link always look for the green lock icon and "secure" label
that signify a validated SSL service. This icon alone is not enough to verify the
authenticity of a website, however the lack of the green icon does mean you
should never enter sensitive data into that website.

![Green Lock Example](/images/phishing/green-lock-example.png)

### What to do if you suspect an email is a phishing attack

Whether you believe that you have received an email from our testing platform
or you suspect that the email is targeted specifically at you or GitLab, please forward
the phishing email to `phishing@gitlab.com` as an attachment for it to be investigated. Once you have done so, please proceed to step 2 and report the email as phishing from inside GMail.

To forward the email as an attachment from inside GMail:

  1. Right click the email
  2. Select "Forward as attachment"
  3. Send it to `phishing@gitlab.com`

GMail also offers the option to report the email directly to Google as a
phishing attempt, which will result in its deletion. Reporting the email
in this manner will help the security team track phishing metrics and trends over
time within G Suite.

To report the email as `phishing` from inside GMail:

  1. Select the "More" button (three dots) on the email in question
  1. Choose "Report phishing" option from the drop down menu

If you receive an email that appears to come from a service that you utilize,
but other details of the email are suspicious -- a private message from a
sender you don't recognize, for example -- do not click on any links in the
email. Instead use your own bookmark for the site or manually type the address
of the website into your browser.

Unsolicited email should be treated as phishing emails.  For example, if you
did not register for a site claiming to send you email, do not click on links
in the email or visit the site.

## Panic Email

GitLab provides a `panic@gitlab.com` email address for team members to use in
situations that require an immediate security response. This email address is
only accessible to GitLab team members and can be reached from their gitlab.com
or personal email address as listed in BambooHR. Should a team member lose
a device such as a thumb drive, YubiKey, mobile phone, tablet, laptop, etc. that
contains their credentials or other GitLab-sensitive data they should send an
email to `panic@gitlab.com` right away. When the security team receives an email
sent to this address it will be handled immediately. Using this address provides
an excellent way to limit the damage caused by a loss of one of these devices.

Additionally if a GitLab team member experiences a personal emergency the People Group also
provices an [emergency contact email](/handbook/people-group/#in-case-of-emergency).

## Other Security Topics

- [Security Team handbook](/handbook/engineering/security/)
- [Security questions from customers, and their answers](/security)
- [Using GPG Keychain for PGP](pgp_process/)
