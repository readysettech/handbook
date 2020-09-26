---
layout: handbook-page-toc
title: "Product Geolocation Analysis"
---

## On this page
{:.no_toc}

- TOC
{:toc}

---

## Product Geolocation Analysis : Self-Managed

Understanding where your product is used around the world is an important step towards developing a more complete understanding of your customers, your product's global reach, and related location insights.

Currently, the majority of GitLab's customers choose to [download, install, and host a GitLab self-managed instance](/handbook/marketing/product-marketing/dot-com-vs-self-managed/#why-you-probably-want-gitlabcom), which is why we are [focused heavily on delivering a great self-managed customer experience](/direction/#strategic-challenges).

To make the right data-driven decisions on the self-managed product lifecycle and what features to invest in, [our self-managed customers](/is-it-any-good/) sends GitLab a weekly [usage ping](/handbook/customer-success/tam/usage-ping-faq/) at an instance-level by [enabling usage ping on their self-managed instance](https://docs.gitlab.com/ee/user/admin_area/settings/usage_statistics.html#instance-level-statistics) or by sharing the values with our Customer Success team.

This instance-level data allows GitLab to understand country-level statistics and trends in instance adoption, version adoption rate, and instance life cycle.

### Knowledge Assessment & Certification

The Self-Service Data Certificate program is based on the Learning and Development Certification program. The Self-Service Data program provides individual Certificates for each subject-oriented Dashboard Developer or SQL Developer Knowledge Assessment successfully completed. Links to the Knowledge Assessments are located in the appropriate sections below.

### Data Classification

`Coming Soon`

### Solution Ownership

- Source System Owner:
    - Versions: `@jeromezng`
    - Salesforce: `@jbrennan1`
    - Zuora: `@andrew_murray`
    - Location (IP Address): `@m_walker`
- Source System Subject Matter Expert:
    - Versions: `@jeromezng`
    - Salesforce: `@jbrennan1`
    - Zuora: `@andrew_murray`
    - Location (IP Address): `@m_walker`
- Data Team Subject Matter Expert: `@derekatwood` `@mpeychet_` `@m_walker`

### Key Terms

- [Account](/handbook/sales/#additional-customer-definitions-for-internal-reporting)
- Account Instances - the total number of reported instances that can be mapped to an account
- [Host](https://docs.gitlab.com/ee/development/telemetry/event_dictionary.html)
- [Instance](https://docs.gitlab.com/ee/development/telemetry/event_dictionary.html)
- Instance User Count - the total number of users on an instance
- [Paid User](/handbook/product/performance-indicators/#paid-user)
- [Product Tier](/handbook/marketing/product-marketing/tiers/#overview)
- [Usage Ping](https://docs.gitlab.com/ee/development/telemetry/event_dictionary.html)
- [Version](/handbook/sales/process/version-check/#what-is-the-functionality-of-the-gitlab-version-check)

### Key Metrics, KPIs, and PIs

- [Active Hosts](/handbook/product/performance-indicators/#active-hosts)
- [Lost Instances](/handbook/product/performance-indicators/#lost-instances)
- [Paid User](/handbook/product/performance-indicators/#paid-user)
- [Paid UMAU](/handbook/product/performance-indicators/#paid-umau)
- [Unique Monthly Active Users - UMAU](/handbook/product/performance-indicators/#unique-monthly-active-users-umau)

## Self-Service Data Solution

### Self-Service Dashboard Viewer

| Dashboard                                                                                                    | Purpose |
| ------------------------------------------------------------------------------------------------------------ | ------- |
| [Product Geolocation Analysis](https://app.periscopedata.com/app/gitlab/731086/Product-Geolocation-Analysis) | cell    |

### Self-Service Dashboard Developer

| Data Space | Description |
| ---------- | ----------- |
| cell       | cell        |

#### Self-Service Dashboard Developer Certificate

To receive a Certificate, you will need to earn 100% on the [Self-Service Dashboard Developer Knowledge Assessment](https://docs.google.com/forms/d/e/1FAIpQLSeqicaMfWVUfFsex9_o6GTkWJKobYBT8qucz9YNmyDm5ZKqiA/viewform?usp=sf_link). Upon completion of the Knowledge Assessment, you will be emailed your responses and this email will serve as your Certificate.

### Self-Service SQL Developer

#### Self-Service SQL Developer Certificate

To receive a Certificate, you will need to earn 100% on the [Self-Service SQL Developer Knowledge Assessment](https://docs.google.com/forms/d/e/1FAIpQLScH9CkiACQ1worzldjUi6cUWUL03tXrLEEaZALABabZPV7GuQ/viewform?usp=sf_link). Upon completion of the Knowledge Assessment, you will be emailed your responses and this email will serve as your Certificate.

#### Key Fields and Business Logic

`Coming Soon`

#### Entity Relationship Diagrams

| Diagram/Entity                                                                                        | Grain         | Purpose                                                    | Keywords |
| ----------------------------------------------------------------------------------------------------- | ------------- | ---------------------------------------------------------- | -------- |
| [Usage Ping Mart](https://app.lucidchart.com/documents/view/be5f5dc8-8ad5-4586-af53-93ff5e00f720/0_0) | usage_ping_id | Mart for exploring usage ping and related customer metrics |          |

#### Snippets

Snippets are used to create a string of SQL code that can be reused in different charts. For more information, visit the [Sisense SQL Snippets page](https://dtdocs.sisense.com/article/snippets).

##### usage_pings_mart Snippet

This snippet is currently present in Sisense with the name of [usage_pings_mart](https://app.periscopedata.com/app/gitlab/snippet/usage_pings_mart/553a4fc6bf004b749eb60a144d722ccc/edit).

```sql
WITH pings AS (
  
  SELECT *
  FROM analytics.usage_ping_mart
  WHERE ping_source = 'Self-Managed'
    AND is_last_ping_in_month = TRUE
    AND date_id >= 20191101
    AND [ping_product_tier=product_tier]
    AND [ping_country_name=Usage_Ping_Country]
  
)
```

#### Reference SQL

##### Total Number of Accounts sending usage ping in a month

```sql
[usage_pings_mart]

SELECT 
  ping_month,
  COUNT(DISTINCT account_id) AS total_accounts
FROM pings
GROUP BY 1
```

##### Monthly Number of Instances sending usage ping per Country 

```sql
[usage_pings_mart]

SELECT
  ping_month,
  ping_country_name    AS country_name,
  COUNT(DISTINCT uuid) AS instances_reporting
FROM pings
GROUP BY 1,2
```

#### Data Discovery Function in Sisense

If you are not familiar with SQL, there is the Data Discovery function in Sisense wherein you can create charts through a drag-and-drop interface and no SQL query is needed.

##### How to work with the Data Discovery Function

<figure class="video_container">
  <iframe src="https://www.youtube.com/embed/h_b9A8F7Ic8" frameborder="0" allowfullscreen="true"> </iframe>
</figure>

More information here on the [Data Discovery page in Sisense](https://dtdocs.sisense.com/article/data-discovery).

## Data Platform Solution

### Data Lineage

- [dbt model lineage diagram](https://dbt.gitlabdata.com/#!/model/model.gitlab_snowflake.usage_ping_mart?g_v=1&g_i=%2Busage_ping_mart%2B)
- The IP address mapping to geolocation is derived from the [free geolite2 Maxmind database](https://dev.maxmind.com/geoip/geoip2/geolite2/).
- The location information is also derived from the Maxmind database, with the exception of the iso3 country code field which comes from the [Zuora Country CSV in the repository](https://gitlab.com/gitlab-data/analytics/-/blob/master/transform/snowflake-dbt/data/zuora_country_geographic_region.csv).

### DBT Solution

- In order to avoid large joins between tables and the IP-address-to-geolocation mapping consisting of less-than/greater-than join clauses, IP addresses are incrementally mapped to geolocations separate from other models as implemented originally in [this merge request](https://gitlab.com/gitlab-data/analytics/-/merge_requests/3413).

- This approach also gives us the ability to obscure IP addresses in Sisense but still preserving the ability to match IP addresses across different database tables.

## Trusted Data Solution

[Trusted Data Framework](https://about.gitlab.com/handbook/business-ops/data-team/direction/trusted-data/)

### EDM Enterprise Dimensional Model Validations

`Coming Soon`

### RAW Source Data Pipeline validations

`Coming Soon`

### Manual Data Validations

`Coming Soon`
