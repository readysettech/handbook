---
layout: handbook-page-toc
title: "Other apps"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

This page lists various apps that may be useful for your workflow at GitLab.

## Internet browsers

### Ad privacy

Sharing your screen to get your idea across can be very productive, but having personalized ads show up on a webpage may be undesirable.
Shut off interest based ads by setting your preferences.
[Google Ad Settings](https://adssettings.google.com/), [AdChoices](http://optout.aboutads.info)

### Browser extensions

In general, if a particular application or browser extension (sometimes called a plugin) is referenced in the handbook, it is considered "approved".
For example, [1Password](/handbook/security/#1password-guide) is centered around the browser extension.
Another application is [Zoom](/handbook/tools-and-tips/#zoom), which has a scheduler extension.
However, be sure to search for specific information about the application, in case the desktop version is recommended and the browser extension is not (e.g. [Grammarly](#grammarly)).

If you wish to use an extension not referenced in the handbook, consider the following before installing and using it:

* The extension should be work-related and help your overall productivity.
* The extension should be available from a reputable source, such as the browser's library of approved extensions.
* Ask. Feel free to ask your co-workers about good extensions, and if you have security or privacy concerns about an extension, ask the security team in #security on Slack.

Some browser extensions are listed below

#### Adblockers

Adblockers are browser extensions that can block advertising, prevent user tracking, and include other security-related features.
A popular one recommended by the Security Team is [uBlock Origin](https://github.com/gorhill/uBlock/) which can be installed by following the links below:

- [Chrome](https://chrome.google.com/webstore/detail/ublock-origin/cjpalhdlnbpafiamejdnhcphjbkeiagm)
- [Firefox](https://addons.mozilla.org/addon/ublock-origin/)
- [Edge](https://microsoftedge.microsoft.com/addons/detail/odfafepnkmbhccpbejgmiehpchacaeak)

#### One Tab

[One Tab (Free)](https://www.one-tab.com/) tames tabs into a list which can be sorted and exported.

#### SessionBox

[SessionBox](https://sessionbox.io/discover) is a browser extension that helps you deal with multiple sessions.
It binds a particular session to a tab.
This is particularly useful for testing with different users in the same browser.

#### RSS Feed Reader

If you would like to receive daily notifications on newly opened issues, the Chrome extension [RSS Feed Reader](https://chrome.google.com/webstore/detail/rss-feed-reader/pnjaodmkngahhkoihejjehlcdlnohgmp) is an excellent tool for accomplishing this task.
After installing the extension, access the project page you are interested in following, under the project issues click on the "Subscribe to RSS feed" button which you can find in the top right corner of the page.

### Flash (do NOT use)

**Flash**: Due to security flaws, we strongly recommend _not_ using Adobe Flash.
Certainly do not install it on your local machine.
But even the Google Chrome plugin that lets you see embedded Flash content in websites can pose a security hazard.
If you have not already, go to your [Chrome Flash Settings](chrome://settings/content/flash) and disable Flash.
For further context, note that [Google Chrome is removing Flash support soon](https://nakedsecurity.sophos.com/2016/05/18/yet-more-bad-news-for-flash-as-google-chrome-says-goodbye-sort-of/), and while the [plugin is better than a local install of Flash](http://security.stackexchange.com/questions/98117/should-flash-be-disabled-or-are-sandboxes-secure-enough), 
it still leaves vulnerabilities for [zero-day attacks](http://www.pctools.com/security-news/zero-day-vulnerability/).

### Minimizing Google Chrome's resource usage

To minimize Google Chrome browser's memory and CPU usage, you can enable [Tab Freeze](chrome://flags/#proactive-tab-freeze) (you need to manually navigate to this url) which suspends tabs after five minutes of inactivity.

This is enabled by default from Chrome 80 and the option is removed.

### Prototyping in the browser

Sometimes you only need to capture small textual or visual changes in a web page as part of a bug report or a feature proposal.
You can use [development tools](https://en.wikipedia.org/wiki/Web_development_tools) that are usually built-in in most browsers which allow you to select and edit page element attributes as well as move around page elements like buttons or links.

You can also make the entire web page editable, using the [`designMode`](https://developer.mozilla.org/en-US/docs/Web/API/Document/designMode) attribute, by typing `document.designMode="on";` in the development tools console or creating a bookmarklet by dragging the button below to your Bookmarks Bar.

<a href="javascript:document.body.contentEditable='true'; document.designMode='on'; void 0" class="btn btn-primary">Edit page</a>

## Notes/writing

### Bear

[Bear (Free)](https://bear.app/) is a clean writing tool for notes and long-form writing.
[Ulysses $5/month](https://ulysses.app/) is also a great choice.

### Grammarly

[Grammarly](https://www.grammarly.com) is a good tool for those who want to feel more comfortable drafting written communication in English (American or British).
There is a free and premium version.

_Warning_: Grammarly browser extensions are discouraged, Grammarly will have access to everything you type in your browser, and they have had [a security problem](https://gizmodo.com/grammarly-bug-let-snoops-read-everything-you-wrote-onli-1822740378).
If you want to use it to check non-confidential text manually, you should download the [desktop version](https://www.grammarly.com/native/mac) instead.

### Simplenote

[Simplenote](https://simplenote.com/) is a free, open source note taking app which is cross platform, and syncs across all devices.

## Productivity

### Alfred

[Alfred](https://www.alfredapp.com/) is an application launcher and productivity tool for macOS.
The core app is free to download and use, but the paid [Powerpack](https://www.alfredapp.com/powerpack/) enables more powerful searching, a fantastic clipboard history feature, app integrations, easy access to shell commands, and more.
It's a great tool for developers and general productivity enthusiasts alike.
The clipboard history feature is nicely integrated with many tools, and for example will forget passwords copied from 1Password after they have been pasted.

If you'd like to share your calendar with e.g. your partner you can use the 'Share with specific people' feature and set the permissions to 'See only free/busy (hide details)':

```
https://docs.gitlab.com/search/?q={query}
```

```
/handbook/#stq={query}&stp=1
```

### Brain.fm

[Brain.fm (free trial)](http://brain.fm) provides music specially designed to help you focus, relax, meditate, recharge, sleep (great for plane rides).
It's not just music though.
They use scientifically validated brainwave manipulations to get results.
It is AMAZING and really does work.
Make sure to use with headphones, and give it 10-15 minutes for your brain to get used to it.
($6.95/$15.99/$47.40 per month/quarter/year)

### Calendly

[Calendly](https://calendly.com/) connects to your Google Calendar so people outside GitLab can easily book a time with you.
If you are scheduling a meeting with a GitLab team-member, please use Google Calendar and follow handbook guidance when [scheduling a meeting](/handbook/communication/#scheduling-meetings).

1. Set up a [Calendly](https://calendly.com/) account.
1. Link it to your GitLab Google Calendar to make it possible for people to schedule a call with you.
1. Get your personal meeting room URL by going to [Zoom meeting settings](https://gitlab.zoom.us/meeting), selecting the *Personal Meeting Room* tab, and copying the value of *Join URL* (do not use *Copy the invitation*).
1. Set up the 45 minute time slot with the following event description text (replacing text in `{}` with your information):

> This will be a Zoom Meeting at {Zoom personal meeting room URL}
>
> Question? Please email me. {your GitLab email}

1. Set the event name to `45 Minute Meeting`.
1. Change the event link to `45min`.
1. The event description needs to be copied to the 15, 30 and 60 minute meetings as well.
1. If you intend to use any of the other event types, make sure to add this to their event descriptions as well.
1. For people outside of GitLab Inc, send them your Calendly link that links directly to the 45 minute time slot: "Are any of the times on https://calendly.com/XXXXX/45min/ convenient for you? If so please book one, if not please let me know what times are good for you and we'll find an alternative."
1. Update your availability on [Calendy Event Types](https://calendly.com/event_types/) by clicking the action cog and then the edit option on an event type (For Example: 15 minute meeting) and in the event details clicking on the "When can people book this event?" section then clicking the "Availability" section.
   Here you can set your working hours during which you want to accept meetings, and on the "Advanced" tab you can set the minimum scheduling notice you want enforced.
   Although Calendy does synchronize with Google Calendar to show your availability you may wish to set extra restrictions in Calendy.
   You can use the "Copy Availability From" option on all the other events you have configured one event.

Keep in mind that unlike normal Google Calendar events, Calendly events are not automatically synchronized between both parties when changes are made.
If an event needs to be cancelled or modified, make sure to use Calendly to do so.

### Clockwise

[Clockwise](https://www.getclockwise.com/) is a tool for optimizing your schedule to free up time for you to focus. It will look for opportunities to reschedule meetings when it's most efficient for attendees, and give you uninterrupted time to work. Clockwise integrates with your [calendar](/handbook/tools-and-tips/#google-calendar), and when possible will move events automatically on your behalf.

### Freedom

If you find yourself switching to websites you find distracting, especially during periods that require focus, and you worry it may affect your productivity, consider using [Freedom](https://freedom.to/why).
Their browser extensions, mobile apps, and desktop apps block distracting websites and apps for the duration of a configurable session.
If you find yourself typing `f` and hitting `enter` from muscle memory, you will not be scrolling through endless pages of photos of your friends' lunches.

### Paste

[Paste for macOS](https://pasteapp.me/) is a clipboard manager that stores everything you copy and optionally syncs across all your devices.
It allows you to organize frequently copied data in pinboards, so that you do not need to copy the same data over and over, provides search, multiple paste and has nice visual user interface.

### Pomodoro technique

The [Pomodoro Technique](https://en.wikipedia.org/wiki/Pomodoro_Technique) is a simple time management process that can be used to boost productivity by dividing time into "work" and "break" intervals.
In brief, each half-hour block of time is divided into a 25 minute work session followed by a 5 minute break session.
Do this twice per hour until the day is done and marvel at how much you've finished.

Various [Chrome extensions](https://chrome.google.com/webstore/search/pomodoro "Chrome Web Store - pomodoro"), [Firefox add-ons](https://addons.mozilla.org/en-US/firefox/search/?q=pomodoro "Search results for \"pomodoro\" – Add-ons for Firefox (en-US)"), mobile apps, desktop apps, and even fancy physical alarm clocks are available to help you track your intervals, but you can use almost any timer you have on hand&mdash;even and especially that cute little tomato timer in your kitchen.

### Quitter

[Quitter (Free)](https://marco.org/apps) will switch off apps for you after some period of inactivity.
Consider using this to hide Slack after a while to reduce your urge to check new messages all the time.

### TripMode

[TripMode ($7.99)](https://www.tripmode.ch/) lets you control which apps can use the internet.
Especially useful when you're working on a cellular/metered connection.

## Text editors

### JetBrains

We have a central account for managing licenses of JetBrains' products like RubyMine or GoLand.
If you want to use one of their products, please log an [Access Request](https://gitlab.com/gitlab-com/team-member-epics/access-requests) and select the best option for your situation (single user, bulk user, etc.) and, once approved by your manager, assign to the System Provisioner listed in the [Tech Stack](https://docs.google.com/spreadsheets/d/1mTNZHsK3TWzQdeFqkITKA0pHADjuurv37XMuHv12hDU/edit#gid=0) for this system.
Once your access has been provisioned, you will receive a link with which you can redeem your license.
Make sure to use your company email address when creating your Jetbrains account.
If at some point in the future you do not want to use the product anymore, please notify us via `jetbrains@gitlab.com`, so that we can assign the license to someone else.

Useful plugins:

- [GitLink](https://plugins.jetbrains.com/plugin/8183-gitlink/) - It provides a shortcut to open a file or commit in GitLab.

### Sublime Text

Putting the following in Preferences.sublime-settings - User will among other things ensure that if you open the www-gitlab-com website you're not opening the output files by accident:

```
{
  "font_size": 18,
  "spell_check": true,
  "translate_tabs_to_spaces": true,
  "trim_trailing_white_space_on_save": true,
  "folder_exclude_patterns": ["public"]
}
```

## Video calling

### Krisp

[Krisp](https://krisp.ai/) will mute background noise when you're in a noisy environment so you can hear and be heard more easily on calls.

### MobileDay

If you install [MobileDay (Free)](https://mobileday.com/) on your phone and give it access to your Google Calendar it can dial into conference calls for you.
It is very good at detecting the number and password from the calendar invite.

### Shush

[$4.99 tool for macOS](http://mizage.com/shush/) that lets you set a hotkey (e.g. `fn`) to mute your microphone ("push-to-talk" or "push-to-mute").
Never again will you have to switch your window focus to Google Hangouts or Zoom to speak or mute.
The icon will show the current state of your mic input (x means muted).
With a right click (or your configured hotkey) you can switch from push to talk to push to mute.
Don't forget to unblock your mic in Zoom/Google Hangouts immediately after joining.
Be warned that page up with fn+down arrow will activate it.
Use space for page down instead of fn+up arrow.
**Warning**: Check your [headset compatility](http://mizage.clarify-it.com/d/jv2enz) before purchase.
Many usb headsets are unmutable.

#### Shush alternative for Linux

If you use Linux (e.g. [Arch](https://www.archlinux.org/), [Ubuntu](https://www.ubuntu.com/) or [Fedora](https://getfedora.org/)) you can create a system-wide keyboard shortcut to mute/unmute your mic.
Please note that it only works for Linux distributions which use [ALSA](http://alsa-project.org) for sounds (most popular Linux distributions use ALSA).
All you need to do is go to your desktop environment's _Keyboard Settings_ and create a custom shortcut with the command `amixer set Capture toggle` and assign a key combination of your choice (e.g. `Pause Break` key).
Once this is done, you can mute/unmute your mic using the assigned keyboard shortcut while you're in any application.
Refer to this original answer on [Askubuntu](http://askubuntu.com/a/13364/12242) to learn more.

### Webex

GitLab uses [Zoom](https://zoom.us/) as the primary video collaboration platform for internal and external communications. Some of our customers and partners have different preferred tools and to facilitate the communication with those parties, GitLab provides licenses for WebEx. This service is only provided to team members that have a business need to host meetings and where Zoom is not accepted. 

- To request access to those tools, create an [access request](https://gitlab.com/gitlab-com/team-member-epics/access-requests/-/issues/new?issuable_template=Single_Person_Access_Request) and provide a justification for access.  
- Consider installing their [native app](https://www.webex.com/downloads.html).
- Before attending a Webex meeting you can test to ensure your Webex is setup correctly by joining a [test meeting](https://www.webex.com/test-meeting.html).
- The in-browser plugin the screen sharing sometimes doesn't work.

### Whereby

[Whereby](https://whereby.com/) allows you to instantly create a free video chat room for up to 4 participants with no login and no installation.
It also offers a free reliable mobile video conference app.

## Videos, gifs, and screenshots

### Loom

[Loom (Free)](https://www.useloom.com/) is a handy Chrome plugin tool for video walkthroughs.
Nice tool for demo recordings and internal/external documentation.

### Teampaper Snap

[Teampaper Snap (Free / Mac only)](http://teampaper.me/snap/) is the ultimate screen capture tool for Mac to voice your thoughts on anything you can see on a screen.
