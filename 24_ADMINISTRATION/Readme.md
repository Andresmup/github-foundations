# ADMINISTRATION

## MANAGING FEATURES
Github repos have multiple features that can be enable or disable:
- Wiki
- Issues
- Sponsors
- Preserve this repo (goes into Github Actic Code Vault)
- Discussions
- Projects
- and more


## REPO PERMISSION LEVELS

When you add a collaborator (and they accept the invite) you can choose from predefined roles with different level access:
- **Read**
   - View and clone the repository
   - Open and comment on issues and pull requests
   - Download releases
- **Triage**
   - Manage issues and pull requests without write access
   - Label and assign issues and PR
   - Close and open issues and PR
- **Mantain**
   - Push to the repository
   - Manage issues, pull requests, labels and projects boards
   - Create and publish releases
   - Configure repository settings for non-sensitive fields (like assigning collaborators)
- **Admin**
   - Full control over the repository
   - Push to, delete or archive the repo
   - Change repository settings, including sensitive fields like security and billing
   - Manage collaborators and their permisions
   - Access to all funtionalities provided in the Maintain role

<ins>Enterprises accounts can have custom roles</ins>

## BRANCH PROTECTION RULES

Branch protection rules are used to enforce certain workflows or requirements before changes can be merged into a branch.


> [!IMPORTANT]  
> **Protect matching branches rules**:
> - Require a PR before merging
> - Require status checks to pass before merging
> - Require conversation resolution before merging
> - Require signed commits
> - Require linear history
> - Require deployments to succeed before merging
> - Lock branch
> - Do not allow bypassing the above settings
> 
> **Rules applied to everyone including administrators**:
> - Allow force pushes
> - Allow deletions

## SECURITY TAB
In every repo the is a security tab that present a repository security checklist of security options to configure.

### Security Policy
Create a markdown file that explain how security vulnerabilites should be reported.

### Security Advisories
Privately discuss, fix and pushing information about security vulnerabilities in your public repository.

### Private vulnerability reporting
Allow your community to privately report potencial security vulnerabilities to maintainers and repository.

### Dependabot alerts
A bot that alerts you of vulnerabilities due to out-of-date dependencies. Dependabot can automatically create PRs to update dependencies for you to approve.

### Code scanning alerts
Automatically detect common vulnerabilities and coding errors via GraphQL or third-party tools.

### Secret scanning alerts
Get notified when a secret is pushed to the repository.

## MANAGING COLLABORATORS
Collaborators allow you to let other Github users have access to your repo based on the permission level you provide.

You just have to search their username to invite.

The user need to accept the invite. Its best to share the link directly and manually remind them to accept. 

You can access to the repo invitation in `https://github.com/<repo-owner>/<repo-name>/invitations`.

## TEAM TAB
An organization can group organization members in teams.

Some features of teams are:
- Teams can be assigned to projects and issues
- Request reviews from teams
- Teams can be mentioned in discussions, issues and PR
- Control team access to repositories
- New members can be added to teams, instantly giving them access to all relevant repositories and discussions