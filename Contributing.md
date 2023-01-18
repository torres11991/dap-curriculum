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

> ## Style Guide (Work in Progress)
>
> - All code should be within Code Blocks using triple ticks (```) for MarkDown files or >within Code blocks in Jupyter Notebook files.  This enables the "copy code block" functionality when viewing the MarkDown.

### Commit your changes to your local repository

After updates are ready to committing them to your issue branch.   Execute the following steps:

- `git status` to verify that the expected files and changes are going to be committed.
- `git add .` or `git add {filename}` for each file to be committed.
- `git commit -m"{message}"` where the message includes the branch name followed by a colon and then the description of the ticket.

Example: `git commit -m"DAP-11: Create a contribution.md document"`

### Merge latest development branch into issue branch

Once you have completed all your changes and committed them to your local repo and ready to push your issue related changes.  You should merge the latest changes from development into your issue branch so that everything is kept in sync.

- `git checkout development` to checkout the development branch locally.
- `git pull --rebase` to pull the latest changes from the remote repo.
- `git checkout {issue branch i.e.: dap-11}` to checkout your issue branch.
- `git merge development` to merge the latest changes from development

Fix any merge conflicts, then add, commit and push the merged issue branch as described above.

> #### VS Code source control documentation/tutorials:
>
> - [Using Git source control in VS Code](https://code.visualstudio.com/docs/sourcecontrol/overview)
> - [The EXTREMELY helpful guide to merge conflicts](https://www.youtube.com/watch?v=HosPml1qkrg)

### Push your issue branch to the remote repository

After all the remote changes have been merged, the issue branch is now ready to push to the remote repository.

- `git push` to push the latest local changes on the issue branch to the remote repo.

## Create a pull request (PR) for review

> As the `main` branch is protected we use the pull request process to manage changes.
> The official documentation for GitHub Pull Request can be found here:
> https://docs.github.com/en/pull-requests/collaborating-with-pull-requests

Once your issue branch is complete and pushed to the remote branch it is now time to create a pull request (PR) to be reviewed by your peers.  Post in the Slack #curriculum-team channel with the link to the PR and the story which needs to be reviewed.

- Navigate to the appropriate repository's ['Pull requests' tab](https://github.com/savvy-coders/dap-curriculum/issues) 
- Click the 'New pull request' button
  - There may be a 'Compare & pull request' button to create the PR for you branch, this button may be used but make sure that the destination branch is `development` and NOT `master`/`main`
- Select `development` as the compare branch and `main` as the base branch.
- The list of commits and the changed files will be displayed, review the lists to determine that nothing unexpected appears.
![Compare Change](img/contributing/compare-changes.jpg)
- Click the 'Create Pull Request' button
- Fill in the Title with the Issue Number and Title
  - Example: DAP-11 Create a contribution.md document
- Fill in the Description with the Issue Link
![Create Pull Request](img/contributing/create-pr.jpg)
- Assign the appropriate peers to review the changes
- Click the 'Create Pull Request' button

All reviewers will recieve a notification that they were chosen to review the pull request.

## Review curriculum and teacher's guide pull requests

Navigate to the appropriate repository and click on the pull request to be reviewed or follow the link that was in the notification.

![List of pull requests](img/contributing/pr-list.jpg)

The pull request will be displayed with the following tabs showing, Conversation, Commits, Checks and Files changed.

![Pull request conversation tab](img/contributing/pull-request-conversation.jpg)

Click on the "Files Changed" tab and review the files and code that have been updated.

Click the gear to change the "Diff view" and "Hide whitespace" as desired.

The "Viewed" checkbox can be used to collapse the file once it has been reviewed.

The "Code" (<>) and "Preview" ([]) buttons can be used to switch between views.

![Pull request files changed tab](img/contributing/review-pr-files-changed.jpg)

Comments can be left directly in the code by hovering over the line that needs to be changed and clicking the Plus that appears.  Fill out the comment text area and click "Start a review" or "Add single comment".

![](img/contributing/review-pr-review-add-code-comments.jpg)

Once you are ready to finalize your review, click the "Review Changes" or "Finish your review" button.

- If the changes are deemed appropriate with no changes needed, select the "Approve" option
- If you wish to leave a comment and not approve the changes outright, fill in the text area with the appropriate comment then select the "Comment" option
- If comments have been left in the code, fill in the text area with appropriate comment then select the "Request changes" option

Once the form is appropriately filled out click "Submit review" to finalize your review of the pull request.

![](img/contributing/review-pr-review-changes.jpg)

## Merge approved pull request (PR)

Once your pull request has the appropriate approvals, it is time to merge it into the `development` branch.

Click the "Merge pull request" and then confirm the you want to complete the merge.   The pull request is now completed.

![](img/contributing/merge-pr.jpg)

*Please delete the issue branch after a successful PR merge.*

## Releasing the product of the sprint to "Production"

The release process should be done by a single designated person at the appointed time before the beginning of the next cohort.   Typically completed by the Project Lead or Project Manager the Monday prior to Orientation day.

The instructions for this process are to be added as time allows.
