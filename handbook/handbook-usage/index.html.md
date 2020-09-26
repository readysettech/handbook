## Handbook guidelines

Please follow these guidelines and remind others of them.

### How we use the guide every day

1. Most guidelines in this handbook are meant to help, and unless otherwise stated, are meant to help more than being absolute rules. Don't be afraid to do something because you don't know the entire handbook, nobody does. Be gentle when reminding people about these guidelines. For example say, "It is not a problem, but next time please consider the following guideline from the handbook."
1. If you ask a question and someone answers with a link to the handbook, they do this because they want to help by providing more information. They may also be proud that we have the answer documented. It doesn't mean that you should have read the entire handbook, nobody knows the entire handbook.
1. If you need to ask a team member for help, please realize that there is a good chance the majority of the community also doesn't know the answer. Be sure to **document** the answer to radiate this information to the whole community. After the question is answered, discuss where it should be documented and who will do it. You can remind other people of this request by asking "Who will document this?"
1. When you discuss something in chat always try to **link** to a URL where relevant. For example, the documentation you have a question about or the page that answered your question. You can remind other people of this by asking "Can you please link?"
1. Remember, the handbook is not what we hope to do, what we should formally do, or what we did months ago. **It is what we do right now.** Make sure you change the handbook in order to truly change a process. To propose a change to a process, make a merge request to change the handbook. Don't use another channel to propose a handbook change (email, Google Doc, Slack, etc.).
1. When communicating something always include a link to the relevant (and up-to-date) part of the **handbook** instead of including the text in the email/chat/etc. You can remind other people of this by asking "Can you please link to the relevant part of the handbook?"

### How to change or define a process

1. To change a guideline or process, **suggest an edit** in the form of a merge request.
1. When working to get your change merged quickly, make sure you are asking the appropriate team members with merge rights. 
1. After it is merged you can post this in the applicable slack channel(s). You can remind other people of this by asking "Can you please send a merge request for the handbook?"
1. When substantially changing handbook layout, please leave a link to the specific page of the review app **that is directly affected by this MR**. Along with the link, include as much info as possible in the MR description. This will allow everyone to understand what is the purpose of the MR without looking at diffs.
1. Keeping up with changes to the Handbook can be difficult, please be clear and concise on your merge request's title, to ensure someone reading the handbook changelog can quickly understand the MR's content.
1. Communicate process changes by linking to the **merged diff** (a commit that shows the changes before and after). If you are communicating a change for the purpose of discussion and feedback, it is ok to link to an **unmerged diff**. Do not change the process first, and then view the documentation as a lower priority task. Planning to do the documentation later inevitably leads to duplicate work communicating the change and it leads to outdated documentation. You can remind other people of this by asking "Can you please update the handbook first?"
1. When feasible, introduce process changes iteratively. It is important that you contribute to the handbook by making small merge requests. This will help gain adoption among the process's intended audience. We want to avoid significant process changes that are unnecessarily large, top-down, and disruptive. These types of process changes can disempower DRIs (directly responsible individuals) and cause people to focus on process rather than results.
1. Like everything else, our processes are always in flux. Everything is always in draft, and the initial version should be in the handbook, too. If you are proposing a change to the handbook, whenever possible, **skip the issue and submit a merge request**. (Proposing a change via a merge request is preferred over an issue description). Mention the people that are affected by the change in the merge request. In many cases, merge requests are easier to collaborate on since you can see the proposed changes.
1. **If something is a limited test** to a group of users, add it to the handbook and note as such. Then remove the note once the test is over and every case should use the new process.
1. If someone inside or outside GitLab makes a good suggestion invite them to add it to the handbook. Send the person the URL of the relevant page and section and offer to do it for them if they can't. Having them make and send the suggestion will make the change and will reflect their knowledge.
1. When you submit a merge request, make sure that it gets merged quickly. Making single, small changes quickly will ensure your branch doesn't fall far behind master, creating merge conflicts. Aim to make and merge your update on the same day. Mention people in the merge request or reach them via Slack. If you get a suggestion for a large improvement on top of the existing one consider doing that separately. Create an issue, get the existing MR merged, then create a new merge request.
1. If you have to move content have a merge request that moves it and does nothing else. If you want to clean it up, summarize it, or expand on it do that after the moving MR is merged. This is much easier to review.
1. Try to **add the why of a handbook process**, what is the business goal, what is the inspiration for this section. Adding the why makes processes easier to change in the future since you can evaluate if the why changed.


### Editing the handbook

Strongly consider learning how to edit the [handbook using git](/handbook/git-page-update) and/or via [the web IDE](/handbook/git-page-update/#webide-using-the-browser).
Please read through the [Writing Style Guidelines](/handbook/communication/#writing-style-guidelines) before contributing.


### Handbook First Competency

In an all-remote, asyncronous organization, each team member should practice handbook first. For more information on what it means to be handbook first, please refer to the [why handbook first](/handbook/handbook-usage/#why-handbook-first) section of this page.

**Skills and behaviors of handbook first as a Team Member**:

- Actively contributes to the handbook.
- [Everything starts with a merge request](/handbook/communication/#everything-starts-with-a-merge-request)
- Provides links information from the handbook when answering questions and if the information doesn't exist in the handbook, then the team member adds it.

**Skills and behaviors of handbook first as a People Leader**:

- Holds their team and others accountable for being handbook first
- Enables new team members and managers on how to leverage the handbook as a resource.
- Serves as a role model for what it means to be handbook first.

## Merge Rights Guidelines

GitLab team members with `merge rights`, are team members who have the GitLab permissions to _merge_ merge requests (AKA: maintainer-level permissions).
It is important that GitLab team members with maintainer permission use this responsibility responsibly.
Below are a few guidelines for GitLab maintainers:

1. Ensure you have approval from the owner of the page you are merging prior to merging.
1. Avoid merging your own merge request until at least one other team member has reviewed your MR, unless it's a normal part of your role (such as PMs updating direction pages).
_Note: The exception to this rule is if you are modifying something very small (I.E. a typo)_
