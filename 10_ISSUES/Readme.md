# ISSUES

Use GitHub Issues to track ideas, feedback, tasks, or bugs for work on GitHub.

GitHub Issues are items you can create in a repository to plan, discuss and track work.

Issues are simple to create and flexible to suit a variety of scenarios. You can use issues to track work, give or receive feedback, collaborate on ideas or tasks, and efficiently communicate with others.

> [!TIP]
> Issues let you track your work on GitHub. When you mention an issue in another issue or pull request, the issue's timeline reflects the cross-reference so that you can keep track of related work.
> 
> To indicate that work is in progress, you can link an issue to a pull request. When the pull request merges, the linked issue automatically closes.


Repository administrators can disable issues for a repository.

## CREATING ISSUES

Issues can be created in a variety of ways, so you can choose the most convenient method for your workflow. 

Opening an Issue is straight forward.

### Github UI

It can be done via Github UI. If your repository uses issue templates, next to the type of issue you'd like to open, click Get started.

If the type of issue you'd like to open isn't included in the available options, click Open a blank issue.
Just need a title and a markdown supported description.

> [!IMPORTANT]  
> Remember that only if you're a project maintainer: 
> - You can assign the issue to someone
> - Add it to a project (classic)
> - Associate it with a milestone
> - Apply a label.

### Github CLI

To create an issue, use the gh issue create subcommand. To skip the interactive prompts, include the `--body` and the `--title` flags.

```sh
gh issue create --title <title> --body <details>
```

You can also specify assignees, labels, milestones, and projects.

```sh
gh issue create --title <title> --body <details> --assignee <user> --label <label> --project <project> --milestone <milestone>
```

### From a comment

You can open a new issue from a comment in an issue or pull request. When you open an issue from a comment, the issue contains a snippet showing where the comment was originally posted.

Just follow this steps:
 - Navigate to the comment that you would like to open an issue from.
 - In that comment, click the 3 dots <kbd>***</kbd>.
 - Click **Reference in new issue** and complete the form.

### From code

You can open a new issue from a specific line or lines of code in a file or pull request. When you open an issue from code, the issue contains a snippet showing the line or range of code you chose.

<ins>You can only open an issue in the same repository where the code is stored.</ins>

Remember to follow this steps:

1. Locate the code you want to reference in an issue:
   - To open an issue about code in a file, navigate to the file.
   - To open an issue about code in a pull request, navigate to the pull request and click **<kbd>+-</kbd>** Files changed. Then, browse to the file that contains the code you want included in your comment, and click `View`.

2. Choose whether to select a single line or a range.
   - To select a single line of code, click the line number to highlight the line.
   - To select a range of code, click the number of the first line in the range to highlight the line of code. Then, hover over the last line of the code range, press <kbd>Shift</kbd>, and click the line number to highlight the range.

3. To the left of the code range, click the 3 dots <kbd>***</kbd>. In the dropdown menu, click **Reference in new issue** and complete the form.

### From discussion

People with triage permission to a repository can create an issue from a discussion.

When you create an issue from a discussion, the contents of the discussion post will be automatically included in the issue body, and any labels will be retained.

> [!NOTE]  
> Creating an issue from a discussion does not convert the discussion to an issue or delete the existing discussion. 

You only need to:
 - In the list of discussions, click the discussion you want to view.
 - In the right sidebar, click **Create issue from discussion** and complete the form.


## ISSUE BEST PRACTICES

First, create an issue. There are multiple ways to create an issue; you can choose the most convenient method for your workflow. 

### Information

Give your issue a descriptive title. The title should convey at a glance what the issue is about.

Add a description that explains the purpose of the issue, including any details that might help resolve the issue. For example, if this is a bug report, describe the steps to reproduce the bug, the expected result, and the actual result.

You can use markdown to add formatting, links, emojis, and more.

### Add a task list

It can be helpful to break large issues into smaller tasks, or to track multiple related issues in a single larger issue

Add a task list to your issue by prefacing list items with <kbd>[ ]</kbd>. Reference existing issues by issue number or URL. 

### Adding labels 

Add a label to categorize your issue to indicate that an issue is a bug that a first-time contributor could pick up. Users can filter issues by label to find all issues that have a specific label.

You can use the default labels, or you can create a new label.

### Milestone

You can add a milestone to track the issue as part of a date based target. A milestone will show the progress of the issues as the target date approaches.

### Assigning the issue

To communicate responsibility, you can assign the issue to a member of your organization.

Assignees clarify who is working on specific issues.

You can assign multiple people to each issue or pull request, including yourself, anyone who has commented on the issue or pull request, anyone with write permissions to the repository, and organization members with read permissions to the repository. 

<ins>Issues and pull requests in public repositories, and in private repositories for a paid account, can have up to 10 people assigned. Private repositories on the free plan are limited to one person per issue or pull request.</ins>

### Communicating
After your issue is created, continue the conversation by adding comments to the issue. You can `@mention` collaborators or teams to draw their attention to a comment.

To link related issues in the same repository, you can type <kbd>#</kbd> followed by part of the issue title and then clicking the issue that you want to link. 

## LINK PR TO ISSUE

You can link a pull request or branch to an issue to show that a fix is in progress and to automatically close the issue when the pull request or branch is merged.

You can link an issue to a pull request manually or using a supported keyword in the pull request description.

When you link a pull request to the issue the pull request addresses, collaborators can see that someone is working on the issue.

> [!IMPORTANT]  
> When you merge a linked pull request into the default branch of a repository, its linked issue is automatically closed. 

### Keywords

You can link a pull request to an issue by using a supported keyword in the pull request's description or in a commit message. The pull request must be on the default branch.

- `close`
- `closes`
- `closed`
- `fix`
- `fixes`
- `fixed`
- `resolve`
- `resolves`
- `resolved`

<ins>If you use a keyword to reference a pull request comment in another pull request, the pull requests will be linked. Merging the referencing pull request also closes the referenced pull request.</ins>

### Manually linking PR with sidebar

Anyone with write permissions to a repository can manually link a pull request or branch to an issue from the pull request sidebar.

You can manually link up to ten issues to each pull request. The issue and pull request must be in the same repository.

1. Under your repository name, click <kbd>Pull requests</kbd>.
2. In the list of pull requests, click the pull request that you'd like to link to an issue.
3. In the right sidebar, click <kbd>Development</kbd>.
4. Click the issue you want to link to the pull request.


### Manually linking branch with sidebar

Anyone with write permission to a repository <ins>can create a branch for an issue.</ins> **You can link multiple branches for an issue.**

By default, the new branch is created in the current repository, and from the default branch.

Follow the steps:
1. Under your repository name, click Issues.
2. In the list of issues, click the issue that you would like to create a branch for.
3. In the right sidebar under "Development", click <kbd>Create a branch</kbd>. If the issue already has a linked branch or pull request, select and click Create a branch.
   - Optionally, in the "Branch name" field, type a branch name.
   - Optionally, select the Repository destination dropdown menu, then choose a repository.
4. Under "What's next", select whether you want to work on the branch locally or to open the branch in GitHub Desktop.
5. Click Create branch.

> [!IMPORTANT]  
> Using the ID of the related issue in the branch name makes it easy to identify the task and keep track of its progress. Combine ID of issues with key words for the respective task. 
> - A common workflow is creating Feature or Bug branches, and defining the Issue up front to identify it quickly.


## VIEW ALL YOUR ISSUES

The <ins>Issues and Pull Request dashboards list the open issues and pull requests you've created.</ins> You can use them to update items that have gone stale, close them, or keep track of where you've been mentioned across all repositories—including those you're not subscribed to.

Your issue and pull request dashboards are available at the top of any page. On each dashboard, you can filter the list to find issues or pull requests you created, that are assigned to you, or in which you're mentioned. *You can also find pull requests that you've been asked to review.*

 - At the top of any page, click to see your issues or to see your pull requests.
 - Optionally, choose a filter or use the search bar to filter for more specific results.

## PIN ISSUE

You can *pin up to three important issues* above the issues list in your repository.

> In the list of issues, click the issue you'd like to pin. -> In the right sidebar, click <kbd>Pin issue</kbd>.


## TRANSFER ISSUE

To move an issue to a better fitting repository, you can transfer open issues to other repositories.

To transfer an open issue to another repository, you must have write access to the repository the issue is in and the repository you're transferring the issue to. 

When you transfer an issue, comments and assignees are retained. Labels and milestones are also retained if they're present in the target repository, with labels matching by name and milestones matching by both name and due date. 

People or teams who are mentioned in the issue will receive a notification letting them know that the issue has been transferred to a new repository. The original URL redirects to the new issue's URL.

> In the list of issues, click the issue you'd like to transfer. -> In the right sidebar, click <kbd>Transfer issue</kbd>.
>
> Select the Choose a repository dropdown menu, and click the repository you want to transfer the issue to.
>
> Click <kbd>Transfer issue</kbd>.


## CLOSE AN ISSUE

You can close an issue when bugs are fixed, feedback is acted on, or to show that work is not planned.

*Repository owners, collaborators on repositories owned by a personal account, and people with triage permissions or greater on repositories owned by an organization can close issues opened by others.*

> In the list of issues, click the issue you'd like to close.
> 
> Optionally, to change your reason for closing the issue, next to "Close issue," select the arrow, then click a reason.
> 
> Click <kbd>Close issue</kbd>.

## DELETE AN ISSUE

People with admin permissions in a repository can permanently delete an issue from a repository.

Collaborators do not receive a notification when issues are deleted. 

People with admin or owner permissions in the repository will additionally see the username of the person who deleted the issue and when it was deleted.

> Navigate to the issue you want to delete.
> 
> On the right side bar, under "Notifications", click <kbd>Delete issue</kbd>.
> 
> To confirm deletion, click <kbd>Delete this issue</kbd>.


## ISSUE TEMPLATES

<ins>Issue Templates are markdown templates that are preloaded for new issues</ins>. They help ensure creating issues provide all the relevant and expected information.**You can create multiple issues templates to better improve the context of issues.**

> [!IMPORTANT]  
> The 3 default ones are:
> - **Bug report** *Create a report to help us improve* (Get Started)
> - **Feature Request** *Suggest an idea for this repository* (Get Started)
> - **Custom Issue Template** *Describe the issue template's purpose here* (Get Started)
> - **Report Security Vulnerability** *Report a security vulnerability* (Report a vulnerability)

With issue templates, you can customize and standardize the information you'd like contributors to include when they open issues in your repository.

You can customize the templates that are available for contributors to use when they open new issues in your repository.

When you create issue templates for your repository using the issue template builder or with issue forms, contributors can select the appropriate template when they open new issues in the repository.



> [!TIP]
> You can customize the issue template chooser that people see when creating a new issue in your repository by adding a `config.yml` file to the `.github/ISSUE_TEMPLATE` folder. 
>
> **Github has a wizard GUI to easily create Issue Templates**


## ISSUE FORMS

<ins>Issue forms is the evolution of Issue Templates. You use a YAML formatted file to create Issue forms for stricter entry of issue information.</ins>

With issue forms, you can create issue templates that have customizable web form fields. You can encourage contributors to include specific, structured information by using issue forms in your repository. Issue forms are written in YAML using the GitHub form schema. 

Issue templates are helpful when you want to provide guidance for opening issues while allowing contributors to specify the content of their issues. If you want contributors to provide specific, structured information when they open issues, issue forms help ensure that you receive your desired information.

With issue forms, you can create templates that have web form fields using the GitHub form schema. When a contributor opens an issue using an issue form, the form inputs are converted to a standard markdown issue comment. 


### Issue forms and templates comparison

The differences between GitHub issue templates and issue forms:

 - Issue templates are text files that contain pre-written text that can be used to create new issues.
   - They are typically used to provide a consistent format for issues, and to help contributors provide all of the information that is needed to resolve the issue.
 - Issue forms are web forms that can be used to create new issues.
   - They are typically used to collect more structured information from contributors, and to make it easier for contributors to provide the information that is needed to resolve the issue.

Here is a table that summarizes the key differences between issue templates and issue forms:


| Feature | Issue templates |Issue forms| 
| --- | --- | ---| 
| Format| Markdown| YAML| 
| Customization	| Limited	| Extensive| 
| Data collection| 	Basic| 	Structured| 
| Ease of use| 	Easy to use for simple issues| More complex to use, but more powerful| 


> [!NOTE]  
> Ultimately, the best choice for your project will depend on your specific needs. If you need a simple way to provide a consistent format for issues, then issue templates are a good option.
> 
> If you need to collect more structured information from contributors, or if you want to make it easier for contributors to provide the information that is needed to resolve the issue, then issue forms are a better option.


## MILESTONES

Millestone allow you to gruop multiple issues into and end goal which show completitions towards the goal for each closed issues.

- You can associate one by one issues to milestones in the issue page by selecting the milestone in the auxiliar panel
- You can associate multiple issues to milestones by click on the check box of the issue in the issue repository tab an selecting de milestone to be associated with