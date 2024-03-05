# GITHUB ACCOUNTS

Accounts on GitHub allow you to organize and control access to code. 
There are three types of accounts on GitHub..

 - Personal accounts
 - Organization accounts
 - Enterprise accounts

Every person who uses GitHub signs into a personal account. An organization account enhances collaboration between multiple personal accounts, and an enterprise account allows central management of multiple organizations.

## PERSONAL

These are individual accounts with a username and profile.

Every person who uses GitHub.com signs in to a personal account. Your personal account is your identity on GitHub.com and has a username and profile.

Your personal account can own resources such as repositories, packages, and projects. Any time you take any action on GitHub.com, such as creating an issue or reviewing a pull request, the action is attributed to your personal account. They can use either Github Free or Github Pro.


All personal accounts can own an unlimited number of public and private repositories, with an unlimited number of collaborators on those repositories.


> [!TIP]
> Personal accounts are intended for humans, but you can create accounts to automate activity on GitHub. This type of account is called a machine user. For example, you can create a machine user account to automate continuous integration (CI) workflows.

### Personal features

With a Github Personal account you can have a public profile and also host your own public website.

Repos urls for personal account looks like
```sh 
https://github.com/Andresmup/github-foundations #Github domain, follow by username follow by repo name
```

### Personal plans comparison

Each personal account uses either GitHub Free or GitHub Pro here are the main differences.

**Github Free**
 - Github Community Support
 - Dependabot Alert
 - Deployment protections rules for public repositories
 - Two-factor authentication enforcement
 - 500 MB Github Packages storage
 - 120 hs Github Codespaces core per month
 - 15 GB Github Codespaces per month
 - Github actions features (2000 min per month, deployment protection rules for public repos)

**Github Pro**
 - Everything from Github Free and ...
 - Github Support via email
 - 3000 min Github Actions per month
 - 2 GB Github Packages storage
 - 180 hs Github Codespaces core per month
 - 20 GB Github Codespaces per month
 - Advance tools and insights in private repos such
 - Required PR reviewers
 - Multiple PR reviewers
 - Protected branches
 - <ins>Code owners</ins>
 - Auto-link refences
 - Github Pages
 - Wikis
 - Repository insight graphs


## ORGANIZATION

Organizations are shared accounts where an unlimited number of people can collaborate across many projects at once.

The can also own resources like repositories, packages, and projects. But the are managed through individual personal accounts.

> [!NOTE]  
> You cannot sign into an organization. Instead, each person signs into their own personal account, and any actions the person takes on organization resources are attributed to their personal account.

Each personal account can be a member of multiple organizations.

The personal accounts within an organization can be given different roles in the organization, which grant different levels of access to the organization and its data. 

> [!IMPORTANT]  
> All members can collaborate with each other in repositories and projects, but only organization owners and security managers can manage the settings for the organization and control access to the organization's data with sophisticated security and administrative features. 

### Organization features
With a Github Organization account you can have a public profile page.

It can show who belongs withing the organization.

You can manage people into teams with different level of access.

Organizations have their own username

Repos urls for organization account looks like
```sh 
https://github.com/GithubCloudLearners/GithubDemo #Github domain, follow by organization name follow by repo name
```

### Organization plans comparison

Each organization account uses either Free, Team or Enterprise* here are the main differences.

**Organization Free**
 - Everything from Github Free and ...
 - Team access control for managing groups
 - 2000 min Github Actions per month
 - 500 MB Github Packages storage

**Organization Team**
 - Everything from Organization Free and ...
 - Github Support via email
 - 3000 min Github Actions per month
 - 2 GB Github Packages storage
 - Advance tools and insights in private repossuch
 - Required PR reviewers
 - Multiple PR reviewers
 - <ins>Draft PR</ins>
 - Team PR reviewers
 - Protected branches
 - <ins>Code owners</ins>
 - Auto-link refences
 - Github Pages
 - Wikis
 - Repository insight graphs
 - Option to enable or disable Codespaces

> [!TIP]
> Both Draft PR and code owners are important details.

> [!NOTE]  
> You can use a CODEOWNERS file to define individuals or teams that are responsible for code in a repository. Code owners are automatically requested for review when someone opens a pull request that modifies code that they own.


## ENTREPRISE

GitHub Enterprise Cloud and GitHub Enterprise Server include enterprise accounts. 

Which allow administrators to centrally manage policy and billing for multiple organizations and enable innersourcing between the organizations.

Your enterprise account must have a handle, like an organization or user account on GitHub.

In the enterprise settings, enterprise owners can invite existing organizations to join your enterprise account, transfer organizations between enterprise accounts, or create new organizations.

Your enterprise account allows you to manage and enforce policies for all the organizations owned by the enterprise. 

Each enterprise policy controls the options available for a policy at the organization level. You can choose to not enforce a policy, which allows organization owners to configure the policy for the organization, or you can choose from a set of options to enforce for all organizations owned by your enterprise. 

### Billing for enterprise

The bill for your enterprise account includes the monthly cost for each member of your enterprise. 

The bill includes any paid licenses in organizations outside of your enterprise account, subscriptions to apps in GitHub Marketplace, additional paid services for your enterprise like data packs for Git Large File Storage, and usage for GitHub Advanced Security.

### Github deployment options
Github Enterprise include two deployment options:
- Github Enterprise Cloud (hosted on Github.com)
- Github Enterprise Server (self-hosted)

Here are the main differences:

**Github Enterprise (both cloud and server)**
 - Everything from Organization Team and ...
 - Github Enterprise Support
 - Aditional security, compliance, and deployment controls
 - <ins>Authentication with SAML single sign-on</ins>
 - <ins>Access provisioning with SAML or SCIM</ins>
 - Deployment protection rules with Github Actions for private or <ins>internal</ins> repos
 - Github Connect
 - Option to purchase Github Advance Security

> [!TIP]
> Underline features are important details.

> [!NOTE]  
> SAML single sign-on (SSO) gives organization owners and enterprise owners using GitHub Enterprise Cloud a way to control and secure access to organization resources like repositories, issues, and pull requests. Organization owners can invite your personal account on GitHub to join their organization that uses SAML SSO, which allows you to contribute to the organization and retain your existing identity and contributions on GitHub.

**Github Enterprise Cloud (specific features)**
 - 50000 min Github Actions per month
 - 50 GB Github Packages storage
 - A service of agreement of 99,9% monthly uptime
 - <ins>Option to centrally manage policy and billing for multiple Github organizations with an enterprise account</ins>
 - <ins>Option to provision and manage the user accounts for your developers, by using Enterprise Managed Users (EMU)</ins>

> [!TIP]
> Underline features are important details.

> [!NOTE]  
> With Enterprise Managed Users, you manage the lifecycle and authentication of your users on GitHub.com from an external identity management system, or IdP.
You can provide access to GitHub Enterprise Cloud to people who have existing identities and group membership on your IdP.
Your IdP provisions new user accounts with access to your enterprise on GitHub.com. You control usernames, profile data, team membership, and repository access for the user accounts from your IdP.


