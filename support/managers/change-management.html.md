---
layout: handbook-page-toc
title: Change Management in GitLab Support
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Decision Making and Change Management in the GitLab Support Leadership Team
The GitLab Support Team may very well be unique among the many teams within the
company in that its multiple sub-teams each have the same charter. Making
decisions and managing change within this structure come with equally unique
challenges not faced by the other teams. Specifically, managers must determine
the appropriate scope - whether to act individually or in coordination with the
other managers - when they want to make a decision or introduce a process
change. And the worldwide support management team must agree that the scoping
is correct. We define here our most current processes for determining scope,
gathering data and feedback, choosing a path forward, rolling out a change,
managing adoption, and reviewing results for future improvements.

## Determining the Scope
One of the most important considerations when looking to make a change is what
the scope of the change will be.

### Local Change or Global Change?
When thinking about whether a change should be local or global, you might be
tempted to focus on the size of the change (number of lines of code changed,
number of lines of text in a doc that changed, etc.). But that’s actually a
different type of scope that isn’t relevant to this discussion.

Instead, begin with the idea that for the sake of consistency and simplicity,
you should lean toward making your change globally unless it doesn't even make
sense for, or apply to, other regions. If you're considering making the change
locally, be sure that you can answer "no" to **all** of these questions about
potential impacts of making a local change:

1. Will it create a meaningful inconsistency with the rest of the global team?
   Examples:
   1. Your local work products become incompatible with those of the other teams
   1. Terminologies or workflows diverge between your local team and the others,
      inhibiting collaboration
   1. Other teams can’t work in concert with yours because they don’t have
      access to new tools and resources yours is using
1. Will customers notice the local change?
   If so:
   1. Will customers be inconvenienced or even just annoyed by having to work
      differently in some way with your team than with the other teams?
   1. Will customers’ expectations of “normal” service continue to be met?
   1. Will customers like your change enough to be dissatisfied when other teams
      /regions don’t do the same thing?
1. Will it create different job descriptions or performance measures between
   your team and the other regions?

## Communicating a Change Proposal
Whether you’re making a local change, based on the decision criteria above, or
proposing a global one, it’s important to communicate your plans with the rest
of the Support Leadership Team.

### Creating an Issue
The first step toward making a change is to
[create an issue](https://gitlab.com/gitlab-com/support/support-team-meta/-/issues/new?issuable_template=Requested%20Change)
via the
[support-team-meta project](https://gitlab.com/gitlab-com/support/support-team-meta).
Using the linked template (Request Change), it will ensure you supply the
required information (DRI, problem statement, ways to measure success, etc.),
helping to speed the process along.

### Communicating a Local Change
Even for a change that you’ve determined will be local, inform the leadership
team. Put it as an “inform” item in the agenda for the next
[leadership sync meeting](/handbook/support/managers/#organization-of-support-leadership-meetings).
Why?
* Someone else might have a suggestion for you
* Someone else might be interested in what you’re doing
* It aligns well with our Transparency value

### Communicating a Global Change Proposal
Once you’ve determined that your intended change must be global, engage the
leadership team in a conversation through your issue and through a full agenda
topic in the [leadership sync meeting](/handbook/support/managers/#organization-of-support-leadership-meetings):
* Describe the problem you’re working to solve
* Let the team know if you are the DRI, or are seeking a DRI
* Let the team know whether you're proposing a solution based on compelling
  existing data or you're planning to conduct one or more tests (trials) to
  determine which solution to propose.
  * If you will be testing, then it's suggested that you:
    * Present potential solutions and discuss which of them will be tried
    * Discuss any likely impacts of the tests
    * Gain general agreement that you can proceed with your tests
    * If the tests will be large and long running, consider opening an issue for
      each test and link them all to your issue
  * Otherwise, it's suggested that you:
    * present data both demonstrating the need for the change and supporting the
      solution you've chosen
    * propose your solution via a Merge Request (linked to your issue) and
      invite feedback with a reasonable deadline
* Describe how you plan to measure the success of the change (not just the
  tests)

### Constructing a Valuable Test Plan
We make data driven decisions whenever possible. If your proposed change doesn't
have any supporting data, you'll run one or more localized trials. Be frugal if
there is a cost and always be sensitive to disrupting existing workflows:
  * If you are not confident or comfortable designing a test, work with other
    managers to flesh out ideas.
  * Keep in mind that there's a difference between the scope (local or global)
    of a change and the scope of a test. A global change most likely will
    **not** require a global test.
  * Run the tests just long enough to get the data you need
  * Involve only as many people, teams and regions as you need to make the tests
    legitimate
  * If a test in the production environment would be problematic, look for a way
    to run it in a sandbox instead
  * If running more than one trial:
    *  try to run them in parallel with each other to save time
    *  limit your testing to the two or three most likely potential solutions

