# ENTERPRISE

Businesses can use GitHub's enterprise products to improve their entire software development lifecycle.

When you purchase GitHub Enterprise, you get access to both GitHub Enterprise Cloud and GitHub Enterprise Server. GitHub Enterprise Cloud is a set of advanced functionality on GitHub.com, while GitHub Enterprise Server is self-hosted platform.

## GITHUB CONNECT

Github connect enhances Github Enterprise Server (GHES) by allowing your GHES instance access some of Github Cloud only offerings.

You can individually enable these features:
- Automatic user license sync
- Dependabot
- Github Actions
- Server Statistics
- Unified search
- Unified contributions

## INTERNAL REPOS
Github Enterprise Cloud accounts have a third special type of Github Repo called **Internal**

Some features are:
- All enterprise members have read permissions to the internal repository
- Internal repositories are not visible to people outside of the enterprise, including outside collaborators on organization repositories
- Unless your enterprise uses Enterprise Managed Users (EMUs), members of the enterprise can fork any internal repository owned by an organization in the enterprise

> [!NOTE]  
> Internal repositories are the default setting for all new repositories created in an organization owned by an enterprise account

## ADVANCED SECURITY
Github makes extra security features available to customers under a Github Advanced Security (GHAS) license.

Github Advanced Security is available for enterprise accounts on:
- Github Enterprise Cloud
- Github Enterprise Server
- And some features for public repositories on Github.com

Github Advanced Security license provides the following features:
| Feature | Public Repository | Private Repository without Advance Security | Private Repository with Advance Security
| --- | --- | --- | --- |
| Code scanning | :heavy_check_mark: | :x: | :heavy_check_mark: |
| Secret scanning | :heavy_check_mark: | :x: | :heavy_check_mark: |
| Dependency review | :heavy_check_mark: | :x: | :heavy_check_mark: |


## SAML AND SCIM

<ins>SAML and SCIM is available for both Github Enterprise Cloud and Github Enterprise Server</ins>

**Security Assertion Markup Language (SAML)**: is an open standard for exchanging authentication and authorization between an identity provider and a service provider. An important use case for SAML is Single-Sing-On via web browser.

**System for Cross-Domain Identity Management (SCIM)** is an open standard for automating the exchange of user identity information across different identity management systems. A key use case for SCIM is to enable scalable and automated user provisioning and deprovisioning, often integrated with enterprise identity services.

In a resume:
| SAML | SCIM |
| :--- | :--- |
| Is about securely transmitting user authentication and authorization data for single sign-on porpuses | Is about managing user identities across different systems to simply account mantenance and provisioning |


> [!NOTE]  
> They can both complement each other in an ecosystem where you need both federated identity for authentification and a standarized way to manage user accounts across various systems