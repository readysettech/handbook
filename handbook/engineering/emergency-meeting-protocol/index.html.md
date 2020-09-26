---
layout: handbook-page-toc
title: "Emergency Meeting Protocol"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## General information

The guidelines below should be considered in case of emergency meetings.

There are many urgent and important situations that may require an emergency
meeting, including severe customer-impacting issues, security breaches, or any
other time-sensitive situation that has a clear and serious business impact. In
these situations, it is most [efficient](/handbook/values/#efficiency) to call
an emergency meeting to resolve the issue as quickly as possible.

### Video Call

Calls should be organized as soon as it becomes clear that there is a business
impact. Calls should also be considered when there is more than one parallel
discussion in chat. While we hope to resolve most of our incidents in our
\#incident-management room in Slack, there will be situations where a call is
necessary.

Having a call with more than two people will streamline the communication and
make it easier to follow the discussion.

Anyone is welcome to join the call. People that have expertise related to the
emergency meeting are encouraged to join.
Everyone is welcome to contribute to the discussion, however the team members
with direct involvement in the incident should be the ones leading the emergency
resolution.

That does not mean that  people outside of the team cannot contribute or even step in.
In an emergency situation it is easy to develop tunnel vision.
This means that even persons with no subject knowledge can help by pointing to
behaviours that do not lead towards resolution.

### Document

Every emergency meeting has to have a written trace.
When the call is started, open up a new Google Doc.
If a new person joins the call or if it is necessary to share this information
further, it is much more efficient to have all the information in one place.

This document has to be open to everyone with the link by default.

If the document needs to be made private, the first header in the document needs
to describe why this is the case.

Transparency has a practical side; anyone who joins the call does not need to
request access to the document. If the incident has to be publicized, the document will introduce the topic to people outside of the company the same way as it did to the people
inside of the company. Remember that *Transparency* is our core value.

To repeat, the document is public by default and the case needs to be made for
making the document private. Making the case will help everyone think about the
possible impact even before starting the resolution.

### Call etiquette and document structure

Everyone in the call is responsible for adding items to the document,
but one person should be making sure that the things are being documented.

If no one volunteers to take this role, select the person with highest rank in
the call. The highest ranking person can delegate this role if they can
contribute more effectively to resolving the situation at hand.

One person cannot physically document everything that is happening so everyone
needs to contribute to organizing the situation. By having one person focused on
guiding the documenting task, everyone involved is kept on track towards resolving the problem.

All written communication needs to be directed to the document. Any discussion in Slack and in calls chat should not be discouraged. The document has to be the single source of truth.

Reason for this is: when the call ends the call logs are gone.
When the call ends, work continues and all Slack discussions will become part of the backlog.
One document will always remain the witness of the incident.

The document should have the impact section.  

Evaluating the impact is important because that gets to drive the further actions.
By discussing the impact first, everyone involved gets to contribute to better understanding the problem.
The urgency is not the same when 30 people are affected or when 3 Million people are affected.
This also drives the decisions that can be made, the less of an impact, the more safe approach can be taken.

The document should contain the summary header.
This header should contain the most up-to-date situation, including the agreed facts.
Summary should be kept short and refer to other parts of the document for further details.
Any new person joining the call or enquiring about the progress will get up to
speed quickly without needing to interrupt any ongoing conversations.

The document should have a timeline of the events.

Having a timeline written while the incident is being resolved will make it easier to understand what is the general trend of the situation, e.g. the changes being made are making the situation better, so this should be continued. Having this section will mean that there is no need for writing a new root cause analysis document.

The document should have an Async questions section.

This section serves as a reminder to anyone involved in the call when there is another conversation running. Ideas pop up randomly but the idea might not have the direct relation
to the current conversation. By writing it down in this section, it is easy to
get back to it when the time is more suitable.

Finally, when the issue is resolved, it is important to write down questions
that will require a retrospective. Retrospective section should be updated
both while the work is ongoing, but also at the end of the call as some questions
might be answered during the course of the call. By writing the questions while
the issue is “hot”, you can capture the knowledge while the task is ongoing.
It will be much more challenging to remember the questions after the call is disbanded.

## Example document

Below you can find the document example snippet:
```
Title: User projects not accessible

Meeting lead: John Doe

Impact

2018-01-01 01:00 UTC: Estimating that around 5 Million users can’t access their projects. This impacts both new and old users so the impact is rising.

Summary

2018-01-01 00:30 UTC User reported that they can’t access their project.
2018-01-01 00:45 UTC Confirmed that our projects are not accessible as well.
2018-01-01 00:55 UTC Run the script that queries all projects on the environment, none of them are accessible. Updated the Impact section.
2018-01-01 01:50 Projects are back


Timeline

2018-01-01 00:30 UTC User reported that they can’t access their project.
2018-01-01 00:40 UTC Confirmed that our projects are not accessible as well.
2018-01-01 00:55 UTC Ran script:
find -all projects
It returned nil
2018-01-01 01:05 UTC The joker of the group asked if we ‘tried turning it on and off again’
2018-01-01 01:06 UTC Still no one is amused
2018-01-01 01:45 UTC Someone tried turning it on and off, things started working
2018-01-01 01:47 UTC Collective facepalm
2018-01-01 01:50 Projects are reachable again.
Async questions

Emily: Where are projects stored?
John: How did we not see this in our monitoring

Notes

Here we can put everything that is no longer relevant to the discussion.
Retrospective questions

How did we not see this in monitoring?
```
