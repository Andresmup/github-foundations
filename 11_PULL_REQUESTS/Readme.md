# PULL REQUESTS

A Pull Request (PR) is a format process to put forth changes, that can be manually or automatically reviewed before its accepted into your base (main) branch.

<ins>A pull request is not a feature of Git, but a worflow. Github can automate the Pull Request workflow</ins>

Some benefits of PR:
 - Collaborative Review: Enhaces code quality through team discussions and peer feedback.
 - Change Tracking: Provides a record of code changes and related discussions.
 - Automate Testing: Enables integration with tools for automated checks and tests
 - Controlled Integration: Manage safe and reviewed merging of code changes.
 - Open source friendly: Simplifies contributions and collaboration in open-source projects.

Pull requests let you tell others about changes you've pushed to a branch in a repository on GitHub. Once a pull request is opened, you can discuss and review the potential changes with collaborators and add follow-up commits before your changes are merged into the base branch.

Some goods practices:
 - If you're working in the shared repository model, **use a topic branch for your pull request**. While you can send pull requests from any branch or commit, with a topic branch you can push follow-up commits if you need to update your proposed changes.
 - Be very careful when force pushing commits to a pull request. Force pushing changes the repository history and can corrupt your pull request. **If other collaborators branch the project before a force push, the force push may overwrite commits that collaborators based their work on.**


## REVIEWING PROPOSED CHANGES IN A PR

In a pull request, you can review and discuss commits, changed files, and the differences (or "diff") between the files in the base and compare branches. You can review changes in a pull request one file at a time.

</ins>A progress bar in the pull request header shows the number of files you've viewed. After reviewing as many files as you want, you can approve the pull request or request additional changes by submitting your review with a summary comment. <ins>


> [!TIP]
>  While reviewing the files in a pull request, you can leave individual comments on specific changes. After you finish reviewing each file, you can mark the file as viewed. This collapses the file, helping you identify the files you still need to review.

Starting a review: 
1. Under your repository name, click `Pull requests`.
2. In the list of pull requests, click the pull request you'd like to review.
3. On the pull request, click `Files changed`.
    - You can change the format of the diff view in this tab by clicking `settings` and choosing the unified or split view. The choice you make will apply when you view the diff for other pull requests.
    - You can also choose to hide whitespace differences. The choice you make only applies to this pull request and will be remembered the next time you visit this page.
4. Optionally, filter the files to show only the files you want to review or use the file tree to navigate to a specific file. 
5. Hover over the line of code where you'd like to add a comment, and click the `blue comment icon`. To add a comment on multiple lines, click and drag to select the range of lines, then click the `blue comment icon`.
6. In the comment field, type your comment.
7. Optionally, to suggest a specific change to the line or lines, click , then edit the text within the suggestion block.
8. To comment directly on a file, to the right of the file, click  and type your comment.
9. When you're done, click Start a review. If you have already started a review, you can click Add review comment.

> [!NOTE]  
> Before you submit your review, your line comments are pending and only visible to you. You can edit pending comments anytime before you submit your review. To cancel a pending review, including all of its pending comments, click **Review changes** above the changed code, then click **Abandon review**.

## CREATE PULL REQUESTS

Create a pull request to propose and collaborate on changes to a repository. These changes are proposed in a branch, which ensures that the default branch only contains finished and approved work.

Anyone with read access to a repository can create a pull request.

> [!TIP]  
> If you want to create a new branch for your pull request and do not have write permissions to the repository, you can fork the repository first. 

You can specify which branch you'd like to merge your changes into when you create your pull request. Pull requests can only be opened between two branches that are different.

You can link a pull request to an issue to show that a fix is in progress and to automatically close the issue when someone merges the pull request.

> [!IMPORTANT]  
> Remember:
> - **Base**: Who we are going to merge into
> - **Head**: The changes to pull in

### Github CLI
The Github CLI can be use to create a PR from a branch

Here is a example

```sh
git checkout -b new_branch #Create and checkout a branch named new_branch in a single command
git commit -am "Commit message" #After making code changes, add and commit in a single command
git push -u origin new_branch #Push upstream the new branch
gh pr create --base main --head new_branch #Create PR from new_branch into main
```

### Github UI
You can create a PR using Github in the browser.

Steps for creating the pull request using Giithub UI:
1. On GitHub.com, navigate to the main page of the repository.
2. In the "Branch" menu, choose the branch that contains your commits.
3. Above the list of files, in the yellow banner, click <kbd>Compare & pull request</kbd> to create a pull request for the associated branch.
4. <ins>Use the base branch dropdown menu to select the branch you'd like to merge your changes into, then use the compare branch drop-down menu to choose the topic branch you made your changes in.</ins>
5. To create a pull request that is ready for review, click <kbd>Create Pull Request</kbd>. To create a draft pull request, use the drop-down and select <kbd>Create Draft Pull</kbd> Request, then click Draft Pull Request.


## BASE AND COMPARE

Pull requests display diffs to compare the changes you made in your topic branch against the base branch that you want to merge your changes into.

> [!IMPORTANT]  
> You can also compare forks this is how a fork stay up to date, or how forks cansuggest you to accept their changes.


Base and compare determines the direction of the merge for a pull request.

> [!WARNING]  
> Remember:
> - **Base**: Who we are going to merge into
>      - This is  usually main branch or an enveiromental specific branch
> - **Compare**: The changes to pull in
>      - Compare is choosing a Head <ins>ref</ins>
>      - This usually a bug or feature branch


## DRAFT PULL REQUEST

A Draft Pull Request on Github is a feature that allows you to open a pull request but mark it as work in progress (WIP)

Use case of Draft Pull Request:
 - Indicating Work-In-Progress: Comunicate that the pull request is not ready for review or merging.
 - Preventing Premature Merging: Ensures incomplete work is not accidentally merged.
 - Facilitating Early Feedback and Collaboration: Allows for early sharing and discussion of code changes.
 - Continuos Integration Testing: Enables CI test during the development process.
 - Transitioning to Ready State: Easy switch from draft to ready for final review and merging.
 - Organizing Work and Priorities: Help in managing and tracking ongoing work in large projects.

> [!CAUTION]  
> Must remember:
> - Draft Pull Requests cannot be merged unless it set as ready
> - Code owners are not automatically requested to review draft pull requests.
> - Marking a pull request as ready for review will request reviews from any code owners. 
> - You can convert a pull request to a draft at any time. 

## LINKING ACTIVITY

You can link Issues to PR so that the state of the pull request will automatically close the issue

You can link a pull request to an issue by using a supported keyword in the pull request's description or in a commit message.

> [!IMPORTANT]  
> The PR must be on the default branch.

## STATUSES

- **Open**: The default status when a PR is created. It's open for discussion and review.
- **Draft**: Indicates the PR is in work-in-progress (WIP) and not ready for review.
- **Closed**: The PR has been closed with being merged. The status is used whem the propose changes are no longer needed or if the branch has been rejected.
- **Merged**: The PR's changes have been merged into the target branch. This status indicates a sucessful conclusion of the PR.
- **Changes Requested**: This status is used during the review process when the reviewer requests change before the PR can be merged.
- **Review Required**: Indicate that the PR requires a review before it can be merged. This status is common in repositories where reviews are a mandatory part of the workflow.
- **Aproved**: The PR has been reviewed and approved for merging by the required number of reviewers.
- **Conflic**: Indicates that the are conflicts between the PR's branch and the target branch that need to be resolved before merging.
- **Ready for review**: A PR initially marked as draft can be changed to the status once is ready for review.

## COMMENTING IN PR

When you comment you are submitting a review to be considered before a PR is being accepted.

<ins>If you are not the author, but also a designated reviewer you can request changes as mark the PR as approved so it can be considered for merging.</ins>

Under Files Changed you can also apply a review on a very specific line of code.

## PERMANENT LINK TO FILES

> [!IMPORTANT]
> When viewing a file on GitHub.com, you can press the <kbd>"y"</kbd> key to update the URL to a permalink to the exact version of the file you see.

For a permanent link to the specific version of a file that you see, instead of using a branch name in the URL (i.e. the `main` part in the example above), put a commit id. This will permanently link to the exact version of the file in that commit.

Replaces main with a specific commit id and the file content will not change.

Looking up the commit SHA by hand is inconvenient, however, so as a shortcut you can type y to automatically update the URL to the permalink version. Then you can copy the URL knowing that anyone you share it with will see exactly what you saw.

## PERMANENT LINK TO A CODE SNIPPET

You can create a permanent link to a specific line or range of lines of code in a specific version of a file or pull request.

This type of permanent link will render as a code snippet only in the repository it originated in. In other repositories, the permalink code snippet will render as a URL.

1. On GitHub.com, navigate to the main page of the repository:
2. Locate the code you'd like to link to:
- To link to code from a file, navigate to the file.
- To link to code from a pull request, navigate to the pull request and click `Files changed`. Then, browse to the file that contains the code you want include in your comment, and click View.
3. Choose whether to select a single line or a range.
- To select a single line of code, click the line number to highlight the line.
- To select a range of code, click the number of the first line in the range to highlight the line of code. Then, hover over the last line of the code range, press <kbd>Shift</kbd>, and click the line number to highlight the range.
4. To the left of the line or range of lines, click the three dots icon `...` In the drop-down menu, click `Copy permalink`.
5. Navigate to the conversation where you want to link to the code snippet.
6. Paste your permalink into a comment, and click `Comment`.

## COMMITING CHANGES IN PR BRANCH FROM A FORK

You can commit changes on a pull request branch that was created from a fork of your repository with permission from the pull request creator.

You can only make commits on pull request branches that:
- are opened in a repository that you have push access to and that were created from a fork of that repository
- are on a user-owned fork
- have permission granted from the pull request creator
- don't have branch restrictions that will prevent you from committing

Only the user who created the pull request can give you permission to push commits to the user-owned fork.

## CODEOWNERS

Codeowners is a Github repo specific file to deine individuals or teams that are responsable for specific code in a repository.

Codeowners use a similar syntax to .gitignore.

> [!NOTE]  
> When a PR is opened that modifies any files matching a pattern in the CODEOWNERS file, Github automatically requestes a review from the specifed code owners.

Codeowners files goes in either the project root, .github and docs directory.

## PR OPTIONS

When merging a PR the are few options:
1. **Create a merge commit**: All commits will be added.
2. **Squash and rebase**: 1 commit will be added.
3. **Rebase and merge**: 1 commit will be added and rebase.

The use-case depends on your team's workflow. They may prefer only a single commit is added to keep the base branch clean and readable.

## REQUIRED REVIEWERS

PR can have multiple required reviewers who must write a review that appoves the changes.

If your repository requires reviews, pull requests must have a specific number of approving reviews from people with *write* or *admin* permissions in the repository before they can be merged.

You can comment on a pull request, approve the changes, or request improvements before approving.

> [!TIP]
> You can find a pull request where you or a team you're a member of is requested for review with the search <kbd>qualifier review-requested:[USERNAME]</kbd> or <kbd>team-review-requested:[TEAMNAME]</kbd>

> The review is expected -> The review with Approve is provided -> The changes are approved passing the check for the repo.

## TEMPLATES

PR templates are similar to Issues Templates. The will populate the PR request text area with the specific template.

**You can create the file in the .github/pull_request_template.md**

Technically you create a multiple PR Template in a folder called .github/PULL_REQUEST_TEMPLATE

Github kind of supports multiple PR Templates but you have to assemble your own URL with a querystring, so its not a convenient to use as multiple Issue Templates