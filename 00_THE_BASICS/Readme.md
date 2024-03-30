# THE BASICS

## VERSION CONTROL SYSTEMS (VCS)

Version Control System (VCS) are design to track changes or revision to code.

> [!TIP]
> Version control normally represents revisions being represents as graph like structure. Some terms in use are tree, trunch and branches.

A version control system, or VCS, tracks the history of changes as people and teams collaborate on projects together. As developers make changes to the project, any earlier version of the project can be recovered at any time.

Developers can review project history to find out:

- Which changes were made?
- Who made the changes?
- When were the changes made?
- Why were changes needed?

VCSs give each contributor a unified and consistent view of a project, surfacing work that's already in progress. Seeing a transparent history of changes, who made them, and how they contribute to the development of a project helps team members stay aligned while working independently.

### Distributed version control system

Descentralized VSC (DVSC) became very popular for many reasons including:
- Full local history and complete a copy of the repo locally.
- Straigthforward and efficient branching and merging.
- Better perfomance, improve fault tolerance, flexible workflows, work fully offline.

> [!NOTE]  
> In a distributed version control system, every developer has a full copy of the project and project history. Unlike once popular centralized version control systems, DVCSs don't need a constant connection to a central repository. 


### GIT 

Git is a distributed version control system (DVSC).

Each change of your code (git commit) can be captured and tracked throughout the history of your project (git tree)

In resume Git offers:
- Git lets developers see the entire timeline of their changes, decisions, and progression of any project in one place. From the moment they access the history of a project, the developer has all the context they need to understand it and start contributing.
- Developers work in every time zone. With a DVCS like Git, collaboration can happen any time while maintaining source code integrity. Using branches, developers can safely propose changes to production code.
- Businesses using Git can break down communication barriers between teams and keep them focused on doing their best work. Plus, Git makes it possible to align experts across a business to collaborate on major projects.

### Git common terms

- Repository: Represents the logical container holding the codebase
- Commit: Represents a change of data in the local repository
- Tree: Represents the entiry history of a repo
- Remote: A version of your project hosted elsewhere, used for exchanging commits
- Branches: Divergent paths of development, allowing isolated changes
    - Main (Github) and Master (Git) are the most commnon names used for the default branch
- Clone: Creates a complete local copy of the repository and merges them into your branch
- Checkout: Switches between different branches or commits in your repo
- Pull: Downloads changes from a remote repository and merges them into your branch
- Fetch: Downloads data from a remote repository without integrating it into your work
- Push: Uploads your local repository changes to a remote repository
- Reset: Undoes local changes, with options to unstage or revert commits
- Merge Combines multiple commits histories into one
- Staging files: Prepares and organizes changes for a commit
    - Commit: Saves your changes as snapshots in the local repository
    - Add: Adds changes to the staging area for the next commit

## VERSION CONTROL SERVICES (VCS)

Version Control Services (VCS) are fully managed cloud servicies that host your version controlled repositories. These services often have addicional functionality going beyond just being a remote host you repos. Github is the most popular and often the only choice for VCS. Often we call these services "git providers"

### Github
Github is a Version Controll Service that initially offered hosted managed remote git repositories and has expanded to provide other offerings around hosted codebases.

Owned by Microsoft its the most popular VSC offering due to ease of use and being aroung the longest. Github is primarly where open-source projects are hosted and offer rich functionalities such:
- Git Repository Hosting
- Project Management Tools
- Issue Tracking
- Pull Requests and Code Review
- Github Pages and Wiki
- Github Actions
- Github Copilot
- Github Codespaces
- Github Marketplace
- Github Gists
- Github Discussions
- Collaboration Features (Organizations and Teams)
- API Access and Deployment Tools (Github Desktop, Github CLI)
- Security Features (eg: Autodetecting credentials in repos)
- Educational Resources and Course Automation (Github Classroom)

## COMPARISON GIT vs GITHUB

| Feature | Git | Github |
| --- | --- | --- |
| Nature | Distributed Version Control System (DVCS) | Version Control as a Service (VCS) |
| Functionality | Manages source code history | Provides cloud storage for Git repositories |
| Access | Local system installation | Access via web browser |
| Scope | Local repository managment | Online collaboration and repository hosting |
| Collaboration | Local changes, requires manual sharing | Integrated tools for collaboration (issues and PR) |
| Usage | Command-line commands | Graphical interface and additional features | 

## GITHUB REPOSITORY

A Github Repository is a Git Repository that is pushed upstream to Github. Github allows to access and manage your Git repo with several functionality.

In a Github repo page you can:
- View different branches
- View tags
- View commit history
- Explore repo's file
- See codebase language markdown
- View the top level markdown files
    - Readme.md
    - License.md

You can perform actions suchs as:
- Pinning
- Watching
- Forking
- Starring
- Cloning (downloading)

> [!IMPORTANT]  
> Github Fork allows to create a copy of a repository in your Github account and it's also reference to the original.
> 
> Forking a repository allows to freely experiment with changes without affecting the original project.

## COMMIT

A Git commit represents incremental changes to a codebase represented with a git tree (graph) at a specific time.

A git commit contains:
- Additions, modifications and deletion files
- Additions and deletions of file contents
- Not the whole files themselves

Each commit has a SHA hash that acts as an ID

> [!IMPORTANT]  
> Git does not store the whole files in each commit but rather the state of changes. This greatly reduces the files sizes. To developers the files will appear whole.

Components of a Git commit:
- Commit Hash: A unique SHA-1 hash identifier to the commit
- Author Information: The name and email of the person who made the commit
- Commit Message: A description of what changes the commit contains
- Timestamp: The date and time when the commit was made
- Parent Commit Hash(es): The SHA-1 hash of the commit(s) this commit is based on
- Snapshot of Content: A snapshot of the project at the time of the commit (not the actual files, but references to them)

Commit messages are often written in a tool as its more convenient to quickly add, remote files and audit changes. 

VSC (including the version for Codespaces and Github dev) has that ability via Source Control windows.

Create a new commit containing the current contents of the index and the given log message describing the changes. The new commit is a direct child of HEAD, usually the tip of the current branch, and the branch is updated to point to it (unless no branch is associated with the working tree, in which case HEAD is "detached" as described in git-checkout).

## BRANCH

A Git branch its a divergence of the state of the repo.

You can think of branches as being copies of a point in time that have been modified to be different.

A Git branch is a separate line of development within a Git repository that allows users to work on features or fixes independently from the main codebase. Branches enable collaboration, experimentation, and isolation of changes before integrating them into the main code.

You can have branches for:
- Specific enviroments (staging, development, production)
- Specific developers (andres, muñoz)
- Per features (ml-prediction)
- Per bug (hotflix-data-not-loading)

A common workflow for developers is to create a branch or a feature, and they need to push their branch upstream to the remote name origin.

## REMOTE

A git remote represents the reference to the remote location where a copy is hosted.

Remote repository is a repository which is used to track the same project but resides somewhere else.

The remotes entries are stored in `.git/github`. Notice remotes names can be reference.

You can have multiple remotes entries for your git repo.
`origin` as a remote name almost always seen for a repo. It indicates the central or golden repo everyone is working from and represents the source of truth.

## UPSTREAM AND DOWNSTREAM

| Upstream | Downstream |
| --- | --- |
| The repository to which we push changes | A repository that pulls or clones from another repositories |
|  Is the repository that your local repository is based on. | Its a copy of the upstream repository to which you have made changes. |

## GITHUB FLOW

GitHub flow is a lightweight, branch-based workflow. The GitHub flow is useful for everyone, not just developers. It allow for multiple developers to work on a single repository. Follow GitHub flow to collaborate on projects.

Following GitHub flow:
- **Create a branch**: Create a branch in your repository. A short, descriptive branch name enables your collaborators to see ongoing work at a glance. By creating a branch, you create a space to work without affecting the default branch. Additionally, you give collaborators a chance to review your work.
- **Make changes**: On your branch, make any desired changes to the repository. Commit and push your changes to your branch. Continue to make, commit, and push changes to your branch until you are ready to ask for feedback.
- **Create a pull request**: Create a pull request to ask collaborators for feedback on your changes. Pull request review is so valuable that some repositories require an approving review before pull requests can be merged.
- **Address review comments**: Reviewers should leave questions, comments, and suggestions. Reviewers can comment on the whole pull request or add comments to specific lines or files. You can continue to commit and push changes in response to the reviews. Your pull request will update automatically.
- **Merge your pull request**: Once your pull request is approved, merge your pull request. This will automatically merge your branch so that your changes appear on the default branch. 
- **Delete your branch**: After you merge your pull request, delete your branch. This indicates that the work on the branch is complete and prevents you or others from accidentally using old branches.

## OCTOCAT

Github's octocat is the platform's official mascot. The caracter is a hybrid of an octopus and a cat, symbolizes Github's friendly and engaging nature in the world of software development and collaboration.

You can create your own in https://myoctocat.com


