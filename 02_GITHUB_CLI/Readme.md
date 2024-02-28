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

## INSTALL
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

> [!NOTE]  
> To perform all the actions wanted make sure the (PAT) token has the permissions required or instead use SSH.

This command will open the menu for login.
```sh
gh auth login
```

## REPO
Using the CLI tool actions on the repositories can be done, this are the most usefull.

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

## ISSUES
The Github CLI allows to manage and see issues.

### List
The info show by the issue list is ID, title, labels, update. To check the open issues list in the current repository run.
```sh
gh issue list
```

The `-R` flags allow to work with a specific repository.
```sh
gh issue list -R <owner_name>/<repo_name>
```

By default only open issues are display, to see closed ones use `-s <state>` flag. Stated can be `closed, open, all`.
```sh
gh issue list -s close
```

Issues can be filtered by one or multiple labels using `-l` flag
open, all`
```sh
gh issue list -l <label_name> -l <label_name> 
```

### Status
Using status can be chech the issues assigned to you, the issues mentioning you and the issues opened by you in a repo.
```sh
gh issue status
```


### View
Display the title, body, and other information about an issue.
```sh
gh issue view <ID>
```

Using the `-w` flag it will be opened in the browser.
```sh
gh issue view <ID> -w
```

### Close
To close and issue using the cli follow the syntax. Where `-c` flag enable to leave a comment and `-r` to choose the reason which can be `completed,not planned`.
```sh
gh issue close <ID> -c "Comment" -r <reason>
```

## PULL REQUEST
Working with GitHub pull requests using the CLI.

By default it will be executed in the actual repo, it can be changed using the `-R` flag in any command detailing the `<owner_name>/<repo_name>`

### List
Info like ID, title, branch and created add will be display using.
```sh
gh pr list
```

By defualt only open PR are displayed. But using the `-s` flag this states can be selected `open,closed,merged,all`
```sh
gh pr list -s <state>
```

The filter can be done by head branch with `-H` flag.
```sh
gh pr list -H <branch_name>
```

### Status
It's posible to check current status of open PR with.
```sh
gh pr status
```

### Create
This command will open the menu for creating a PR from the current branch into main.

The ID, name of the PR and branch will be display.
```sh
gh pr create
```

### Close
For closing PR run the command using the syntax.
```sh
gh pr close <ID>
```
Optionally using the `-c` flag a comment can be writte and/or deleting the branch after closing `-d`.
```sh
gh pr close <ID> -c "Optional comment" -d
```

### Ready
Allow to swich (mark) a PR as ready for review, or as draft (work in progress)

If the PR is draft now, tranform in ready for review with.
```sh
gh pr ready <ID>
```

Using the `--undo` flag can convert a PR as draf (work in progress)
```sh
gh pr ready <ID> --undo
```

### Merge
In order to accept and merge a PR the easiest way it's by using the next command, that will open the menu for merging a specific PR.
```sh
gh pr merge <ID>
```

## ORGANIZATION

To see the list organizations for the authenticated user.
```sh
gh org list
```

## HELP
To see info about a command or an specific options type.
```sh
gh help <commnad>
```