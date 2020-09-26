---
layout: handbook-page-toc
title: "Trusted Data Framework"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .toc-list-icons .hidden-md .hidden-lg}

## Overview

`This page contains forward-looking content and may not accurately reflect current-state or planned feature sets or capabilities.`

Please see the [Trusted Data Framework](/handbook/business-ops/data-team/platform/#tdf) section of our Data Platform page for the current implementation.

## Trusted Data Dashboard

The Trusted Data Dashboard is used to quickly evaluate the health of the Data Warehouse. The most important data is presented in a simple business-friendly way with clear color-coded content for test PASS or FAIL status.

![Trusted Data Dashboard](/handbook/business-ops/data-team/direction/trusted-data/trusted_data_dashboard.png)

## Test Run

A Test Run is when the collection of Test Cases are executed. Typically, Test Runs will be executed daily. Test Runs can also be useful for:

- testing data quality BEFORE and AFTER a major or critical schema deployment (A/B testing)
- establishing a quality baseline before executing a large [SQL Data Manipulation Language](https://en.wikipedia.org/wiki/Data_manipulation_language) (DML) operation

| Test Run Type         | Purpose                                                                                         |
| --------------------- | ----------------------------------------------------------------------------------------------- |
| Daily Validation      | Run a nightly Test Run to ensure all data passes validation.                                    |
| Release Validation    | Execute a Test Run prior to a major DML or DDL change AND after the change and compare results. |
| Spot-Check Validation | Execute a subset of Test Cases to validate a specific subject area.                             |
