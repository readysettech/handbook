---
layout: handbook-page-toc
title: "Version Production Architecture"
---

The version service is hosted in Google Cloud on a Kubernetes cluster.
Version is used to store available GitLab versions as well as if it contains a vulnerability,
render version check badge for self-hosted GitLab instances, and collect data sent during version check
and usage ping from self-hosted instances.

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Architecture
{: #infra-prod-environment}

We are running the version.gitlab.com on Kubernetes and use Auto DevOps for managing deployments The application runs on multiple pods. Google Cloud SQL with PostgreSQL is used by the pods to store data, Cloud SQL has two replicas configured. Google Cloud Memorystore is used as a cache store.

### Production environment
{: #infra-prod-components}

<img src="/images/handbook/engineering/infrastructure/production-architecture/version-gitlab-com-arch.png">

[Source](https://drive.google.com/file/d/1_ESP2-hT0giqIEHYiY6ZtzAcJMk7cnk1/view?usp=sharing), GitLab internal use only

