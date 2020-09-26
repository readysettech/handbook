---
layout: handbook-page-toc
title: "Gemnasium Service Production Architecture"
---

The Gemnasium service used in Dependency Scanning is hosted in Google Cloud on a Kubernetes cluster.

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Architecture
{: #infra-prod-environment}

We are running the Gemnasium service on Kubernetes. The application runs on multiple pods which communicate through a NSQ service. The needed PostgreSQL DB
is provided by a Google Cloud SQL instance. The "web" pods receive HTTPS traffic directly, they serve API endpoints and a web UI.

### Production environment
{: #infra-prod-components}

<img src="https://docs.google.com/drawings/d/e/2PACX-1vQDDKfZsuynorz64THC4TCDbRd0LhBxIX3B9DhFbh8CMiqHnbv3lk2Q4gJl0mfF1i-_nWLxb2f7Nh0b/pub?w=1566&h=1035">

[Source](https://docs.google.com/drawings/d/1A7Uw4hVC1US_I6nEY79_mIyX1dnBegKyLhKjGkf70Mc/edit), GitLab internal use only

### High level component view
{: #infra-prod-components}

<img src="https://docs.google.com/drawings/d/e/2PACX-1vRENZDwgciEb5lwATJrT9QKdW2ss_vu-1CQPPMah66mZqJMfgrRy_BNCw4WXKLC8IHCsjq40axN_65b/pub?w=1527&h=1121">

[Source](https://docs.google.com/drawings/d/1AJ21B-6zgJAF_g8L_dhbdRtIuZ2XCSA1pY0f0u-Z9kQ/edit), GitLab internal use only


### Pods Definition
{: #infra-proposed-archi-pods}

<img src="https://docs.google.com/drawings/d/e/2PACX-1vSu_DTqRC6FzproU3SUOZRaxS0ySo27h4IOZAqwTVHTiRtr9fLA74OL8sbLoOioXxwp1apucZK7Nsq-/pub?w=1201&h=807">

[Source](https://docs.google.com/drawings/d/1pSC4Y1rQeNNLVk9iudBjn0J6gY9QTBC7FAzaae3SpMI/edit), GitLab internal use only

