---
layout: handbook-page-toc
title: "Infrastructure Labels and Tags"
---

## On this page
{:.no_toc}

- TOC
{:toc}

## Quick Reference

We use the `gl_` prefix for all labels and tags. All keys use underscores (`snake_case`). All values should use hyphens (`alpha-dash` for slug'd values), however underscores are allowed.

In labels and tags for specific realms should be prefixed with the realm prefix. You can learn more about the realm variables in the respective realm's documentation.

### Global Labels/Tags

| Slug/Label/Tag/Key         | Usage       | Human Name                     | Documentation |
|----------------------------|-------------|--------------------------------|---------------------------------------------------------------------------------------|
| `gl_realm`                 | Required    | Environment Realm              | [Usage Documentation](#environment-realm-gl_realm)                                    |
| `gl_env_type`              | Required    | Environment Type               | [Usage Documentation](#environment-type-gl_env_type)                                  |
| `gl_env_name`              | Required    | Environment Name               | [Usage Documentation](#environment-name-gl_env_name)                                  |
| `gl_env_id`                | Optional    | Environment ID                 | [Usage Documentation](#automated-infrastructure-environment-id-gl_env_id)             |
| `gl_env_continent`         | Optional    | Environment Continent          | [Usage Documentation](#geographic-continent-region-of-environment-gl_env_continent)   |
| `gl_owner_email_handle`    | Required    | Owner Email Handle             | [Usage Documentation](#owner-email-handle-gl_owner_email_handle)                      |
| `gl_owner_timezone`        | Optional    | Owner Timezone                 | [Usage Documentation](#owner-timezone-gl_owner_timezone)                              |
| `gl_entity`                | Optional    | GitLab Entity                  | [Usage Documentation](#gitlab-entity-gl_entity)                                       |
| `gl_dept`                  | Required    | GitLab Department              | [Usage Documentation](#gitlab-department-gl_dept)                                     |
| `gl_dept_group`            | Required    | GitLab Department Group        | [Usage Documentation](#gitlab-department-group-gl_dept_group)                         |
| `gl_product_stage`         | Optional    | GitLab Product Stage           | [Usage Documentation](#gitlab-product-stage-gl_product_stage)                         |
| `gl_resource_type`         | Optional    | Cloud Resource Type            | [Usage Documentation](#resource-type-gl_resource_type)                                |
| `gl_resource_name`         | Optional    | Cloud Resource Name            | [Usage Documentation](#resource-name-gl_resource_name)                                |
| `gl_resource_host`         | Optional    | Cloud Resource Host            | [Usage Documentation](#resource-host-gl_resource_host)                                |

### Realm Labels/Tags

Please see the realm label and tag handbook pages for labels and tags specific to the realm.

* [business-ops](/handbook/infrastructure-standards/realms/business-ops/labels-tags)
* [eng-dev](/handbook/infrastructure-standards/realms/eng-dev/labels-tags)
* [eng-infra](/handbook/infrastructure-standards/realms/eng-infra/labels-tags)
* [eng-security](/handbook/infrastructure-standards/realms/eng-security/labels-tags)
* [eng-support](/handbook/infrastructure-standards/realms/eng-support/labels-tags)
* [gitter](/handbook/infrastructure-standards/realms/gitter/labels-tags)
* [saas](/handbook/infrastructure-standards/realms/saas/labels-tags)
* [sales-cs](/handbook/infrastructure-standards/realms/sales-cs/labels-tags)
* [sandbox](/handbook/infrastructure-standards/realms/sandbox/labels-tags)

### Design Decisions and Change Log

Here is a summary of changes made during the design of these standards based on team feedback that should be preserved for historical reference.

* Based on feedback in the issue, we have revamped the list of departments and groups based on functional teams rather than people manager reporting structure.
* The GitLab Division has been deprecated since it is prefixed on the `gl_department`.
* We have renamed `gl_department` to `gl_dept` to allow it to be shorter as a prefix for `gl_dept_group`.
* We have renamed `gl_team` to `gl_dept_group` based on feedback about the ambiguity of `team` and the remapping that we did in the spreadsheet that most departments have groups/teams but none have sub-groups other than engineering which has the sub-department/stage (Ex. `Dev` - `Plan`) organizational hierarchy. The engineering sub-department is not used in our label/tag structure.
* We have added `gl_product_stage`. Earlier iterations used `gl_stage` however the term `stage` is ambiguous so we identify it as the product stage.
* We have abbreviated all values to allow for easier prefixing using industry recognizable abbreviations. We use full words where an abbreviation is not universally recognizable. For OKTA integration, we remap values from BambooHR to their short names that we use for infrastructure.
* We removed `gl_owner_username` since GitLab.com usernames can have characters not allowed cloud provider labels and tags.
* We renamed `gl_owner_email` to `gl_owner_email_handle` to provide clarity of the value that is expected.
* We have removed `gl_owner_slack_id` since we won't perform any action from a cloud resource and will use owner lookup in separate tools using `gl_owner_email_handle`.
* We added the `allocate` value to `gl_entity` for legacy parity with how we allocate global costs based on percentage of revenue for each entity.
* We added the `gl_resource_type` and `gl_resource_name` fields since GCP doesn't support easy reporting based on type of resource or name unless you use labels.
* We added `gl_resource_host` to help show aggregate costs of a parent resource for all resources (ex. disk, network, etc.)

## Environment Realm (`gl_realm`)

This label/tag is required.  
{: .alert .alert-success}

```
gl_realm: `eng-dev`
```

This is for the top-level identification of what type of resources reside here, and which infrastructure team has authoritative ownership of it.

Any custom labels or tags that are created should use the respective realm slug as the prefix for the label/tag key (Ex. `gl_sandbox_keyname`).

### Shared Services

<table>
    <thead>
        <tr>
            <th style="width: 25%;">Value</th>
            <th style="width: 25%;">Human Friendy Name</th>
            <th style="width: 40%;">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>saas</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/saas">GitLab SaaS</a>
            </td>
            <td>
                This is for GitLab.com SaaS that is managed by Engineering Infrastructure and Site Reliability Engineers.
            </td>
        </tr>
        <tr>
            <td><code>gitter</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/gitter">Gitter SaaS</a>
            </td>
            <td>
                This is for Gitter hosted services.
            </td>
        </tr>
        <tr>
            <td><code>sandbox</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/sandbox">Compute Sandbox Cloud</a>
            </td>
            <td>
                This is for sandbox and ephemeral testing resources that provides an account/project for each user that are self-administered by each team member.
            </td>
        </tr>
    </tbody>
</table>


### Department Realms

<table>
    <thead>
        <tr>
            <th style="width: 25%;">Value</th>
            <th style="width: 25%;">Human Friendy Name</th>
            <th style="width: 50%;">Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td><code>business-ops</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/business-ops">Business Operations (IT)</a>
            </td>
            <td>
                This is for resources managed by the Business Operations and IT team, including all departments and groups that do not have their own realm.
            </td>
        </tr>
        <tr>
            <td><code>eng-dev</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/eng-dev">Engineering Development</a>
            </td>
            <td>
                This is for additional services managed by Engineering Development (including `eng-ux` and `product` department resources) that don't belong in `saas`, `eng-infra`, or `sandbox` realms.
            </td>
        </tr>
        <tr>
            <td><code>eng-infra</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/eng-infra">Engineering Infrastructure</a>
            </td>
            <td>
                This is for additional services managed by Engineering Infrastructure and Site Reliability Engineers that may not be specific to GitLab.com SaaS (Ex. tools, release and package management services, etc).
            </td>
        </tr>
        <tr>
            <td><code>eng-security</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/eng-security">Engineering Security</a>
            </td>
            <td>
                This is for resources managed by the Security team.
            </td>
        </tr>
        <tr>
            <td><code>eng-support</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/eng-support">Engineering Support</a>
            </td>
            <td>
                This is for resources managed by the Customer Support team.
            </td>
        </tr>
        <tr>
            <td><code>sales-cs</code></td>
            <td>
                <a href="/handbook/infrastructure-standards/realms/sales-cs">Customer Success</a>
            </td>
            <td>
                This is for resources managed by the Customer Success team, including demo and training systems.
            </td>
        </tr>
    </tbody>
</table>

## Environment Type (`gl_env_type`)

This label/tag is required.  
{: .alert .alert-success}

```
gl_env_type: 'experiment'
```

### Expected values

| Value         | Description                                                             |
|---------------|-------------------------------------------------------------------------|
| `experiment`  | (default) This is for individual user experiments are not impacted if powered off by infrastructure or security team, or data lost due to systems change. |
| `test`        | This is for experiments that affect multiple users (ex. customer proof-of-concept or load testing) and would have disruptive impact if powered off. |
| `stg`         | This is for a staging environment for tools/etc that would have major impact if powered off. These are for environments that are known to infra/security teams. The infra team has standardized on the use of `stg` instead of `stag` or `stage`, so we've universally adopted that here. |
| `prd`         | This is for a production or production-like environment for tools/etc that would have major impact if powered off. These are for environments that are known to infra/security teams. The infra team has standardized on the use of `prd` instead of `prod`, so we've universally adopted that here. |
| `other`       | As a last resort, you can use the other category. These are subject to periodic review. |

> New values can be added to this list and used without any other changes needed. This list was created for this label/tag and is not inherited from another source.

## Environment Name (`gl_env_name`)

This label/tag is required.  
{: .alert .alert-success}

```
gl_env_name: 'learning-kubernetes'
```

The environment name is a short name or description of the purpose of the environment or service. This is a sub-descriptor of `gl_realm` and `gl_env_type`. The standards and use of this label/tag vary based on the `gl_realm` that it is used in, and each team can use it however it makes sense to them.

### Realm Usage Guidelines

| Realm              | Usage Guidelines or Standards                                                              |
|--------------------|--------------------------------------------------------------------------------------------|
| `saas`             | (Placeholder for future use)                                                               |
| `gitter`           | (Placeholder for future use)                                                               |
| `business-ops`     | (Placeholder for future use)                                                               |
| `eng-dev`          | (Placeholder for future use)                                                               |
| `eng-infra`        | (Placeholder for future use, this is currently called `pet_name`)                          |
| `eng-security`     | (Placeholder for future use)                                                               |
| `eng-support`      | (Placeholder for future use)                                                               |
| `sales-cs`         | (Placeholder for future use)                                                               |
| `sandbox`          | Descriptive name of the purpose (Ex. `learning-kubernetes`, `tanuki-industries-iac-demo`)  |

## Automated Infrastructure Environment ID (`gl_env_id`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_env_id: 'a1b2c3d4'
```

The environment ID allows various inputs, but in general is a short UUID, long UUID, SHA or other alphanumeric identifier that is systematically generated. The use of this label/tag will vary based on the `gl_realm` that it is used in, and each team can use it however it makes sense to them.

### Realm Usage Guidelines

| Realm              | Usage Guidelines or Standards  |
|--------------------|--------------------------------|
| `saas`             | (Placeholder for future use)   |
| `gitter`           | (Placeholder for future use)   |
| `business-ops`     | (Placeholder for future use)   |
| `eng-dev`          | (Placeholder for future use)   |
| `eng-infra`        | (Placeholder for future use)   |
| `eng-security`     | (Placeholder for future use)   |
| `eng-support`      | (Placeholder for future use)   |
| `sales-cs`         | (Placeholder for future use)   |
| `sandbox`          | For AWS accounts and GCP projects, this is the short UUID of the corresponding database record in the Sandbox Cloud portal that handled account provisioning. For Terraform-managed environments, this is the commit ID or SHA of the Terraform configuration (implementation varies).  |

## Geographic Continent (Region) of Environment (`gl_env_continent`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_env_continent: 'america'
```

> We use `continent` to avoid confusion with `region` since that is an ambiguous word.

This is the continent where this environment's resources are consumed by users. This may not necessarily be where it is deployed or where the environment owner resides. This allows us to understand impact to users if infrastructure maintenance is needed or security incidents occur. This can also be used as meta data for global resources with autoscaling resources in specific continents/regions, however the `gl_entity` label/tag is needed for explicit cost allocation.

The abbreviation used by the business can change over time (Ex. `APJ`, `APAC`, `Asia Pacific`), and the cloud providers use different nomenclature, so we are standardizing using full names based on the prefix of programmatic timezones (Ex. `America/Los_Angeles` is `america`). For non-regional services, you can use the `global` value.

### Expected Values

| Value         | Business Acronyms     | Cloud provider regions                                                   |
|---------------|-----------------------|--------------------------------------------------------------------------|
| `global`      |                       | (default) For global resources or any non-region specific services.      |
| `america`     | `AMER`, `US`, `NORAM` | AWS `us-*`/`ca-*`/`sa-*`, GCP `us-*`/`southamerica-*`/`northamerica-*`   |
| `europe`      | `EMEA`, `METNA`       | AWS `eu-*`/`me-*`, GCP `europe-*`                                        |
| `africa`      |                       | AWS `af-*`                                                               |
| `asia`        | `APAC`, `APJ`         | AWS `ap-*`/`cn-*`, GCP `asia-*`                                          |
| `australia`   | `APAC`, `APJ`         | AWS `ap-*`, GCP `australia-*`                                            |

> Some possible prefix values have been omitted from this list for brevity and unlikely applicability (Ex. `brazil`, `hongkong`, `indian`, etc.). They can be added at environment owner's discretion.


## Owner Email Handle (`gl_owner_email_handle`)

This label/tag is required.  
{: .alert .alert-success}

```
gl_owner_email_handle: 'jmartin'
```

The email handle before `@gitlab.com`. We only use the handle since labels and tags do not support `@` and `.` symbols. Values can be individual users or G-Suite group aliases. For people handles, this should be `{firstinitial}{lastname}` and not any username aliases (Ex. `jeff`) since user aliases cannot be looked up programatically with our current architecture.

This is used for association with OKTA account, infrastructure notifications, and identifying the user's account with additional meta data. Users may receive emails with security advisory notifications.

## Owner Timezone (`gl_owner_timezone`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_owner_timezone: 'america-los_angeles'
```

This is the timezone of the environment owner that is used for determining working hours. We assume that working hours are between 6am (06:00) and 6pm (18:00). This is usually only used when there is only one or two people who own a system. For systems with global coverage, you should not use this label/tag.

This is the based on the programmatic timezone ID that usually follows the format `Continent/Locality`. You can see the full list of examples in the [GCP documentation](https://cloud.google.com/dataprep/docs/html/Supported-Time-Zone-Values_66194188).

Due to limitations with the allowed characters in labels, the `/` is not allowed and we use lowercase labels. Therefore, we replace the slash `/` with a hyphen `-` and use lowercase letters exclusively. This is the same reason that we chose not use UTC values since cannot use `+` symbols.

### Example Values

* `america-los_angeles`
* `america-denver`
* `america-chicago`
* `america-new_york`
* `asia-singapore`
* `asia-tokyo`
* `australia-sydney`
* `africa-johannesburg`
* `europe-amsterdam`
* `europe-berlin`
* `europe-london`
* `europe-paris`
* `europe-vienna`

> These are examples and not an exhaustive list. As part of our inclusive values, please know that all timezones are valued equally and this was created based on some of the localities on the team map with the largest number of team members per capita.

## GitLab Entity (`gl_entity`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_entity: 'allocate'
```

This allows us to allocate costs to the respective business entity in financial reports. If not set, we will assume `allocate`.

### Expected Values

| Value         | Description                                      |
|---------------|--------------------------------------------------|
| `allocate`    | (global default) Allocate based on % of revenue  |
| `inc`         | GitLab Inc, United States of America             |
| `ltd`         | GitLab Ltd, United Kingdom                       |
| `bv`          | GitLab BV, the Netherlands                       |
| `gmbh`        | GitLab GmbH, Germany                             |
| `pty`         | GitLab PTY Ltd, Australia                        |
| `canada`      | (future use) GitLab Canada Corp., Canada         |
| `gk`          | (future use) GitLab GK, Japan                    |

See the [GitLab Mailing addresses](https://about.gitlab.com/company/visiting/) for details about each entity.

### Realm Usage Guidelines

| Realm              | Usage Guidelines or Standards  |
|--------------------|--------------------------------|
| `saas`             | (Placeholder for future use)   |
| `gitter`           | (Placeholder for future use)   |
| `business-ops`     | (Placeholder for future use)   |
| `eng-dev`          | (Placeholder for future use)   |
| `eng-infra`        | (Placeholder for future use)   |
| `eng-security`     | (Placeholder for future use)   |
| `eng-support`      | (Placeholder for future use)   |
| `sales-cs`         | Use `allocate` for all resources |
| `sandbox`          | The GitLab entity that the team member is associated with in BambooHR. |

### BambooHR Mapping

During testing of OKTA integration, this field is populating additional values we did not expect (ex. `safeguard-italy`, `federal`). This is documented in [www-data/data/entity_mapper.yml](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/data/entity_mapper.yml) and we will map the respective entities to our cost center entities listed.

## GitLab Department (`gl_dept`)

This label/tag is required.  
{: .alert .alert-success}

```
gl_dept: eng-dev
```

We have abbreviated all values to allow for easier prefixing using industry recognizable abbreviations. We use full words where an abbreviation is not universally recognizable. For OKTA integration, we use YAML data file to remap values from BambooHR to their short names that we use for infrastructure. You can see a quick reference in the table below.

### Expected Values

| Division    | Department             | gl_dept (Slug/Label/Tag)   |
|-------------|------------------------|----------------------------|
| Engineering | Customer Support       | `eng-support`              |
| Engineering | Development            | `eng-dev`                  |
| Engineering | Infrastructure         | `eng-infra`                |
| Engineering | Quality                | `eng-quality`              |
| Engineering | Security               | `eng-security`             |
| Engineering | UX                     | `eng-ux`                   |
| GA          | Accounting             | `ga-accounting`            |
| GA          | Business Operations    | `ga-business-ops`          |
| GA          | CEO                    | `ga-ceo`                   |
| GA          | Finance                | `ga-finance`               |
| GA          | Legal                  | `ga-legal`                 |
| GA          | People Success         | `ga-people`                |
| GA          | Recruiting             | `ga-recruiting`            |
| Marketing   | Awareness              | `mktg-awareness`           |
| Marketing   | Brand & Digital Design | `mktg-brand-design`        |
| Marketing   | Campaigns              | `mktg-campaigns`           |
| Marketing   | Communications         | `mktg-communications`      |
| Marketing   | Community Relations    | `mktg-community`           |
| Marketing   | Content Marketing      | `mktg-content`             |
| Marketing   | Digital Marketing      | `mktg-digital`             |
| Marketing   | Field Marketing        | `mktg-field`               |
| Marketing   | Inbound Marketing      | `mktg-inbound`             |
| Marketing   | Marketing Ops          | `mktg-ops`                 |
| Marketing   | Owned Events           | `mktg-events`              |
| Marketing   | Partner Marketing      | `mktg-partner`             |
| Marketing   | Sales Development      | `mktg-sales-dev`           |
| Marketing   | Strategic Marketing    | `mktg-strategic`           |
| Product     | Product Management     | `product-mgmt`             |
| Sales       | Business Development   | `sales-alliances`          |
| Sales       | Channel                | `sales-channel`            |
| Sales       | Commercial Sales       | `sales-commercial`         |
| Sales       | Customer Success       | `sales-cs`                 |
| Sales       | Enterprise Sales       | `sales-ent`                |
| Sales       | Field Operations       | `sales-field-ops`          |
| Sales       | Practice Management    | `sales-practice-mgmt`      |


## GitLab Product Stage (`gl_product_stage`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_product_stage: eng-dev-manage
```

Since the `eng-dev` department has many groups, we use the [Product sections, stages, groups and categories](/handbook/product/product-categories/#devops-stages) handbook page to define a parent group using the product stage. During the design discussion, we iterated with using product categories and sub-departments, and the stage made the most sense.

For GitLab SaaS and infrastructure cost allocation or attribution, the Engineering Infrastructure department team members can use the `gl_product_stage` label to attach to resources that should be attributed to a specific stage. You can optionally use the `gl_dept_group` if you need more granular attribution.

### Expected Values

| Value | Product Category Documentation |
|------------------------|----------------------------------------------------------------------------------------------------------|
| `eng-dev-manage`       | [Manage Stage](/handbook/product/product-categories/#manage-stage)                                       |
| `eng-dev-plan`         | [Plan Stage](https://about.gitlab.com/handbook/product/product-categories/#plan-stage)                   |
| `eng-dev-create`       | [Create Stage](https://about.gitlab.com/handbook/product/product-categories/#create-stage)               |
| `eng-dev-verify`       | [Verify Stage](https://about.gitlab.com/handbook/product/product-categories/#verify-stage)               |
| `eng-dev-package`      | [Package Stage](https://about.gitlab.com/handbook/product/product-categories/#package-stage)             |
| `eng-dev-release`      | [Release Stage](https://about.gitlab.com/handbook/product/product-categories/#release-stage)             |
| `eng-dev-configure`    | [Configure Stage](https://about.gitlab.com/handbook/product/product-categories/#configure-stage)         |
| `eng-dev-monitor`      | [Monitor Stage](https://about.gitlab.com/handbook/product/product-categories/#monitor-stage)             |
| `eng-dev-secure`       | [Secure Stage](https://about.gitlab.com/handbook/product/product-categories/#secure-stage)               |
| `eng-dev-defend`       | [Defend Stage](https://about.gitlab.com/handbook/product/product-categories/#defend-stage)               |
| `eng-dev-growth`       | [Growth Stage](https://about.gitlab.com/handbook/product/product-categories/#growth-stage)               |
| `eng-dev-enablement`   | [Enablement Stage](https://about.gitlab.com/handbook/product/product-categories/#enablement-stage)       |


## GitLab Department Group (`gl_dept_group`)

This label/tag is required.  
{: .alert .alert-success}

```
gl_dept_group: eng-support-americas
```

For Engineering Development (`eng-dev`) department groups, the product stage slug (`gl_product_stage`) is used as the prefix for the `gl_dept_group` value. For all other departments, the `gl_dept` slug is used as the prefix.

All departments or stages have a default `shared-infra` label/tag/AWS account/GCP project that can be used when a separately distinguished/functional group is not needed. For groups with heavy infrastructure usage, we use the group name as a suffix and provide an isolated AWS account/GCP project for group team members to use.

For the groups that provide a shared service to other departments at GitLab, we also have a `shared-services` group value that can be used for shared cost attributions. We use `shared-infra` for our own team's resources and `shared-services` for everyone else's resources that we manage.

You can get an editable version of this table in the [spreadsheet](https://docs.google.com/spreadsheets/d/1adgn5CLB4DdhpoG3TnFsOmeSYg8n8Bvl_g7GFPEl8vs/edit#gid=26160192) that we used to design this schema, however recent changes may not be reflected and this handbook page is the SSOT.

### Expected Values

If a group listed below does not have a group documentation link, it is safe to assume that a AWS account or GCP project has not been created for that group yet. Please follow the instructions for provisioning the group (TODO).
{: .alert .alert-warning}

<!-- To add group documentation, please add a link to a new page [Group Documentation](/handbook/infrastructure-standards/realms/{realm_name}/groups/{gl_dept_group}) -->

| gl_realm        | gl_dept                  | gl_product_stage                  | gl_dept_group                        | Group Documentation |
|-----------------|--------------------------|-----------------------------------|--------------------------------------|---------------------|
| eng-dev         | eng-dev                  | eng-dev-manage                    | eng-dev-manage-shared-infra          | |
| eng-dev         | eng-dev                  | eng-dev-manage                    | eng-dev-manage-access                | |
| eng-dev         | eng-dev                  | eng-dev-manage                    | eng-dev-manage-compliance            | |
| eng-dev         | eng-dev                  | eng-dev-manage                    | eng-dev-manage-import                | |
| eng-dev         | eng-dev                  | eng-dev-manage                    | eng-dev-manage-analytics             | |
| eng-dev         | eng-dev                  | eng-dev-plan                      | eng-dev-plan-shared-infra            | |
| eng-dev         | eng-dev                  | eng-dev-plan                      | eng-dev-plan-project-mgmt            | |
| eng-dev         | eng-dev                  | eng-dev-plan                      | eng-dev-plan-portfolio-mgmt          | |
| eng-dev         | eng-dev                  | eng-dev-plan                      | eng-dev-plan-certify                 | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-shared-infra          | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-source-code           | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-knowledge             | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-static-site-editor    | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-editor                | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-gitaly                | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-gitter                | |
| eng-dev         | eng-dev                  | eng-dev-create                    | eng-dev-create-ecosystem             | |
| eng-dev         | eng-dev                  | eng-dev-verify                    | eng-dev-verify-shared-infra          | |
| eng-dev         | eng-dev                  | eng-dev-verify                    | eng-dev-verify-ci                    | |
| eng-dev         | eng-dev                  | eng-dev-verify                    | eng-dev-verify-runner                | |
| eng-dev         | eng-dev                  | eng-dev-verify                    | eng-dev-verify-testing               | |
| eng-dev         | eng-dev                  | eng-dev-package                   | eng-dev-package-shared-infra         | |
| eng-dev         | eng-dev                  | eng-dev-package                   | eng-dev-package-package              | |
| eng-dev         | eng-dev                  | eng-dev-release                   | eng-dev-release-shared-infra         | |
| eng-dev         | eng-dev                  | eng-dev-release                   | eng-dev-release-progressive-delivery | |
| eng-dev         | eng-dev                  | eng-dev-release                   | eng-dev-release-release-mgmt         | |
| eng-dev         | eng-dev                  | eng-dev-configure                 | eng-dev-configure-shared-infra       | |
| eng-dev         | eng-dev                  | eng-dev-configure                 | eng-dev-configure-configure          | |
| eng-dev         | eng-dev                  | eng-dev-monitor                   | eng-dev-monitor-shared-infra         | |
| eng-dev         | eng-dev                  | eng-dev-monitor                   | eng-dev-monitor-apm                  | |
| eng-dev         | eng-dev                  | eng-dev-monitor                   | eng-dev-monitor-health               | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-shared-infra          | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-static-analysis       | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-dynamic-analysis      | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-composition-analysis  | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-fuzz-testing          | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-threat-insights       | |
| eng-dev         | eng-dev                  | eng-dev-secure                    | eng-dev-secure-research              | |
| eng-dev         | eng-dev                  | eng-dev-defend                    | eng-dev-defend-shared-infra          | |
| eng-dev         | eng-dev                  | eng-dev-defend                    | eng-dev-defend-container-security    | |
| eng-dev         | eng-dev                  | eng-dev-defend                    | eng-dev-defend-insider-threats       | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-shared-infra          | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-acquisition           | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-conversion            | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-expansion             | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-retention             | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-fulfillment           | |
| eng-dev         | eng-dev                  | eng-dev-growth                    | eng-dev-growth-telemetry             | |
| eng-dev         | eng-dev                  | eng-dev-enablement                | eng-dev-enablement-shared-infra      | |
| eng-dev         | eng-dev                  | eng-dev-enablement                | eng-dev-enablement-distribution      | |
| eng-dev         | eng-dev                  | eng-dev-enablement                | eng-dev-enablement-geo               | |
| eng-dev         | eng-dev                  | eng-dev-enablement                | eng-dev-enablement-memory            | |
| eng-dev         | eng-dev                  | eng-dev-enablement                | eng-dev-enablement-search            | |
| eng-dev         | eng-dev                  | eng-dev-enablement                | eng-dev-enablement-database          | |
| eng-infra       | eng-infra                |                                   | eng-infra-shared-infra               | |
| eng-infra       | eng-infra                |                                   | eng-infra-shared-services            | |
| eng-infra       | eng-infra                |                                   | eng-infra-analytics                  | |
| eng-infra       | eng-infra                |                                   | eng-infra-scalability                | |
| eng-infra       | eng-infra                |                                   | eng-infra-deliverability             | |
| eng-infra       | eng-infra                |                                   | eng-infra-reliability                | |
| eng-dev         | eng-quality              |                                   | eng-quality-shared-infra             | |
| eng-dev         | eng-quality              |                                   | eng-quality-ops-ci-cd                | |
| eng-dev         | eng-quality              |                                   | eng-quality-secure-enablement        | |
| eng-dev         | eng-quality              |                                   | eng-quality-productivity             | |
| eng-dev         | eng-quality              |                                   | eng-quality-growth-defend            | |
| eng-security    | eng-security             |                                   | eng-security-shared-infra            | |
| eng-security    | eng-security             |                                   | eng-security-shared-services         | |
| eng-security    | eng-security             |                                   | eng-security-ops-red                 | |
| eng-security    | eng-security             |                                   | eng-security-ops-incident-response   | |
| eng-security    | eng-security             |                                   | eng-security-ops-trust-safety        | |
| eng-security    | eng-security             |                                   | eng-security-risk-compliance         | |
| eng-security    | eng-security             |                                   | eng-security-eng-app-sec             | |
| eng-security    | eng-security             |                                   | eng-security-eng-automation          | |
| eng-security    | eng-security             |                                   | eng-security-eng-research            | |
| eng-support     | eng-support              |                                   | eng-support-shared-infra             | |
| eng-support     | eng-support              |                                   | eng-support-saas                     | |
| eng-support     | eng-support              |                                   | eng-support-self-managed             | |
| eng-support     | eng-support              |                                   | eng-support-americas                 | |
| eng-support     | eng-support              |                                   | eng-support-emea                     | |
| eng-support     | eng-support              |                                   | eng-support-apac                     | |
| eng-dev         | eng-ux                   |                                   | eng-ux-shared-infra                  | |
| eng-dev         | eng-ux                   |                                   | eng-ux-technical-writing             | |
| eng-dev         | eng-ux                   |                                   | eng-ux-research                      | |
| business-ops    | ga-accounting            |                                   | ga-accounting-shared-infra           | |
| business-ops    | ga-business-ops          |                                   | ga-business-ops-shared-infra         | |
| business-ops    | ga-business-ops          |                                   | ga-business-ops-shared-services      | |
| business-ops    | ga-business-ops          |                                   | ga-business-ops-operations           | |
| business-ops    | ga-business-ops          |                                   | ga-business-ops-data                 | |
| business-ops    | ga-business-ops          |                                   | ga-business-ops-systems              | |
| business-ops    | ga-ceo                   |                                   | ga-ceo-shared-infra                  | | 
| business-ops    | ga-finance               |                                   | ga-finance-shared-infra              | |
| business-ops    | ga-legal                 |                                   | ga-legal-shared-infra                | |
| business-ops    | ga-people                |                                   | ga-people-shared-infra               | |
| business-ops    | ga-recruiting            |                                   | ga-recruiting-shared-infra           | |
| business-ops    | mktg-awareness           |                                   | mktg-awareness-shared-infra          | | 
| business-ops    | mktg-brand-design        |                                   | mktg-brand-design-shared-infra       | | 
| business-ops    | mktg-campaigns           |                                   | mktg-campaigns-shared-infra          | |
| business-ops    | mktg-communications      |                                   | mktg-communications-shared-infra     | |
| business-ops    | mktg-community           |                                   | mktg-community-shared-infra          | |
| business-ops    | mktg-content             |                                   | mktg-content-shared-infra            | | 
| business-ops    | mktg-digital             |                                   | mktg-digital-shared-infra            | |
| business-ops    | mktg-field               |                                   | mktg-field-shared-infra              | |
| business-ops    | mktg-inbound             |                                   | mktg-inbound-shared-infra            | |
| business-ops    | mktg-ops                 |                                   | mktg-ops-shared-infra                | |
| business-ops    | mktg-events              |                                   | mktg-events-shared-infra             | | 
| business-ops    | mktg-partner             |                                   | mktg-partner-shared-infra            | |
| business-ops    | mktg-sales-dev           |                                   | mktg-sales-dev-shared-infra          | |
| business-ops    | mktg-strategic           |                                   | mktg-strategic-shared-infra          | |
| business-ops    | mktg-strategic           |                                   | mktg-strategic-technical-mktg        | |
| eng-dev         | product-mgmt             |                                   | product-mgmt-shared-infra            | |
| business-ops    | sales-alliances          |                                   | sales-alliances-shared-infra         | |
| sales-cs        | sales-channel            |                                   | sales-channel-shared-infra           | |
| business-ops    | sales-commercial         |                                   | sales-commercial-shared-infra        | |
| sales-cs        | sales-cs                 |                                   | sales-cs-shared-infra                | |
| sales-cs        | sales-cs                 |                                   | sales-cs-demo-cloud                  | |
| sales-cs        | sales-cs                 |                                   | sales-cs-training-cloud              | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-shared-infra             | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-us-west                  | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-us-east                  | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-pub-sec                  | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-mid-market               | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-emea                     | |
| sales-cs        | sales-cs                 |                                   | sales-cs-sa-apac                     | |
| sales-cs        | sales-cs                 |                                   | sales-cs-tam-shared-infra            | |
| sales-cs        | sales-cs                 |                                   | sales-cs-tam-us-west                 | |
| sales-cs        | sales-cs                 |                                   | sales-cs-tam-us-east                 | |
| sales-cs        | sales-cs                 |                                   | sales-cs-tam-pub-sec                 | |
| sales-cs        | sales-cs                 |                                   | sales-cs-tam-emea                    | |
| sales-cs        | sales-cs                 |                                   | sales-cs-tam-apac                    | |
| sales-cs        | sales-cs                 |                                   | sales-cs-ps-shared-infra             | |
| sales-cs        | sales-cs                 |                                   | sales-cs-ps-consulting               | |
| sales-cs        | sales-cs                 |                                   | sales-cs-ps-education                | |
| sales-cs        | sales-cs                 |                                   | sales-cs-ps-pub-sec                  | |
| business-ops    | sales-ent                |                                   | sales-ent-shared-infra               | |
| business-ops    | sales-field-ops          |                                   | sales-field-ops-shared-infra         | |
| business-ops    | sales-practice-mgmt      |                                   | sales-practice-mgmt-shared-infra     | |

## Resource Type (`gl_resource_type`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_resource_type: compute-instance
```

GCP doesn't support easy reporting based on type of resource and name unless you use labels. This is optional, but recommended for resources that cost a significant amount of money or are part of a production service. This is not recommended for sandbox and ephemeral use cases.

### Expected Values

| Value                  | Recommended Usage |
|------------------------|---------------------------------------------------------------------------|
| `compute-cluster`      | AWS EKS, GCP Kubernetes Engine (GKE) cluster                              |
| `compute-container`    | AWS ECS                                                                   |
| `compute-instance`     | AWS EC2 instance, GCP Compute Engine instance                             |
| `serverless`           | AWS Lambda, GCP AppEngine                                                 |
| `storage-disk`         | Persistent Storage Disks for instances                                    |
| `storage-snapshot`     | (Placeholder for discretionary usage, not easy to auto label/tag)         |
| `storage-bucket`       | AWS S3, GCP Google Cloud Storage (GCS)                                    |
| `network`              | AWS VPC, GCP Network/VPC                                                  |
| `network-lb`           | AWS ELB                                                                   |
| `network-nat`          | AWS NAT                                                                   |
| `network-firewall`     | Firewall rules                                                            |
| `network-ip`           | External IP addresses                                                     |
| `network-bandwidth`    | (Placeholder for discrentionary usage)                                    |
| `database`             | AWS RDS, AWS Aurora, GCP CloudSQL, etc.                                   |
| `queue`                | AWS ElastiCache, MQ, SQS, GCP CloudTasks, etc.                            |
| `logging`              | (Placeholder for discretionary usage)                                     |

## Resource Name (`gl_resource_name`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_resource_name: prod-app1-web1
```

The value of this key should match the name of the resource in the cloud console.

GCP doesn't support easy reporting based on type of resource and name unless you use labels. This is optional, but recommended for resources that cost a significant amount of money or are part of a production service. This is not recommended for sandbox and ephemeral use cases.

## Resource Host (`gl_resource_host`)

This label/tag is optional.  
{: .alert .alert-info}

```
gl_resource_host: prod-app-web1
```

This is used for associating child resources (disks, snapshots, buckets, network IPs, etc) with the parent resource (ex. `compute-instance`) to show the aggregate costs of the resource.

The value of this key should match the name of the parent resource in the cloud console.

GCP doesn't support easy reporting based on type of resource and name unless you use labels. This is optional, but recommended for resources that cost a significant amount of money or are part of a production service. This is not recommended for sandbox and ephemeral use cases.

## Accounting and Financial Reporting

In alignment with our [transparency value](https://about.gitlab.com/handbook/communication/#not-public), financial information cannot be shared publicly. Team members can see the details of how labels and tags impact financial reporting in this [issue](https://gitlab.com/gitlab-com/compute-sandbox/issue-tracking/-/issues/3#impact-to-accounting-and-financial-reporting). The cost allocation methodology for production environments that in this [document](https://docs.google.com/document/d/1p4pzquEZjXRZfcdgSUQZ2Kw988o3sdknq5ZQVxtGAkw/edit?usp=sharing).

## Impact to Business Owners and Infrastructure Team

The largest impact of the label and tag schema is known owner and department identification for every resource provisioned in each cloud provider, and cross-reference to the Terraform configuration that can be referenced during infra/security review.

There are significant cost savings possible with the ability to set time limits on resources that solve the abandoned infrastructure problem. We can also save up to 65% of spending by implementing automation to power off infrastructure during non-working hours (overnight and weekends).

## Impact to Users and Managers

With the label and tags, we can easily report on infrastructure and help you understand what's running and help you self manage the costs of the resources that you provision.

Since most labels and tags will be automatically added with Terraform and automation, or at the account/project level for sandbox accounts, there is not a significant burden on users to remember to add labels/tags to resources.

With future automation, we can also create frictionless experience for users with notification of system vulnerabilities, security incidents, and friendly reminders in Slack about upcoming expiration of infrastructure since your email, GitLab username, and Slack ID are automatically associated.
