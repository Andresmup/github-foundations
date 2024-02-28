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

### Create
A repo can be created using CLI, completing the required fields throw the display nemu.
```sh
gh repo create
```

### View
Display the description and the README of a GitHub repository.

Any repository content can be access and see using.
```sh
gh repo view <repository_name>
```

With no argument, the repository for the current directory or the default repository content can be access and see using.
```sh
gh repo view
```

Use the flag `-b` to see a specific branch of the repository.
```sh
gh repo view <repository_name> -b <branch_name>
```

Use the flag `-w` the repository is open on the browser.
```sh
gh repo view <repository_name> -w
```

### Clone
A repository can be cloned localy by using 
```sh
gh repo clone <repo_name_or_URL>
```

### Delete
If the current repo is required to be deleted use.
```sh
gh repo delete
```

Or any repository can be delete by passing the name
```sh
gh repo delete <repository_name>
```

To confirm deletion without prompting use flag `--yes`
```sh
gh repo delete <repository_name> --yes
```

### Edit
A repository can be edited using de CLI.

The repositories can be personal or from an organization (if you have permissions). To the define it set the `<owner_name>`

A panel with the options to edit the repository will display with.
```sh
gh repo edit <owner_name>/<repository_name>
```
Some usefull flag are:

Use `--allow-forking` in a organization repository

```sh
gh repo edit <owner_name>/<repository_name> --allow-forking
``` 

Use `--default-branch <name>` to set the default branch name for the repository
```sh
gh repo edit <owner_name>/<repository_name> --default-branch <branch_name>
``` 

With `--visibility <string> ` the visibility of the repository can be change the posibilies are `public,private,internal`
```sh
gh repo edit <owner_name>/<repository_name> --visibility <option_selected>
``` 

Multiple flags can be combined like, enable wiki in the repository with `--enable-wiki`, enable discussions in the repository with `--enable-discussions` and enable issues in the repository with `--enable-issues`.
```sh
gh repo edit <owner_name>/<repository_name> --enable-wiki --enable-discussions --enable-issues
``` 

To toggle a setting off, use the `--<flag>=false` syntax.
```sh
gh repo edit <owner_name>/<repository_name> --enable-auto-merge=false
``` 

### Sync
A local repository can be syncronized from a remote repo.

If it is not detailed the current reposity is the syncronized.
```sh
gh repo sync
```
Or it can be specified.
```sh
gh repo sync <repository_name>
```
If the syncronization is required in a specific branch use `-b <branch_name>` flag
```sh
gh repo sync -b <branch_name>
```

### Rename

To rename a repository use by default it will apply to the current repository
```sh
gh repo rename <new_name> 
```

To use in any repostory use the flag `-R`.
```sh
gh repo rename <new_name> -R <owner_name>/<repo_name>
```

## GIST
Gist can be access by cli, allowing to manage, create, delete and see this.

### Clone
A local copy of a remote gist can be done by cloning it with
```sh
gh gist clone <URL or ID>
```

### List 
The gist from an account with the ID, descrition, files, visibily and update can be listed using.
```sh
gh gist list
```

### View 
To see a gist locally (without cloning) use
```sh
gh gist view <ID>
```

To open the gist in the web browser use the `-w` flag
```sh
gh gist view <ID> -w
```

## LABEL
The CLI allows to see, work and edit with labels.

### List
To see the current list of labels use.
```sh
gh label list
```

### Create
To create a new label. Must specify name for the label.

The description is set with `-d` flag and color with `-c` (both are optional). If a color isn't provided, a random one will be chosen. The label color needs to be 6 character hex value.
```sh
gh label create <label_name> -d "description text" -c <hex_color>
```

### Edit

To update name, description and/or color from an existing label use.
The name is set with `-n` flag, description is set with `-d` and color with `-c`. Not allways all need to be updated. They can be choosen.
```sh
gh label edit <label_name> -n <new_label_name> -d "new description" -c <new_hex_color>
```

### Delete
Delete a label from a repository
```sh
gh label delete <label_name>
```

## ORGANIZATION

To see the list organizations for the authenticated user.
```sh
gh org list
```