# ACTIONS

Github actions is CI/CD pipeline directly integrated with your Github Repository.

Within a Github repo you'll have a tab for Actions.

Github actions allows you to automate:
- Running test suites
- Building images
- Compiling static sites
- Deploy code to servers
- and more...

Github Actions has templates you can use to get started.

Github Actions files are defined as YAML files located in the `.github/workflow` folder of your repo. You can have multiple workflows in a repo triggered by different events.


When you run Github Actions you'll get a history of workflows runs where it will indicate if it was success, failure, in progress and how long it took to run it.

## FINDING GITHUB ACTIONS

In Actions repository starter-workflow are examples of workflows, that you can use to get started. https://github.com/actions/starter-workflows

## BASIC SYNTAX WORKFLOW

> [!IMPORTANT]
> Here are some of the important words in the Github Action yaml file syntax.
> - **name** GitHub displays the names of your workflows under your repository's "Actions" tab.
> - **on** This attribute specifies the <ins>event trigger</ins> to be used. Example: `on: [push]`
> - **runs-on** Define the type of machine to run the job on, some common options are `ubuntu-latest` `windows-latest` `macos-latest`
> - **jobs** A workflow run is made up of one or more jobs, which run in parallel by default.
> - **steps** A job contains a sequence of tasks called steps. Steps can run commands, run setup tasks, or run an action in your repository, a public repository, or an action published in a Docker registry. 
> - **runs** In a job each step runs command-line programs using the operating system's shell.
> - **uses** In a job selects an action to run as part of a step in your job. An action is a reusable unit of code. 



## EVENT TYPES

Event Triggers causes a Github Action to run.

Github Actions has 35+ events triggers.

> [!WARNING]  
> For the exam you should remember this ones for sure:
> - **push**: Trigger action on any push to the repository.
> - **pull_request**: Run actions when pull request are opened, synchronize, reopened, updated or merged.
> - **branch_protection_rule**: Runs your workflow when branch protection rules in the workflow repository are changed.
> - **issues**: Execute actions base on issue activities, like creation or labeling.
> - **release**: Automate workflows when a new release is published.
> - **registry_package**: Runs your workflow when activity related to GitHub Packages occurs in your repository.
> - **repository_dispatch**: Allow to use the GitHub API to trigger a workflow for activity that happens outside of GitHub.
> - **gollum**: Runs your workflow when someone creates or updates a Wiki page.
> - **watch**: Runs your workflow when the workflow's repository is starred. 
> - **fork**: Runs your workflow when someone forks a repository.
> - **schedule**: Schedule actions to run at specific times (events).
> - **workflow_dispatch**: Allow manual triggering of action the Github UI.
> - **workflow_call**: Is used to indicate that a workflow can be called by another workflow. 
> - **workflow_run**: This event occurs when a workflow run is requested or completed. 


Be aware that also exists:
- **check_run**: Runs your workflow when activity related to a check run occurs. A check run is an individual test that is part of a check suite.
- **check_suite**: Runs your workflow when check suite activity occurs. A check suite is a collection of the check runs created for a specific commit.
- **create**: Runs your workflow when someone creates a Git reference (Git branch or tag) in the workflow's repository.
- **delete**: Runs your workflow when someone deletes a Git reference (Git branch or tag) in the workflow's repository.
- **status**: Runs your workflow when the status of a Git commit changes (error, failure, pending, or success).
- **deployment**: Runs your workflow when someone creates a deployment in the workflow's repository.
- **deployment_status**: Runs your workflow when a third party provides a deployment status. 
- **discussion**: Runs your workflow when a discussion in the workflow's repository is created or modified.
- **discussion_comment**: Runs your workflow when a comment on a discussion in the workflow's repository is created or modified. 
- **issue_comment**: Runs your workflow when an issue or pull request comment is created, edited, or deleted.
- **label**: Runs your workflow when a label in your workflow's repository is created or modified.
- **milestone**: Runs your workflow when a milestone in the workflow's repository is created or modified. 
- **merge_group**: Runs your workflow when a pull request is added to a merge queue, which adds the pull request to a merge group. 
- **page_build**: Runs your workflow when someone pushes to a branch that is the publishing source for GitHub Pages, if GitHub Pages is enabled for the repository. 
- **project**: Runs your workflow when a project (classic) is created or modified. 
- **project_card**: Runs your workflow when a card on a project (classic) is created or modified. 
- **project_column**: Runs your workflow when a column on a project (classic) is created or modified. 
- **public**: Runs your workflow when your workflow's repository changes from private to public. 
- **pull_request_review**: Runs your workflow when a pull request review is submitted, edited, or dismissed. 
- **pull_request_target**: Runs your workflow when activity on a pull request in the workflow's repository occurs. 