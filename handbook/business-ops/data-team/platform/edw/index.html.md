---
layout: handbook-page-toc
title: "Enterprise Dimensional Model"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

{::options parse_block_html="true" /}

## Background

This is to demo work currently done as part of data team's effort to develop EDW using dimensional modeling.

- [Proposal issue](https://gitlab.com/gitlab-data/managers/-/merge_requests/1)
- [Pilot Enterprise Data Warehouse epic](https://gitlab.com/groups/gitlab-data/-/epics/76)

## Dimensional modeling

Dimensional modeling is part of the Business Dimensional Lifecycle methodology developed by Ralph Kimball which includes a set of methods, techniques and concepts for use in data warehouse design.

_a logical design technique that seeks to present the data in a standard, intuitive framework that allows for high-performance access_

Dimensional Modeling is business process oriented and can be built in 4 steps:

1. Choose the business process e.g. track monthly revenue
1. Declare the grain e.g. per customer
1. Identify the dimensions
1. Identify the fact

## Fact and dimension tables

Dimensional modeling always uses the concepts of facts (measures), and dimensions (context).
Facts are typically (but not always) numeric values that can be aggregated, and dimensions are groups of hierarchies and descriptors that define the facts.

In the simplest version fact table is a central table and is linked to dimensional tables with foreign keys creating a star schema.
Star schema with dimensional tables linking to more dimensional tables are called snowflake schemas, multi fact tables schemas are called galaxies.

### First iteration in GitLab DWH

OKR: Reporting on both ARR and Customer counts entirely supported in a Kimball Dimensional Warehouse

The graphical schema of dimensional model developed for calculating  ARR/ Customer count

```mermaid
classDiagram
    fct_charges --|> dim_subscriptions
    fct_charges --|> dim_accounts
    fct_charges --|> dim_dates
    fct_charges --|> dim_product_details
    dim_accounts --|> dim_customers
    dim_subscriptions --|> dim_customers
    fct_invoice_items_agg <|-- fct_charges
    fct_invoice_items <|-- fct_charges
    fct_charges : FK: invoice_item_id
    fct_charges : FK: account_id
    fct_charges: FK: product_id
    fct_charges: FK: subscription_id,
    fct_charges: FK: effective_start_date_id,
    fct_charges: FK: effective_end_date_id,
    fct_charges: FK: product_details_id
    fct_charges : PK: charge_id
    fct_charges: mrr()
    fct_charges: rate_plan_name()
    fct_charges: rate_plan_charge_name()
    fct_invoice_items_agg: PK: charge_id
    fct_invoice_items_agg: charge_amount_sum()
    fct_invoice_items: PK: invoice_item_id
    class dim_accounts{
        PK: account_id
        FK: crm_id
        account_name()
        country()
    }
    class dim_subscriptions{
        PK: subscription_id
        FK: crm_id
        subscription_status()
    }
    class dim_dates {
        PK: date_id
    }
    class dim_customers {
        PK: crm_id
        customer_id
    }
    class dim_product_details {
        PK: product_details_id
    }
```

More on use and conventions of Dimensional Modeling in Data Team Handbook [here](/handbook/business-ops/data-team/dbt-guide/#dimensional)

## How to interact with the dim and fct tables -  building Data Marts

Fct_ and dim_ dbt models are created in `COMMON` schema indicating that they are not source related and create basis to build data marts.

In Snowflake they can be found in `ANALYTICS_STAGING` schema.

The advantage of dimensional schema is ease of querying and building data marts.

Data mart is where the dimensions labels selection and aggregation can happen.

```sql
    SELECT
    COALESCE(dim_customers.merged_to_account_id , dim_customers.CRM_ID) AS customer_id,
    subscription_name_slugify,
    dateadd('month',-1,dim_dates.first_day_of_month) as mrr_month,
    mrr
    FROM ANALYTICS.ANALYTICS_STAGING.dim_dates
     INNER JOIN ANALYTICS.ANALYTICS_STAGING.fct_charges ON fct_charges.effective_start_date_id <= dim_dates.date_id
     AND fct_charges.effective_end_date_id > dim_dates.date_id  AND dim_dates.day_of_month=1
    INNER JOIN ANALYTICS.ANALYTICS_STAGING.fct_invoice_items_agg ON fct_charges.charge_id = fct_invoice_items_agg.charge_id
    INNER JOIN ANALYTICS.ANALYTICS_STAGING.dim_subscriptions ON dim_subscriptions.SUBSCRIPTION_ID = fct_charges.subscription_id
    INNER JOIN  ANALYTICS.ANALYTICS_STAGING.dim_customers ON dim_customers.crm_id = dim_subscriptions.crm_id;

```

- Example Data Mart build with dbt [WIP](https://gitlab.com/gitlab-data/analytics/-/blob/b7375abfc6ab32eb6d9988df6ae5a98ebc7f72ba/transform/snowflake-dbt/models/marts/mrr/mrr_data_mart.sql)

## Why is it worth using fact and dim tables

- simpler to query as fully normalized data models are way too complex for non-developers to deal with
- centralized implementation of business logic, consistent definitions across business users e.g. one source of truth of customer definition
- easier to add data to existing dimensional model
- easier to communicate with business
- definitions should be source system independent

## How dimensional modeling can improve weaknesses of what we are using now

- very often our models follow source models which are normalized and difficult for business user to understand
- plenty of xf_ models (re-)use similar but yet not the same logic for defining customer
- redundancy, reinventing definitions when building model using source models
- hard to identify which xf_/intermediate models are affected by changes in source/base models

## Useful links and resources

- [dbt Discourse about Kimball dimensional modelling](https://discourse.getdbt.com/t/is-kimball-dimensional-modeling-still-relevant-in-a-modern-data-warehouse/225/6) in modern data warehouses including some important ideas why we should still sue Kimball
- [Dimensional modelling manifesto](https://www.kimballgroup.com/1997/08/a-dimensional-modeling-manifesto/)
- [Dimensional Modelling techniques](https://www.kimballgroup.com/data-warehouse-business-intelligence-resources/kimball-techniques/dimensional-modeling-techniques/) by Kimball Group