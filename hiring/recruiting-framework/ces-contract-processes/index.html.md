---
layout: handbook-page-toc
title: "Recruiting Process - Candidate Experience Specialist Contract Processes"
---

## On this page
{:.no_toc .hidden-md .hidden-lg}

- TOC
{:toc .hidden-md .hidden-lg}

## Recruiting Process - Candidate Experience Specialist Contract Processes
{: #framework-coord}

Assuming that the [hiring process](/handbook/hiring/) went smoothly, now it is time to prepare the applicable contracts. Once the verbal offer is made, the coordinator will send the contract to the applicant, using DocuSign in Greenhouse. On rare occasion, the coordinator may have to create the contract outside of Greenhouse using Google Docs; if this is the case, the coordinator needs to have a People Ops team member review the contract for accuracy before sending it out for signature.

First, be sure to validate the following:

1. The currency listed in the offer package in Greenhouse should normally be the local currency of the new team member unless they explicitly request USD/EUR because their local currency has a lot of inflation. This needs to be confirmed and approved by our People Ops Analyst prior to making the offer, as any changes to the currency will require complete reapproval in Greenhouse, regardless if it is the same amount just in a different currency.
1. Confirm if the team member would be an employee or contractor and [through which entity the team member would be employed or contracted](/handbook/people-group/contracts-and-international-expansion/#team-member-types-at-gitlab). If the team member wants to be contracted through a company, it can either be their own established legal entity or a separate and unaffiliated 3rd party company; please confirm which with the team member prior to sending out the contract. If the team member will be contracted through their own entity (or as an independent contractor), please use the BV Contractor Agreement. If the team member will be contracted through a 3rd party company, please inform Legal so that we can enter into a vendor contract with the company. The 3rd party company will then enter into a contract with the team member, and People Ops Analyst will provide the necessary specific salary and position information.

### Send the contract through Greenhouse

1. Once the offer package has been approved in Greenhouse and the recruiter has given the verbal offer, go to the candidate's profile in Greenhouse. Verify the address is listed on the details tab. If the address is not listed you can locate it on the background check, or in the reference request email reply.
1. If necessary click Edit Profile to update the candidate's name to their legal name (given during the reference/background check stage) and list any preferred names in quotes as the first name. Legal names are required on contracts and for proper export to Bamboo HR.
1.  Update signatory and entity by clicking "Update" under Offer Details. Add signatory name and title, as well as entity based on candidate's location.
1. Scroll to the section "Offer Documents" and click "Generate". Then click in the box and select from the options the appropriate template for the team member's entity, employment/contractor status, full-time or part-time, and any applicable bonuses. An example is `GitLab Inc full-time, with variable bonus/commission`. Then click "Generate". It will now populate and .docx and .pdf files under the "Offer Documents" section. Download the pdf and preview it to ensure everything populated correctly. If there are any token errors (i.e. problems with the information pulling from the candidate's profile and into the contract), Greenhouse will notify you. Most likely, if that happens it is because a field in the candidate profile is not accurately filled in. Once you fix the error, you'll need to "Regenerate" the contract.
1. Next, click "Send with DocuSign" right below the offer documents. You will need to have first connected your Greenhouse account with your DocuSign account by going to the integrations tab in Greenhouse.
1. Choose the correct template according to country, or if no country template is available select `Offer through DocuSign`. In the "To User" field, choose the GitLab signatory for the contract. In the "CC" field, add the recruiter and the hiring manager. Then click "Preview on DocuSign".
1. You will be redirected to DocuSign.
1. On the top left of the screen, click where it says the candidate's name, then click "Edit Recipients". Change the `2` next to the GitLab signatory's name to a `1`, change the `1` next to the candidate's name to a `2` and change the `1` next to the hiring manager's name to a `2`. This ensures that the contract goes to the GitLab signatory to sign first, as well as the recruiter for a Cc and once signed by them it will go to the candidate and the hiring manager with a Cc. Then click "Done".
1. Scroll throughout the contract and double check that the candidate and GitLab signatory signature and date fields are accurately added. If there is an Exhibit A to the PIAA section of the contract, be sure to add add a dropdown box assigned to the candidate.
On the right side of the screen, under `fill in list of options` click `add option` type in YES.  Click `add option` again, type in None. Click `save as custom field`, name it as desired.  Click Save
On the left side of the screen, navigate to standard field icon. Select Text, resize the box as desired.
On the right side of the screen, scroll down, select `Conditional Logic` click on `Create a rule`
Click on the `Yes/None` dropdown, at the top of the screen, where it says `Click on the field to show when trigger field`, type YES in the equal to box.  Click `Done`
Click on the Text box.  Click `save as custom field` name it as desired.
**You will need to create the conditional logic rule each time you send out contracts**, it does not save for future use.
There may also be other fields you'll need to add a textbox for, so double check if there are any other fields that need to be completed by either the candidate or GitLab signatory (as contracts for different entities vary; one that is easy to miss is the UK contract which requires the candidate to input their national insurance number). Once you've verified that all the information is correct and appropriately assigned, click "Send" at the top right corner.
1. You'll now be redirected back to Greenhouse, where you can monitor the progress of the contract and be able to see when each party signs it. Once it is signed by all parties, you and everyone cc'd on the original request will receive a confirmation email that it has been signed.
1. If you need to resend the contract, follow the same steps, but be sure to log into your DocuSign account and first delete the original one to avoid confusion.

### How to add a contract into Greenhouse

1. In the Google Drive, go to the folder titled "Employee and Contractor Templates and Staging". Only the People Group, Finance, and Legal should have access to this folder.
1. Click the folder called "Templates" to find the relevant template contract (each document is also linked below).
1. Make a copy of the contract and move it into the "Greenhouse Templates" folder.
1. Log in to Greenhouse and go to "[Configure](https://app2.greenhouse.io/configure)" by clicking the gear at the top right corner, then choose "[Offer Templates](https://app2.greenhouse.io/account/offer_letter_templates)".
1. For each of the fields with curly brackets (`{ }`) in the template on Google Drive, find and replace that field (including the curly brackets) with the corresponding Greenhouse tokens (including the curly bracket). For example, `{Contributor Name}` in the Drive template will be replaced with `{{CANDIDATE_NAME}}`.
   1. Some fields that are not necessarily clear are the compensation fields as there are separate fields for the _vacancy_ and for the _candidate_; we want the candidate fields for the contract, so in Greenhouse, the appropriate token for salary is `{{CURRENCY}}`, bonus is `{{BONUS_AMOUNT}}`, and stock options is `{{STOCK_OPTIONS}}`. Another field that is easily confused is the title; the `{{JOB_NAME}}` is the name of the vacancy, which is not always necessarily the same as the title the candidate will have; to make sure it is always correct and includes the appropriate level and specialty for the candidate, use the token `{{FULL_TITLE__INCLUDING_LEVEL_AND_SPECIALTY_}}`.
   1. The one exception to the curly bracket find and replace process is the Belgian contract. The fields that need to be edited are highlighted.
   1. If there is no corresponding field in the Greenhouse tokens, go to "Configure", "Custom Options", "Offers". Then click "Add Field" at the top, and add the name of this field (being as succinct yet descriptive as possible), add a description if needed (this will only show up when hovering over the field), the type of field it will be (this cannot be changed once the field is created), and check off "Create new email token (optional)" which will allow you to include it in the contract. Then click save. The new field will populate at the bottom, and you'll be able to drag it elsewhere in list, but do keep in mind that this is the list that populates the offer package, so unless it's crucial to the offer/approval process, it's usually best left towards the bottom. It is, however, best practice to at least move it above the "Signatory Name" and "Signatory Title" fields, so that they are always last. Then, go back to the "Offer Templates" section in Greenhouse, and you'll see the new field you created is a new token option.
   1. When removing optional clauses, take care that the paragraph / section numbering still makes sense.
   1. Double check that each field that needs to be filled out is replaced with a Greenhouse token. Sometimes it is not always obvious, as the curly bracket might be regular brackets by mistake.
   1. For each signature section, the following tokens **must** be on their own line in the document, with nothing else on the line: `{{CANDIDATE_SIGNATURE}}`, `{{CANDIDATE_SIGNATURE_DATE}}`, `{{COMPANY_SIGNATURE}}`, and `{{COMPANY_SIGNATURE_DATE}}`. Find each signature page, then hit enter to create the new line after the "Signature", "Name", "Title", and "Date" sections, then copy the corresponding Greenhouse tokens. These can be easy to miss, so double check each signature section has the appropriate Greenhouse tokens, each on their own line.
   1. Most contracts will have various versions that need to created, e.g. one that contains bonus language for variable bonus/commission, director/executive bonuses, or signing bonuses. Best practice is to create the contract containing all of the additional information and title it accordingly, then once you are done go to "File" in Google Docs and choose "Make a copy". Then remove the information as needed and rename the new document and continue the steps below. You can view other documents in the Greenhouse Templates folder for examples.
   1. For contract templates with variable bonus/commission plans, replace all paragraphs with the token `{{VARIABLE_BONUS_TYPE_OFFER_SECTION}}` which will tell Greenhouse to automatically choose the correct bonus type based on the offer package created in Greenhouse.
1. Once you have completed customizing the contract for Greenhouse, click "File" in Google Docs, then "Download as" and "Microsoft Word (.docx)".
1. Then go back to the "[Offer Templates](https://app2.greenhouse.io/account/offer_letter_templates)" section in Greenhouse and scroll down to "Template Name" and click "Upload New" to the left.
1. Choose the document you've downloaded and add a name for the template. The convention is typically "GitLab `Entity` `employment-type`, `with/without bonus`", e.g. `GitLab Inc full-time, with variable bonus/commission`.
1. Greenhouse will upload the document and it will appear at the bottom of the page. There will be a `Test` button next to it; click this, and it will validate that all of the Greenhouse tokens are correctly inputted. If there are any errors, it will notify you. You will then need to go back to the template in Google Docs and correct the errors, redownload it, and reupload it to Greenhouse (after deleting the original one with mistakes). If all of the tokens are functioning properly, there will be green checkmarks, and you're ready to use this template for contracts!
1. To delete a contract template from Greenhouse, click the three dots `...` to the right of the template name, then click delete and confirm.

The "source of truth" for the contract templates are in the Google Drive, in the folder titled "Employee and Contractor Templates and Staging". Any updates to contracts will be done there first, and then the recruiting team needs to be pinged to be made aware of the changes so they can update the corresponding Greenhouse template.

To change or update a contract that has already been created and uploaded into Greenhouse, return to the corresponding Google Drive doc in the "Greenhouse Templates" folder, open the templates that need to be updated (there may be multiple that need to be changed, since there are different varieties of each contract to accommodate bonus structures, full-time/part-time, etc.), then update each accordingly. If you need to add new tokens to accommodate the change, be sure to follow step 5.3 in the above instructions. Once you have finished making any updates, click "File" in Google Docs, then "Download as" and "Microsoft Word (.docx)". Then go back to the "[Offer Templates](https://app2.greenhouse.io/account/offer_letter_templates)" section in Greenhouse. Find the contract that you are replacing, copy the name of it so you can maintain consistency, then click the three dots `...` to the right of the template name, then click delete and confirm. Then click "Upload New", paste the name of the template, and upload the new version. Click "Test" to validate that everything translated correctly (per step 9 above), and you are ready to use the new template.

### How to Send a Family Member Relationship Acknowledgment 

Consistent with GitLab’s policy governing Hiring Significant Others or Family Members, GitLab is committed to a policy of employment and advancement based on **qualifications and merit** and does not discriminate in favor of or in opposition to the employment of significant others or family members. Any new hire that has a family member relationship that is currently employed at GitLab must sign [this acknowledgment](https://docs.google.com/document/d/1IseZy4zJZMgP0VCAsGqCP3I6sfnavGdD81THnqljaPI/edit?usp=sharing) along with the GitLab team member. This process is done in conjuction with sending out the contract.

1. If you have not been notified by the recruiter that there is a family relationship in play, there is now a field in the 'Offer Details' that will show whether a relationship exists. There should also be a *Family Member* tag on their profile. It, however, will not show who that family member is. 
1. The Recruiter will post the name of the family member in the Private Notes within the Greenhouse profile. If not there, the CES will reach out to the recruiter to find out who the current GitLab team member is. 
1. Once the family member is identified, you will send the [Family Member Relationship Acknowledgment](https://docs.google.com/document/d/1IseZy4zJZMgP0VCAsGqCP3I6sfnavGdD81THnqljaPI/edit?usp=sharing) via DocuSign to the new hire as well as the GitLab team member for signing. 
1. After all parties have signed, upload a copy into both the new hire and the current GitLab team members BambooHR profile.

### How to Update a Start Date After the Contract is Signed

To change a start date after a **GitLab entity** contract has been signed and the new team member has been "hired" in GreenHouse the Candidate Experience Specialist will complete the following steps:

1. Confirm the start date via email with the new team member, the recruiter, the hiring manager, and the Candidate Experience Specialist.
1. Save the email as a pdf file for upload into BambooHR.
1. Update GreenHouse:
   - Offer Details
   - Click the edit pencil next to the start date
   - Select the new Start Date
   - Save
   - In the "Make a Note" section in Greenhouse state the old start date and the new state date
   - Save
1. Update the People Experience Team in Slack Workflow.
    - Open private Slack channel `#people-exp_ces`
    - Click Shortcuts button in the bottom left corner (looks like a lightning bolt)
    - Click "New Start Date        Workflow"
    - Fill in Team Member Name with the New Hire Name
    - Fill in Original Start Date (YYYY-MM-DD)
    - Fill in New Start Date (YYYY-MM-DD)
    - Fill in Reason For Change. This is to inform the People Experience team of the reason for the new date (i.e. Public Holiday, New Hire request, Hiring Manager request, etc.).
    - Optional: Fill in Any other changes.
    - Click Submit
1. Update BambooHR to reflect the new start date.
   - Sign into Bamboo HR
   - Search of the new team member's name
   - Click on the Job tab under the name and title
   - Update the hire date to reflect the adjusted date
   - Save Changes
   - Click on the Documents tab under the name and title
   - Upload
   - Choose File(s)
   - Select the saved email pdf file
   - Open
   - Folder: Contracts and Changes
   - Check the "Share these File(s) with the Employee" box
   - Upload

To change a start date after a **PEO** contract has been signed and the new team member has been "hired" in GreenHouse the Candidate Experience Specialist will complete the following steps:

1. Confirm the start date via email with the new team member, the recruiter, the hiring manager, and the Candidate Experience Specialist.
1. Forward the email to the contact at the PEO.
1. The PEO will generate a new contract and send to the new team member.
   * The Candidate Experience Specialist will need to follow-up with the PEO contact to ensure the new contract is signed.
1. Update GreenHouse:
   - Offer Details
   - Click the edit pencil next to the start date
   - Select the new Start Date
   - Save
   - In the "Make a Note" section in Greenhouse state the old start date and the new state date
   - Save
1. Update the People Experience Team in Slack Workflow.
    - Open private Slack channel `#people-exp_ces`
    - Click Shortcuts button in the bottom left corner (looks like a lightning bolt)
    - Click "New Start Date        Workflow"
    - Fill in Team Member Name with the New Hire Name
    - Fill in Original Start Date (YYYY-MM-DD)
    - Fill in New Start Date (YYYY-MM-DD)
    - Fill in Reason For Change. This is to inform the People Experience team of the reason for the new date (i.e. Public Holiday, New Hire request, Hiring Manager request, etc.).
1. Update BambooHR to reflect the new start date.
   - Sign into Bamboo HR
   - Search of the new team member's name
   - Click on the Job tab under the name and title
   - Update the hire date to reflect the adjusted date
   - Save Changes
   - Click on the Documents tab under the name and title
   - Upload
   - Choose File(s)
   - Select the saved email pdf file
   - Open
   - Folder: Contracts and Changes
   - Check the "Share these File(s) with the Employee" box
   - Upload

### How to Void a Contract Before a Candidate Signs

In rare cases, we may rescind our offer before a candidate signs the contract. Work with the Recruiter, Hiring Manager, People Business Partner, VP of Recruiting, and Contract Employment Counsel on ensuring uniform communication. Once the candidate has been informed verbally and via email by the recruiting team, follow these steps:
1. Ensure the email is exported into the Activity Feed in Greenhouse.
1. Void the contract in DocuSign utilizing the same communication that was emailed.
1. Reject the candidate in Greenhouse. Be sure to select 'Reject and Don't Send Email.'

### How to Unhire a Candidate After Contract is Signed

In rare cases, candidates may reject our offer after they have signed the contract.  If they have been hired in Greenhouse and exported to BambooHR, follow these steps:
1. Unhire the candidate in Greenhouse.
1. Reject them in Greenhouse; add reasons in notes, you may add the email that was sent by the candidate. Click ‘reject and don’t send email’.
1. Cancel any scheduled emails in Greenhouse.
1. Tag the assigned People Ops specialist on the tracker sheet so they are aware of this change.  If no People Ops specialist has been assigned, ping the People Ops specialist team in the specialist-ces slack channel. It is important to inform the People Ops specialist team in order for them to delete the candidate from BambooHR.
1.  If they were hired via a PEO, inform the contact person of this change.

### How to Resend a Contract After Being Marked as Hired

There are certain times when a contract needs to get resent to the candidate after they have been hired into the system, should that happen. Follow the steps below: 
1. If the req is already closed, tag the recruiting operations team in the greenhouse profile explaining the situation and that the req needs to be reopened to resend a contract. 
1. Unhire the candidate in Greenhouse. 
1. Resend the correct contract and follow standard steps for doing this. 
1. Once you receive the contract back, **before** marking the candidate as hired in Greenhouse. You will need to ping the Sr. People Operations Director in the `#people-group-confidential` asking for the BambooHR profile be deleted due to having to resend a contract and not wanting a duplicate profile. Provide the BambooHR link in the message.
1. Once they confirms the profile is deleted, proceed with marking the candidate as hired in Greenhouse and closing out the req again. 
1. If a People Experience Specialist was involved, make sure you ping them and let them know the contract has been updated and the new BambooHR profile has been created. 

For Recruiting Ops:
1. Once notified by the CES team, copy the Job Approval Chain and add it to the Approval Details Notes section. Include the names of the approvers, the dates approved, and the reason as to why the requisition is being re-opened. Tag the Finance Business Partner, CES, and Recruiter in this note.
1. From the Approvals page, select 'Edit Job & Openings'
1. Duplicate the Opening that needs to be re-opened.
1. Bypass approvals in the Job Approval section to change the Job Status from Draft to Open.
1. Inform CES once the req is open.
1. When the revised contract is uploaded by the CES, verify if the core fields on the offer remain the same. If it remains the same, bypass offer approvals and inform the CES once completed.
1. Once the CES team marks the candidate as hired in Greenhouse, close the duplicated opening and save changes.

## Amended Contracts

Contract amendments or modifications are processed by the Candidate Experience Specialist if the team member has not started or by the People Operations Specialist if they have.

1. Amendments prior to starting with GitLab:

If an amendment needs to be made and the previous contract was never active, the Candidate Experience Specialist should:

* Delete the previous contract from BambooHR
* Upload the updated contract in the BambooHR file 'Contracts and Changes'
* Notify the People Operations Specialist of the change in the [GitLab Onboarding Tracker](https://docs.google.com/spreadsheets/d/1L1VFODUpfU249E6OWc7Bumg8ko3NXUDDeCPeNxpE6iE/edit#gid=1721125348)

_Note: It is essential that People Operations Specialists are informed of all changes, as various fields must be updated in BambooHR._

2. Amendments after starting with GitLab:

A contractor requests a modification to their contract due to a name change/company incorporation (Example: The individual recently incorporated a company, and would like to invoice GitLab through their company versus individually)

* The People Operations Specialist should log the requested change in BambooHR in the `Contracts & Changes`
section of the employee's profile
* The People Operations Specialist should draft the new contract using the appropriate template in the [Employment and Contractor Agreements](/handbook/people-group/contracts-and-international-expansion/#employment-and-contractor-agreements) section. ***Please remember to always make a copy of the template before editing.***

_Important: Employment contracts cannot be backdated. If a team member requests to backdate a contract for invoicing purposes, an addendum should be added to the contract stating: "As the Contractor has not invoiced GitLab for payment since their start date on `contractor start date`, GitLab will pay the Contractor for this period of time in accordance with the Contractor’s base compensation". The start date on the new contract should always reflect the date the contract is staged for signatures._

* The People Operations Specialist should stage the contract in HelloSign to be signed by both the team member and the Director of People Operations.
* Once siged by both parties, the contract should be uploaded to the team members BambooHR profile in the `Contracts & Changes` section.


## Process for GitLab team-members in the Netherlands
In this location, a temporary contract (tijdelijk contract) is for 12 months, with a pre-determined end date. A dismissal procedure is not required to terminate a temporary contract at the end of its duration. However communication about the extension of the contract must happen at the latest 1 month before the actual contract end date (aanzegtermijn). 

It is common for Dutch employers to offer a second temporary contract when the first expires, but it's not guaranteed. As a Dutch employer, this is standard procedure for GitLab. As of 2015-07-01, employees who have worked with an employer on temporary contracts for at least two years are entitled to an indefinite contract if the work agreement continues, and this is known as the chain rule (ketenregeling). 

The process for New Hires is as follows: 

1. The offer is made by the recruiter per the [hiring process](https://about.gitlab.com/handbook/hiring/).
1. The Candidate Experience Specialist emails the new team member the Contract Info Request - the Netherlands from GreenHouse.
1. The Candidate Experience Specialist will update the GreenHouse Offer Details with BSN and Date of Birth when the new team member provides the necessary details and then generates the "IT BV Employee Temporary - the Netherlands" contract out of GreenHouse.
1. The Candidate Experience Specialist will stage the contract for signature via DocuSign, CC the hiring manager, and CC the HRSavvy group email. This will ensure our payroll provider in this location can start their onboarding, well ahead of ours. 

The People Operation Specialist are in charge of [contract renewals](/handbook/people-group/contracts-and-international-expansion/#contract-renewals). The process the **end of the first 12-month GitLab BV Netherlands temporary contract** is listed in their [Netherlands Renewal Process](/handbook/people-group/contracts-and-international-expansion/#contract-renewals) section of the [Contracts & International Expansion](handbook/people-group/contracts-and-international-expansion/) handbook page. 

_GitLab IT BV contracts should only be used for contractors. All Netherlands **employees** should be issued the GitLab BV contract. PEO contract templates should be provided by the PEO directly. We should not use GitLab BV or GitLab IT BV contracts for PEO models._

## Process for GitLab Team Members in Australia
GitLab has an entity in Australia and use this [contract](https://docs.google.com/document/d/1YjvQnYsXBVDIRdV950az7Nw7vfEdUZyrEzXl0Jqqivk/edit) in this location. All team members in this location are employees.

## Process for GitLab Team Members in New Zealand
GitLab has an entity in Australia, and New Zealand falls under that entity. These two contracts are used for this location: [Without OTE](https://docs.google.com/document/d/1TWrlDF9geNZGfuQ7FK1UUh17mM9ocqP7saQjDM8NN2U/edit#) and [With OTE](https://docs.google.com/document/d/1lO4T32nK2tZEUZQ6_sLEmg1gIhYNaJSwExzzMVrV2vI/edit). All team members in this location are employees.

## CXC

GitLab is working in partnership with [CXC Global](http://cxcglobal.com/) to employ GitLab team-members located in **Poland**, **Ukraine**, **Romania**, and **Russia**. The actual employment contracts will be sent and issued by CXC and are in accordance with local labor law. CXC also handles the processing and payment of payroll and associated taxes and compliance in each of the countries on behalf of GitLab. The contracts themselves are between the individual and CXC. 

CXC provides a 12 month contract in these locations, and this can be extended. They are only able to support contractors that have an established entity/company in these countries (listed above). The offer details will be provided to CXC by GitLab's hiring team.

To create the contract:

1. Offer is made by the recruiter per the [hiring process](/handbook/hiring).
1. The Candidate Experience Specialist emails the new team member the Contract Info Request - CXC from GreenHouse.
    -Click “Email CANDIDATE NAME”
    -Select “Contract Info Request-CXC” from dropdown.
    -CC Recruiter
    -Click “Send Email”
1. The Candidate Experience Specialist will check if there is a probationary period.
    - Go to [Probationary Periods for Team Members Employed by a PEO](/handbook/people-group/contracts-and-international-expansion/#probation-periods-of-team-members-employed-through-a-peo) and check the candidate's country.
    - Select the duration of the probationary period (if any) in the "Offer Details" dropdown. If there isn't one, select "N/A" in that field.
1. The Candidate Experience Specialist will check if the contract is indefinite or fixed.
    - If the contract is indefinite, select "Indefinite" from the dropdown in "Offer Details".
    - If the contract is fixed, select "Fixed Contract" from the dropdown in "Offer Details" and enter the end date under "End Date".     
1. Once the additional information is received, The Candidate Experience Specialist will generate the PEO form out of GreenHouse.
    -Click “Generate”
    -Select “PEO New Hire Template” from the dropdown
    -Click “Generate”
1. The Candidate Experience Specialist will stage the form for their own signature via DocuSign, the new team member and the appropriate CXC contact. Contact details can be found in 1password => People Operations Vault => Entity & Co-employer HR Contacts.
1. The Candidate Experience Specialist should add the candidate to the [PEO Tracking Sheet](https://docs.google.com/spreadsheets/d/1gSOVTJ1Yv-YsSaliJwKVf-1H0vBZXxb5NWFiqCwT-uo/edit#gid=0) and keep track of communication between GitLab.
1. CXC will then prepare the SOW and contract.
1. CXC will then reach out to the candidates directly to coordinate the contract signing and onboarding to CXC's payroll.
1. Kindly allow a duration of one week for CXC to complete their process. This might mean that a two week notice period to start at GitLab, could increase to three weeks, its important to communicate this duration to new hires in this location.
1. CXC will inform the Candidate Experience Specialist when the contract is signed.
1. The Candidate Experience Specialist will mark the candidate as hired.
1. The CES will adjust the 'Accepted' date to match the 'Sent' date.
1. The Candidate Experience Specialist will now [mark the candidate as hired](/handbook/hiring/recruiting-framework/coordinator/#send-contract)[](see steps 10-12).




## Safeguard

GitLab has partnered with [Safeguard](http://www.safeguardworld.com/) to hire in Hungary, South Africa, Switzerland, Ireland, France, Italy, Brazil, Spain, South Korea, Japan. You can also review this [document](https://drive.google.com/file/d/1aUjgb37XO-3LqdW8WF8l-QV2ZcTLBTPj/view?usp=sharing) that Safeguard created regarding frequently asked questions about their process.

To create the contract:

1. The Offer is made by the recruiter per the [hiring process](/handbook/hiring).
1. The Candidate Experience Specialist emails the new team member to gather additional details required to generate the contract.
   - From the GreenHouse profile, under tools, click to email the new team member
   - From the template drop down list select: Contract Info Request - Safeguard
   - Send Email
1. The Candidate Experience Specialist will check if there is a probationary period.
    - Go to [Probationary Periods for Team Members Employed by a PEO](/handbook/people-group/contracts-and-international-expansion/#probation-periods-of-team-members-employed-through-a-peo) and check the candidate's country.
    - Select the duration of the probationary period (if any) in the "Offer Details" dropdown. If there isn't one, select "N/A" in that field.
1. The Candidate Experience Specialist will check if the contract is indefinite or fixed.
    - If the contract is indefinite, select "Indefinite" from the dropdown in "Offer Details".
    - If the contract is fixed, select "Fixed Contract" from the dropdown in "Offer Details" and enter the end date under "End Date".
1. When the new team member provides the necessary details, the Candidate Experience Specialist will update GreenHouse offer details and generate the PEO form out of GreenHouse.
   - Offer Details
   - Update
   - Nationality
   - Probationary Period
   - Indefinite or Fixed Contract
   - Save
   - Navigate to Offer Documents
   - Generate
   - Click in the white space below Select templates
   - Select PEO New Hire Template from the drop down list
   - Generate
   - Send with DocuSign
   - Template: Offer through DocuSign - Safeguard
   - To User: yourself
   - Add our single point of contact at Safeguard and the global email address to the list of CC email addresses. If they are not populating automatically you can find their contact details in 1password => People Operations Vault => Entity & Co-employer HR Contacts.
   - Preview on DocuSign
   - Select the new team member's name in the upper left hand corner
   - Edit Recipients
   - On the new team member's block change Needs to Sign to Receives a Copy
   - Edit the signing order to yourself 1 and everyone else 2
   - Done
   - Add fields to Section 5 of the form if they do not auto populate: Name, title, email, and date
   - Send
   - Do you want to sign this now? Yes
   - Sign the form
1. The Candidate Experience Specialist should add the candidate to the [PEO Tracking Sheet](https://docs.google.com/spreadsheets/d/1gSOVTJ1Yv-YsSaliJwKVf-1H0vBZXxb5NWFiqCwT-uo/edit#gid=0) and keep track of communication between GitLab.
1. Once Safeguard receives the form they will contact the candidate directly to onboard them. This first contact usually takes 2-3 days, but can take up to a week.
1. If the Candidate Experience Specialist does not hear back from Safeguard within 72 hours, they will follow up to check if the start date is viable, get timing on when they will hear back and when the new hire will receive their contract and other important employee information.
1. The new hire should be kept updated by the Candidate Experience Specialist or Recruiter by email. If the contract has not been received by GitLab 5 business days prior to the start date, we'll need to reconsider the start date.
1. SafeGuard will inform the Candidate Experience Specialist when the contract is signed.
1. The Candidate Experience Specialist will mark the candidate as hired.
1. The CES will adjust the 'Accepted' date to match the 'Sent' date.
1. The Candidate Experience Specialist will now [mark the candidate as hired](/handbook/hiring/recruiting-framework/coordinator/#send-contract)[](see steps 10-12).

## Preparing Employment Agreements for GitLab team-members in India and Philippines- Global Upside

GitLab is working in partnership with [Global Upside](https://globalupside.com) for employing GitLab team-members located in India and Philippines. The process for creating and sending an agreement is as follows:

1. The Offer is made by the recruiter per the [hiring process](/handbook/hiring).
1. CES sends “Contract Info Request-Global Upside (India and Philippines)” email to the new hire to collect additional details.
1. The Candidate Experience Specialist will check if there is a probationary period.
    - Go to [Probationary Periods for Team Members Employed by a PEO](/handbook/people-group/contracts-and-international-expansion/#probation-periods-of-team-members-employed-through-a-peo) and check the candidate's country.
    - Select the duration of the probationary period (if any) in the "Offer Details" dropdown. If there isn't one, select "N/A" in that field.
1. The Candidate Experience Specialist will check if the contract is indefinite or fixed.
    - If the contract is definite, select "Indefinite" from the dropdown in "Offer Details".
    - If the contract is fixed, select "Fixed Contract" from the dropdown in "Offer Details" and enter the end date under "End Date".
1. Once additional details are obtained, update the offer details to reflect all information. The CES should be the signatory.
1. Generate “PEO New Hire Template” in Offer Documents to Send through DocuSign
1. Choose template *Offer through DocuSign -Global Upside (India and Philippines)*
    -To User, Self (CES)
    -Sign and complete
1. Download the completed Statement of Work in PDF form to upload it into Egnyte.
    -Make sure the downloaded file is titled with new hire’s full name
1. Once in Egnyte, navigate to *“/Shared/GPS/Active Clients/GitLab/IN/HR/Employee Master/Client Upload/New Employee Information”*
1. Click *Upload* to place new hire’s statement of work in this folder
1. Inform the Gitlab Implementation alias (gitlab.implementations@globalpeoservices.com) of any new hires by sending email template *Email to Global Upside-India and Philippines* under “Email the Team” in Greenhouse to let them know that a new SOW was uploaded into Egnyte and the employee’s name.
1. The Candidate Experience Specialist should add the candidate to the [PEO Tracking Sheet](https://docs.google.com/spreadsheets/d/1gSOVTJ1Yv-YsSaliJwKVf-1H0vBZXxb5NWFiqCwT-uo/edit#gid=0) and keep track of communication between GitLab.
1. Once Global Upside has drafted up the contract, they will place it in Egnyte and email the CES to review and approve.
    -CES should double-check that the contract reflects all the correct information that we sent to them.
1. Once the contract is signed by the new hire, Global Upside will notify the CES.
1. Proceed with marking them as hired in Greenhouse, adjusting the ‘Accepted’ date to match the ‘Sent’ date, sending the welcome email, and making sure all other candidates have been rejected prior to marking as hired and closing the req.
1. Lastly, once the background check is completed for the new hire, the CES needs to share that background check with Global Upside.     - Send the new hire the 'India - Background Check Notification' email that is located in the candidate email templates. This notifies the new hire that GitLab will be sharing their background check with Global Upside. 
    - The CES will upload the PDF of the completed background check to the safe and encrypted portal, Egnyte, in the 'Background Checks' folder under Client Upload.


## Employment Agreements for GitLab team-members in China

GitLab is working in partnership with [CIIC](http://www.ciicsh.com/ciicsh/ywsy/index.html) to employ GitLab team-members located in China. Signed agreements between GitLab and CIIC are required to employ any new hire. Therefore, there will be a lead time of approximately three weeks prior to starting. As soon as it becomes clear that an offer to a candidate is going to be made, People Ops will reach out to CIIC to begin the process. The process for preparing the agreements between all parties is as follows:

**GitLab and New Hire:**

1. Once the verbal offer has been made by the recruiter [hiring process](/handbook/hiring/) complete the [Template-GitLab China Employee Offer letter](https://docs.google.com/document/d/1c69dG9TuAB0MgiKj_gLDuHTHpzjocvEAm2okUOKqRIs/edit#) as per [How to use this page to prepare a contract](#how-to-use).
1. CIIC require a Chinese version of a [Letter of Employment Intent](https://docs.google.com/document/d/1BEHvveYUJkS1xwyd037P_zzitOSotF_68Kbi-c7k8hY/edit).
1. Complete the Letter of Intents with all of the information required/known. This should be completed in [English](https://docs.google.com/document/d/1b3fHqHzXhhoJeskUN-Km9vTLeuszysWPj8PlvXm45ug/edit) first then translated into Chinese using Google Translate.
1. Once this has been done send the GitLab (Chinese & English) versions of the Letter of Employment Intent to the new hire for their review, completion and signature using DocuSign. Ensure that Peopleops and CIIC are copied.
1. Once everything has been signed, print and FedEx the Chinese and English Letter of Intents to CIIC. The address can be found in the PEO China folder > China Employment Options > CIIC in the Google Drive.
1. The Candidate Experience Specialist should add the candidate to the [PEO Tracking Sheet](https://docs.google.com/spreadsheets/d/1gSOVTJ1Yv-YsSaliJwKVf-1H0vBZXxb5NWFiqCwT-uo/edit#gid=0) and keep track of communication between GitLab.
1. The PEO will inform the Candidate Experience Specialist when the contract is signed.
1. The Candidate Experience Specialist will mark the candidate as hired.
1. The CES will adjust the 'Accepted' date to match the 'Sent' date.
1. The Candidate Experience Specialist will now [mark the candidate as hired](/handbook/hiring/recruiting-framework/coordinator/#send-contract)[](see steps 10-12).

**GitLab & CIIC:**

1. GitLab has a Secondment Agreement in place with CIIC, this may need to be updated but CIIC will confirm.
1. Once CIIC have received the documents they will prepare a payment notice and send this to GitLab (peopleops) for payment. This must be paid upfront and may need CFO approval.
1. After CIIC receive payment they will reach out to the new hire to complete a Labor Contract.

**CIIC & New Hire**

Once the Labor Contract has been signed by both CIIC and the new hire the individual can now commence their work with GitLab.

## Employment Agreements for GitLab team-members in Germany

Please note, due to German labor law, the stock options are not included in the contract template and are not to be listed on the contract. If the candidate asks specifically for this information to be listed on the contract, please seek guidance from the CES Team Lead and/or Legal. A wet signature is required for German employment agreements the following process must be followed:

1. The Offer is made by the recruiter per the [hiring process](/handbook/hiring).
1. The Candidate Experience Specialist sends the new team member the GreenHouse email template: German Contract Step 1.
1. The Candidate Experience Specialist generates the German Contract form out of GreenHouse and stages for signature though GreenHouse and DocuSign. The Recruiting Manager or the VP of Recruiting (with the CPO and the People Ops Director as backup) signs the German Contract.
1. The Candidate Experience Specialist saves the unsigned contract to be used in a future step. It may require a manual edit to remove the signature tokens.
1. Once the DocuSign contract is signed you may hire the candidate and send the Welcome Email in Greenhouse.
1. The Candidate Experience Specialist saves the DocuSign Contract for upload into BambooHR as per the standard procedure.
1. Using the Greenhouse email template "German Contract to Mail" the Candidate Experience Specialist emails the unsigned contract to a Recruiting Manager, or the Recruiting Director or CPO as backup. Be sure to attach the unsigned contract to that email.
   Information that will auto populate in the email includes;
   * German Power of Attorney (POA) document (Google Drive: Employee and Contractor Templates and Staging => German Contracts)
   * new team member's name
   * new team member's name address
1. The Recruiting Manager or the VP of Recruiting will print two copies of the unsigned contract, sign and then send them to the new team member by postal service or FedEx (details of the fedex account can be found in 1Password => Secretarial Vault => Fedex).
1. Once the documents have been sent the Recruiting Manager will add the tracking number to the activity feed in the GreenHouse profile.
1. The Candidate Experience Specialist should set a Greenhouse reminder for 2 weeks time to follow-up with the new team member if they have not received an update.
1. When the new team member has emailed stating they received and signed the paper version, the Candidate Experience Specialist will email them back the GreenHouse email template German Contract Step 2.
1. Once the law firm has received the contract they will scan and email a copy to People Operations Specialist to file in BambooHR.

## Employment Agreements for GitLab team-members in Japan

In this location, a temporary contract is for 1 year (12 Months) with a pre-deterined end date.
1. The Candidate Experience Specialist emails the new team member to gather additional details required to generate the contract.
    - From the GreenHouse profile, under tools, click to email the new team member
    - From the template drop-down list select: Contract Info Request - Safeguard
    - Send Email
1. When the new team member provides the necessary details the Candidate Experience Specialist will save the required forms of ID, update GreenHouse offer details and generates the Safeguard form out of GreenHouse.
    - Offer Details
    - Update
    - Work Authorization ID
    - Nationality
    - Country of Citizenship
    - Level of Role
    - Position Category
    - Travel Percentage
    - Save
1. Navigate to Offer Documents and Generate
    - Click in the white space below Select templates
    - Select Safeguard - Template from the drop-down list
    - Generate
1. Send with DocuSign
    - Template: Offer through DocuSign - Innovare (Japan)
    - To User: yourself
    - Add the Innovare contacts to the list of Cc email addresses (If they are not populating automatically you can find their contact details in 1password => People Operations Vault => Entity & Co-employer HR Contacts.)
    - Fill in the Project Lead contact details with the hiring manager's name and email address
    - Confirm the Probation Period, Leave Benefits, and Termination Notice are correct
    - Attachments: Choose Files
    - Select the saved forms of ID file
    - Open
    - Preview on DocuSign
1. Select the new team member's name in the upper left-hand corner
    - Edit Recipients
    - On the new team member's block change Needs to Sign to Receives a Copy
    - Edit the signing order to yourself 1 and everyone else 2
    - Done
1. Add fields to Section 5 of the form if they do not auto-populate: Name, title, email, and date
    - Send
1. Do you want to sign this now? Yes
    - Sign the form
1. The Candidate Experience Specialist should add the candidate to the [PEO Tracking Sheet](https://docs.google.com/spreadsheets/d/1gSOVTJ1Yv-YsSaliJwKVf-1H0vBZXxb5NWFiqCwT-uo/edit#gid=0) and keep track of communication between GitLab.
1. Once GitLab receives a signed copy of contract, they will proceed to upload to GH and complete normal steps.

## Employment Agreements for GitLab team-members located everywhere else (IT BV contractor agreements)

1. Review the [Hiring Status](/handbook/people-group/contracts-and-international-expansion/#country-hiring-guidelines) of the location you are working with. If the location has not been evaluated yet, we issue a IT BV contractor agreement.
1. If the candidate would like to use their own entity for the contractor agreement update the offer details with the Contractor Name and Address. You will use the IT BV Contractor Agreement - C2C in these cases.
1. Generate IT BV Contractor Agreement - Independent or the IT BV Contractor Agreement - C2C
1. Select Send with DocuSign
1. Select "Offer through DocuSign-IT BV" email template
1. Update the "To" field to include the GitLab signatory and include the hiring manager in CC field
1. Select Preview on DocuSign
1. Once in DocuSign, update the signing order as you would with other contracts and hit send
