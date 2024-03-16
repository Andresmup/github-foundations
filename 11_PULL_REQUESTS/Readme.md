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