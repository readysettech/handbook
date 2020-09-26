---
layout: handbook-page-toc
title: "Data Team CI Jobs"
description: "GitLab Data Team CI Jobs"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .toc-list-icons .hidden-md .hidden-lg}

{::options parse_block_html="true" /}

---

This page documents the CI jobs used by the data team in Merge Requests.

## Stages

CI jobs are grouped by stages.

### ❄️ Snowflake

#### clone_analytics

Runs automatically when the MR opens to be able to run any dbt jobs. Subsequent runs of this job will be fast as it only verifies if the clone exists. This is an empty clone of the analytics db.

#### clone_analytics_real

Run this if you need to do a real clone of the analytics warehouse. This is a full clone of the db.

#### clone_raw

Run this if you need to run extract, freshness, or snapshot jobs. Subsequent runs of this job will be fast as it only verifies if the clone exists.

#### force_clone_both

Run this if you want to force refresh both raw and analytics.

### 🚂 Extract

#### boneyard_sheetload

Run this if you want to test a new boneyard sheetload load. This requires the real analytics clone to be available.

#### sheetload

Run this if you want to test a new sheetload load. This requires the RAW clone to be available.

#### pgp_test

Run this if you're adding or updating a postgres pipeline manifest. Requires a clone of RAW and the `MANIFEST_NAME` variable, possibly `TASK_INSTANCE` variable if it's an SCD table.

### ⚙️ dbt Run

> As part of a DBT Model Change MR, you need to trigger a pipeline job to test that your changes won't break anything in production. To trigger these jobs, go to the "Pipelines" tab at the bottom of this MR and click on the appropriate stage (dbt_run or dbt_misc).

These jobs are scoped to the `ci` target. This target selects a subset of data for the snowplow and version datasets.

Note that job artificats are available for all dbt run jobs. These include the compiled code and the run results.

These jobs run against the primary `RAW` database.

> Most dbt run jobs can be parameterized with a variable specyfing dbt model that requires testing. Watch [this this intro](https://youtu.be/l14N7l-Sco4) to see an example of how to set the variable.
> The variable is a stand-in for any of the examples in [the dbt documentation on model selection syntax](https://docs.getdbt.com/docs/model-selection-syntax#section-specifying-models-to-run).

You can also add `--fail-fast` to the end of the model selection to quickly end the dbt call at the first failure. Read the [dbt docs](https://docs.getdbt.com/reference/commands/run#failing-fast) for more information.

#### specify_model

Specify which model to run with the variable `DBT_MODELS`

#### specify_xl_model

Specify which model to run using an XL warehouse with the variable `DBT_MODELS`

#### specify_exclude

Specify which model to exclude with the variable `DBT_MODELS`

#### specify_xl_exclude

Specify which model to exclude using an XL warehouse with the variable `DBT_MODELS`

This jobs runs against the clone of `RAW`. Requires the `clone_raw` job to have been run.

#### specify_raw_model

Specify a dbt model against the clone of the RAW database.

#### specify_csv_seed

This job tests specific seed file.

Specify seed file with the variable `DBT_MODELS`.

#### specify_snapshot

Specify which snapshot to run with the variable `DBT_MODELS`.
Requires running `clone_raw` beforehand.

### 🛠 dbt Misc

#### all_tests

Runs all of the tests

- Note: it is not necessary to run this job if you've run any of the dbt_run stage jobs as tests are included.

#### data_tests

Runs only data tests

#### freshness

Runs source freshness test (requires RAW clone)

#### periscope_query

This job runs automatically and only appears when `.sql` files are changed. In its simplest form, the job will check to see if any of the currently changed models are queried in Periscope. If they are, the job will fail with a notification to check the relevant dashboard. If it is not queried, the job will succeed.

Current caveats with the job are:

- It will not tell you which dashboard to check
- It is not able to validate tables that are queried with any string interpolation syntax (i.e. `retention_[some_variable]`)
- It is not able to validate if a table is aliased via dbt

##### Explanation

This section explains how the periscope query works.

`git clone -b periscope/master --single-branch https://gitlab.com/gitlab-data/periscope.git --depth 1`

This clones the periscope project.

`git diff origin/$CI_MERGE_REQUEST_TARGET_BRANCH_NAME...HEAD --name-only | grep -iEo "(.*)\.sql" | sed -E 's/\.sql//' | awk -F '/' '{print tolower($NF)}' | sort | uniq > diff.txt`

This gets the list of files that have changed from the master branch (i.e. target branch) to the current commit (HEAD). It then finds (grep) only the sql files and substitutes (sed) the `.sql` with an empty string. Using `awk`, it then prints the lower-case of the last column of each line in a file (represented by $NF - which is the number of fields), using a slash (/) as a field separator. Since the output is directoy/directoy/filename and we make the assumption that most dbt models will write to a table named after its file name, this works as expected. It then sorts the results, gets the unique set, and writes it to a file called diff.txt.

`periscope_check.py`

This recursively searches the entire periscope repo for a string that matches a `from|join` statement from any of the 3 currently queryable schemas. It does some cleaning on files that match and creates a dictionary of table name mapping to all of the files it is referenced in. It then reads in `diff.txt` to do a lookup and write to comparison.txt and matches based on the model name.

`if (( $(cat comparison.txt | wc -l | tr -d ' ') > 0 )); then echo "Check these!" && cat comparison.txt && exit 1; else echo "All good" && exit 0; fi;`

This uses word count (wc) to see how many lines are in the comparison file. If there is more than zero it will print the lines and exit with a failure. If there are no lines it exits with a success.

#### schema_tests

Runs only schema tests

#### snapshots

Runs snapshots (requires RAW clones)

#### specify_tests

Runs specified model tests with the variable `DBT_MODELS`

### 🐍 Python

There are several jobs that only appear when `.py` files have changed. All of them will run automatically on each new commit where `.py` files are present. Otherwise they are unavailable to run. Other jobs are:

#### permifrost_manual

Manual job to do a dry run of [Permifrost](https://gitlab.com/gitlab-data/permifrost/).

#### yaml_validation

Triggered when there is a change to `load/snowflake/roles.yml`. Validates that the YAML is correctly formatted.

### 🛑 Snowflake Stop

#### clone_stop

Runs automatically when MR is merged or closed. Do not run manually.
