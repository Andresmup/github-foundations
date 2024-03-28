# AUTHENTICATION AND SECURITY

## 2 FACTOR AUTHENTICATION

2-Fact Authenticator (2FA) is when you use a second device (eg:phone) to enter a code as extra security precaution when signing-in or performing sensitive actions.

The two factor methods available are:
- Github Mobile app
- Authenticator app: You can download third-party authenticator apps via your phone like:
   - Authy
   - Google Authenticator
   - Microsoft Authenticator
- SMS/Text Message: Get UFA code sent as text message
- Security keys: Hardware devices like YubiKeys

**Recovery codes** are long secrets codes you need to print and store someone safe in case you get locked out.

## ACCESS PERMISION PERSONAL ACCOUNTS
Personal accounts has two permission levels:
- Repository owner: the person who own the account
  - Repositories owned by personal accounts have their owner
  - Ownership permission can't be shared with other personal accounts
- Collaborators: people add to collaborate and help in the repo


### Owner

Repository owner has full control of the repository and can perform this actions:
- Invite collaborators
- Change the visibility of the repository
- Limit interactions with the repository
- Rename a branch, including the default branch
- Merge a PR on a protected branch, even it there are no approving reviews
- Delete the repository
- Manage the repository's topics
- Manage security and analysis settings for the repository
- Enable the dependency graph for a private repository
- Delete and restore packages
- Customize the repository's social media preview
- Create a template from the repository
- Control access to Dependabots alerts
- Dismiss Dependabots alerts in the repository
- Manage data use for a private repository
- Define a codeowners for the repository
- Archive the repository
- Create security advisories
- Display a sponsor button
- Allow or disallow auto-merge for PR
- Manage deploy keys
- Manage webhooks


### Collaborator

Collaborators can pull (read) the contents of the repository, push (write) changes to the respository and can perform this actions:
- Fork the repository
- Rename a branch other than the default branch
- Create, edit, and delete comments on commits, pull requests and issues in the repository
- Create, assign, close and re-open issues in the repository
- Manage labels for issues and PR in the repository
- Manage milestones for issues and PR in the repository
- Mark an issue or PR as duplicate
- Create, merge and close PR
- Enable or disable auto-merge for a PR
- Apply suggested changes to PR
- Create a PR from a fork of the repository
- Submit a review on a PR that affects the mergeability of the PR
- Create and edit a wiki for the repo
- Create and edit releases for the repo
- Act as code owner for the repository
- Publish, view or install packages
- Remove themselves as collaborators on the repo


### Comparison

| Repository owner actions | Collaborators actions
| --- | --- |
| Has full control of the repository | Can pull (read) the contents of the repo. And push (write) changes to the repo |


## ORGANIZATION ROLES

From least access to most access, the roles for an organization repository are:

- Read: Recommended for non-code contributors who want to view or discuss your project
- Triage: Recommended for contributors who need to proactively manage issues, discussions, and pull requests without write access
- Write: Recommended for contributors who actively push to your project
- Maintain: Recommended for project managers who need to manage the repository without access to sensitive or destructive actions
- Admin: Recommended for people who need full access to the project, including sensitive and destructive actions like managing security or deleting a repository

> [!NOTE]  
> GitHub Enterprise Cloud allows you can create custom repository roles

## EMUs

Enterprise Managed Users (EMUs) allows you to manage the lifecycle and authentication of your users on Github from an external identity management system or IdP.

Github partner with some developers of identity management systems to provide a "paved-path" integration with EMUs.

These IdPs mostly provide authentication using SAML.

Microsoft Entra ID (ex Azure AD) also offers OCID for authentication.

The IdP applications provision users with System for Cross-domain Identity Management (SCIM)

| Partner IdP | SAML | OCID | SCIM |
| --- | --- | --- | --- |
| Microsoft Entra ID | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| Okta | :heavy_check_mark: | :x: | :heavy_check_mark: |
| PingFederate | :heavy_check_mark: | :x: | :heavy_check_mark: |


## SECURITY SCANNERS

You can use code scanning to find security vulnerabilities and errors in the code for your project on GitHub.

> [!IMPORTANT]  
> Remenber there are three main vulnerability alets:
> - Dependabot
> - Code Scanning
> - Secret scanning

## CODEQL

CODEQL allows you to discover vulnerabilities across a codebase with CodeQL, its industry-leading semantic code analysis engine. CodeQL lets you query code as though it were data. Write a query to find all variants of a vulnerability, eradicating it forever. Then share your query to help others do the same.

CodeQL is free for research and open source.

CodeQL is the code analysis engine developed by GitHub to automate security checks. You can analyze your code using CodeQL and display the results as code scanning alerts.

> [!NOTE]  
> Remember the are three main ways to use CodeQL analysis for code scanning:
> -Use default setup to quickly configure CodeQL analysis for code scanning on your repository. Default setup automatically chooses the languages to analyze, query suite to run, and events that trigger scans. If you prefer, you can manually select the query suite to run and languages to analyze. After you enable CodeQL, GitHub Actions will execute workflow runs to scan your code.
> - Use advanced setup to add the CodeQL workflow to your repository. This generates a customizable workflow file which uses the github/codeql-action to run the CodeQL CLI.
> - Run the CodeQL CLI directly in an external CI system and upload the results to GitHub.

### About CodeQL
CodeQL treats code like data, allowing you to find potential vulnerabilities in your code with greater confidence than traditional static analyzers.

1. You generate a CodeQL database to represent your codebase.
2. Then you run CodeQL queries on that database to identify problems in the codebase.
3. The query results are shown as code scanning alerts in GitHub when you use CodeQL with code scanning.


CodeQL supports both compiled and interpreted languages, and can find vulnerabilities and errors in code that's written in the supported languages (C/C++, C#, Go, Java/Kotlin, JavaScript/TypeScript, Python, Ruby, Swift)

### About CodeQL queries

GitHub experts, security researchers, and community contributors write and maintain the default CodeQL queries used for code scanning. The queries are regularly updated to improve analysis and reduce any false positive results.

#### Writing your own queries
The queries are open source, so you can view and contribute to the queries in the github/codeql repository.

#### Running additional queries
If you are scanning your code with advanced setup or an external CI system, you can run additional queries as part of your analysis. These queries must belong to a published CodeQL query pack (beta) or a CodeQL pack in a repository. 