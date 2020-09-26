---
layout: handbook-page-toc
title: Corporate Marketing
---
## Welcome to the Corporate Marketing Handbook
{:.no_toc}

The Corporate Marketing team includes Content Marketing, Corporate Events, PR (Public Relations), All-Remote Marketing, and Design. Corporate Marketing is responsible for the stewardship of the GitLab brand and the company's messaging/positioning. The team is the owner of the Marketing website and oversees the website strategy. Corporate Marketing develops a global, integrated communication strategy, executes globally, and enables field marketing to adapt and apply global strategy regionally by localizing and verticalizing campaigns for in-region execution. Corporate marketing also ensures product marketing, outreach, and marketing & sales development are conducted in a way that amplifies our global brand.

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## How We Work

### Project Management

There is an initiative underway to simplify Project Management across all of Marketing.

In the meantime, we have implemented a few practices to help us get organized:

- Add weekly milestones to issues based on the week you expect to work on the issue (format is `Fri: Apr 17, 2020`)
- Move issues forward into future milestones, or place them in the `backlog` milestone if they're no longer planned
- We close out the week's milestone each week, and issues will be moved forward if they are not closed out
- You can use labels however you like, they are a tool for you and your team to filter/sort issues

## Brand personality

GitLab's brand has a personality that is reflected in everything we do. It doesn't matter if we are hosting a fancy dinner with fortune 500 CIOs, at a hackathon, or telling our story on about.gitlab.com...across all our communication methods, and all our audiences, GitLab has a personality that shows up in how we communicate.

Our personality is built around four main characteristics.

1. Human: We write like we talk. We avoid buzzwords and jargon, and instead communicate simply, clearly, and sincerely. We treat people with kindness.
1. Competent: We are highly accomplished, and we communicate with conviction. We are efficient at everything we do.
1. Quirky: We embrace diversity of opinion. We embrace new ideas based on their merit, even if they defy commonly held norms.
1. Humble: We care about helping those around us achieve great things more than we care about our personal accomplishments.

These four characteristics work together to form a personality that is authentic to GitLab team-members, community, and relatable to our audience. If we were `quirky` without being `human` we could come across as eccentric. If we were `competent` without being `humble` we could come across as arrogant.

GitLab has a [higher purpose](/company/strategy/#mission). We want to inspire a sense of adventure in those around us so that they join us in contributing to making that mission a reality.

## Tone of voice

The following guide outlines the set of standards used for all written company
communications to ensure consistency in voice, style, and personality, across all
of GitLab's public communications.

See [the Blog Editorial Style Guide](/handbook/marketing/growth-marketing/content/editorial-team/) for more.

### About

#### GitLab the community

GitLab is an [open source project](https://gitlab.com/gitlab-org/gitlab-ce/)
with a large community of contributors. Over 3,000 people worldwide have
contributed to GitLab's source code.

#### GitLab the company

GitLab Inc. is a company based on the GitLab open source project. GitLab Inc. is
an active participant in our community (see our [stewardship of GitLab CE](/company/stewardship/)
for more information), as well as offering GitLab, a product (see below).

#### GitLab the product

GitLab is a complete DevOps platform, delivered as a single application. See the
[product elevator pitch](/handbook/marketing/product-marketing/messaging/)
for additional messaging.

### Tone of voice

The tone of voice we use when speaking as GitLab should always be informed by
our [mission & vision](https://about.gitlab.com/company/strategy/#mission).
Most importantly, we see our audience as co-conspirators, working together to
define and create the next generation of software development practices. The below
table should help to clarify further:

<table class="tg">
  <tr>
    <th class="tg-yw4l">We are:</th>
    <th class="tg-yw4l">We aren't:</th>
  </tr>
  <tr>
    <td class="tg-yw4l">Equals in our community</td>
    <td class="tg-yw4l">Superior</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Knowledgeable</td>
    <td class="tg-yw4l">Know-it-alls</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Empathetic</td>
    <td class="tg-yw4l">Patronizing</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Straightforward</td>
    <td class="tg-yw4l">Verbose</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Conscientious</td>
    <td class="tg-yw4l">Disrespectful</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Playful</td>
    <td class="tg-yw4l">Jokey</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Helpful</td>
    <td class="tg-yw4l">Dictatorial</td>
  </tr>
  <tr>
    <td class="tg-yw4l">Transparent</td>
    <td class="tg-yw4l">Opaque</td>
  </tr>
</table>

We explain things in the simplest way possible, using plain, accessible language.

We keep a sense of humor about things, but don't make light of serious issues or
problems our users or customers face.

We use colloquialisms and slang, but sparingly (don't look like you're trying too hard!).

We use [inclusive, gender-neutral language](https://litreactor.com/columns/5-easy-ways-to-make-your-writing-gender-neutral).

## Updating the press page

### Adding a new press release

1. Create a new merge request and branch in www-gitlab-com.
1. On your branch, navigate to `source` then `press` and click on the [`releases` folder](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master/source/press/releases).
1. Add a new file using the following format `YYYY-MM-DD-title-of-press-release.html.md`.
1. Add the following to the beginning of your document:

```
---
layout: markdown_page
title: "Title of press release"
description: "short sentence overview of press release'
twitter_image: "/location/of/image.png"
twitter_creator: "@gitlab"
twitter_site: "@gitlab"
twitter_image_alt: "Celebrating GitLab's press release about xx with fun emojis"
---
```

`description`, `twitter_image`, and `twitter_image_alt` would be the three, net-new tags needed to be custom to every single release. `twitter_creator` and `twitter_site` would be static with the value "@gitlab".

1. Add the content of the press release to the file and save. Make sure to include any links. It is important to not have any extra spaces after sentences that end a paragraph or your pipeline will break. You must also not have extra empty lines at the end of your doc. So make sure to check that when copying and pasting a press release from a google doc.
1. Assign @wspillane to the MR to add the social sharing image to the `twitter_image:` section above and to merge the release. If the team has previously discussed the work, the social team may have already created a sharing image. If not, they will need to create it from this mention. The social team will add the data necessary to the MR for social sharing and merge the press release.

### Updating the `/press/#press-releases` page

When you have added a press release, be sure to update the index page too so that it is linked to from [/press/#press-releases](/press/#press-releases).

1. On the same branch, navigate to `data` then to the [`press_releases.yml` file](https://gitlab.com/gitlab-com/www-gitlab-com/blob/master/data/press_releases.yml).
1. Scroll down to `press_releases:`, then scroll to the most recent dated press release.
1. Underneath, add another entry for your new press release using the same format as the others, ensuring that your alignment is correct and that dashes and words begin in the same columns.
1. The URL for your press release will follow the format of your filename for it: `/press/releases/YYYY-MM-DD-title-of-press-release.html`.

### Updating the recent news section

1. Every Friday the PR agency will send a digest of top articles.
1. Product marketing will update the `Recent News` section with the most recent listed at the top. Display 10 articles at a time. To avoid formatting mistakes, copy and paste a previous entry on the page, and edit with the details of the new coverage. You may need to search online for a thumbnail to upload to `images/press`, if coverage from that publication is not already listed on the page. If you upload a new image, make sure to change the path listed next to `image_tag`.

- - -

## Design

Read more about our brand guidelines in the [Brand and Digital Handbook](/handbook/marketing/growth-marketing/brand-and-digital-design/).

- - -

## Speakers

##### For GitLab Team-members Attending Events/ Speaking

- If you are interested in finding out about speaking opportunities join the #cfp Slack channel. Deadlines for talks can be found in the Slack channel and in the master GitLab [events spreadsheet](https://docs.google.com/spreadsheets/d/16usWToIsD-loDQYpflaMiGTmERMYSieNj_QAuk5HBeY/edit#gid=1939281399).
- If you want help building out a talk, coming up with ideas for a speaking opportunity, or have a customer interested in speaking start an issue in the marketing project using the [CFP submissions template](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=CFPsubmission) and tag any associated event issues. Complete as much info as possible and we will ping you with next steps. We are happy to help in anyway we can, including public speaking coaching, and building out slides.
- If there is an event you would like to attend, are attending, speaking, or have proposed a talk and you would like support from GitLab to attend this event the process goes as follows:

1. Contact your manager for approval to attend/ speak.
1. After getting approval from your manager to attend, [add your event/ talk](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/data/events.yml) to the [events page](/events/) and submit merge request to Emily Kyle.
1. If your travel and expenses are not covered by the conference, GitLab will cover your expenses (transportation, meals and lodging for days said event takes place). If those expenses will exceed $500, please get approval from your manager. When booking your trip, use our travel portal, book early, and spend as if it is your own money. Note: Your travel and expenses will not be approved until your event / engagement has been added to the events page.
1. If you are speaking please note your talk in the description when you add it to the Events Page.
1. If you are not already on the [speakers page](/events/find-a-speaker/), please [add yourself](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/data/speakers.yml).
1. We suggest bringing swag and/or stickers with you. See notes on #swag on this page for info on ordering event swag.

- If your talk is recorded, we encourage speakers to publish their talks to YouTube. Speakers should [upload their talks to GitLab Unfiltered](/handbook/marketing/marketing-operations/youtube/#uploading-conversations-to-youtube) or, if published elsewhere on YouTube, [add the recording](https://support.google.com/youtube/answer/57792) to the `GitLab Tech Talks` playlist on GitLab Unfiltered.

##### Finding and Suggesting Speakers and Submitting to CFPs

- Speaker Portal: a catalogue of talks, speaker briefs and speakers can be found on our [Find a Speaker page](/events/find-a-speaker/). Feel free to add yourself to this page and submit a MR if you want to be in our speaker portal and are interested in being considered for any upcoming speaking opportunities.
- If you have a customer interested in speaking start an issue in the marketing project using the CFP submissions template and tag any associated event issues. Complete as much info as possible and we will ping you with next steps. We are happy to help in anyway we can, including public speaking coaching.

##### Best practices for public speaking

Below are some tips on being a better presenter. For an in-depth book that covers the entire speaking process, from submitting an abstract through preparing a structured talk to practicing and delivering read [Demystifying Public Speaking](https://abookapart.com/products/demystifying-public-speaking).

1. Use a problem/solution format to **tell a story**. Many talks, especially tech talks, talk about what they built first and then what the result was. Flip this around and [start with the why](https://www.ted.com/talks/simon_sinek_how_great_leaders_inspire_action). Why did you need to take the action that you did? Talking about what problems you were encountering creates a narrative tension and people will listen intently to the talk because they want to hear the solution.
1. **Drive towards an action**. Ask yourself, "What will people do once they hear this talk?" The answer can't be, "be more aware of this topic." By deciding what action you expect the audience to take you can build your talk to drive towards this action. Talks that motivate the audience to action are more engaging and memorable than talks that simply describe. Some good example answers are
    1. Contribute to an open source project.
    1. Implement the technology or process you've come up with
    1. Follow the best practices you've outlined
1. **Practice how you play**. Practicing your talk is key to being a great presenter. As much as possible, practice exactly how you plan to give the talk. Sand up and pretend you are on stage rather than sitting down. If you'll demo, build the demo first and practice the demo. Even practicing while wearing the outfit you plan to wear can help.
1. **Give concrete examples**. Real life details bring a talk to life. Examples help people to understand and internalize the concepts you present. For each of your points try to have a "for instance." As an example, "We recommend using this script to delete old logs and free up diskspace. For instance, one time our emails lit up as users were complaining about slow performance. Some were reporting tasks hanging for over an hour when they should have completed in less than a minute. It turned out we were out of diskspace because we had verbose logging enabled. Once we ran the script we saw performance return to normal levels."
1. **Be mindful of your body language** when presenting as it will impact the way the audience perceives your presentation. Move around the stage purposefully (don't pace or fidget). Make natural gestures with your hands, and maintain good posture to convey confidence and openness which will help you to better connect with your audience.

### Customer Speakers

For ideas to help customers get their submissions accepted, see [How to Get Your Presentation Accepted (video)](https://www.youtube.com/watch?v=wGDCavOCnA4) or schedule a chat with a [Developer Evangelism](/handbook/marketing/community-relations/developer-evangelism/) team member.

- - -

## Corporate Events

### Mission Statement

- The mission of the Corporate Events Team is to:
    - Showcase the value and strengths of GitLab on all fronts
    - Deliver creative solutions to problems
    - Provide exceptional service
    - Build lasting and trusting vendor and internal relationships
    - Treat everyone like they are our most valued customer, including fellow GitLab team-members

### What does the corporate Events team handle?

- **Sponsored events** (events with global audience of 5000+ attendees for NA, 3000+ for other territories (50% or more of audience is national or global). There are some exceptions. There are handful smaller events that we handle due to the nature of the audience, product specific, and the awareness and thought leadership positions we are trying to build out as a company). The primary goal is always driving brand awareness but that cannot be the only result.
- **Owned events**
    - [GitLab Commit](/events/commit/), our User Conference
    - GitLab Culture Open House Events- by invite only
- **Internal events** (Contribute-sized events)
    - [GitLab Contribute](/events/gitlab-contribute/), our internal company and core community event
    - We also serve as DRI for all internal Sales events- [SKO's](/events/sko21/), Force Management planning, Rewards Travel, SQS, QBR's. Must be above 25 people attending for corp events involvement.
    Please review our events decision tree to ensure Corporate Marketing is the appropriate owner for an event. If it is not clear who should own an event based on the [decision tree](https://docs.google.com/spreadsheets/d/1aWsmsksPfOlX1t6TeqPkh5EQXergt7qjHAjGTxU27as/edit?usp=sharing), please email events@gitlab.com.
- **Speaker management and session production** for internal and external GitLab speakers. This includes management of the GitLab-owned call for proposal (CFP) process, agenda-buildng sessions, coordinating speaker communications, and establishing work-back and event-day run of show schedules.

### Corporate Events Strategy / Goals

- **Brand**
    - For Sponsored Events: Get the GitLab brand in front of 15% of the event audience. 40,000 person event we would hope to get 4,000+ leads (10%) and 5% general awareness and visibility with additional branding and activities surrounding participation.
    - Human touches- Tracked by leads collected, social interactions, number of opportunities created, referrals, current customers met, and quality time spent on each interaction.
    - Audience Minimum Requirements- volume, relevance (our buyer persona, thought leaders, contributors), reach (thought leaders?), and duration of user/ buyer journey considered.
- **ROI**
    - Work closely with demand gen campaigns and field marketing to ensure events are driving results and touching the right audience.
    - Exceed minimum threshold of ROI for any events that also have a demand gen or field component- 5 to 1 pipe to spend within a 1-year horizon.
    - Aim to keep the cost per lead for a live event around $100.
    - [ROI Calculator](https://docs.google.com/spreadsheets/d/1SAYGXysUHGXPKrTDFf9yRcQrh9TYNxR9_Ts6H9dq8JY/edit?usp=sharing) we aim to make 5x ROI on pipeline focused events but this can be used to estimate what return we might get on an event.
- **Thought Leadership and Education**

### GitLab Commit User Conferences

- [Link to 2020 Slack Channel](https://gitlab.slack.com/archives/CK8HV2A10/)
- Commit Virtual 2020- [Planning Epic](https://gitlab.com/groups/gitlab-com/marketing/-/epics/915)
- Goal Call for proposals (CFP) and agenda-setting process:
    - 9+ months pre-event: Open an internal call for track issue (GitLab team members)
    - 7+ months pre-event: Select Commit track(s)
    - 6+ months pre-event: Open a public call for proposals (CFP) form and invite contributions
        - Track manager trainings and establishment of deadlines and workflows
    - 5+ months pre-event: Convene the CFP selection committee
    - 4+ months pre-event: Early session acceptances begin
    - 3+ months pre-event: CFP closes; Next round of acceptances sent
    - 2+ months pre-event: Final acceptances sent; sponsorships close
        - Any submissions not selected are thanked and – should the proposal be a potential fit for a future event – invited to stay in touch for participation at a later date
        - Draft agenda is reviewed by stakeholders for strength and diversity of content and speakers
    - 1+ month pre-event: Agenda is final and publishable
- GitLab's event experience is unique for speakers in the hands-on approach that the Corporate Events team takes to ensure that speakers feel supported and prepared. A typical Commit speaker experience will include:
    - Access to a speaker page with all relevant deadlines, resources, and contact information
    - One-on-one access to a presentation support team, including the session track manager and production manager
    - Dedicated working document or email thread between the speaker, track manager, and production manager to work through final session title, description, and slide content
    - 2-3 Zoom meetings to discuss session flow and practice for timing, pace, and polish
    - Weekly communication and updates
    - Optional training and slide creation support
- Commit Virtual for GitLabbers:
    - We need support the day of the event with such tasks as chat moderator, booth staffing, social monitoring support...
- Onsite at Commit for GitLabbers:
    - You will be assigend one or multiple onsite tasks. It is crititcal you show up for your set duty and communicate any changes in your plans. Clean your schedule on the day of the event, as it will be a full day commitment.
        - Tasks include:
            - Track Scanning- it is essential you show up and stay for this if you are assigned. Our partners have paid to get leads form thir talks and it is our promise to provide said leads. All talk attendees must be scanned for this purpose.
            - Check in Support
            - Swag table
            - Questions/ help desk
            - Booth Duty (Hiring, UX, Support, Security, Demo..) - do not leave the booth unstaffed. We have back up. Ask for helpo on coverage if you need it.
    - Dress code: casual to business casual. Wear what you feel comfortable in. No open toed shoes for safety reasons.
    - Team Travel
        - Team members may come in the day before the event and stay the night of the event. No additional days will be covered unless you have arranged a special circumstance with the Commit planning team.
        - We can only provide Visa support for speakers and extrenal attendees for this event series.
        - If you live within 60 miles of the event you will be asked to commute to the event unless you have a specific arrangement with the Commit planning team.

<figure>
  <iframe src="https://calendar.google.com/calendar/b/1/embed?height=600&amp;wkst=1&amp;bgcolor=%23ffffff&amp;ctz=UTC&amp;src=Z2l0bGFiLmNvbV9sbzZ0dm92Nmhtdm50NTYybGlwYWVnbGJ2b0Bncm91cC5jYWxlbmRhci5nb29nbGUuY29t&amp;color=%23009688&amp;showPrint=0" style="border-width:0" width="800" height="600" frameborder="0" scrolling="no"></iframe>
</figure>

### RFP Process

- See finance handbook for when you need to go through RFP process
- Use RFP Templates for uniform evaluation of vendors
    - [Questionnaire](https://docs.google.com/spreadsheets/d/154wEnFfBBOq0l_dq23LfGBWI1JHPwL1U_ERDZNjF67k/edit?usp=sharing) to send to vendors bidding
    - [DMC RFP Template](https://docs.google.com/document/d/1dGEffBse3FMnsM3YSVDUs848AU7Rn4DJRfn2l_nTcTQ/edit?usp=sharing)
    - Questions on using the templates ask them in the corporate-events-team Slack channel.

### Event Execution

For event execution instructions, please see the [Marketing Events page](/handbook/marketing/events/#event-execution) for detail instruction and the criteria used to determine what type of events are supported.

### Best Practices on site at a GitLab event

- [Employee Booth Guidelines](/handbook/marketing/events/#employee-booth-guidelines)
- [Scanning Best Practices](/handbook/marketing/events/#scanning-best-practices)

## Accessibility at GitLab Hosted Events

### In advance of the event, we promise that we will take into account the following:

- Accessibility will not be an afterthought.
- Events will be inclusive and accessible.
- Venues will meet International Accessibility Standards guidelines.
- There will be seating available and accessible seating made available upon request
- There will be gender neutral pronouns in event communication.
- General dress guidance will not include male/female binary descriptors, and attendees can decide for themselves what works best for them.
- Feedback will be collected during and after the event to gauge accessibility and comfort levels.
- Designated confidential resources will be available for team members.
- Name badges will have write-in areas, printed or stickers for preferred pronouns.
- Large group meals will have ingredients and allergens listed. If you have communicated your needs with the event staff and the kitchen cannot provide a suittable meal for you, there will be a designated amount you can expense per meal on site.
- The Events team will commit to the idea that no detail is too small
- For all GitLab hosted events of 300+ we hire security that is also certified in first aid.

### Communicating Accessibility

- Gathering attendee needs during registration.
    - Dietary restrictions: If you have any questions, please follow up with the individual privately. Determine the specific restrictions and provide information on how ingredients will be provided. Offer solutions in case there is an issue onsite so that the attendee is prepared.
    - Additional needs: Include an open text area in which attendees can list specific needs to help ensure full guest participation. Example requests include interpreting services, assistive listening devices, accessible parking, accessible hotel rooms, captioning, Reserved front row seat, wheelchair access to working tables throughout the room, Lactation room, or seating for in-person events. The team will make all good faith efforts to carry out requests, or will open lines of disscussion for options when not available.
    - Preferred pronouns: Aim to avoid a closed field for gender and instead provide a blank write-in field or inclusive dropdown options so attendees can select/type their preference pending on the badging system. This information will be displayed on name badges, or available to add with stickers etc.
    Email and landing page communication
- Put accessibility information in the event page footer or have a page dedicated to accessibility.
- Send out email on accessibility specifics and resources in advance of the event. Examples of what to communicate in that email:
    - Use of flash photography
    - Any sort of strobe lights or flashing images that may cause seizures
    - Distinctly amplified sounds/music
    - The use of fog machines/any other chemicals or smells that may make your space inaccessible to individuals with Multiple Chemical Sensitivity (MCS) or Idiopathic Environmental Intolerances (IEI)
    - Whether interpreting services will be provided for various speakers, panels, talks, etc.
    - Whether assistive listening devices will be provided.
    - All optional parts of your event, including off-site social activities, that may not be fully accessible.
    - Information about meals and dietary restrictions.
    - Accessible transportation options
    - First Aid/Medical Assistance options
    - Info on how to get in touch with questions or concerns.

### For speakers

- Speak clearly (ideally facing forward without covering your mouth)
- Avoid acronyms and colloquialisms as much as possible
- When addressing someone specifically, ask for his/her/their name and confirm pronouns
- Specify when you’re finished speaking
- For interpreters, always look at and address the participating attendee
- Repeat questions posted by the audience before responding, especially if there is not a roving microphone available.

### Coming soon

- **Supplier/ Vendor diversity list that encourages the use of LGBTQ-, woman-, veteran-, or minority-owned businesses.**
- **Venue Sourcing Accessibility Checklist**

- - -

## Swag

### Swag for Events - [see details on Events page](/handbook/marketing/events/#swag)

All swag requests, creation and vendor selection is handled by the Corporate Marketing team.

- We aim to have our swag delight and/or be useful. We want to create swag that is versatile, easy to store and transport.
- As a remote company with team members in over 50 countries - our swag often has to go on miraculous journeys.
- With this in mind we try to ship things that are durable, light and that will unlikely get stuck in customs.
- We strive to make small batch, limited edition and themed swag for the community to collect.
- Larger corporate events will have custom tanuki stickers in small runs, only available at the specific event.
- Region specific sticker designs are produced quarterly.
- Our goal is to do swag in a way that doesn't take a lot of time to execute -> self-serve => [web shop](https://gitlab.myshopify.com/)

### Community & External Swag Requests

If you would like to get some GitLab swag for your team or event, email your request to `sponsorships@gitlab.com` (managed by the [community advocacy team](/handbook/marketing/community-relations/community-advocacy/#expertises)).
In your request include:

- expected number of guests
- best shipping address
- phone number
- type of swag you are hoping for

The swag we have available can be found on our online store. **Note**: It is recommended submit your request for swag at least **4 weeks in advance** from the event date or we may not be able to accommodate your request.

### Internal GitLab Swag Ordering:

- Event Swag (for FM and community): To request GitLab swag for an event you are attending see instructions below.
    - The event must be 3 or more weeks away for all swag and material requests. Rush shipping is not an option.
    - NORAM Field marketing and Community Relations should email our contact at Nadel for event swag shipments. Let them know what you want, when and where you need it. They will send your parcel with a return shipping label to get any remaining items shipped back to their warehouse. We have a list of approved items with Nadel you can order from. Any new items must be approved by brand team for brand consistency - Nadel will email all final designs to brand team for approval.
    - Not in Field Marketing or Community Relations? You can place small event swag orders by emailing `sponsorships@gitlab.com`. Include the date needed, shipping address and items / volume desired. The request will be approved on the back end by the community team. All requests must be made 3 or more weeks out. You can expect a response within 5 business days.
    - Paper/Print Collateral: In order to be [efficient](/handbook/values/#efficiency), we do not make custom print assets for events. We avoiod printed materials because they are instantly out of date and to help support the efforts to reduce waste.
    - We have an event kit with a [banner and table cloth](/images/events/GitLabPopupBoothMarch2019.pdf). Contact `events@gitlab.com` if you would like to borrow this setup. You will be shipped this set along with a return label.
    - For larger swag orders (stickers in a quantity of 100 or greater), do not go through the swag store but rather use our [Stickermule](https://www.stickermule.com/) account or ping `dsumenkovic@gitlab.com`. Include address, date needed and order quantity in request.
    - If you have any issues with your order please email `events@gitlab.com` with your concerns.
- GitLab team-member Swag - if you would like to order something from the GitLab swag shop we have a discount code you can use for 30% off (found in the channel description). Please see the swag Slack channel to get code to be used in the [store](https://shop.gitlab.com/) at checkout.
- We have specific shirts available for customer meetings. If you feel you need one of these shirts please email `events@gitlab.com`.

### Returning Swag to Warehouse

- If you have items that need to be returned to the warehouse please contact `events@gitlab.com` or find the FexEx account number in 1password to create a return label. Returns are only recommended if you have a very large number of items (50+) or a booth setup (banner, tablecloth, backdrop) that need to be returned.

### Swag for customer/ prospects

- Anyone can request to send swag to customers, prospects, candidates, or partners by following the process outlined for external [Swag Requests](/handbook/marketing/community-relations/community-advocacy/workflows/merchandise-handling/#swag-requests).
- Questions about the order process should be posted in the #swag Slack channel. A Corporate Marketing team member or Community Advocate will reply within 24-48 business hours.
- Please review the following guidelines for what is appropriate to send based on customer deal size:

| Deal Size, by License | Suggested Order |
| --------------------- | --------------- |
| 50-100 | 2 shirts, 2 socks, up to 20 stickers |
| +100-250 | 2 shirts, 2 socks or stojo mugs, up to 200 stickers |
| +250-500 | 5 shirts, 5 socks or stojo mugs, 5 DevOps or purple pens, up to 100 stickers |
| +500-1000 | 10 shirts, 5 socks or stojo mugs, 5 DevOps or purple pens, up to 250 stickers |
| +1000 | 1 hoodie, 20 shirts, 8 socks or stojo mugs, 5 DevOps or purple pens, max 500 stickers |

Baby Onesies: Baby onesies are available in the sales swag campaign can be sent to customers as needed/requested.

####Additional Items Available:

The following items are currently available to be sent to customers based in the US. This restriction is in place to keep shipping costs low as we move through extra inventory.

| Item | Suggested Order |
| ---- | --------------- |
| Black Leater Power Bank | up to 5 |
| Collapsible Straw | up to 10 |
| Colored Pencils | up to 5 |
| Orange Squid Charger | up to 5 |
| Luggage Tag | up to 5 |
| Lanyard Water Bottle Holder | up to 15 |
| Purple Notebook | up to 3 |
| Packable Bag | up to 5 |
| Purple Tanuki Socks | up to 3 |
| Tanuki Top Squid Charger | up to 5 |

- If you have additional questions on what is appropriate to send, please review [sending swag to customers parameters](https://gitlab.com/gitlab-com/sales/issues/144).
- SA's, TAM's, and AE's should coordinate with their SDR to send swag to customers.
- Each SDR with an account has a set budget of $50 to spend on sending swag and gift cards monthly. Mid market and SMB reps have $100.
- All sends are tracked in SFDC, in either the physical or coffee swag campaign.
- Orders placed for customers via the Printfection link are subject to change based on inventory availability and cost.
- _NOTE:_ Please keep in mind the [list of countries we do not do business in](/handbook/sales/#export-control-classification-and-countries-we-do-not-do-business-in).

### Swag Providers We Use

- See [issue](https://gitlab.com/gitlab-com/marketing/general/issues/1554) for vendors we use and what we order from them.
- Please direct swag vendor suggestions to the `#swag` Slack channel.

### New and Replenishment Swag Orders

Corporate handles the creating and ordering of all new swag. All swag designs should be run past design (Luke) for approval before going to production.

- If you need swag for an upcoming event complete the swag selection of the event template and corporate will be in touch on issue to complete request. Note: at least 6 weeks to produce anything new and 2-3 weeks to reorder current designs.
- Triggers are setup in Sendoso to remind our account admins when balances and swag inventory is low. No need to ping anyone if you see inventory is low.
- Reordering of inventory for internal swag requests is done by corporate team. See section above on swag providers we use for items not produced by Sendoso.

### Suggesting new items or designs

- You can suggest new designs in the swag Slack channel or more formally in an issue in the [swag project](https://gitlab.com/gitlab-com/swag_suggestions).

- - -

## Social Marketing and Social Media

Please consult the [Social Marketing Handbook](/handbook/marketing/corporate-marketing/social-marketing/).

## All-Remote Marketing

Please consult the [All-Remote Marketing Handbook](/handbook/marketing/corporate-marketing/all-remote/).

## Corporate Communications and PR (Public Relations)

### Mission Statement

The mission of GitLab’s Corporate Communications team is to amplify GitLab's product, people and partner integrations in the media. This team is responsible for global PR (public relations).

### Our audience

The audience we aim to reach is external press/media. This includes business, lifestyle, workplace, finance, and beyond, using mediums such as print, digital, video, events, podcasts, etc.

### GitLab Master Messaging Document

GitLab's corporate communications team is the [DRI](/handbook/people-group/directly-responsible-individuals/) (directly responsible individual) for the GitLab Master Messaging Document. If this document is needed, please request access in the `#external-comms` Slack channel.

### Objectives and goals

As detailed in GitLab’s public [CMO OKRs](/company/okrs/), GitLab’s corporate communications team seeks to elevate the profile of GitLab in the media and investor circles, positioning it as a pioneer of remote work, increasing share of voice against competitors, and pulling through key messages in feature articles.

- Leverage events to generate media interest in GitLab's people and products
- Form and foster relationships with key reporters and publications
- Position GitLab executives and subject matter experts as thought leaders in their areas of expertise
- Increase GitLab's presence in media awards and accolades
- Increase GitLab's contributed content
- Work with social media team to cross-promote and amplify GitLab's media inclusions

### Contacting GitLab's PR team

For external parties, please visit our [Get In Touch page](/press/#get-in-touch).

For GitLab team members, please use the `#external-comms` Slack channel and please follow the [Communication Activation Tree](https://docs.google.com/document/d/1qos3kjM_yIhS8-syey7WfR22SzmnHYFSCZpnFnBv7Rw/edit).

### Requests for Announcements

This process allows us to decide on the best channel to communicate different types of updates and news to our users, customers, and community.

Please follow the instructions below to request a formalized announcement around any of the following:

- A new product feature and capabilities
- A partner integration
- A significant milestone achieved
- A new initiative
- A customer case study
- Inclusion in an analyst report
- A breaking change
- A deprecation
- A change in policy or pricing
- A product promotion (launching or ending)
- Something else? If you're not sure if your case applies, please follow the directions below anyway, so the team can assess how best to proceed.

Please submit a request via an `announcement` [issue template in the Corporate Marketing project](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=announcement) before opening an issue for a blog post, for example. In the issue template, you will be able to provide additional information on the proposed announcement. As a general guide, below the team has outlined three levels for announcements based on the type of announcements and suggested communications activities associated with each tier. The PR team will assess your request in the issue and determine how to proceed. If you are requesting a joint announcement and you are not part of the [Partner Marketing team](/handbook/marketing/product-marketing/partner-marketing/), please ensure you ping them on your issue.

- **Level 1** - A level 1 announcement will be announced via a press release and amplified with social media and an optional blog post. The execution of a blog post will be determined by the blog editorial team on a case by case basis. If the editorial team agrees to have a blog, then the social amplification will be the blog link as it includes assets that are helpful in the link cards across social channels. If there isn't an associated blog post, the social amplification can be for the press release link or relevant news coverage of the announcement. (In this case, the DRI needs to ensure there is an associated image to use with the release link or would make the decision of which news outlet link to select for social amplification.) Example announcements and news include but are not limited to: major GitLab company news around funding, earnings, executive new hires, analyst firm industry awards, acquisitions/mergers, Commit announcements, major joint partner news (ex. a partner such as AWS or Google) and major customer announcement (ex. enterprise or government agencies).
- **Level 2** - A level 2 announcement will be announced via a blog post and amplified with social media. The DRI/SME of the announcement will be responsible for working with the blog editorial team on creating the content and MR for the blog post (please see [the blog handbook](/handbook/marketing/blog/index.html#process-for-time-sensitive-posts) for more on this process). Example announcements and news include but are not limited to: partner integrations, new feature/capability highlights from the monthly release cycles (ex. Windows Shared Runners), customer case study announcement (not household names).
- **Level 3** - A level 3 announcement will be announced and promoted via GitLab’s social media channels. Example announcements and news include but are not limited to: awards from media publications (ex. DEVIES), speaking opps that GitLab employees are participating in (drive attendees/awareness) and ecosystem partner integrations.
- **Other** - In some cases, the following communications channels may be more appropriate:
    - A targeted email to affected users
    - Including an item in an upcoming release post (where the announcement is specifically tied to a release, does not require communication in advance of the release, and is not a sensitive topic)
    - A public issue (see [below](#using-public-issues-to-communicate-with-users))

### Press Releases

GitLab's corporate communications team is the [DRI](/handbook/people-group/directly-responsible-individuals/) (directly responsible individual) for writing all press releases that are issued by the company and routing through the appropriate approval process. The team has developed an [issue template to help make the press release development and approval process](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=press-release-template) more streamlined and consistent.  If you have any questions on the press release process or how to make an announcement request, please reach out via the `#external-comms` Slack channel or submit an `announcement` [issue template in the Corporate Marketing project](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/new?issuable_template=announcement) (see Requests for Announcements section above).
#### Best Practices for an Announcement and Understanding Media Embargoes

GitLab team members will find [embargo and announcement guidelines in a confidential issue](https://gitlab.com/gitlab-com/marketing/corporate_marketing/corporate-marketing/-/issues/3348) (_must be logged in to access_).

This answers the following questions.

1. What is an embargo?
1. Why do we set embargoes?
1. Why don’t we talk about embargoed news prior to the announcement?
1. Who do we share embargoed news with?
1. Who is it okay to discuss this news with?
1. When can I talk about news freely with anyone?

### Using public issues to communicate with users

In some cases it may be more appropriate and [efficient](/handbook/values/#boring-solutions) to communicate with users in a public issue. Below are some examples of the types of communications that may suit an issue as opposed to a blog post, press release, or email, for example:

- Soliciting feedback (e.g. gathering community input on a proposal)
- Explaining upcoming or ongoing changes to GitLab (**not** breaking changes, changes which require users to take action, or otherwise sensitive)
- Sharing updates on a live, ongoing incident (this would be owned by the [Communications Manager on Call](/handbook/engineering/infrastructure/incident-management/#communications-manager-on-call-cmoc-responsibilities))
- See [below](#creating-your-communication-issue) for some examples

Using a public issue has a few advantages:

- In cases where you are seeking feedback or input from the community, your issue can serve as the single source of truth for communication on the subject, rather than spreading communication across a blog post and another page.
- You can easily add related epics and issues so that users can browse all the relevant information and contribute to the discussion. This also keeps the conversation all on GitLab, rather than spreading it across different channels.
- There is one fewer step/link to click on for community members to share their feedback.
- When seeking feedback, keeping things in an issue reinforces that a final decision has not yet been made. A blog post can give the impression of being a formal announcement rather than a proposal, which can have a negative impact on brand sentiment.
- You can get your message out there more quickly, because for most team members creating an issue is more familiar than writing and formatting a blog post. There's also no need to coordinate with the Editorial teams. However, please follow the guidelines in the [PR review and media guidelines](#public-gitlab-issues) section for review from the Corp Comms team.

#### Creating your communication issue

Below are some examples of using an issue to communicate something with our audience. Feel free to use these as a template for your issue. See below [PR review and media guidelines section](#public-gitlab-issues) for more details on the review process.

- [Feedback for ending support for Internet Explorer 11](https://gitlab.com/gitlab-org/gitlab/issues/197987)
- [Recent changes in GitLab routing](https://gitlab.com/gitlab-org/gitlab/-/issues/214217)
- [Color updates in GitLab to establish an accessible baseline](https://gitlab.com/gitlab-org/gitlab/-/issues/212881)

At a minimum, your issue should:

- **Be created in the most relevant GitLab project.** This would likely be the project where most of the discussion or work on your initiative is being done.
- **Have the `user communication` label applied.**
- **Include context for your message.** What background information might someone need to know to understand what you are communicating or asking? What relevant issues or epics can you add to help people understand?
- **Use subheadings for structure.** This makes your issue easy for readers to skim and pick out the most relevant information to them.
- **Include any key dates.** Be sure to call out if there is a deadline for submitting feedback.

#### Promoting your public issue

We can spread the word about a public issue in the same way that we would promote a blog post:

- You can [request promotion of your item on GitLab's social channels](/handbook/marketing/corporate-marketing/social-marketing/#social-medias-place-in-an-integrated-marketing-and-communications-strategy).
- You can request that your item be included in an upcoming newsletter by leaving a comment on the appropriate [newsletter issue](https://gitlab.com/gitlab-com/marketing/digital-marketing-programs/issues?label_name%5B%5D=Newsletter).
- Ask in #marketing on Slack if you would like to promote in some other way.

We can promote other items this way as well: for example surveys, landing pages, or handbook pages.
### PR review and media guidelines

Speaking on behalf of GitLab via a public channel such as a media interview (in-person or via phone), a podcast, a public issue on GitLab, a forum, a conference/event (live or virtual), a blog or an external platform is a significant responsibility. If you are unsure whether or not you should accept a speaking opportunity, create a public issue to gather feedback/communicate a message, or provide comment representing GitLab to a member of the media or influencer, please see below for guidance.

#### Speaking opportunities

If you are asked to speak on behalf of GitLab, consider reaching out to the PR and Technical Evangelist teams to ensure that the opportunity aligns with GitLab objectives. Inquiries should be initiated in the `#external-comms` Slack channel.

#### Media mentions and interviews

If you are asked to be quoted or to provide commentary on any matter as a spokesperson of GitLab, please provide detail of the opportunity to the PR team in the `#external-comms` Slack channel.

In the event that a media member, editor, or publisher offers a draft or preview of an article where you are quoted, please allow the PR team to review by posting in the `#external-comms` Slack channel. The PR team will ensure that the appropriate GitLab team member(s) review and approve in a timely manner.

#### Public GitLab Issues

If you would like to [use a GitLab public issue to communicate an update](#using-public-issues-to-communicate-with-users) to customers/users or gather feedback from customers/users, please complete the `announcement` [issue template](/handbook/marketing/corporate-marketing/#requests-for-announcements) with the details of the specific request and draft of the issue announcement copy. The PR team will review the request details and issue copy, as well as recommend other relevant teams (product, product marketing, legal, etc) to loop in for review before posting.

#### Social media

Please consult the [Social Marketing Handbook](/handbook/marketing/corporate-marketing/social-marketing/). If you are contacted on a social media platform and asked to share/retweet or provide commentary as a spokesperson of GitLab, feel welcome to provide detail of the opportunity to the social team in the `#social-media` Slack channel.

#### Writing about GitLab on your personal blog or for external platforms

You are welcome to write about your experience as a GitLab team member on your personal blog or for other publications and you do not need permission to do so. If you would like someone to check your draft before submitting, you can share it with the PR team who will be happy to review. Please post it in the `#external-comms` Slack channel with a short summary of what your blog post is about.

- - -

Return to the main [GitLab Marketing Handbook](/handbook/marketing/).
