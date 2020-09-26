---
layout: handbook-page-toc
title: "WIP Sales Funnel"
---

## On this page
{:.no_toc}

- TOC
{:toc}

The following content is still *under review* by the [Marketing and Sales data SSOT group (internal link)](https://docs.google.com/document/d/1zwGAAU4PUq2LArjJpeUN44kNsdRdHqJ5v5lWKOO2Cfc)
{: .alert .alert-warning}

## Solution Overview - Sales Funnel

This page describes facts and dimensions for sales funnel metrics and analysis. These models provide common dimensions for our crm data, such as `dim_crm_persons`, which is a union of Salesforce leads and contacts. As of now this includes the following objects (hyperlinks are to the detailed documentation for each object):

Facts:
- [`fct_crm_marketing_qualification`](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.fct_crm_marketing_qualification)
- [`fct_crm_sales_accepted_opportunity`](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.fct_crm_sales_accepted_opportunity)

Dimensions:
- [`dim_crm_accounts`](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.dim_crm_accounts)
- [`dim_crm_persons`](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.dim_crm_persons)

These facts represent conversion events in the Sales funnel. For mor information on Marketing Qualification please refer to the [Marketing Operations handbook](https://about.gitlab.com/handbook/marketing/marketing-operations/marketo/#mql-definition).

## Entity Relationship Diagram

<div style="width: 640px; height: 480px; margin: 10px; position: relative;"><iframe allowfullscreen frameborder="0" style="width:640px; height:480px" src="https://app.lucidchart.com/documents/embeddedchart/87c51c3d-1198-4c5f-aa7c-f29fdc9e394f" id="9sCy~CH7PMVB"></iframe></div>

## Data Security Classification

With the exception of some the data in `dim_crm_accounts`, which is [Orange](/handbook/engineering/security/data-classification-standard.html#orange), this data should be anonymized/masked in the case of `dim_crm_persons` or generally only relevant to our internal business operational performance in the Sales Funnel. If a user needs access to the personal data related to `dim_crm_persons` they would need to submit an access request for approval. Such data is out of scope for this sales funnel program and so is not covered here.

## Reference SQL

The following example queries are meant to demonstrate how to use these facts and dimensions. The Single Source of Truth for Metrics and KPIs is in [Sisense](/handbook/business-ops/data-team/platform/periscope/)
{: .alert .alert-warning}

### Marketing Qualified Leads (MQLs)

To get MQLs you use the [`fct_crm_marketing_qualification`](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.fct_crm_marketing_qualification) table, which containts all MQLs on leads and contacts. Since you can have multiple converted leads per contact, you'll want to select the first or last MQL using [`MIN()` or `MAX()`](https://docs.snowflake.com/en/sql-reference/functions/min.html) as in:
{: .alert .alert-info}

```sql
WITH mql AS ( -- get first or last mql by person

  SELECT
    crm_person_id,
    MIN(event_timestamp) AS first_mql,
    MAX(event_timestamp) AS last_mql
  FROM analytics_staging.fct_crm_marketing_qualification
  GROUP BY 1

)

SELECT -- mqls per month this calendar year
    DATE_TRUNC(month, first_mql) AS mql_month,
    COUNT(*)
FROM mql
WHERE YEAR(first_mql) = YEAR(current_date)
GROUP BY 1
ORDER BY 1 ASC
```

You can also join this to `dim_crm_persons` do add any of the person dimension columns to that data.
{: .alert .alert-info}

```sql
WITH mql AS (

  SELECT
    crm_person_id,
    MIN(event_timestamp) AS first_mql,
    MAX(event_timestamp) AS last_mql
  FROM analytics_staging.fct_crm_marketing_qualification
  GROUP BY 1

)

SELECT
  first_mql,
  dim_crm_persons.*
FROM analytics_staging.dim_crm_persons
INNER JOIN mql ON dim_crm_persons.crm_person_id = mql.crm_person_id
```
### Sales Accepted Opportunities (SAOs)

You can use the same basic logic for Sales Accepted Opportunities. With this fact table, however, you can also join directly to `dim_crm_accounts` to add any columns from that dimension as well.
{: .alert .alert-info}

```sql
WITH sao AS (
 
  SELECT
    crm_person_id, -- using dim_crm_accounts is also available
    min(sales_accepted_date) AS first_sao,
    max(sales_accepted_date) AS last_sao
  FROM analytics_staging.fct_crm_sales_accepted_opportunity
  GROUP BY 1

)

SELECT
    date_trunc(month,first_sao) sao_month,
    count(*)
FROM sao
WHERE year(first_sao) = year(current_date)
GROUP BY 1
ORDER BY 1 ASC;
```

Both of these facts can be joined to the [`dim_crm_persons`](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.dim_crm_persons) dimension table to get conversion data:
{: .alert .alert-info}

```sql
WITH first_sao AS ( -- get SAOs

    SELECT
        crm_person_id,
        min(sales_accepted_date) AS first_sao
    FROM analytics_staging.fct_crm_sales_accepted_opportunity
    GROUP BY 1

), first_mql AS ( -- get first mql

    SELECT
        crm_person_id,
        date_trunc(day, min(event_timestamp))::date AS first_mql --  match the SAO type
    FROM analytics_staging.fct_crm_marketing_qualification
    GROUP BY 1    
    
)

SELECT
    first_mql.first_mql,
    first_sao.first_sao,
    datediff(day,first_mql, first_sao) AS mql_to_sao,
    *
FROM analytics_staging.dim_crm_persons crm_persons
INNER JOIN first_mql
    ON first_mql.crm_person_id = crm_persons.crm_person_id
LEFT JOIN first_sao
    ON first_sao.crm_person_id = crm_persons.crm_person_id
```

