# REPOSITORIES

A repository is the most basic element of GitHub. It's a place where you can store your code, your files, and each file's revision history. Repositories can have multiple collaborators and can be either public or private.

You can own repositories individually, or you can share ownership of repositories with other people in an organization.
In either case, access to repositories is managed by permissions.

## TERMINOLOGY

|Term|Definition|
|---|---|
|Branch|A parallel version of your code that is contained within the repository, but does not affect the primary or main branch.|
|Clone|To download a full copy of a repository's data from GitHub.com, including all versions of every file and folder.|
|Fork|A new repository that shares code and visibility settings with the original "upstream" repository.|
|Merge|To take the changes from one branch and apply them to another.|
|Pull request|A request to merge changes from one branch into another.|
|Remote|A repository stored on GitHub, not on your computer.|
|Upstream|The branch on an original repository that has been forked or cloned. The corresponding branch on the cloned or forked branch is called the "downstream."|

## BASIC REPO NAVIGATION

Within a Github repo you'll have a navigation bar to the various features of your Github repo:

 - Code: The main tab where the repository's source code, files, and folder are located.
 - Issues: Tracks problems or ideas for the project, allowing collaboration and discussion.
 - Pull request: Used for managing contributions form other users, enabling code review and discussions before merging changes.
 - Actions: Manages continuos integration and contributions deployment (CI/CD) workflows.
 - Projects: A board for organazing and prioritazing work, similar to kanban or task management boards.
 - Wiki: A space for the project's documentation.
 - Security: Features security-related resources, including security policies and vulnerability reports.
 - Insights: Provides statistics and insights on the project's activity and contributions.
 - Settings: Contains repository settings, including access controls, webhooks and other configurations.


Within a Github Repo when you click into a file you can then easily navegate all repo files. Allowing to jump into specific files using the search. And see a preview of the file content.

## READMEs

Readme files are markdown files that provided documentation/instructional information.

> [!TIP]  
> If you put your README.md (or readme.md, or Readme.md) file in your repository's hidden .github, root, or docs directory, GitHub will recognize and automatically surface your README to repository visitors, this will be rendered on the Github Repo page for each access.


> [!IMPORTANT]  
> If a repository contains more than one README file, then the file shown is chosen from locations in the following order: the .github directory, then the repository's root directory, and finally the docs directory.


You can add a README file to a repository to communicate important information about your project. A README, along with a repository license, citation file, contribution guidelines, and a code of conduct, communicates expectations for your project and helps you manage contributions.

### Auto-generated table of contents for README files

For the rendered view of any Markdown file in a repository, including README files, GitHub will automatically generate a table of contents based on section headings.

### Section links in README files and blob pages

You can link directly to a section in a rendered file by hovering over the section heading to expose.

## CREATE REPOSITORY

You can create a new repository on your personal account or any organization where you have sufficient permissions.

The are three main ways to create a repository, using the web browser, the CLI or desktop app. Let's dive into the browser options:

1. In the upper-right corner of any page, select , then click New repository.

2. Other option its in the repository section of your profile, click in New.

3. Optionally, to create a repository with the directory structure and files of an existing repository, select the Choose a template dropdown menu and click a template repository. You'll see template repositories that are owned by you and organizations you're a member of or that you've used before. 

4. Optionally, if you chose to use a template, to include the directory structure and files from all branches in the template, and not just the default branch, select Include all branches.

5. Use the Owner dropdown menu to select the account you want to own the repository.

6. Type a name for your repository, and an optional description. The scope name availability its given by the account.

7. Choose a repository visibility, which can be private or public.

> [!IMPORTANT]  
> 8. If you're not using a template, there are a number of optional items you can pre-populate your repository with. If you're importing an existing repository to GitHub, don't choose any of these options, as you may introduce a merge conflict. 
>  - You can create a README.
>  - You can create a .gitignore file, which is a set of ignore rules.
>  - You can choose to add a software license for your project. 

9. Optionally, if the personal account or organization in which you're creating uses any GitHub Apps from GitHub Marketplace, select any apps you'd like to use in the repository.

10. Click Create repository.

11. At the bottom of the resulting Quick Setup page, under "Import code from an old repository", you can choose to import a project to your new repository. To do so, click Import code.
