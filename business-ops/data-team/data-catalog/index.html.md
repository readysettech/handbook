---
layout: handbook-page-toc
title: "Data Catalog"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .toc-list-icons .hidden-md .hidden-lg}

---

## Introduction

This page is the list of GitLab Self-Service Data Subject Areas and Data Definitions (collectively known as "The Data Catalog"). To maintain a Single Source of Truth for Trusted [Self-Service Data](/handbook/business-ops/data-team/direction/self-service/), content is organized by function and maintained within the Data Team handbook. In cases where a Data Subject (such as Product SKU) crosses function boundaries, content will reside alongside the function that owns the source system of record (e.g. Product SKU will reside in Finance because Zuora is the SSOT for SKUs).

### Self-Service Development Workflow

1. Create a merge request to add the Subject Area definition to the the appropriate section of the Data Catalog.
1. Define the Subject Area page as completely as possible with all of its parts based on the [Level 2 Reference](/handbook/business-ops/data-team/direction/reference/).
1. Self-Service Development is considered complete once all key parts are operationalized, a Knowledge Assessment is published, and the Self-Service entry on this page is tagged with the appropriate [operational status](/handbook/business-ops/data-team/data-catalog/#legend).

### Data Definition Development Workflow

1. Create a merge request to add the Data Definition to the appropriate section of the Data Catalog. If a Data Definition is part of an existing Subject Area page, only add a link to it from the Data Catalog Index and do not create a new stand-alone page with the Definition.
1. Define the Data Definition page as completely as possible with all of its parts, including a business summary and links to source systems of record and dashboards.
1. Data Definition is considered complete once all key parts are defined and the entry on this page is tagged with the appropriate [operational status](/handbook/business-ops/data-team/data-catalog/#legend).

## Data Catalog

### Finance

1. 🚧  [WIP Self-Service Data: Finance ARR](/handbook/business-ops/data-team/data-catalog/finance-arr/)

### Product

1. 🚧  [WIP Self-Service Data: Product Geolocation Analysis](/handbook/business-ops/data-team/data-catalog/product-geolocation/)
1. 📊  [Data Definition: Product Stage](/handbook/product/product-categories/#devops-stages)

### Sales

1. 🚧  [WIP Self-Service Data: Customer Segmentation Analysis](/handbook/business-ops/data-team/data-catalog/customer-segmentation/)
1. 🚧  [WIP Self-Service Data: Sales Funnel](/handbook/business-ops/data-team/data-catalog/sales-funnel/)
1. 📊  [Data Definition: Customer](/handbook/sales/#customer)

### Legend

📊 indicates that the solution is operational and is embedded in the handbook.

🚧 indicates that the solution is in a `Work In Progress` and is actively being developed. When using this indicator, an issue should also be linked from this page.

🐔 indicates that the solution is unlikely to be operationalized in the near term.
