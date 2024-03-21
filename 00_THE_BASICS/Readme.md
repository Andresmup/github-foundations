# THE BASICS

## VERSION CONTROL SYSTEMS (VCS)

Version Control System (VCS) are design to track changes or revision to code.

Git is a Descentralized VSC (DVSC), and it became very popular for many reasons including:
- Full local history and complete a copy of the repo locally.
- Straigthforward and efficient branching and merging.
- Better perfomance, improve fault tolerance, flexible workflows, work fully offline.

> [!TIP]
> Version control normally represents revisions being represents as graph like structure. Some terms in use are tree, trunch and branches.

A version control system, or VCS, tracks the history of changes as people and teams collaborate on projects together. As developers make changes to the project, any earlier version of the project can be recovered at any time.

Developers can review project history to find out:

- Which changes were made?
- Who made the changes?
- When were the changes made?
- Why were changes needed?

VCSs give each contributor a unified and consistent view of a project, surfacing work that's already in progress. Seeing a transparent history of changes, who made them, and how they contribute to the development of a project helps team members stay aligned while working independently.


### GIT 

Git is a distributed version control system (DVSC).

Each change of your code (git commit) can be captured and tracked throughout the history of your project (git tree)

In a distributed version control system, every developer has a full copy of the project and project history. Unlike once popular centralized version control systems, DVCSs don't need a constant connection to a central repository. 

In resume Git offers:
- Git lets developers see the entire timeline of their changes, decisions, and progression of any project in one place. From the moment they access the history of a project, the developer has all the context they need to understand it and start contributing.
- Developers work in every time zone. With a DVCS like Git, collaboration can happen any time while maintaining source code integrity. Using branches, developers can safely propose changes to production code.
- Businesses using Git can break down communication barriers between teams and keep them focused on doing their best work. Plus, Git makes it possible to align experts across a business to collaborate on major projects.

### Git common terms

- Repository: Represents the logical container holding the codebase
- Commit: Represents a change of data in the local repository
- Tree: Represents the entiry history of a repo
- Remote: A versión of your project hosted elsewhere, used for exchanging commits
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

Version Control Services (VCS) are fully managed cloud servicies that host your version controlled repositories. These services ofter have addicional functionality going beyond just being a remote host you repos. Github is the most popular and often the only choice for VCS. Often we call these services "git providers"

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

## OCTOCAT

Github's octocat is the platform's official mascot. The caracter is a hybrid of an octopus and a cat, symbolizes Github's friendly and engaging nature in the world of software development and collaboration.

You can create your own in https://myoctocat.com


