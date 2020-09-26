---
layout: markdown_page
title: "Usecase: GitOps"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

#### Who to contact

| Product Marketing | Technical Marketing |
| ---- | --- |
| @williamchia | @csaavedra1 |

# The Market Viewpoint

## The need for GitOps

Modern applications are developed with rapid iteration and run at highly dynamic scale. In an organization with a mature DevOps culture code can be deployed to production hundreds of times per day. Applications can then run under highly dynamic loads from a few users to millions. Modern infrastructure needs to be elastic. Capacity that can be dynamically provisioned and de-provisioned is able to keep pace with load maintaining optimal performance and minimal cost. With the demands made on today's infrastructure it's becoming increasingly crucial manage infrastructure automation with a robust and cohesive methodology.

## What is GitOps?

```
GitOps == IaC + MRs + CI/CD
```
> GitOps is an operational framework that takes DevOps best practices used for application development such as version control, collaboration, compliance, and CI/CD, and applies them to infrastructure automation.

<iframe width="100%" height="500" src="https://www.youtube.com/embed/JtZfnrwOOAw" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


[GitOps](/topics/gitops/) involves managing your IT infrastructure using practices well-known in software development such as version control, code review, and CI/CD pipelines. For example, infrastructure teams that practice GitOps use configuration files stored as code. Similar to how application source code generates the same application binaries every time it's built, GitOps configuration generates the same infrastructure environment every time it is deployed.



* *IaC* - GitOps uses a Git repository as the single source of truth for infrastructure definition. **Infrastructure as Code (IaC)** is the practice of keeping all infrastructure configuration stored as code. The actual desired state may or may not be not stored as code (e.g., number of replicas, pods).
* *MRs* - GitOps uses **Merge Requests (MRs)** as the change mechanism for all infrastructure updates. The MR is where teams can collaborate via reviews and comments and where formal approvals take place. Merge commits to your master(or trunk) branch serve as a change log for auditing and troubleshooting.
* *CI/CD* - GitOps automates infrastructure updates using a Git workflow with Continuous Integration and Continuous Delivery (CI/CD). When new code is merged, the CI/CD pipeline enacts the change in the environment. Any configuration drift, such as manual changes or errors, is overwritten by GitOps automation so the environment converges on the desired state defined in Git. GitLab uses CI/CD pipelines to manage and implement GitOps automation, but other forms of automation such as definitions operators could be used as well.

As with any emerging technology term, "GitOps" isn't strictly defined the same way by everyone across the industry. GitOps emerged in the cloud native community and some definitions restrict GitOps to say "Kubernetes is required to be doing GitOps." GitLab takes a broader approach. We've seen GitLab users and customers applying GitOps principals to all types of infrastructure automation including VMs and containers, as well as Kubernetes clusters.

While many tools and methodologies promise faster deployment and seamless management between code and infrastructure, GitOps differs by focusing on a developer-centric experience. Infrastructure management through GitOps happens in the same version control system as the application development, enabling teams to collaborate more in a central location while benefiting from all the built-in features of Git.

GitOps is a prescriptive workflow for using Infrastructure as Code. GitOps with GitLab helps you manage physical, virtual and cloud native infrastructures (including Kubernetes and serverless technologies) using tight integration with industry-leading infrastructure automation tools like Terraform, AWS Cloud Formation, Ansible, Chef, Puppet, and the like.

### Benefits of GitOps

* *Distribution of work* - Enable more engineers to collaborate on infrastructure changes. Since every change will go through the same change/merge request/review/approval/merge process, this enables senior engineers to focus on other areas beyond the critical infrastructure management while still maintaining the ability to review and contribute as needed.
* *Improved access control* There's no need to give credentials to all infrastructure components since changes are automated only by your CI/CD needs access.
* *Faster time to market* - execution via code is faster than manual point and click, test cases can be automated and hence repeatable in a consistent manner to deliver stable environments rapidly, at scale
* *Less risk* The shift-left approach to infrastructure as Code helps to identify and resolve issues before changes are rolled out to production preempting unexpected downtime and providing higher environment stability and reliability and better user experience.
* *More compliant* All changes to infrastructure are tracked, leaving traceability for audit and ability to rollback to a previous desired state with ease.
* *Reduce costs* - automation of infrastructure definition and testing eliminates manual tasks and rework improving productivity, reduced downtimes due to built in revert/rollback capability
* *Less error prone* - infrastructure definition is codified, hence repeatable and less prone to human error

## Personas

### User Persona
Infrastructure as Code requires understanding of the platform and the desired state of the application environment. Users of Infrastructure as Code have a good understanding of both Git as a SCM tool as well as the platform they are expected to provision and manage. Below are a few power users Infrastructure as Code:

* [Sam, the SRE](/marketing/product-marketing/roles-personas/#site-reliability-engineer)
  Sam works embedded into a service team with feature developers. They works on keeping the service up, deploying it, and managing the infrastruture needs of that service. They collaborate with the Platform team to systamatize best practices.


* [Devon, the DevOps Engineer](/marketing/product-marketing/roles-personas/#devon-devops-engineer)
  Devon is often the Ops interface for the development team. He provides support for infrastructure, environments and integrations. Devon is fairly conversant with code and would prefer administering infrastructure via code rather than a multitude of different tools and context switches.

* [Priyanka, the Platform Operator](/marketing/product-marketing/roles-personas/#priyanka-platform-operator)
  Infrastructure management is one of the main responsibilities of the platform team. [Priyanka](/handbook/marketing/product-marketing/roles-personas/#priyanka-platform-engineer) is responsible for providing, maintaining, and operating a shared platform - either traditional or modern cloud platform  - which the development teams utilize to ship and operate software more quickly.

* [Sydney, the System Administrator](/marketing/product-marketing/roles-personas/#sidney-systems-administrator)
  Sydney defines, maintains and scales the infrastructure and configuration for the application teams. She often receives repetitive requests on the same task. Sydney's primary motivation is to automate repetitive tasks to minimize errors and save time as well as define the infrastructure and configuration in a way that changes are tracked and to stop infrastructure changes becoming the [wild west](https://en.wikipedia.org/wiki/Cowboy_coding).

### Buyer Personas
Buyers of Infrastructure as Code are usually leaders who lead infrastructure / automation initiatives. Typical buyer personas are:
* **CIO / Vice President of IT** - experience in planning, design and execution of digital transformation programs, implementing new operating models. Typically leads both engineering and operations teams
* **Vice President of IT Infrastructure** (also referred to as IT Operations in some organizations) - experience in planning, design and execution of IT infrastructure services - including deploying and managing cloud services, system management and service desk. Frequently has the agenda of reducing IT costs for the organization.
* **Vice President of Platform Engineering** - Managing a shared platform for development teams is one of the main agendas of the Platform Engineering team. The platform team has expertise in new technologies like Kubernetes. Key KPIs of the platform engineering team are Automation, Efficiency and Self Service.

## Analyst Coverage

List key analyst coverage of this usecase


## Market Requirements

Below are the [market requirements](/handbook/marketing/product-marketing/usecase-gtm/#market-requirements) for GitOps

### Foster Collaboration

   - Description: The solution is designed to enable and foster collaboration among team members. The collaboration system includes manual gates and approvals as well as automated workflows.
   - Typical features:
     - Add a general comment
     - Tag individuals or groups 
     - Add an inline comment on code
     - Add a suggestion
     - Show the total unresolved threads at the tops
     - Show you can’t merge until you resolve comments/suggestions
     - Resolve a thread
     - Resolve a thread by creating a new issue
     - Apply a suggestion (accept a suggestion)
     - Show codeowners
     - Show approval

  Other features
     - Quickly create new branches of a project
     - Add new files/assets
     - Collaborate on proposed changes (review comments, suggest changes, WebIDE, suggestion approvals, conflict resolution, merge, diffing, hand-offs)
     - Workflow automation
     - Wiki snippets
     - Version-controlled snippets
     - Automatically update or close related issue(s) when a merge request is merged
     - Configurable issue closing pattern
     - Display merge request status for builds in CI system
     - Terraform plan output
     - Visibility into security scans and build stats
   - Value: Quality of the code changes being made increases which leads to
        - greater accuracy of fulfilled requests
        - greater infrastruture stability
        - and improved release velocity
        through team review and validation.

### Compliance and Auditing

   - Description: All changes to production are automated and gated by merging to a Git branch. Permission and access are built-in via the Git management tool.
        Approvals and merge access can be restricted to certain personnel or groups.
        Commit history shows the log of changes.
   - Typical Features: CMRs/PRs, code review features, RBAC, branch permissions, group permission setting, CodeOwners, MR approvals
   - Value: Don't have to manage separate permissions for your infrastructure; they can match that of your development process.
        Strong adherence to internal and regulatory compliance standards.
        Audits take less time and are easier to conduct.
        Changes to infra are more secure because they are locked down.
        \

### Version controlled environements 

- Description: Ability to roll back and roll forward your environements when their state is definine via text stored under Git version control. 


### Test Automation

   - Description: Run and manage automated tests and validate changes before they're merged to production. This includes everything from basic to more in-depth tests and extends test automation into areas of functional, system, performance testing, and more. Ensure software is consistently tested to meet both technical and business requirements without manual intervention, enabling developers to get rapid feedback if their code changes introduce potential defects or vulnerabilities.
   - Typical Features: The ability to run automated tests in CI/CD pipelines in isolated and ephemeral environments. Various tests may include (but aren't limited to) unit testing, code integration testing, regression testing, static code analysis, functional testing, and accessibility testing. **Most types of testing for app code also apply to any type of code (infra, policy, etc.)**.
   - Value: Catch potential errors sooner, rather than later- before they impact production.
Increase security by testing for potential vulnerabilities, before going to production.

### Pipeline configuration management

   - Description: Engineers can automate the build and test workflow, specifically connecting to their source code repository, defining specific actions/tasks in build pipelines, and set parameters for exactly how/when to run jobs, using scripts and/or a GUI to configure pipeline changes. Configurations are repeatable and traceable to allow for quick comparisons and tracking of changes to environments.
   - Typical Features: Configurations via web UI or supports config-as-code in a human readable syntax, like YAML.
      Pipeline templates. Project Templates.
      Pipeline linking - store pipeline template in central repo
      Pipeline dependancy - child/parent, upstream/downstream
   - Value: Maximize development time and improves productivity. Less manual work.
      Centralize management to lower adminstration.
      Increase consistency by using the templates to adhere to best practices and required testing.


# The GitLab Solution

## How GitLab Meets the Market Requirements

A collection of short demonstrations that show GitLab's GitOps capabilities.

| Market Requirements | How GitLab Delivers | GitLab **Stage**/Category | Demos |
| ------ | ------ | ------ | ------ | ----
| Foster Collaboration | Discussions, user tagging, general comments, inline comments, inline suggestions, unresolved thread tracking, issue creation from comment, suggestion management, CODEOWNERS, approvals |  [Discussions](https://docs.gitlab.com/ee/user/discussions/), [CODEOWNERS](https://docs.gitlab.com/ee/user/project/code_owners.html), [MR approvals](https://docs.gitlab.com/ee/user/project/merge_requests/merge_request_approvals.html) | [![Foster Collaboration with GitOps](../../images/youtube_social_icon_red-32x23.png) Foster Collaboration with GitOps](https://youtu.be/onFpj_wvbLM) |

## Top 3 Differentiators

| Differentiator | Value | Proof Point  |
|-----------------|-------------|---------------|
|  abc  | def | ghi  |


## [Message House](./message-house/)

The message house (coming soon) for the use case provides a structure to describe and discuss the value and differentiators for the use case.

Current messaging can be found in the [market viewpoint](#the-market-viewpoint) section for this page and on the topic page which answers [What is GitOps?](/topics/gitops/).

### Discovery Questions
- list key discovery questions


## Competitive Comparison
TBD - will be a comparison grid leveraging the capabilities

### Industry Analyst Relations (IAR) Plan
- The IAR Handbook page has been updated to reflect our plans for [incorporating Use Cases into our analyst conversations](/handbook/marketing/product-marketing/analyst-relations/#how-we-incorporate-use-cases-into-our-industry-analyst-interactions).
- For  details specific to each use case, and in respect of our contractual confidentiality agreements with Industry Analyst firms, our engagement plans are available to GitLab team members in the following protected document: [IAR Use Case Profile and Engagement Plan](https://docs.google.com/spreadsheets/d/14UthNcgQNlnNfTUGJadHQRNZ-IrAe6T7_o9zXnbu_bk/edit#gid=1124037301).

For a list of analysts with a current understanding of GitLab's capabilities for this use case, please reach out to Analyst Relations via Slack (#analyst-relations) or by submitting an [issue](https://gitlab.com/gitlab-com/marketing/product-marketing/issues/new) and selecting the "AR-Analyst-Validation" template.

## Proof Points - customers

### Quotes and reviews
- [Video: kiwi.com on Infrastructure as Code](https://www.youtube.com/watch?v=Un2mJrRFSm4) - Learn how kiwi.com uses GitLab and Terraform to manage their infrastructure as code. Bonus info - see how they deploy self hosted gitlab instance from gitlab CI/CD and Infrastructure as Code
- [Video: VMware - Infrastructure as Code with GitLab and Terraform Cloud](https://www.youtube.com/watch?v=qXj4ShQZ4IM) - GitLab and Terraform have worked well together for some time; Learn how VMware uses GitLab CI/CD and Terraform Cloud to manage infrastructure as code
- [Video: ValidaTek's journey of DevOps and Infrastructure as code](https://www.youtube.com/watch?v=3uZE-ktP2Pc) - ValidaTek work with all areas of the US Federal government from civilian to military to IC. See how they's set up GitLab to manage their client's infrastruture.

#### Gartner Peer Insights

"Very efficient tool for managing releases and versions. We have a development and deployment process, and at all stages [GitLab] is involved. In addition to storing development code, we also store all packaging and deploy scripts in git"
> * Full-stack Developer, [Gartner Peer Insights Review](https://www.gartner.com/reviews/market/application-release-orchestration-solutions/vendor/gitlab/product/gitlab/review/view/1112407)

"Finally, the most amazing thing about GitLab is how well integrated the GitLab ecosystem is. It covers almost every step of development nicely, from the VCS, to CI, and deployment."
> * Software Engineer, [Gartner Peer Insights Review](https://www.gartner.com/reviews/market/application-release-orchestration-solutions/vendor/gitlab/product/gitlab/review/view/1038051)

"GitLab is the most preferred service in the world and its user community is very wide. We can authorize project or branch based user authorization on Gitlab. In addition, continuous deployment integrations can be done very quickly. In addition, you can create merge requests within the constraints you want and easily manage them. It is very easy to prevent conflicts. A service that must be used for software development teams."
>* Software Development Lead, [Gartner Peer Insights Review](https://www.gartner.com/reviews/market/application-release-orchestration-solutions/vendor/gitlab/product/gitlab/review/view/1324677)

### Case Studies

-**[Northwestern Mutual](https://www.youtube.com/watch?v=yw7N82mXmZU)**
* **Problem**  Manual processes, provisioning of resources from On-Prem Datacenters created inefficient practices.
* **Solution** GitLab Premium (SCM,CI) and Terraform
* **Result** Drastically improved lead time to production, Environments can be created in under an hour. Everything is done as code and there are no risks from patching.
* **Sales Segment:** Enterprise

-**[Wag Labs](https://about.gitlab.com/blog/2019/01/16/wag-labs-blog-post/)**
* **Problem** Lack of control complex CI toolchain.
* **Solution** GitLab Ultimate (SCM,CI,CD) and Terraform
* **Result** It's so easy to deploy something and roll it back if there's an issue. It's taken the stress and the fear out of deploying into production.
* **Sales Segment:** Mid-Market

### References to help you close
- Find customers that are [using GitLab with GitOps](https://docs.google.com/spreadsheets/d/1j31jz71BBMM-8IPHZWUzi8IogYq2m-VhyofzJmd3wk8/edit?usp=sharing)

## Partners
GitLab is not a replacement for existing Infrastructure Automation tools, but rather complements them to provide a comprehensive solution. As per the [JetBrains DevOps Ecosystem 2019](https://www.jetbrains.com/lp/devecosystem-2019/devops/) survey, **Terraform** is the most popular infrastructure provisioning tool used by customers. Terraform is cloud-agnostic and helps manage complex infrastructures for distributed applications. GitLab will [focus on Terraform support](/direction/configure/infrastructure_as_code/#whats-next) as the first step towards building a comprehensive GitOps solution.

## Resources
### Presentations
* GitOps Industry Talk - What is GitOps? Why is it important? How can you get started? - [slide deck](https://docs.google.com/presentation/d/18cuZjvkMT8uv241dqJZMdaWOyvZiwBOzFvRZ4HaP1iE/edit), [video](https://www.youtube.com/watch?v=JtZfnrwOOAw)

### WebPage, Whitepapers, infographics, blogs
* [What is GitOps?](/topics/gitops/)
* [Infrastructure as Code using GitLab & Ansible](/blog/2019/07/01/using-ansible-and-gitlab-as-infrastructure-for-code/)
* [Part 1 of 3: Why collaboration technology is critical for GitOps](/blog/2019/11/04/gitlab-for-gitops-prt-1/)
* [Part 2 of 3: How infrastructure teams use GitLab and Terraform for GitOps](/blog/2019/11/12/gitops-part-2/)
* [Part 3 of 3: How to deploy to any cloud using GitLab for GitOps](/blog/2019/11/18/gitops-prt-3/)

### Videos (including basic demo videos)
* [What is GitOps? Why is it important? How can you get started?](https://www.youtube.com/watch?v=JtZfnrwOOAw)
* [What is Infrastructure as Code](https://www.youtube.com/watch?v=zWw2wuiKd5o)
* [Infrastructure as Code using GitLab & Ansible](https://youtu.be/M-SgRTKSeOg)
* [Part 1 of 3: How GitLab supports GitOps: The Process](https://www.youtube.com/watch?v=wk7YAXijIZI)
* [Part 2 of 3: How GitLab supports GitOps: The Infrastructure](https://www.youtube.com/watch?v=5rqoLj8N5PA)
* [Part 3 of 3: How GitLab supports GitOps: The Application](https://www.youtube.com/watch?v=heQ1WY_08Tc)
* [GitOps with GitLab and Terraform](https://www.youtube.com/watch?v=G7JOjI6V3AY)
* [Using GitLab for GitOps to break down silos and encourage collaboration](https://www.youtube.com/watch?v=5ykRuaZvY-E)

### Clickthrough & Live Demos
* [GitOps Click Through Demo](https://drive.google.com/open?id=1UT32lLvXtwAslkK7o8asbko3a231WKrjmlcM0z9coPw)

## Buyer's Journey
Inventory of key pages in the buyer's Journey

| **Awareness** <br> learning about the problem  |  **Consideration** <br> looking for solution ideas  |  **Decision** <br> is this the right solution|
| ------ | -------- |-------- |
| [topic page?]()  | [solution page]() | [proof points]() |
| [landing pages?]() | ?comparisons?  | [comparisons]() |
| -etc?            |   |  - [product page x]() <br>  - [product page y]() <br>  - [product page z]() |
