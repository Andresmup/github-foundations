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

## REPO TEMPLATES

Github Repo Template is a feature for public and private repos that allows you and other Github users to make a copy of the contents of the template repo to use as starting point of their own repo.

A repository can be set up as template in the settings section.


### Create a repo using a template

You can generate a new repository with the same directory structure and files as an existing repository.

You can create a template from an existing repository. Anyone with access to the template repository can create a new repository based on the template with the same directory structure, branches, and files.

> [!NOTE]  
> Creating a repository from a template is similar to forking a repository, but there are important differences:
>  - A new fork includes the entire commit history of the parent repository, while a repository created from a template starts with a single commit.
>  - Commits to a fork don't appear in your contributions graph, while commits to a repository created from a template do appear in your contribution graph.
>  - A fork can be a temporary way to contribute code to an existing project, while creating a repository from a template starts a new project quickly.

You can choose to include the directory structure and files from only the default branch of the template repository or to include all branches. Branches created from a template have unrelated histories, which means you cannot create pull requests or merge between the branches.

### Create a template

You can make an existing repository a template, so you and others can generate new repositories with the same directory structure, branches, and files.

To create a template repository, you must create a repository, then make the repository a template.

After you make your repository a template, anyone with access to the repository can generate a new repository with the same directory structure and files as your default branch.

Your template repository cannot include files stored using Git LFS.

The steps are:

1. On GitHub.com, navigate to the main page of the repository.

2. Under your repository name, click  Settings. If you cannot see the "Settings" tab, select the  dropdown menu, then click Settings.

3. Select Template repository.


## SECURITY

Security researchers can assess the security settings of a public repository, suggest a security policy and report a vulnerability.

Anyone can view a public repository's security settings, and contact the repository maintainers regarding security issues.

Evaluating a public repository's security settings can help security researchers understand the repository's security posture. This information can help you decide whether to engage with the repository maintainers, for example, by reporting a vulnerability in the repository.

If a repository is public, high level information about the repository's security settings is available to anyone.

If you have admin permissions to the repository, and the repository is owned by an organization, you can see more detailed information about the repository's security settings through the security overview. 

### Security features

In the security overview tab of a repository (can also be found in the settings section) you can find the following features.

#### Private repos:

 - **Security policy:** Define how users should report security vulnerabilities for this repository
 - **Security advisories:** View or disclose security advisories for this repository
 - **Dependabot alerts:** Get notified when one of your dependencies has a vulnerability
 - **Code scanning alerts:** *Advanced Security is only available for Organizations*

#### Public repos:
All the private features and:


 - **Private vulnerability reporting:** Allow users to privately report potential security vulnerabilities
 - **Code scanning alerts:** Automatically detect common vulnerability and coding errors *(available in all public repos)*
 - **Secret scanning alerts:** Get notified when a secret is pushed to this repository



### Suggesting a security policy for a repository

If you do not have admin or security permissions for a public repository, you can still suggest a security policy to the repository maintainers if one doesn't already exist. The repository maintainers can then choose to accept or reject your suggestion. If the repository maintainers accept your suggestion, the security policy will be associated with the repository.

1. On GitHub.com, navigate to the main page of the repository.
2. Under the repository name, click Security.
3. If the repository has a security policy, it will be displayed. If no security policy is associated with the repository, click Suggest a policy.
4. A SECURITY.md file will be created in the repository's default branch. The file will contain a template for a security policy. You can edit the file to add your suggested security policy.
5. When you are done, click Commit changes.
6. Fill out the Commit changes dialog.
  - Under "Commit message", enter a commit message.
  - Optionally, under "Extended description", describe the changes being made.
  - Select "Create a new branch for this commit and start a pull request"
  - Click Commit changes.
7. Click Create pull request.
8. Optionally, leave a comment.
9. Click Create pull request.


> [!NOTE]  
> In case you have the permissions it will only require to fill up and commit like any other adition of files into repositories.

<ins>The security police can be access and will be render in the Security tab next like the readme in the root of the repo.</ins>

## MAINTAINING A REPO

Some of the actions you can make in a repo are:

### Rename

You can rename your repo name <ins>(try to avoid because it can break external links and documentation pointing to a public repo).</ins>

Repo names are scoped based on the personal or organizational account.

When you rename a repository, all existing information, with the exception of project site URLs, is automatically redirected to the new name

### Rename default branch

You can choose the default branch for a repository. The default branch is the base branch for pull requests and code commits. 

You can change the base branch (default branch). You can rename it, "main" is the unspoken best practice for naming your base branch.


### Enable features

You can opt-in-and-out some features for your Github Repo. Features will be appear in the Github repo navigation bar.

Some of them are:
 - Wikis: Wikis host documentation for your repository. GitHub Wikis is a simple way to let others contribute content. Any GitHub user can create and edit pages to use for documentation, examples, support, or anything you wish. *(Available for free publics repos, and privates in PRO, teams, Enterprise Cloud and Enterprise Server)*.
 - Issues: Issues integrate lightweight task tracking into your repository. Keep projects on track with issue labels and milestones, and reference them in commit messages. If you pass from enable to disable and decide to enable issues again in the future, any issues that were previously added will be available.
   - Issue templates: Give contributors issue templates that help you cut through the noise and help them push your project forward.
 - Sponsorships: Sponsorships help your community know how to financially support this repository. By enable it you can display a "Sponsor" button you add links to GitHub Sponsors or third-party methods your repository accepts for financial contributions to your project.
 - Discussions: You can use GitHub Discussions in a repository as a place for your community to have conversations, ask questions, and post answers without scoping work in an issue.
 - Projects: Projects on GitHub are created at the repository owner's level (organization or user) and can be linked to a repository's Projects tab. Projects are suitable for cross-repository development efforts such as feature work, complex product roadmaps or even Issue triage.


## DANGER ZONE

The Danger Zone contains actions you need to think twice about the cannot be undone.

### Change repo visibility

When you make a private repo to public:
 - The code will be visible to everyone who can visit github.com
 - Anyone can fork you repository
 - All pushes rullsets will be disable
 - Your changes will be published as activity

When you make a public repo to private:
 - Could permanently erase these counts by removing stars and watchers associated to users that will no longer have access to this repository:
 - If you decide to make this repository public in the future, it will not be possible to restore these stars and watchers and this will affect its repository rankings.
 - Dependency graph and Dependabot alerts will remain enabled with permission to perform read-only analysis on 
 this repository. Any custom Dependabot alert rules will be disabled unless GitHub Advanced Security is enabled for this repository.
 - Code scanning will become unavailable.
 - Current forks will remain public and will be detached from this repository.

### Disable branch protection rules

Branch protect rules are strict workflow rules like disallowing anyone pushing to main. You can disable all protection rules temporarily eg. Quick fixes

Disabling branch protection rules allows you to enforce branch and tag protections exclusively with Repository Rules.

This action will disable:
 - Branch protection rule enforcement
 - Branch protection rule APIs


### Transfer ownership

Transfer this repository to another user or to an organization where you have the ability to create repositories.

When you transfer a repository to a new owner, they can immediately administer the repository's contents, issues, pull requests, releases, projects (classic), and settings. You can also change the repository name while transferring a repository.

When you transfer a repository, its issues, pull requests, wiki, stars, and watchers are also transferred. If the transferred repository contains webhooks, services, secrets, or deploy keys, they will remain associated after the transfer is complete. Git information about commits, including contributions, is preserved.

### Archiving

You can archive a repository to make it read-only for all users and indicate that it's no longer actively maintained. You can also unarchive repositories that have been archived.

Irs recommend that you close all issues and pull requests, as well as update the README file and description, before you archive a repository.

Once a repository is archived, you cannot add or remove collaborators or teams. Contributors with access to the repository can only fork or star your project.

When a repository is archived, its issues, pull requests, code, labels, milestones, projects, wiki, releases, commits, tags, branches, reactions, code scanning alerts, comments and permissions become read-only.


### Deleting

You can delete any repository or fork if you're either an organization owner or have admin permissions for the repository or fork. Deleting a forked repository does not delete the upstream repository.

> [!NOTE]  
>  - Deleting a repository will permanently delete release attachments and team permissions. This action cannot be undone.
>  - Deleting a private repository will delete all forks of the repository.


Only members with owner privileges for an organization or admin privileges for a repository can delete an organization repository. If Allow members to delete or transfer repositories for this organization has been disabled, only organization owners can delete organization repositories.



> [!IMPORTANT]  
> You can restore some deleted repositories to recover their contents. Anyone can restore deleted repositories that were owned by their own personal account. Organization owners can restore deleted repositories that were owned by the organization. 
> 
> **A deleted repository can be restored within 90 days, unless the repository was part of a fork network that is not currently empty.**


## LARGE FILE STORAGE

When creating source code archives, you can choose to include files stored using Git LFS in the archive.

You can innclude Git LFS objects in archives. Git LFS usage in archives is billed at the same rate as usage with the client.

You can choose whether Git Large File Storage (Git LFS) objects are included in source code archives, such as ZIP files and tarballs, GitHub creates for your repository.

GitHub creates source code archives of your repository in the form of ZIP files and tarballs. People can download these archives on the main page of your repository or as release assets.

By default, Git LFS objects are not included in these archives, only the pointer files to these objects. To improve the usability of archives for your repository, you can choose to include the Git LFS objects instead.

To be included, the Git LFS objects must be covered by tracking rules in a .gitattributes file that has been committed to the repository.

> [!NOTE]  
> If you choose to include Git LFS objects in archives of your repository, every download of those archives will count towards bandwidth usage for your account. Each account receives 1 GiB per month of bandwidth for free, and you can pay for additional usage. 

## LIMIT PUSHES

You can limit how many branches and tags can be updated in a single push. Pushes will be rejected if they attempt to update more than the value defined.


> Developers have had branches deleted from their repository when someone pushes changes with Git's <kbd>--mirror</kbd> option.

> The <kbd>--mirror</kbd> option is potentially destructive because it makes the remote repository exactly match the local clone.

> [!WARNING]  
> When run by accident, if the remote has more branches or different data than the local clone, many branch deletes and force-pushes can happen at the remote without any warning. This is often embarrassing for the one who pushed and a big challenge to recover from.

Then toggle the setting named Limit how many branches and tags can be updated in a single push as shown below. Set the number appropriately for your needs.

The default maximum of 5 branch or tag updates allowed in one push.

The minimum value is 2 since two branch updates are required by Git to rename a branch in a single push: delete branch and create branch.

Lower numbers are more restrictive of which pushes are allowed, and higher numbers are less restrictive but have more potential for being destructive. 

## ADD FILES

To add a file you can do via Github UI:
 - Multiple Text and Binary files can be uploaded
 - New single text files can be created

When creating files in places, you have a basic text editor.

You can also created nested folder by typing a foward slash in the file name.

> [!TIP]
> When adding multiples files that you also need to edit, you can quickly use Github.dev (crtl + alt + . ) at no cost.

Files that you add to a repository via a browser are limited to 25 MiB per file. You can add larger files, up to 100 MiB each, via the command line. 


> [!NOTE]  
> If a repository has any protected branches, you can't edit or upload files in the protected branch using GitHub.

## CREATE BRANCHES

The are many ways to create a branch using git and/or github.

The first new branch you create will be based on the default branch. If you have more than one branch, you can choose to base the new branch on the currently checked out branch or the default branch.

### Git command
The easiest way to create a branch using git locally is with:

```sh
git chechout -b <branch_name> # The `-b` flag create and checkout the branch directly
```

To push it upstream:

```sh
git push -u origin <branch_name> # The `-u` flag is for --set-upstream
```

### Issues

Branches can be created from Issues. 

Branches connected to an issue are shown under the "Development" section in the sidebar of an issue. When you create a pull request for one of these branches, it is automatically linked to the issue. The connection with that branch is removed and only the pull request is shown in the "Development" section.

### UI

Branches can be directly created within Github UI

You can only create a branch in a repository to which you have push access.

From the file tree view on the left, select the branch dropdown menu, then click View all branches. You can also find the branch dropdown menu at the top of the integrated file editor. Select New branch.

### Desktop

You can always create a branch in GitHub Desktop if you have read access to a repository, but you can only push the branch to GitHub if you have write access to the repository.

In the repository section, it the  branch tab, click on <kbd>New branch...</kbd>


## STARS

Similar to bookmarking, it's a way to mark a repository as interesting or to keep track of it for reference.

Stars are public and can be seen by everyone, often use as a measure of a project's popularity.

You can star repositories and topics to keep track of projects you find interesting and discover related content in your news feed. You can star repositories and topics to discover similar projects on GitHub. When you star repositories or topics, GitHub may recommend related content on your personal dashboard.

You can access yours stars in:
> - https://github.com/stars
> - https://github.com/USERNAME?tab=stars

Starring a repository also shows appreciation to the repository maintainer for their work. Many of GitHub's repository rankings depend on the number of stars a repository has.


### Who has starred a repository
You can view everyone who has starred a public repository or a private repository you have access to.
To view everyone who has starred a repository, add `/stargazers` to the end of the URL of a repository. 

### Starred list

Anyone can see repositories that you've starred with public lists. You can create public lists that appear on your stars pageat https://github.com/USERNAME?tab=stars.

If you add a private repository to a list, then the private repository will only appear in your list for people with `read` access to the repository.
