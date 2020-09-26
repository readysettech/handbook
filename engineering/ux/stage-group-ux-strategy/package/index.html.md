---
layout: markdown_page
title: "UX Vision: Package"
---

## Overview
Many projects depend on a growing number of packages that must be fetched from external sources with each build. This slows down build times and introduces availability issues into the supply chain. In addition, many of these external sources come from unknown and unverified providers, introducing potential security vulnerabilities. For organizations, this presents a critical problem. In order to address this need, we're focused on:

* Providing a seamless experience geared towards storing and accessing packages and images for safer more reliable builds
* Building tools around security policies and vulnerability remediation all while limiting exposure to known vulnerabilities
* Establishing a transparent, performant supply chain to improve collaboration and drive conversational development

### Our customer
The customer is anyone that is using GitLab to build, test and deploy software and is or would like to leverage a variety of package and/or image registries manage their dependencies. This sort of customer can be in any size or specific industry. A different customer is a large organization that utilizes several programming languages across teams and they would like to centralize all of their external dependencies in one location, GitLab. 

### Our user
We have different user types we consider in our experience design effort. Even when a user has the same title, their responsibilities may vary by organization size, department, org structure, and role. Here are some of the people we are serving:

* [Systems administrators](/handbook/marketing/product-marketing/roles-personas/#sidney-systems-administrator)
* [Software developers](/handbook/marketing/product-marketing/roles-personas/#sasha-software-developer)
* [Devops engineers](/handbook/marketing/product-marketing/roles-personas/#devon-devops-engineer)
* [Security analysts](/handbook/marketing/product-marketing/roles-personas/#sam-security-analyst) (future)

### Our UX Scorecards 
##### Primary Jobs to be done

**Enable and configure the container registry:**
When I first create a new project in GitLab, I want to be able to enable and configure the container registry, package registries and the dependency proxy, so that I can ensure my organisation can use GitLab in a scalable fashion.
* Current benchmark score: coming soon
* Current baseline: coming soon
* Recommendations: coming soon

**Optimize registry storage:**
As part of regular project maintenance, I want the ability to optimize storage by expiring old images and artefacts and running garbage collection, so that I can optimize storage usage.
* Current benchmark score: coming soon
* Current baseline: coming soon
* Recommendations: coming soon

**Use Ci pipelines to run and build docker images:**
When I commit code, I want my CI pipeline(s) to run and build a docker image, so that I can ensure that my integrations tests pass and that my team/org can deliver high-quality code.
* Current benchmark score: coming soon
* Current baseline: coming soon
* Recommendations: coming soon

**Lookup specific image/tag/package:**
After I create a tag of a new image, I want to be able to find data related to that specific image, so that I can confirm it was built as expected and update my code as necessary.
* Current benchmark score: coming soon
* Current baseline: coming soon
* Recommendations: coming soon

**Deleting a specific image/tag/package:**
As part of keeping my project organized, I need the ability to delete images/tags/packages that I am no longer using, so that I can maintain a well-groomed project.
* Current benchmark score: coming soon
* Current baseline: coming soon
* Recommendations: coming soon


### Our team
Our team continues to grow. We currently have 3 members that contribute to Package UX efforts:

* [Nadia Udalova](https://gitlab.com/nudalova) - UX Manager 
* [Iain Camacho](https://gitlab.com/icamacho) - Sr. Product Designer, Package
* [Lorie Whitaker](https://gitlab.com/loriewhitaker) - Sr. UX Researcher

#### Our team meetings
Following in GitLab's tradition of async over sync, a majority of our communication is done through issues and merge requests. We do have a few regular synchronous meetings: 

* Product Management, Research, and Design meet monthly to coordinate user research efforts
* Product Management and Design meet weekly to coordinate design efforts for Package
* Front-end and Design meet weekly to coordinate UI improvement efforts

<!--
### Our strategy
The Package UX team uses a human-centered data-driven approach to uncover customers core needs, understand our users’ workflows, and define how we can make our users experience better. Our strategy depends on quantitative and qualitative data from our users which we gather in a variety of ways:

* [UX Scorecards and recommendations](/handbook/engineering/ux/experience-baseline-recommendations/)
* [Problem Validation](/handbook/product-development-flow/#validation-phase-2-problem-validation) and [Solution Validation](/handbook/product-development-flow/#validation-phase-3-solution-validation) research efforts, coordinated with Product Management
* Robust usage-data gathered directly from the product (in progress)
* Classic user interviews, surveys, and moderated testing

Additionally, we value the following:
* Testing features with usefulness and usability studies
* Collaborating with stakeholders on proof of concepts and discovery
* Prioritizing issues based on active user needs
* Small improvements with big impact to the user

The source of truth lives with shipped features, therefore we:
* Make data-driven decisions quickly and thoughtfully 
* Optimize to deliver our solutions as soon as possible
* Learn, iterate, test, and repeat

-->