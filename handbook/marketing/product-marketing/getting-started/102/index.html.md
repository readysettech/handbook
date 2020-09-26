---
layout: markdown_page
title: "102 - Working at local speed"
---

## Objective:  Faster website editing: the basics.
Want to be able to quickly make updates to the handbook or about.gitlab.com and not have to wait for every commit to go through a pipeline?   This workshop will show you how to setup git and docker on your local machine and get your work done 200% faster.   

Approach: There may be steps that take too long for everyone to complete LIVE in the workshop (like cloning about.gitlab.com).   We plan on getting you started and then showing you how the end to end flow can work.

#### Prework

1. Install docker
   1. [Download and install the Mac version of Docker](https://www.docker.com/get-started)
   1. You will be asked to create a docker account, then download and install docker
2. Install an IDE (Install Atom if you don't have an IDE)
   1. [Download and install Atom](https://atom.io/)


#### Overview

:5

**Comparison:** In-line edit vs WebIDE vs working locally
In-line editor, for super-quick minor edits


| **Approach** |  **Pros**  | **Cons** |
**WebIDE**  |  - WebIDE is simple to access <br> - WebIDE is awesome <br>- No environment setup <br> - No git commands necessary <br> - Easy to make quick edits <br> - One integrated flow (edit -> MR -> pipeline) | - No advanced git capability <br> - Full pipeline run to see effect of any changes <br> - Limited IDE functionality (compared to tools like Atom) |
| **Working locally** | - Work off-line <br> - Use whatever editor you want <br> - Most minimal feedback loop - see effect of changes immediately (just reload your browser)  |  - Need to remember to push back changes <br> - Need to know git commands <br> - Need to get setup (and maintain) local environment <br> - Need to understand working in a terminal |

#### So why work locally?
Simply, it's faster with the shortest and tightest feedback loops.  If you're making  a non-trivial change to a page, working locally will often be faster.

#### What does it take to work locally?

Not much:  Simply 3 things
1. a local copy of about.gitlab.com (git does this),
2. an editor or development tool (IDE) - I use Atom,
3. a way to build and run about.gitlab.com (docker)

#### A little terminal time

:10

1. What is a 'Terminal'?
  Simply a way to enter commands into your PC.  To work with Git and Docker, you need to use the Terminal.  ![Opened Terminal](/images/workshop/terminal_opened.png)
1. To open the terminal from
   1. Type 'terminal' in smart search
   1. Or.  Go to Launch Pad--> Other, and you should see "Terminal"
   ![open terminal](/images/workshop/open_terminal.png)
1. a few key commands to navigate the terminal (from http://doors.stanford.edu/~sr/computing/basic-unix.html)<br>
- **Files**
    - **ls** --- lists your files
    - **ls -l** --- lists your files in 'long format', which contains lots of useful information, e.g. the exact size of the file, who owns the file and who has the right to look at it, and when it was last modified.
    - **ls -a** --- lists all files, including the ones whose filenames begin in a dot, which you do not always want to see.  
    - **ls -la** --- lists all files in 'long format'
    - **more filename** --- shows the first part of a file, just as much as will fit on one screen. Just hit the space bar to see more or q to quit. You can use /pattern to search for a pattern.<br>

- **Folders and directories** <br> Directories, like folders on a Macintosh, are used to group files together in a hierarchical structure.<br>
    - **pwd** --- tells you where you currently are.
    - **cd dirname** --- change directory. You basically 'go' to another directory, and you will see the files in that directory when you do 'ls'. You always start out in your 'home directory', and you can get back there by typing 'cd' without arguments. 'cd ..' will get you one level up from your current position. You don't have to walk along step by step - you can make big leaps or avoid walking around by specifying pathnames.

#### Background:


*Note:* The [read.me file from the www-gitlab-com project](https://gitlab.com/gitlab-com/www-gitlab-com?nav_source=navbar) is a key reference for getting set up to work remotely.   Specifically, this section of the [read.me](https://gitlab.com/gitlab-com/www-gitlab-com?nav_source=navbar#use-docker-to-render-the-website) are concise directions.

Git - gets and manages your copy of about.gitlab.com
<br>
**What is Git ?**

> "Git is a free and open source distributed version control system designed to handle everything from small to very large projects with speed and efficiency.
 Git is easy to learn and has a tiny footprint with lightning fast performance. It outclasses SCM tools like Subversion, CVS, Perforce, and ClearCase with features like cheap local branching, convenient staging areas, and multiple workflows." (from: https://git-scm.com/)

<br>
   Git is powerful and sometimes Git might be intimidating.  
<br>
   **(don't panic)** because GitLab makes it easy to use Git.

   Just in case - Bookmark or print the [Git CheatSheet](/images/press/git-cheat-sheet.pdf) and it's probably a good idea to check out [GitLab Basics](https://docs.gitlab.com/ee/gitlab-basics/README.html)

### Step One: Setup your SHA key
   First - make sure you have a SHA key set up in GitLab so you can easily synchronize your Git repository with GitLab: Follow the instructions about how to [Set up SHA key](https://docs.gitlab.com/ee/gitlab-basics/create-your-ssh-keys.html).

:20

### Step Two: Get and Configure Git
   1. [Check if Git has already been installed](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#check-if-git-has-already-been-installed)
   1. [Install and Configure Git](https://docs.gitlab.com/ee/gitlab-basics/start-using-git.html#add-your-git-username-and-set-your-email)
   1. [Clone about.gitlab.com](https://gitlab.com/gitlab-com/www-gitlab-com/tree/master#use-docker-to-render-the-website) Use the command in step 1 to clone the website.

<hr>

### Everyone needs a Middleman.   

:30

Install Docker and then configure a docker container we call **“Middleman”** that builds and runs about.gitlab.com locally on your computer.

#### What’s docker?

>"Docker is a tool designed to make it easier to create, deploy, and run applications by using containers. Containers allow a developer to package up an application with all of the parts it needs, such as libraries and other dependencies, and ship it all out as one package." (from https://opensource.com/resources/what-docker)

#### Step Three: Get Docker and configure Middleman:
   1. [Download and install the Mac version of Docker](https://www.docker.com/get-started)
   1. You will be asked to create a docker account, then download and install docker
   1. Configure Docker to build and run a local copy of about.gitlab.com  <br>
   <br>

   **Read and follow step 2 of the about.gitlab.com read.me file for the exact command:** <br>
   - [Middleman Create command / instructions](https://gitlab.com/gitlab-com/www-gitlab-com?nav_source=navbar#use-docker-to-render-the-website)<br>
   **Important Note:** Make sure you are in the directory ABOVE where the Git copy of the website lives (`www-gitlab-com`) .   <br>Typically you should be in your **home directory**.

   FYI: If you have problems installing Docker, check out the Docker troubleshooting tips at the end of this page.
   1. a few docker commands you will need: <br>
      To start middleman: `docker start middleman` <br>
      To see middleman logs: `docker logs -f middleman` (type `control + c` to exit the logs program) <br> 
      To stop middleman:  `docker stop middleman`

<hr>
### Test it: Does it work locally?

:35

You should be able to check everything out.

|  1. Open a browser and type: `localhost:4567` <br> in the url. If middleman is **NOT** started, then you will see this response in the browser window. |  ![middleman NOT Started](/images/workshop/middleman_not_running.png){: .margin-right20 .margin-left20 .margin-top20 .margin-bottom20 .image-width50pct } |
| 2. Go to your terminal window and start middleman. <br>  `docker start middleman`<br>  |  ![start middleman](/images/workshop/start_middleman.png)  |
| 3. Now, refresh your browser to see the web site. <br> First you will see this response.  Notice how it is different from the first message.  This tells you it is starting. | ![Middleman Starting](/images/workshop/middleman_just_started.png){: .margin-right20 .margin-left20 .margin-top20 .margin-bottom20 .image-width50pct } |
| After a few minutes, refresh the browser and you should see the website. |  ![middleman running](/images/workshop/middleman_running.png)  |

<hr>

### Get a development tool to make it easier.

1. Get an IDE (such as Atom)  [Download and install Atom](https://atom.io/)

note:  If you have preferred IDE, use it.  Atom works for me.

<hr>

### Working Remotely.  (my workflow)

:40

|  **Step**   | **What it looks like** |
| 1. In gitlab.com Create a new branch of about.gitlab.com   call it “name_of_branch” | ![new branch](/images/workshop/1_new_branch.png)   ![new branch](/images/workshop/2_create_branch.png) |
| 2. In gitlab.com - create a new MR for the branch I just created  | ![Create MR](/images/workshop/3_create_mr.png) ![MR Title](/images/workshop/4_mr_title.png) ![MR Details](/images/workshop/5_mr_details.png) |
| 3. In the MR - click on Checkout Branch and copy the commands | ![Checkout Branch](/images/workshop/6_checkout_branch.png) ![Copy Git Commands](/images/workshop/7_copy_git_commands.png)|
| 4. Local:   Open terminal | ![open terminal](/images/workshop/open_terminal.png)|
| 5. Local:   navigate to the Git directory where about.gitlab.com is stored.   Command: cd ww*   (use the wildcard * so I don’t have to type out ‘www.gitlab.com’ | ![Change Director](/images/workshop/terminal_cd.png) |
| 6. Local: Start the website running locally:  in the terminal type: docker start middleman  <br>   - this tells docker to start the container named middleman | ![Start middleman](/images/workshop/start_middleman.png)  |
| 7. Local: in the terminal Paste the checkout commands and hit enter <br>   - this will refresh your local copy of the project (website) with all the changes <br>  - and will tell git to point to the branch that you’ve created. | ![Paste terminal](/images/workshop/8_paste_in_terminal.png) ![Checkout Command (hit enter)](/images/workshop/9_checkout_command.png)  |
| 8. Local: Open Atom - the IDE to make edits. <br>   1. Local: in Atom - make a change to a file <br>    2. Local: in Atom - save the change  You can either go to the menu `file -> save`, or use the `command+s` key combination.|  ![Atom Editing File](/images/workshop/atom_editing_file.png) |
| 9. Local: in Browser- in the URL window - type: http://localhost:4567/ <br> - This will show you what the Middleman container sees in your local files.  You will instantly (almost) see the changes after you’ve saved your changes. |  ![middleman running](/images/workshop/middleman_running.png) |
| 10. Local: in Atom - make and save more changes.   | ![Atom IDE](/images/workshop/atom_editing_file.png) |
| 11. Local: in Browser - review changes  | ![middleman running](/images/workshop/middleman_running.png)  |
| 12. Local: when you’re done.  In Atom - On the ‘git tab’.   <br>   1. Stage your change <br>   2. Type a commit message that summarizes your change<br>   3. Click Commit to commit your changes to your local branch <br>   - keep working. (making changes, reviewing, committing)... But all of your work is only on your local workstation.  |  ![Atom Stage Changes](/images/workshop/atom_stage_changes.png)  ![Atom commit changes](/images/workshop/atom_commit_changes.png) ![Atom push changes](/images/workshop/atom_push_changes.png)  |
|  13. When you’re ready to push your changes back to the server.   Click on Push (command in lower right corner of Atom window) <br> - When you Push, your commits to your branch will be sent to the Git server.  GitLab will see these changes and kick off a pipeline to build, test and deploy your changes to a review app.  | ![Pipeline Running](/images/workshop/push_pipeline_running.png)  |
| 14. In gitlab.com: When the pipeline finishes, review your changes and then have someone Approve your Merge Request.  |  |
| 15. Local: when you are done working on this branch, delete the local branch. Use 'git branch' command to view all local branches and 'git branch -d your branchname' to delete the local branch | [Delete Branch](/images/workshop/102-git-branch-delete.png) |

### Summary:
- Git
- Docker
- Terminal
- IDE

### Docker Troubleshooting:
If Docker does not seem to work, here are a few tips:
1. Look at the status of the container:  run the following command in the terminal window:
`docker container ls -a`

1. If you need to delete your containers to rebuild them:
`docker container prune`

1. If you need an alternative way to build and run your docker middleman container:
Be sure that you’re in the `www-gitlab-com` directory, and execute:
    1. `cd sites/mysite` (see [monorepo docs](https://gitlab.com/gitlab-com/www-gitlab-com/-/blob/master/doc/monorepo.md) for more details)
    1. ```docker run --rm --name middleman -v "$PWD":/site -w /site -p 4567:4567 -e LC_ALL=C.UTF-8 ruby /bin/bash -c 'bundle install && bundle exec middleman'```

With `run` instead of `create` you will not need to call additional `docker start middleman` next. And `--rm` will ensure, that when exited, the container will be removed so it will not complain next time when you will try to create another one with the same name.
