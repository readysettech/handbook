---
layout: handbook-page-toc
title: Tools and Resources
---
## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

[**SA Practices**](/handbook/customer-success/solutions-architects/sa-practices) - [**Sales Plays**](/handbook/customer-success/solutions-architects/sales-plays) - [**Tools and Resources**](/handbook/customer-success/solutions-architects/tools-and-resources) - [**Career Development**](/handbook/customer-success/solutions-architects/career-development) - [**Demonstration**](/handbook/customer-success/solutions-architects/demonstrations) - [**Processes**](/handbook/customer-success/solutions-architects/processes)

# Tools and Resources
{:.no_toc}

## Product Releases

- check [Product Release Updates](/handbook/marketing/product-marketing/release-updates/) for enablement on new features in recent releases
- [Upcoming Releases](https://about.gitlab.com/upcoming-releases/)
- [Previous Releases](https://gitlab.com/gitlab-org/gitlab/-/releases)
- [Releases Blog](https://about.gitlab.com/releases/categories/releases/)
- Compare Two Releases with the [What is New Since? Release Feature Overview Tool](https://gitlab-cs-tools.gitlab.io/what-is-new-since/?)

## Customer Facing Meeting Tools

Solutions Architects frequently interact with customers for demos, presentations or Q&A. These calls should enable the customer to clearly experience the value of GitLab without distraction or interruption. The below list of tools was compiled by the GitLab SA team as commonly used solutions. Note, this list does not represent a requirement to use any of these products or an endorsement for these products.

- [Muzzle](https://muzzleapp.com/) to mute all notifications prior to beginning a call
- [Tab Resize Chrome plugin](https://chrome.google.com/webstore/detail/tab-resize-split-screen-l/bkpenclhmiealbebdopglffmfdiilejc?hl=en-US) to break tabs into split-screen viewing
- [Screenbrush](http://screenbrush.imagestudiopro.com/) to draw on the screen
- [Toby](http://www.gettoby.com/) or [Tabs Outliner](https://chrome.google.com/webstore/detail/tabs-outliner/eggkanocgddhmamlbiijnphhppkpkmkl) to launch many preset tabs at once
- [Station](https://getstation.com/) to group pages by application in a smart dock
- [MouseBeam](https://geeky.gent/tag/mousebeam/) enables the mouse cursor to use multiple screens like a circle
- [Rectangle](https://rectangleapp.com/) to quickly move and resize windows in macOS using keyboard shortcuts or snap areas
- [Dark Reader](https://darkreader.org/) enables browser dark mode to better fit room lighting
- [Postman](https://www.getpostman.com/) for API interaction
- [Atom.io](https://atom.io/) lightweight IDE text editor
    - [git-plus](https://atom.io/packages/git-plus) Package for atom to make commits and other git actions without the terminal

Related macOS tips

- [Switch between full screen applications](https://www.intego.com/mac-security-blog/how-to-enter-and-exit-full-screen-mode-in-macos/) using the trackpad, Command keys or other options
- Use the [Zoom Accessibility Features](https://www.imore.com/how-use-zoom-mac) to zoom in on targeted screen locations
- [Work in multiple spaces on a single monitor](https://support.apple.com/en-gb/guide/mac-help/mh14112/mac) to keep multiple app windows or browser tabs open in fullscreen mode
    - Enables switching between windows or tabs with trackpad gestures, keeping display screen clean and uncluttered

## POV Resources

The [POV Guidelines document](https://about.gitlab.com/handbook/sales/POV/) describes how to kick off a POV.  The Solutions Architect (SA) is the key actor in the process.  A POV is part product evaluation, part trust building exercise. This is a key moment in the sales cycle to establish deep conversations with the customer, and become the trusted advisor.  This is done by bringing your experience to the table.  In addition, it is very helpful to have some set exemplar projects that can be shared with customers to show different areas of the product.  List below is an evolving list of projects that have come in handy during POVs and may be a great starting point to offer customers.

### End-to-end Proof projects

These projects have a very simple set of code that provides the ability to demonstrate the `happy-path` for a POV.  While these are more in the Hello World category of projects, they tend to have simple mechanizations to exercise different parts of GitLab.  SAs have used these in the past as a way to assess the installation of self-managed environments.

- [Insecure Tanuki Tech Project](https://gitlab-core.us.gitlabdemo.cloud/demosys-users/skamani/insecure-tanuki) was developed internally to show the usage of Auto DevOps. It is predominantly focused on Secure features, but serves well to present all stages.

### Demonstrative of specific stages

These projects are demonstrative of specific stages.  They are generally built on existing code OSS bases which the customer may be familiar with, are easy to understand, and have good literature to refer to.

#### Secure Stage Projects

- [Nodejs Juice Shop](https://github.com/bkimminich/juice-shop) repository comes with a .gitlab-ci.yml file to get started with SAST and Dependency Scanning.  Incorporate others incrementally as needed.
- [OWASP WebGoat.NET](https://gitlab-core.us.gitlabdemo.cloud/tanuki-group/dot-net-webgoat) repository can be enabled with SAST, License Management and Secrets Scanning very quickly using the packaged templates.  This validates our positioning in .NET application development (both Framework and Core).

## Useful Customer Facing Presentations

No two presentations are the same and we often find ourselves mixing and matching content tailored to our Customer's journey.  From Agile to CI/CD to Kubernetes and beyond, below are several commonly used decks rich in content to pull from.

- [Official Customer Facing Presentations](https://about.gitlab.com/handbook/marketing/product-marketing/#customer-facing-presentations) - Here you will find the [Company Pitch Deck](https://docs.google.com/presentation/d/1dVPaGc-TnbUQ2IR7TV0w0ujCrCXymKP4vLf6_FDTgVg/) with the GitLab narrative, [Customer Value Deck](https://docs.google.com/presentation/d/1SHSmrEs0vE08iqse9ZhEfOQF1UWiAfpWodIE6_fFFLg/) with Value Drivers and Differentiators, and [Security Deck](https://docs.google.com/presentation/d/1WHTyUDOMuSVK9uK7hhSIQ_JbeUbo7k5AW3D6WwBReOg/edit?usp=sharing) with best practices on Shift-Left security.   _These should be the starting point of any tailored deck!_
- [All The Things](https://docs.google.com/presentation/d/1mGMyciRrobnOgazoc20_Q5HiBcP8ydp_JWjzgBj4tRI/) - Not a pitch deck.  Owned by a Solution Architect, this is a holistic, tactical guide to GitLab as a Product constantly updated with screenshots.
- [General Demo](https://docs.google.com/presentation/d/17SoRPxPCswT_FublXCsi3rm3TBnHAYI-/) - Product Walk-through from the lens of a Solution Architect covering Velocity, Visibility, and Security & Compliance.
- [Getting Started](https://docs.google.com/presentation/d/1LJTZ7SC4EWcXJx3ptiA23Cf1i33GJHTE) - Kicking off a POV? This is a fantastic deck to help Customers on their journey to setting up Users, Groups, Pipelines, Auto DevOps, and more!

## RFP Responses
### Best Practices for writing RFx responses

Responding to a Request for _____ (RFx) is part of the standard process within Public Sector. RFx is a general category that includes Request for Information, Request for Proposal, Request for Quote, etc. RFIs are generally less structured than RFPs. While RFQs rarely need technical write ups, occasionally technical input is required, especially if the RFx requests an `or alike` product.

### Evaluating RFI and RFPs for response

Solutions Architects have a big role in responding to RFIs and RFPs where there are considerable number of technical asks.  There is a saying used commonly when responding: `Make sure you answer the mail`. This has two connotations:

1. Evaluate what is asked for and do your best to address it, and
1. Answer the questions directly and provide context

But more importantly, be sure that there is a product fit. If what is asked for in the RFI/RFP is not directly met with GitLab, or seems too much like a different software entirely, then stop and talk to the Strategic Account Leader or Inside Sales Representative. Also identify the strategic impact if the requirements do not seem to match GitLab functionality.  If GitLab fits only a piece of the RFx, collaborate with the Strategic Account Leader and/or Inside Sales Representative to understand who the other players in the response might be.   

### Responding to RFIs

RFIs are generally issued to shape procurement. In some situations, they are just a step in the process as the customer may already have an advising team that may be following protocol. An RFI is generally non-binding unless otherwise specified. Responses to questions in an RFI don't have to be precise. They can have some idealistic statements to lay the groundwork and pivot points to educate the customer on what GitLab offers. It is good to follow the GitLab Value Framework response methodology, as there is no ability to have a dialog. The RFI is about positioning. Provide context around the following factors that can grab the attention of the readers:

- Positioning and value of the product
- Truth about capabilities
- Solution options and flexibility
- How risk is mitigated by the solution

Some RFIs have a length limit, but be sure to verify and be mindful if there is one. Start with a simple overview of what the product does. GitLab Marketing does a great job with text that is vetted. For example, utilize the write-ups for each of the [stages of the DevOps workflow](https://about.gitlab.com/stages-devops-lifecycle/). Do not reinvent the wheel, especially for an RFI. Keep it simple and succinct.

An RFI may ask open-ended questions. This is good for providing detailed solution responses. Keep the language simple and describe the solution GitLab offers. Instead of stating that GitLab does or does not do something, direct the reader to why GitLab doesn't do it, if it is on the roadmap, or how they would implement a workaround.

When responding to an RFI, it's critical to document how the product solves customer problems, but it's also important to include the company behind the product. GitLab's all-remote leadership, its company values, its culture, and its professional services offerings shape the entire customer relationship.

### Including Links to Documentation

In general, for Public Sector responses, adding links to documentation is not a good practice. Essentially, anything that makes a reader have to do extra work is not going to work well. There are also cases in which the reader may not be able to readily access the link provided.

For example, if the question asks for a Roadmap for the next product release, it is a good idea to include a link to our roadmap, but then also explain GitLab's release velocity and consistency so the customer understands the dynamic nature of the GitLab release process. Another instance when links are desirable is when relevant customer use cases may be referenced.

If, however, the customer asks for a descriptive concept like the architecture of GitLab, use that as a way to include as much detail as possible inline, a summary of why the architecture is what it is, including the benefits, and then a link for them to read more. Also, including images and screenshots is highly encouraged where possible.

The customer may ask for a description of the CI process or other complex process. In these cases, it is acceptable to copy as much of the documentation from our documentation as possible, including many details to differentiate GitLab from competitive products. Using CI as an example, include a description of how GitLab CI operates, a description of the yml file, a link to the yml file documentation, and add information regarding unique or differentiating functions that GitLab offers like Auto DevOps, Directed Acyclic Graphs, multi-project pipelines, etc.

### Tips and Tricks in Response Writing

- As much as possible use [active rather than passive voice](https://www.grammarly.com/blog/active-vs-passive-voice/)
- Eliminate pronouns: Example 1, "GitLab CI will do x" rather than "Our CI will do x". Example 2, "The GitLab team will x" rather than "We will x".
- Organization of the response is as important as the content
- Create a strong introduction and summary leveraging existing Marketing information which presents the breadth of the entire GitLab solution
- If specific requirements are expected to be answered by the response, add notations to the requirement number being met within the text of the response: Example, "GitLab's SAST scanner will analyze your source code for known vulnerabilities (Req 1.a.1)"
- Use customer terminology wherever possible
- Include relevant customer use cases whenever possible
## Hands On Workshop
