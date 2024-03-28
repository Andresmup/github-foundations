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

## ROLES IN ORGANIZATIONS
Organization owners can assign roles to individuals and teams giving them different sets of permissions in the organization.

To perform any actions on GitHub, such as creating a pull request in a repository or changing an organization's billing settings, a person must have sufficient access to the relevant account or resource. This access is controlled by permissions. A permission is the ability to perform a specific action. 

Repository-level roles give organization members, outside collaborators and teams of people varying levels of access to repositories.

Team-level roles are roles that give permissions to manage a team. You can give any individual member of a team the team maintainer role, which gives the member a number of administrative permissions over a team. 

Organization-level roles are sets of permissions that can be assigned to individuals or teams to manage an organization and the organization's repositories, teams, and settings. 

You can assign people to a variety of organization-level roles to control your members access to your organization and its resources. 

### Organization owners
Organization owners have complete administrative access to your organization. This role should be limited, but to no less than two people, in your organization.

### Organization members
The default, non-administrative role for people in an organization is the organization member. By default, organization members have a number of permissions, including the ability to create repositories and projects.

### Organization moderators
Moderators are organization members who, in addition to their permissions as members, are allowed to block and unblock non-member contributors, set interaction limits, and hide comments in public repositories owned by the organization. 

### Billing managers
Billing managers are users who can manage the billing settings for your organization, such as payment information. This is a useful option if members of your organization don't usually have access to billing resources. 

### Security managers
Security manager is an organization-level role that organization owners can assign to any team in an organization. When applied, it gives every member of the team permissions to view security alerts and manage settings for code security across your organization, as well as read permissions for all repositories in the organization.

If your organization has a security team, you can use the security manager role to give members of the team the least access they need to the organization.

### GitHub App managers
By default, only organization owners can manage the settings of GitHub App registrations owned by an organization. To allow additional users to manage GitHub App registrations owned by an organization, an owner can grant them GitHub App manager permissions.

When you designate a user as a GitHub App manager in your organization, you can grant them access to manage the settings of some or all GitHub App registrations owned by the organization. The GitHub App manager role does not grant users access to install and uninstall GitHub Apps on an organization.

### Outside collaborators
To keep your organization's data secure while allowing access to repositories, you can add outside collaborators. An outside collaborator is a person who has access to one or more organization repositories but is not explicitly a member of the organization, such as a consultant or temporary employee.


### Permissions for organization roles comparison

Here it's a comparison between different permissions and if a role its allow. (Some of the features listed below are limited to organizations using GitHub Enterprise Cloud.)


| Organization permission | Owners | Members | Moderators | Billing managers | Security managers |
| --- | --- | --- | --- | --- | --- |
|Create repositories| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|View and edit billing information| :heavy_check_mark: | :x: | :x: | :heavy_check_mark: | :x: |
|Invite people to join the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Edit and cancel invitations to join the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Remove members from the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Reinstate former members to the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Add and remove people from all teams| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Promote organization members to team *maintainer*| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Configure code review assignments| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Set scheduled reminders| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Add collaborators to all repositories| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Access the organization audit log| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Edit the organization's profile page| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Delete all teams| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Delete the organization account, including all repositories| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Create teams| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|Move teams in an organization's hierarchy| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Create projects | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|See all organization members and teams| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|@mention any visible team| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|Can be made a team maintainer| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|Hide comments on writable commits, pull requests, and issues| :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|Hide comments on all commits, pull requests, and issues| :heavy_check_mark: | :x: | :heavy_check_mark: | :x: | :heavy_check_mark: |
|Block and unblock non-member contributors| :heavy_check_mark: | :x: | :heavy_check_mark: | :x: | :x: |
|Limit interactions for certain users in public repos| :heavy_check_mark: | :x: | :heavy_check_mark: | :x: | :x: |
|Set a team profile picture in all teams| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Sponsor accounts and manage the organization's sponsorships| :heavy_check_mark: | :x: | :x: | :heavy_check_mark: | :heavy_check_mark: |
|Manage email updates from sponsored accounts| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Attribute your sponsorships to another organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Manage the publication of GitHub Pages sites from repos in the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Manage security and analysis settings| :heavy_check_mark: | :x: | :x: | :x: | :heavy_check_mark: |
|View security overview for the organization| :heavy_check_mark: | :x: | :x: | :x: | :heavy_check_mark: |
|Transfer repositories| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Purchase, install, manage billing for, and cancel GitHub Marketplace apps| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|List apps in GitHub Marketplace| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Receive Dependabot alerts about insecure dependencies for all of an organization's repos| :heavy_check_mark: | :x: | :x: | :x: | :heavy_check_mark: |
|Manage Dependabot security updates| :heavy_check_mark: | :x: | :x: | :x: | :heavy_check_mark: |
|Manage the forking policy| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Limit activity in public repositories in an organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Pull (read) all repositories in the organization| :heavy_check_mark: | :x: | :x: | :x: | :heavy_check_mark: |
|Push (write) and clone (copy) all repositories in the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Convert organization members to outside collaborators| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|View people with access to an organization repository| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Manage the default branch name| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Manage default labels| :heavy_check_mark: | :x: | :x: | :x: | :x: |
|Manage pull request reviews in the organization| :heavy_check_mark: | :x: | :x: | :x: | :x: |


## BRANCH PROTECTION RULES

> [!NOTE]  
> Only repository administrators or custom roles with the "edit repository rules" permission can enable protections on a branch.

If you're working on a branch that's protected, you won't be able to delete or force push to the branch. Repository administrators can additionally enable several other protected branch settings to enforce various workflows before a branch can be merged.


> [!WARNING]  
> You must remember for the exam that when a branch is protected:
> - You won't be able to delete or force push to the branch.
> - If required status checks are enabled on the branch, you won't be able to merge changes into the branch until all of the required CI tests pass.
> - If required pull request reviews are enabled on the branch, you won't be able to merge changes into the branch until all requirements in the pull request review policy have been met.
> - If required review from a code owner is enabled on a branch, and a pull request modifies code that has an owner, a code owner must approve the pull request before it can be merged.
> - If required commit signing is enabled on a branch, you won't be able to push any commits to the branch that are not signed and verified. 
> - If you use GitHub's conflict editor to fix conflicts for a pull request that you created from a protected branch, GitHub helps you to create an alternative branch for the pull request, so that your resolution of the conflicts can be merged.


Branch protection rules are used to enforce certain workflows or requirements before changes can be merged into a branch.

> [!IMPORTANT]  
> **Remember this are the protect matching branches rules**:
> - Require a PR before merging
> - Require status checks to pass before merging
> - Require conversation resolution before merging
> - Require deployments to succeed before merging
> - Require signed commits
> - Require linear history
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