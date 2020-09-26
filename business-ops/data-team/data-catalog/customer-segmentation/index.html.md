---
layout: handbook-page-toc
title: "Customer Segmentation"
---

## On this page
{:.no_toc}

- TOC
{:toc}

---

## Customer Segmentation Analysis

Customer segmentation is the process of dividing our customers into groups based on common characteristics so that we can understand who our customers are and provide them with a great customer experience. There are many characteristics that identify our customers including industry, product category, sales segment, delivery, and territory to name a few. The Customer Segmentation Analysis page will provide the information and tools that GitLab team members can use to explore customer data and develop customer insights.

This data solution delivers three [Self-Service Data](/handbook/business-ops/data-team/direction/self-service/) capabilities:

1. Dashboard Viewer - a new SiSense dashboard to visualize ARR and customer count by industry, product category, sales segment, delivery, account owner team, and territory  (Self-Service Dashboard)
1. Dashboard Developer - a new SiSense data model containing the complete dimensional model components to build new dashboards and link existing dashboards to customer segmentation data.
1. SQL Developer - an Enterprise Dimensional Model subject area

From a Data Platform perspective, the solution delivers:

1. An extension to the Enterprise Dimensional Model for Customer Segmentation Analysis
1. Testing and data validation extensions to the Data Pipeline Health dashboard
1. ERDs, dbt models, and related platform components

### Knowledge Assessment & Certification

The Self-Service Data program provides individual Certificates for each subject-oriented Dashboard Developer or SQL Developer Knowledge Assessment successfully completed (score of a 100%). The Knowledge Assessments are located in the respective links below.

- [Dashboard Developer](https://forms.gle/TjGprqkKxNS8WmES9)
- [SQL Developer](https://forms.gle/9E9GBFhzFViCnB9q7)

### Data Security Classification

Much of the data within and supporting the Customer Segmentation Dashboard is [Orange](/handbook/engineering/security/data-classification-standard.html#orange) or [Yellow](/handbook/engineering/security/data-classification-standard.html#yellow). This includes ORANGE customer metadata from the account, contact data from Salesforce and Zuora and GitLab's Non public financial information, all of which shouldn't be publicly available. Care should be taken when sharing data from this dashboard to ensure that the detail stays within GitLab as an organization and that appropriate approvals are given for any external sharing. In addition, when working with row or record level customer metadata care should always be taken to avoid saving any data on personal devices or laptops. This data should remain in [Snowflake](/handbook/business-ops/data-team/platform/#data-warehouse) and [Sisense](/handbook/business-ops/data-team/platform/periscope/) and should ideally be shared only through those applications unless otherwise approved. 


**ORANGE**

- Description: Customer and Personal data at the row or record level.
- Objects:
  - `dim_billing_accounts`
  - `dim_crm_accounts`
  - `dim_crm_persons`

**YELLOW**

- Description: GitLab Financial data, which includes aggregations or totals.
- Objects:
  - `dim_subscriptions`
  - `fct_charges`
  - `fct_invoice_items`
  - `fct_mrr`


### Solution Ownership

- Source System Owner:
    - Salesforce: `@jbrennan1`
    - Zuora: `@andrew_murray`
- Source System Subject Matter Expert:
    - Salesforce: `@jbrennan1`
    - Zuora: `@andrew_murray`
- Data Team Subject Matter Expert: `@msendal` `@paul_armstrong` `@jeanpeguero` `@jjstark` `@iweeks`

### Key Terms

1. [Product Category, Product Tier, Delivery](https://about.gitlab.com/handbook/marketing/product-marketing/tiers/#overview)
1. [Sales Segment](https://about.gitlab.com/handbook/sales/field-operations/gtm-resources/#segmentation)
1. [Account Owner Team](https://about.gitlab.com/handbook/sales/#initial-account-owner---based-on-segment)
1. [Territory](https://about.gitlab.com/handbook/sales/territories/#territories)
1. Industry

### Key Metrics, KPIs, and PIs

1. [ARR](https://about.gitlab.com/handbook/sales/#annual-recurring-revenue-arr)
1. [Customer Count](https://about.gitlab.com/handbook/sales/#customer)

## Self-Service Data Solution

### Self-Service Dashboard Viewer

| Dashboard                                                                                                        | Purpose |
| ---------------------------------------------------------------------------------------------------------------- | ------- |
| [Customer Segmentation](https://app.periscopedata.com/app/gitlab/718514/Customer-Segmentation-Analysis) | Provide insights into Quarterly ARR and Customer Count metrics by various customer dimensions |

### Self-Service Dashboard Developer

A great way to get started building charts in Sisense is to watch this 10 minute [Data Onboarding Video](https://www.youtube.com/watch?v=F4FwRcKb95w&feature=youtu.be) from Sisense. After you have built your dashboard, you will want to be able to easily find it again. Topics are a great way to organize dashboards in one place and find them easily. You can add a topic by clicking the `add to topics` icon in the top right of the dashboard. A dashboard can be added to more than one topic that it is relevant for. Some topics include Finance, Marketing, Sales, Product, Engineering, and Growth to name a few. 

### Self-Service SQL Developer

#### Key Fields and Business Logic

- Data is sourced from Zuora and Salesforce.
- Parent customers can have more than 1 product; therefore, they can be counted more than once in the product category and delivery dimensions. To get a unique count of total customers, you have to either aggregate the products and delivery into an `ARRAY` and do a `COUNT DISTINCT` of customers or do a `COUNT DISTINCT` of customers without the product category or delivery dimensions included. 
- For a charge to be considered recurring, the effective end month must be greater than the effective start month in the data.
- In Zuora, the `effective_end_date` and `effective_end_month` of the charge is the first day or month of the renewal respectively.
- In the monthly ARR calculation, the effective end month indicates when churn would happen and we do not count the effective end month in the ARR calculation. For example, a subscription with `effective start month` = 2020-07-01 and `effective end month` = 2021-07-01 would have its ARR summed from 2020-07-01 through 2021-06-01 for 12 months of ARR.

#### Entity Relationship Diagrams

| Diagram/Entity                                                                                              | Grain | Purpose | Keywords |
| ------------------------------------------------------------------------------------------------------------| ----- | ------- | -------- |
| [ARR and Customer Count Analytics ERD](https://app.lucidchart.com/documents#/documents?folder_id=226551757) |  Month, Subscription, Product Category     |  Provide insights into ARR and Customer Count by various customer dimensions       |   Parent Customer, Product Category, Delivery, Industry, Account Owner Team, Territory, and Sales Segment       |
| [Lead to Cash Overview ERD](https://app.lucidchart.com/documents/edit/c3e88869-774b-468f-aafc-60124aa71c31) |  All of the below | General overview of all processes for lead to cash | Parent Customer, Product Category, Delivery, Industry, Account Owner Team, Territory, Sales Segment, CRM, Persons, Accounts | 

#### Reference SQL

| Snippet Library                                                                                                            | Description |
| -------------------------------------------------------------------------------------------------------------------------- | -------- |
| [Customer Segmentation SQL Script](https://app.periscopedata.com/app/gitlab/snippet/customer_segmentation_level_2/55f848a751c548ceb1f55c7cac173821/edit)                                                                                           | Query to slice ARR and Customer Count by Product Category, Delivery, Industry, Account Owner Team, Territory, and Sales Segment | 
| [Customer Segmentation TY Quarter vs. LY Quarter SQL Script](https://app.periscopedata.com/app/gitlab/snippet/customer_segmentation_level_2_y_o_y_quarter_growth/55b645fe026e4d42ba43a42bfc843f86/edit) | Query to pull TY versus versus LY ARR and Customer Count by Quarter and slice by Product Category, Delivery, Industry, Account Owner Team, Territory, and Sales Segment |

## Data Platform Solution

### Data Lineage

- Data is sourced from Salesforce.com and Zuora, exluding accounts from manually managed list of [zuora excluded accounts](https://gitlab.com/gitlab-data/analytics/-/blob/master/transform/snowflake-dbt/data/zuora_excluded_accounts.csv)
- A complete data lineage can be found at [dbt mart_arr lineage chart](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.mart_arr?g_v=1&g_i=%2Bmart_arr%2B)

### DBT Solution

The dbt solution generates a dimensional model from RAW source data. 
The exceptions are the following fields that are calculated based on business logic implemented within specific dbt models:

| field | business logic |
| ------ | ------ |
| product_category | Calculated based of [Zuora product_rate_plan_name](https://gitlab.com/gitlab-data/analytics/-/blob/master/transform/snowflake-dbt/macros/zuora/product_category.sql) |
| delivery | Calculated based of [product_category](https://gitlab.com/gitlab-data/analytics/-/blob/master/transform/snowflake-dbt/macros/zuora/delivery.sql) |
| service_type | Calculated based of [product_rate_plan_name](https://gitlab.com/gitlab-data/analytics/-/blob/master/transform/snowflake-dbt/models/staging/common/dim_product_details.sql#L39) 

## Trusted Data Solution

See overview at [Trusted Data Framework](https://about.gitlab.com/handbook/business-ops/data-team/direction/trusted-data/)

[dbt guide examples](https://about.gitlab.com/handbook/business-ops/data-team/platform/dbt-guide/#trusted-data-framework) for
details and examples on implementing further tests

### Dashboards 

* [(WIP) Data insights exploration dashboard](https://app.periscopedata.com/app/gitlab/697774/WIP:-Data-Insights-Exploration-Dashboard)
    * Can be used to view data insights on any data set available to periscope to assist in the development of new dashboards or highlight potential issues.    
    
#### Zuora 
* [Trusted data dashboard](https://app.periscopedata.com/app/gitlab/738737/Zuora-Trusted-Data-Dashboard)
    * Reporting on all Zuora data tests which include the tdf tag.  
* [Data pipeline health dashboard](https://app.periscopedata.com/app/gitlab/715938/Data-Pipeline-Health-Dashboard)
    * Reporting on the row count to highlight any data issues in Zuora account and Subscription data. 

### EDM Enterprise Dimensional Model Validations

`Coming Soon`

### RAW Source Data Pipeline validations

[Data Pipeline Health Validations](https://app.periscopedata.com/app/gitlab/715938/Data-Pipeline-Health-Dashboard)
