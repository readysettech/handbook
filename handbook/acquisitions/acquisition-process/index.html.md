---
layout: handbook-page-toc
title: "Acquisition Process"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

This is a detailed view of our acquisition process. For more information about
our acquisitions approach visit our [acquisitions handbook](/handbook/acquisitions/).

### Acquisitions Deal Funnel

The corporate development team conducts a comprehensive screening of our industry ecosystem in order to identify potential acquisition opportunities. Below is an overview of our target funnel.

| Funnel                                                                                                                                                                  | Volume / Year |
| ----------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------- |
| **Pipeline Building**                                                                                                                                                   |               |
| DevOps ecoystem companies                                                                                                                                               | 15,000+       |
| Sourced Pipeline: generate pipeline of companies operating in a DevOps segment relevant for GitLab from three sources:                                                  | 1,000         |
| _--> 1. Third-party databases_                                                                                                                                          | _800_         |
| _--> 2. Inbound (companies approach us or PMs refer us)_                                                                                                                | _100_         |
| _--> 3. Pro-active (Identify key areas with Product leadership)_                                                                                                        | _100_         |
| Prioritized Pipeline                                                                                                                                                    | 400           |
| _--> Review funding status, headcount and headquarters location_                                                                                                        |               |
| _--> Prioritize potential softlanding deals (&lt;$1M deal consideration) in countries without GitLab hiring restrictions_                                               |               |
| _--> Prioritize by product priority_                                                                                                                                    |               |
| **Exploratory**                                                                                                                                                         |               |
| Reach out for intro calls                                                                                                                                               | 400           |
| Intro calls with priority targets                                                                                                                                       | 300           |
| Qualified Pipeline: Share relevant call summary with product management lead to confirm interest in setting up initial call between product management lead and company | 100           |
| Product and Tech Call                                                                                                                                                   | 50            |
| **Early diligence**                                                                                                                                                     |               |
| Early Diligence, Team Interviews, Business Case                                                                                                                         | 30            |
| **Confirmatory due diligence**                                                                                                                                          |               |
| Signed Term Sheet / Confirmatory Due Diligence                                                                                                                          | 15            |
| **Integration**                                                                                                                                                         |               |
| Deal Signing, Closing & Integration                                                                                                                                     | 10            |

## Acquisition process

The process is comprised of four key stages:

1. Pipeline Building
1. Exploratory
1. Early Diligence
1. Confirmatory Due Diligence
1. Integration

### Pipeline Building

1. Sourcing: The corporate development team closely collaborates with GitLab's product leadership to identify key areas for potential M&A. We source acquisition opportunities ("Sourced Pipeline") from:
    1. Ecosystem screen with the help of third party databases such as Crunchbase
    1. Inbound introductions from GitLabbers and industry contacts
    1. Proactive outreach to companies aligned with our vision and strategic priorities

### Exploratory

1. We prioritize companies that fit with our product and acquisition priorities ("Prioritized Pipeline") and reach out to their leadership to set up intro calls.
1. Intro calls: The purpose of this 30-min call is to learn more about the potential target company and assess if further acquisition discussions make sense. The agenda for the call is:
    1. Company overview including team, products, financials, and funding
    1. Discuss which features could accelerate GitLab's roadmap
    1. Review the GitLab acquisition process including deal terms, as appropriate ([acquisitions handbook](/handbook/acquisitions/))
    - TARGET TEAM: Ahead of this call please review our [roadmap](/direction/) and outline which of your current and future product features can be implemented into GitLab's product categories. Outline a simple integration timeline for those features, considering an MVC release on the first month after joining GitLab and monthly releases following with quick iterations.
1. Share call summary ([Initial Acquisition Review Template](https://docs.google.com/document/d/1RekjfQj89pIV7DZzeNZ00HYOwqlqlDFm7Gy4yZET9rc/edit?usp=sharing), a GitLab internal document) of companies that are aligned with GitLab's acquisition strategy ("Qualified Pipeline") with relevant product lead.
    - Create a new, private Slack channel (format: `#acq-company_name`) and add the internal GitLab document to the top. Add EVP Product and the relevant product and engineering leaders to help with the initial assessment of the opportunity.
1. Product call: If the Dir. Product sees a potential fit and wants to proceed, set up an initial 60-minute product call to dive into the product and tech. The call must include the Dir. Product and may also include Section Leaders and specific Product Managers relevant to the call. Section Leaders and Product Managers should keep in mind the early stage of this evaluation and attempt to think expansively about how the potential acquisition could be additive to GitLab. The agenda for the call is:
    1. Product demo with highlights on key functionality and technologies
    1. Concise roadmap overview with a focus on near-term plans
    1. [GitLab roadmap](https://about.gitlab.com/direction/) fit - discuss which features could be built into GitLab and into which product stage
    1. Start the discussion about what an integration into GitLab's code base will look like
1. Initial internal review: preliminary assessment of product and technology fit of the potential opportunity to GitLab's [product roadmap](/direction/) as well as integration options into GitLab. If the product lead is supportive of moving forward towards developing a more in depth business case, confirm whether the proposed acquisition can be funded with planned headcount allocations. Otherwise, set up a discussion with EVP Product before proceeding with further diligence.

### Early Diligence

1. Select [code name](#acquisitions-are-confidential) to use instead of target company name. Update Slack channel: `#acq-code_name`.
1. Sign a mutual NDA as linked on our [legal handbook page](/handbook/legal/).
1. [Form the acquisition team](#acquisition-team) and add entire team to the channel and documents.
1. Confirm internal acquisition champion - every acquisition needs a lead champion; someone who is advocating for the acquisition, helping drive the acquisition rationale, and seeing its successful integration. For most acquisitions that fit our [approach](/handbook/acquisitions), the champion will come from GitLab's Product team, at the Director level, accompanied by an engineering champion from the GitLab's Engineering team, at the Director level, respectively. For other acquisitions, champions may come from other internal functions.
1. Preliminary diligence - below is a list of documents to share with GitLab:
    1. Financials:
        1. Balance sheet
        1. Profit and Loss sheet
        1. Cashflow statement
        1. Tax returns
    1. Employees:
        1. Roster with: employee name, title, role, tenure, years of experience, location, salary, LinkedIn profile, programming languages proficiency
        1. Employee resumes
        1. Employee agreements and PIAA
    1. Customer list with name, monthly revenue, contract termination date and any other fields if relevant.
    1. Vendor list with monthly spend
    1. Asset list:
        - Any assets that are needed for the business and will be part of the acquisition
        - Assets excluded from the acquisition
    1. Technical Bill of Materials (BOM) - a complete document which lists:
        1. Repositories
        1. Issue trackers / bug management systems
        1. Additional (non-code) assets
        1. Domain names
        1. Servers
        1. Dependencies
        1. Database schemas
        1. Data
        1. Trademarks
        1. Social media accounts
1. Early technical diligence:
    1. In case the target company has open source components, the respective Dir. Engineering (dependent on GitLab stage) will start an early code review to determine: code quality, development practices, contributions, license compliance and more. That should be turned around within 2-3 business days.
    1. Hands-on product and code screen-share session (2 hours): the technical lead, as assigned by the respective Dir. Engineering, together with the respective Dir. Product will lead a screen-share session aimed at a hands-on validation of the product functionalities and an overview of the code.
    1. Founder technical interviews - founders will go through two rounds of interviews to assess technical and cultural alignment.
1. Resume review - Review of all employee resumes
1. Compensation review to identify any gaps and possible flags led by the HR Business Partner
1. Optional interviews for the key technical employees - to increase the success rate of the deal post-Term Sheet, we recommend conducting interviews for the key technical employees identified before signing the Term Sheet. This will greatly reduce the likelihood of personnel gaps becoming a blocker during the Confirmatory Due Diligence stage. The interviews will include a technical interview and a manager interview as detailed in the Confirmatory Due Diligence stage below.
    1. The key technical employees are those identified as critical to the success of the acquisition, the proposed integration plan and the future of the team at GitLab post integration.
1. Product integration strategy: the GitLab product and engineering acquisition champions will formalize the integration strategy with a focus on feature sets/functionalities:
    1. What we keep as-is
    1. What we reimplement in GitLab
    1. What we discard/EOL
    1. What is critical for user migration
    1. Target [product tiers](/handbook/marketing/product-marketing/tiers/) in GitLab
    1. Barriers for implementation
    1. Deal Milestones:
        1. We aim to set 3 milestones at 2, 4 and 6 months from joining GitLab, to provide a concise set of goals which should cover the bulk of our product interest in the target company
        1. Milestones should be articulated as objectives as opposed to tasks. This will help target companies focus on driving the objectives and not be tied to, and concerned with, a specific task as changes are likely to occur once integration work starts. The milestones outline the objectives to facilitate the work required in achieving the roadmap advancement the deal was identified with delivering.
        1. First milestone shipped within 60 days of joining GitLab:
            1. Accounting for 3 weeks of onboarding, targets will ship the first milestone 5 weeks following the onboarding period
            1. Critical to adopting our culture and successful future integration of the target's engineering team in GitLab
            1. Allows us to show early fruits of the acquisitions soon, aligned with our value of iteration
        1. Integrated within 6 months:
            1. 6 months is an optimal timeframe which allows for incremental integration of the target's functionality, covering its entirety at best or its fudemantals at the very least, while not being overly extended. We would want to refrain from using a longer time frame as our roadmap priorities may change such that we could potentially find ourselves abandoning certain milestones, negating some or all of the rationale behind the deal.
            1. Will help establish focus on both acquired target and our product team
            1. Be able to complete payouts to the target's entity and shut it down sooner
1. To determine the deal ROI, the acquisition team will perform the analysis using the [cost-revenue acquisition calculator](https://docs.google.com/spreadsheets/d/1ke36-mtEi8MhfMKXpYGMRP6H3HH6MimxXt86Zv_QkzM/edit#gid=0) (_internal_ GitLab document). Make a copy of the master cost-revenue acquisition calculator file and save it in the relevant project folder in Google Drive before making changes to the file.
1. Presenting the business case for approvals (by order of occurence):
    1. Champions' approval: The acquisition team will review the business case together and approve the suggested deal. This includes approval of all the following:
        1. Complete executive summary (with link to term sheet draft) including budget and headcount allocation for the acquisition
        1. Complete businees case ([templates](https://docs.google.com/document/d/1RekjfQj89pIV7DZzeNZ00HYOwqlqlDFm7Gy4yZET9rc/edit) for both) including Deal Milestones
        1. Complete term sheet ([template](https://docs.google.com/document/d/1_G2bXxhMe_qXrF8LdZcXwsCcIs1GJAS1-v42U2MV8a4/edit)) draft with proposed details (asset payment, retention bonuses, Deal Milestones, closing schedule, customer termination and closing conditions) filled in.
    1. Functional approvals: The corporate development acquisition lead, Dir. Product and Dir. Engineering will present the business case for acquisition to the EVP Product and EVP Engineering. They will review to approve the items listed in the Champions' approval (complete: executive summary, business case, term sheet)
    1. CEO, CFO and CLO approvals: The corporate development acquisition lead, Dir. Product and Dir. Engineering (deal champions) will present the business case for acquisition to the CEO, CFO and CLO. This meeting will also capture the **explicit approval** of the term sheet to start negotations.
             1. Approval of term sheet to start negotiations will be tracked in a [term
        sheet approval issue](<https://gitlab.com/gitlab-com/corporate-development/issues/new?issuable_template=term_sheet_approval>). We don't include any financial and milestone information in the approval tracking issue for confidentiality reasons.
1. Term Sheet:
    1. Once the terms to start negotations have been approved, the corporate development acquisition lead will reach out to the target company to share the offer and term sheet.
    1. Once an agreement on terms with the target has been reached, the term sheet (with any changes) will be brought forward for approval from: CLO, CFO, CEO (in that order). These approvals will be captured in the term sheet approval issue.
    1. Once all approvals have been obtained, the corporate development acquisition lead will stage the term sheet for signing on HelloSign for target CEO and GitLab CEO (in that order). Add CLO, CFO, and EVP Product on Cc on the agreement.
        1. Approval tracking will be tracked on the term sheet approval issue mentioned earlier. Any changes to previously-approved terms need to be reviewed and approved once more by the following: Dir. Product, Dir. Engineering, EVP Product, EVP Engineering, CLO, CFO, CEO. The changes should be referenced on the term sheet approval tracking issue _before_ seeking approvals.

### Confirmatory Due Diligence

1. To kick-off the Due Diligence stage, the corporate development acquistion lead emails the target company CEO with the following clarifications and information requests:
    1. All employees and their profiles will be reviewed by the GitLab team
    1. The employees who will be invited for interviews will go through GitLab's standard interview process
    1. Key employees who were interviewed during the Early Diligence stage may go through further interview rounds as determined by the GitLab team to qualify for a role at GitLab
    1. All employees must identify an open vacancy at GitLab which they think best matches their professional profile. This will be shared in a spreadsheet gathered by the target's CEO.
1. The acquisition lead will create an engagement debrief and lessons learned document and share it with the team for on-demand capturing of insights.
1. Complete [Technical diligence](acquisition-process-technical-diligence/)
1. Complete financial diligence
1. Legal diligence - Once both the technical and the financial diligence have been completed and signed off by the Dir. Engineering champion and Finance acquisition team member, respectively, the acquisition lead will contact legal to start the legal diligence. Legal will tag the relevant owners for each of the diligence tasks in the [template diligence table](https://docs.google.com/document/d/1RekjfQj89pIV7DZzeNZ00HYOwqlqlDFm7Gy4yZET9rc/edit#bookmark=id.o9gv1rfld9h2)(GitLab internal document) in the main acquisition doc.
1. The progress of the diligence will be synced on a regular stand-up call with the acquisition team
1. The corporate development acquisition lead and the legal lead negotiate the definitive deal documentation with the target company CEO and legal team
1. Final review and approval:
    1. Conclusive call - Final internal review call with the acquisition team to recap the acquisition as a whole, review the acquisition agreement and present a final recommendation. This meeting will also capture the **explicit approval** of the acquisition agreement from the CLO, CFO and CEO. Approvals from the call as well as additional required approvals will be tracked using the definitive agreement approval [issue template](https://gitlab.com/gitlab-com/corporate-development/issues/new?issuable_template=definitive_agreement_approval).
    1. BoD approval:
        1. Legal will facilitate the final deal approval from GitLab's Board of Directors
        1. A board pacakge will be shared with the BoD members before requesting their approval. It should include:
            1. Executive summary email:
                1. Will be sent to the BoD members by the CEO
                1. The Dir. Corp Dev will create a 1-2 page executive summary email message. It should include a high level coverage of the following topics:
                    1. Deal details and rationale (including roadmap acceleration, projected revenue gain)
                    1. Expertise of team joining
                    1. Key terms for the APA and any additional costs
                    1. Diligence conducted: legal, tax, financial, technical, people
                    1. Known risks, indemnification conditions as well as representations and warranties
            1. Link to final version of APA
1. The corporate development acquisition lead will coordinate the signing and closing of the deal

### [Integration](/handbook/acquisitions/acquisition-process/integration/)

The Corporate Development team is responsible for overseeing and facilitating the integration of the acquisition post-closing, working closely with Legal, Product, Engineering, and Finance.

The integration process is outlined in our [acquisition integration page](/handbook/acquisitions/acquisition-process/integration/).

## Acquisition Team

An acquisition team will consist of the following GitLab functional team members:

1. Dir. Corporate Development - acquisition lead
1. Dir. Product Management
1. Product Manager
1. Dir. Engineering
1. Engineering team member
1. Finance team member
1. Director of Tax
1. Principal Accounting Officer
1. Legal team member
1. HR Business Partner
1. People Ops Business Partner
1. Recruiting manager

To assign the product manager, after the product call or as soon as it's clear which product category the features will be implemented into, contact the category product director for the assignment.

To assign the engineering team member, contact the engineering manager of the relevant category for assignment.

### Acquisition Team Responsibilities

| Function                    | Role                                                                                                                                                               | Deliverables                                                                         |
| --------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------ |
| Corporate Development       | 1. Main POC for acquired team 1. Identify potential areas for integration 1. Create case for acquisition and customer transition story 1. Integration              | 1. Business case with deal structure                                                 |
| Product                     | 1. Outline current product features to be implemented into GitLab 1. Outline potential future functionalities to be built into GitLab after the integration period | 1. Integration strategy                                                              |
| Engineering                 | 1. Technical diligence                                                                                                                                             | 1. Code quality review 1. Integration strategy validation - feasibility and timeline |
| Finance                     | 1. Lead financial diligence 1. Validate business case and deal structure                                                                                           |                                                                                      |
| Legal                       | 1. Review entity, assets and existing agreements 1. Evaluate sunset and customer transition path                                                                   | 1. Term Sheet 1. Acquisition agreement                                               |
| People Ops Business Partner | 1. Lead the compensation review 1. Lead the interview process during the early and due diligence stages to completion                                              |                                                                                      |

## Acquisitions Are Confidential

At GitLab, we treat all acquisition discussions as confidential and share any information internally on a need-to-know basis.

To ensure confidentiality during the acquisition process, we assign code names to each potential transaction once we enter the Early Diligence stage.

To maintain confidentiality, we follow the following guidelines:

1. When creating a new acquisition slack channel:
    1. Set the channel topic to: "This channel is confidential. Please confirm with acquisition lead `name here` before inviting people to the channel or related docs."
    1. Set the channel description to: "Please review our [acquisition handbook and process](/handbook/acquisitions/acquisition-process/) to familiarize yourself with our approach to acquisitions. Please review the confidentiality section of the process and our guidelines".
1. We strive to keep the number of people involved in an acquisition as small as possible to reduce legal exposure and maintain a low potential risk.
1. If you're part of an acquisition Slack channel, Google Doc, or other internal GitLab discussion and would like to invite another GitLab team member to one of those, please confirm with the acquisition lead before doing so.
1. We collect all notes on an acquisition in the main acquisition doc shared on the topic of the acquisition's slack channel. If you must create a new document, make sure it is set to invite-only and add the relevant people manually. That document needs to be kept inside the acquisition G-Drive folder on the Corporate Development Shared Drive.
1. Everyone involved in the project should use the code name in place of the actual company name in all communication about the deal until it is publicly announced.
