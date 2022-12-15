# Contributing to the Data Analytics & Python curriculum

We welcome contributions from everyone and appreciate your consideration in helping us to improve our documentation.  

## Sprints

We work in 12 week sprints that align from the cohort Orientation day to cohort Orientation Day.

Enhancement and Bug Issues are created in the respective project repositories under the Issues tab.

Each issue will be placed in the appropriate swimlane and prioritized on a routine basis as meeting times allow.

## Issue reporting

We encourage people to report issues whether a bug or enhancement. The most important advice from there is:

1. Do as thorough a search as you can to see whether the issue has already been reported
1. Be as precise and complete as you can when reporting a new issue.

### To report a issue

- Go to the appropriate repository
  - [DAP Curriculum](https://github.com/savvy-coders/dap-curriculum)
  - [DAP Teacher's Guide](https://github.com/savvy-coders/dap-teachers-guide)
- Click the Issues button on the left of the window
- Click the "New issue" button
- Fill out the Title and the prepopulated template within Description
- Assign the appropriate labels (Bug or Enhancement are required)
- Assign the Projects to 'DAP Curriculum'
- Leave Milestone as 'No Milestone' unless otherwise directed

After you create an issue, the team will assign a priority to the issue, ensure it is labeled properly, and perhaps request additional information from you.

## Select an issue

Please review the issues on the [DAP Curriculum kanban board](https://github.com/orgs/savvy-coders/projects/3) and select an issue.

### The columns in the kanban board are as follows:

<dl>
  <dt>Ideas</dt>
  <dd>A swimlane for issues that are considered ideas but not worked until additional debate and consideration</dd>
  <dt>Intake</dt>
  <dd>A swimlane for issues that are for future sprints or that need further details added</dd>
  <dt>Backlog</dt>
  <dd>A swimlane for issues in the current sprint backlog.</dd>
  <dt>In Progress</dt>
  <dd>A swimlane for issues currently being worked by a team member.  As an issue is assigned to themselves by a team member when they decide to pick up the issue it should be moved the In Progress</dd>
  <dt>In Review</dt>
  <dd>A swimlane for issues that the work has been completed and a pull request created</dd>
  <dt>Done</dt>
  <dd>A swimlane for issues that have been had the pull request reviewed, approved and merged</dd>
</dl>

This Backlog swimlane should be prioritized by the team during a sprint planning ceremony that occurs during the weekly curriculum meeting.

It is preferred that you select an issue from the Backlog swimlane as near the top as possible, assuming you are comfortable with the topic.  As an staff member claims an issue they should sign it to themselves it should be moved to the the In Progress swimlan immediately.

## Update the curriculum and teacher's guide

The steps included in this section should be completed for all appropriate repositories.

Review the [Style Guide](#style-guide) before making any changes

### Clone the appropriate repository (If necessary)

If necessary please follow the [Setting Up your Git and GitHub security](Section00/0.1.1-GitHub_SSH_Key.md) process outlined in the curriculum.

Open a terminal and navigate to a base folder where you would like to clone the repositories in using the `cd` command.

Example: `cd /c/git/savvy-coders`

Execute the Git clone command to create a local copy of the remote repository locally.

Example: `git clone git@github.com:savvy-coders/dap-curriculum.git`

The repository Git SSH clone paths are:

- DAP Curriculum : git@github.com:savvy-coders/dap-curriculum.git
- DAP Teacher's Guide : git@github.com:savvy-coders/dap-teachers-guide.git
  
Change directories into the newly created local repository

Example: `cd dap-curriculum`

### Update dependencies using NPM

Execute the NPM install command to update any development dependencies the project has configured.

Example: `npm install`

### Create the issue branch within your local repository

Verify that you are on the `development` branch and that it is up to date.

Example: `git checkout development` && `git pull --rebase`

We use the [Gitflow process](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) during the development process.  We use releases and tags instead of creating release branches.

Create the issue/feature branch to begin your work using a prefix of `dap-` and the issue number assigned.  There is no need to provide a description in the branch name.   The description will be added later during the commit and pull request processes.

Example: `git checkout -b dap-11`

The above command will create and checkout the branch at the same time.   You are now ready to begin altering files.

### Update the appropriate files

Open your editor and begin updating files as required by the acceptance criteria of the issue following the below [Style Guide](#style-guide).

Example `code .`

## Style Guide

- All code should be within Code Blocks using triple ticks (```) for MarkDown files or within Code blocks in Jupyter Notebook files.  This enables the "copy code block" functionality when viewing the MarkDown.

### Commit your changes to your local repository

After updates are at a place where you are comfortable with committing them to your issue branch.   Execute the following steps:

- `git status` to verify that the expected files and changes are going to be committed.
- `git add .` or `git add {filename}` for each file to be committed.
- `git commit -m"{message}"` where the message includes the branch name followed by a colon and then the description of the ticket.

Example: `git commit -m"DAP-11: Create a contribution.md document"`

### Merge latest development branch into issue branch


### Push your issue branch to the remote repository


## Create a pull request (PR) for review

- Navigate to the appropriate repository's 'Pull requests' tab
- Click the 'New pull request' button
  - There may be a 'Compare & pull request' button to create the PR for you branch, this button may be used but make sure that the destination branch is `development` and NOT `master`/`main`
- Select `development` as the compare branch and `main` as the base branch.
- The list of commits and the changed files will be displayed

## Review curriculum and teacher's guide pull requests

## Merge approved pull request (PR)

## Releasing the product of the sprint to "Production"

The release process should be done by a single designated person at the appointed time before the beginning of the next cohort.   Typically completed by the Project Lead or Project Manager the Monday prior to Orientation day.
