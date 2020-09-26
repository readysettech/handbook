---
layout: handbook-page-toc
title: "Dovetail Tips & Tricks"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

### Getting started with Dovetail

1. Learn the basics of Dovetail in under 10 minutes by watching this [video](https://dovetailapp.com/help/videos/getting-started-with-dovetail/).

1. Read about Dovetail’s [video highlights and transcription feature](https://dovetailapp.com/features/video-audio-transcription-for-research/).

1. Read the UX Research team’s [guide for documenting insights](/handbook/engineering/ux/dovetail/#the-ux-research-teams-guide-to-documenting-insights-in-dovetail) in Dovetail.

1. Check out [Dovetail’s help center](https://dovetailapp.com/help/) for commonly asked questions.

1. Check out this [project](https://dovetailapp.com/projects/7fa7fb97-1c9e-41ab-ad3a-55a32987b048/readme) (internal access only) for a great example of how to organize your data, use tags, and turn highlights into insights.

### The UX Research team's guide to documenting insights in Dovetail

#### Creating a project
Go to `Projects`. Locate your stage group. Click `New project` and select the `Problem or Solution Validation Research` template. You will be redirected to the Project’s ReadMe file.

####  Updating the ReadMe file
In the ReadMe file, update the name of your project from `Problem or Solution Validation Research` to something more recognisable. Ensure you add a link to your research request/brief. There is no need to add further information about your project to the ReadMe file unless you wish to do so.

#### Importing raw data into Dovetail
Click `Data` in the left-hand menu. Add your raw data to the project, such as notes/observations taken during research sessions, video recordings, support tickets from customers, user sentiments from social media, and so on. Organize and structure your raw data in a way that resonates with you.

This video demonstrates how to use the import feature and how to structure your data around research questions / tasks:
<figure class="video_container">
<iframe src="https://www.youtube.com/embed/dod5EUYYgDk" frameborder="0" allowfullscreen="true" width="640" height="360"> </iframe>
</figure>

#### Highlight and Tag content
Once you have imported all your raw data, you are ready to start highlighting and tagging content. Think of a highlight as anything interesting that you heard or observed during a research session. For example: a user pain point or motivation. 

A bit like [affinity mapping](https://en.wikipedia.org/wiki/Affinity_diagram), tags in Dovetail help you identify and keep track of patterns that emerge across your research data. A single highlight can have one or many tags associated with it.

By default, tags in Dovetail live in a specific project. You can create as many tags as you like and use them for a variety of tracking purposes. 

We encourage you to tag highlights with:

1. The feature/area of GitLab to which the highlight relates (for example: ‘Merge Requests’, ‘Navigation’, etc)

1. The persona (‘Sasha: Software Developer’, ‘Sam: Security Analyst’, etc) who made the comment if possible. 

This will make searching for and locating highlights in the future much easier.

If you find yourself re-creating the same tag over and over again for multiple projects, please let your UX Researcher know. The UX Research team is in the process of creating a range of global tags that you can apply to your highlights. 

The UX Research team is responsible for creating, maintaining and auditing global tags (also known as [extensions](https://dovetailapp.com/help/organize-your-data/migrate-to-extension/)). 

#### Charts & Insights
Use `Charts` to quickly get an overview of how frequently themes are mentioned across your research data. Themes that frequently reoccur in your data warrant an insight. `Insights` help you to summarise your research findings. Select multiple highlights in order to create an insight. 

Sometimes during research studies you’ll note something of interest but perhaps don’t have enough data yet to decide whether what you observed or heard was an [edge case](https://en.wikipedia.org/wiki/Edge_case) or something which may be impacting other users. 

A general rule of thumb: If you’re uncertain about whether something should be turned into an insight and/or only have 1-2 highlights that support the theme. Your observation should remain as a ‘highlight’ rather than be converted into an ‘insight’.

Highlights can still be searched, tracked and revisited again in the future when you’ve gathered more research data. 

#### Suggestions for managing your content
This video demonstrates how to take structured notes in Dovetail similarly to a google spreadsheet with multiple notetakers.
   <figure class="video_container">
   <iframe src="https://www.youtube.com/embed/K7WuC0QCOyM" frameborder="0" allowfullscreen="true" width="640" height="360"></iframe>
   </figure>

### F.A.Qs

#### I'm a Product Manager and I’d like to use Dovetail to keep track of the calls I have with customers. Is that okay?

Yes! When creating a new project, please select the `Customer calls` template. In the ReadMe file, update the name of your project from `Customer calls` to something more recognisable. Continue to follow the steps outlined under [The UX Research team's guide to documenting insights in Dovetail](/handbook/engineering/ux/dovetail/#the-ux-research-teams-guide-to-documenting-insights-in-dovetail) starting with [Importing raw data into Dovetail](/handbook/engineering/ux/dovetail/index.html#importing-raw-data-into-dovetail). 

Note: If you're only speaking to one customer and haven't heard evidence from other customers that they are experiencing the same problem or want the same feature improvement, it's highly likely that your finding should remain as a `highlight` rather than be converted into an `insight`. Feel free to reach out to your UX Researcher if you're not sure.

#### I'd like an idea of how to structure my data in Dovetail, do you have any examples?

Yes, scroll to the bottom of the Project list and under `Sample data`, you will see some sample projects created by the folks at Dovetail.

#### I'd like to create a private project to synthesize sensitive information

While our Dovetail projects are currently only accessible by GitLab employees, sometimes you have a project you feel should be only seen by you or a few others. You do this by [controlling who has access](https://dovetailapp.com/blog/2018/access-controls/) to your project. 

##### Guidelines for what constitutes sensitive information

Please refer to our [Code of Business Conduct: Material Nonpublic Information / Inside Information](/handbook/people-group/code-of-conduct/#material-nonpublic-information--inside-information) handbook page.

### Feedback and questions

Please post feedback and questions in the #ux_research Slack channel.

If you find out something useful which you feel will benefit others, please submit an MR to this page and assign it to `@sarahj`.
