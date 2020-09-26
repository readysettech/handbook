---
layout: handbook-page-toc
title: "GitLab Navigation"
---

#### On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

The UX team owns the navigation structures of the GitLab product. Please review this information if you plan to propose changes to GitLab navigation.

## GitLab Navigation

Navigation refers to both how the GitLab application is organized and how that organization is presented to users to enable them to move around the application. Navigation is important, because it
affects the usability and discoverability of our products.

We can think of our navigation as having two main types: **global navigation** (view projects, groups, account and user information) and **contextual navigation**
(access content specific to each page, primarily product features within a project or group). There is more detail on this in our [Pajamas documentation of navigation](https://design.gitlab.com/regions/navigation).

## Who Makes Navigation Changes

Anyone can propose a navigation change by creating an issue, but a product team will have to take some ownership to get the change implemented. Typically this is the product team that owns the feature impacted by the navigation change.
Changes to the global navigation often fall under the [Growth](/handbook/product/product-categories/#growth-section) section, so consider engaging them in your proposed change.

## How to Make Navigation Changes

1. Create your issue, and add as much detail as you can. You can create the issue in the [GitLab.com](https://gitlab.com/gitlab-org/gitlab) project.
1. Label the issue with `UX`, `UI text`, `documentation`. Also add `Category:Navigation` label and mention "@gitlab-org/growth/expansion" so the issue is visible to the Expansion team.
1. Engage your UX partners in product design and research. If the team doesn't have a product designer, reach out to the UX Manager for the stage group.
1. Engage your Technical Writer. Our docs often refer to navigation, so a documentation update is likely required.
1. Follow the [product development workflow](/handbook/product-development-flow/#validation-phase-2-problem-validation) validation process to ensure you are solving a well understood problem and that the proposed change is understandable and non-disruptive to users. Consider doing navigation-specific research.
1. Consider whether you need to communicate the change somehow, or if you will have an interim period in the UI where your nav item will live in more than one place.
1. Kindly update this [navigation map in Mural](https://app.mural.co/t/gitlab2474/m/gitlab2474/1589571490215/261462d0beb3043979374623710d3f2d6cfec1cb) with your navigation change.

[ux-guide]: https://docs.gitlab.com/ee/development/ux_guide/
[ux-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX
[ux-ready-label]: https://gitlab.com/groups/gitlab-org/issues?scope=all&state=opened&utf8=%E2%9C%93&label_name%5B%5D=UX+ready
[gitlab-design-project-readme]: https://gitlab.com/gitlab-org/gitlab-design/blob/master/README.md
[twitter-sheet]: https://docs.google.com/spreadsheets/d/1GDAUNujD1-eRYxAj4FIYbCyy8ltCwwIWqVTd9-gf4wA/edit
[everyone-designer]: https://library.gv.com/everyone-is-a-designer-get-over-it-501cc9a2f434
[pajamas]: https://design.gitlab.com