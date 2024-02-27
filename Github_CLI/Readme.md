# GITHUB CLI

GitHub CLI is a command-line tool that brings pull requests, issues, GitHub Actions, and other GitHub features to the terminal.
GitHub CLI is an open source tool for using GitHub from your computer's command line.

Allows to:
 - View, create, clone, and fork repositories.
 - Create, close, edit, and view issues and pull requests.
 - Review, diff, and merge pull requests.
 - Run, view, and list workflows.
 - Create, list, view, and delete releases.
 - Create, edit, list, view, and delete gists.
 - List, create, delete, and connect to a codespace.
 - Retrieve information from the GitHub API.

## Check CLI installed
The easiest way to check if CLI is installed is by tiping `gh` into the terminal.

## Install
The first step is install it.

### Windows
On Windows can be done downloading (and upgrading) it from https://cli.github.com/ or just by using

```sh
winget install --id GitHub.cli	
winget upgrade --id GitHub.cli
```
### Linux
On linux run:

```sh
brew install gh
brew upgrade gh
```

### Codespaces
Add the following to your devcontainer file:

```json
"features": {
  "ghcr.io/devcontainers/features/github-cli:1": {}
}
```

## LOGIN
We have to login using the CLI, to authenticated the user it can be done via ssh or token.
```sh
gh auth login
```

## REPO
Using the CLI tool actions on the repositories can be done

### List
To see a list with all the repositories use:
```sh
gh repo list
```

### Set default repo
To perform actions on a github repository, it can to be set up as default.
```sh
gh repo set-default
```

### View (default)
The default content of repository can be access and see using.
```sh
gh repo view
```

### View (any)
Any repository content can be access and see using.
```sh
gh repo view <repository_name>
```
