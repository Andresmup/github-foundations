# APIS's AND SDK'S

In order to streamlining development and integration Github provides developers two key components.
In this ecosystem are the GitHub API and Software Development Kits (SDKs), which together empower developers to interact with GitHub programmatically and build seamless integrations.

GitHub API and SDKs are complementary tools that often go hand in hand. The API lays the foundation, offering a comprehensive set of functionalities, while SDKs abstract away complexities, making it easier for developers to integrate GitHub features into their applications. 

Both toolkits can be find applications like:

 - Building custom integrations.
 - Automating repetitive tasks.
 - Creating tailored workflows
 - Enhancing collaborative development environments. 

## REST API
You can use GitHub's API to build scripts and applications that automate processes, integrate with GitHub, and extend GitHub. 

Each REST API endpoint is documented individually, and the endpoints are categorized by the resource that they primarily affect.

Some ways to connect and use the Rest API are via Github CLI, Curl and JS.

### CLI

GitHub CLI is the easiest way to use the GitHub REST API from the command line. There is no need to pass a token every request because the authentication is done by the CLI.

Make sure CLI is installed on your device, and the user authenticated via ssh or token.

You can test with.
```sh
gh api /octocat --method GET #This return a draw octocat in your terminal.
```

An easy way of using the Rest API is by requesting the issues from a repo.
```sh
gh api --header 'Accept: application/vnd.github+json' --method GET /repos/<Repo_Owner>/<Repo_Name>/issues
```

Also the results can be save as a .json file, here is a example with pull requests.

```sh
gh api --header 'Accept: application/vnd.github+json' --method GET /repos/<Repo_Owner>/<Repo_Name>/pulls -F per_page=2 > fileName.json
```

### Curl

Make sure `curl` is installed on your machine. To check the version run on the terminal `curl --version`.

> [!WARNING]  
> To use CURL in non read operations you have to pass a Github Personal Access Token, treat the token like a password.

To generate the token it go to, and select the permission you requires:
>Settings -> Developer settings -> Personal Access Tokens -> Fine Grained Token -> Generate New Token

An example of request issues from a repo is.
```sh
curl --request GET \
--url "https://api.github.com/repos/<Repo_Owner>/<Repo_Name>/issues" \
--header "Accept: application/vnd.github+json" \
--header "Authorization: Bearer <Your_Token>" \
```

## GraphQL API
GraphQL enables developers to request precisely the data they need, preventing unnecessary data transfers.

This approach reduces the likelihood of over-fetching or under-fetching data, ensuring a more optimal use of bandwidth.

Its has its own sintax languaje. An example is requesting all your repo.

```gql
{
  viewer {
    repositories(first: 100) {
      nodes {
        name
        owner {
          login
        }
      }
    }
  }
}
```

## APIS's COMPARISON

Here it's a quick comparison between Rest API and GraphQL API in Github.


| Info| Rest API | GraphQL API |
| ------------- |------------- | ------------- |
| Design Philosophy | Resource-based, different endpoints per resource | Single endpoint, query for precise data request |
| HTTP Methods | Uses GET, POST, PUT, DELETE for operations | Mainly uses POST for all operations |
| Data Fetching | Multiple request for related data | Single request for complex, related data |
| Over/Under-fetching | Can have over-fetching or under-fetching | Precice data fetching, no over/under-fetching |
| Perfomance | Less efficient for complex systems | More efficient for complex queries |
| Caching | Easier due HTTP methods | More challenging due to POST method |
| Learning Curve | Generally easier to learn | Steeper but offers powerful features |
| Flexibility | Server-driven structure | Client-driven, highly flexible |
| Versioning | Often requires API versioning | Less need for versioning |
| Ecosystem | Mature with extensive tools | Growing with unique tools for queries |

## SDKs

These Software Development Kits act as wrappers around the API, providing developers with pre-built functions and abstractions that simplify common tasks.
SDKs are available for various programming languages, allowing developers to integrate GitHub features without delving into the intricacies of HTTP requests and authentication processes.
They serve as accelerators, reducing development time and effort while maintaining best practices.

Octokit are the official SDKs to programmatically interact with the Github REST API.

GitHub maintains SDKs for the following languages/frameworks/platforms:
 - JavaScript / TypeScript
 - C# / .NET
 - Ruby
 - Terraform provider

### Terraform

To deploy using terraform make sure it's installed on your device previously. To check if it's available run on your terminal  `terraform --version` to see the version installed.

> [!WARNING]  
> To perform certain actions an authorization via Personal Access Token is required, treat the token like a password.

In order to use terraform, in a folder where there is a repository create a file called `main.tf`. To initiate terraform run in the terminal `terraform init`. 

A simple example is creating a branch.
```tf
terraform {
  required_providers {
    github = {
      source  = "integrations/github"
      version = "~> 5.0"
    }
  }
}

provider "github" {

}

resource "github_branch" "<Branch_Name>" {
  repository = "<Repo_name>"
  branch     = "<Branch_Name>"
}
```

After it preview the changes running in the terminal `terraform plan`.

To deploy the changes use `terraform apply`.

To discard the previos crated branch run `terraform destroy`.

### Octokit.js

You can use Octokit.js to interact with the GitHub REST API in your JavaScript scripts.

Make sure `octokit` is installed on your machine. The easiest way is by `npm install octokit`. 

> [!WARNING]  
> To authorized octokit in non read operations you have to pass a Github Personal Access Token, treat the token like a password.

To generate the token it go to, and select the permission you requires:
>Settings -> Developer settings -> Personal Access Tokens -> Fine Grained Token -> Generate New Token

An example of request issues from a repo is.

```js
//Import octokit
import { Octokit } from "octokit"; 

//Create an instance of Octokit with your token
const octokit = new Octokit({ 
  auth: 'YOUR-TOKEN'
});

//Request issues from a repo
await octokit.request("GET /repos/{owner}/{repo}/issues", {
  owner: "<Repo_Owner>",
  repo: "<Repo_Name>",
});
```