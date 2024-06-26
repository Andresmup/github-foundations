# **GIT w/GITHUB BASICS**

## GIT CONFIG
The first step when using git after installing it, is to set up email and username. This values are storage in a local file named git config file

The gitconfig file is what stores your global configurations for git such an email, name, editor and more

Showing the contents of .gitconfig file
```sh
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email.
```sh
git config --config user.name "Andresmup"
git config --config user.email "andresmunozpampillon@gmail.com"
```

The default global editor can be configure using
```sh 
git config --global core.editor emacs
```

## GIT HIDDEN FOLDER
It's posible to check if there is git repository in a project, folder project o local path.
If there is a hidden folder called `.git` it's tells your that this project is a git repo.

## START GIT
For start a git local repo the are 2 main ways.
 - Creating a new empty repository on the local enviroment, using:
   > git init

 - Creating a local copy from a github repository including the history, using: 
   > git clone

### Git Init 

Some steps to create a new repository by using `git init` can be:
```sh
mkdir /workspaces/tmp/new-project #Create a new folder for the project
cd /worspaces/tmp/new-project #Move into the new folder
git init #Start a new git repository
touch Readme.md #Create a markdown file Readme.md
code Readme.md #Open the Readme.md file and writte something
git status #Uses git status to see what files (if there are) are track and untrack
git add . #If we want to track the changes to all files
git add Readme.md #If we want to track the changes to Readme.md only
git commit -m "Add Readme.md files" #Create a commit, which is a saved snapshot of the tracked files and contains a message.
```


### Git Clone
Can be using via HTTPS, SSH or GitHub CLI. For publics repo there is no key or authorization required.

#### HTTPS
```sh
mkdir tmp
cd /workspaces/tmp
```

```sh
git clone https://github.com/Andresmup/github-foundations.git
cd github-foundations
```

#### SSH

```sh
git clone git@github.com:Andresmup/github-foundations.git
cd github-foundations
```

#### CLI

```sh
gh repo clone Andresmup/github-foundations    
```
## STATUS
Git status shows you what files will or not be commited. Also known as files tracked and untracked.

```sh
git status
```


## ADD
To stage changes that will be included in the commit. Files that are track and untrack.

Can staged all with ```add .```

Can staged a specific file with ```add Readme.md```


## RESET
Reset allows to move Staged changes to be unstaged.
This is a useful to revert all files, for not to be commited.

```sh
git add . #Track all
git reset #Untrack previous
```
> **git reset will revert a git add**

## COMMIT
To commit code we can write git commit which will open up the commit edit message in editor of choice. 
To make the commit and open the editor to complite the info required.
```sh
git commit
```

Make commit and commit messages without opening an editor use the `-m` flag.
```sh 
git commmit -m "Message"
```

There is a way to add and commit in the same command by using `-a` flag.

The `-a` stands for all. This option automatically stages all modified files to be committed. If new files are added the `-a` option will not stage those new files. Only files that the Git repository is aware of will be committed.
```sh
git commit -a -m "Message"
```

It is posible to create an empty commit, useful as a placeholder using `--allow-empty` flag.
```sh
git commit -m "Empty commit" --allow-empty
```

## AMMEND
There is a way to make minor changes to the last commit using the flag `--amend`.
> [!WARNING]  
> **To use `--amend`, the last commit must not have been pushed**

> Amended commits are actually entirely new commits and the previous commit will no longer be on your current branch.

### Change last commit message
Amend can be used to change the las commit message
```sh
git commit --amend -m "Updated commit message"
```
### Include more files changes and change message commit
Amend can be used to add more files changes to the commit
```sh
git add FORGOTTEN-FILE-NAME
git commit --amend --no-edit
```
### An amend may no need a message change
Not always the message needs to be changed
```sh
git add FORGOTTEN-FILE-NAME
git commit --amend --no-edit
```
### Update author of the commit
Other properties like author can be modify
```sh
git commit --amend --author="andresmup <andresmunozpampillon@email.com>"
```

## STASH
If we want to save a work in progress by add but without commiting it into the branch. We can "save" it by stashing. So we can bring it back by poping it

```sh
git add .
git stash #"Save" our work in progress
git stash pop #Bring it our work in progress back
```
The stash work in progress will be put into a list of changes that can be access with. 
```sh
git stash list
```

Another option is name our stash and bring back the last one
```sh
git add .
git stash save name-of-stash
git stash apply
```

## LOG
Show recent git commits to the git tree, with some info like commit hash, author name, author email, branch, date, commit message
```sh
git log
```
The commit info can be compressed with the flag `--oneline`
```sh
git log --oneline
```
If there a need to see all commits in the history of branches, tags and other refs, it can be done by using the flag `--all`
```sh
git log --all
```

### Log Graph
Git can represent in a more "visual" way the commits. `--graph` allows to see in more detail how the branchs, commits, merges and other stuff interact in a more time line format
```sh
git log --graph
```
The flag `--oneline` can be convined with `--graph`
```sh
git log --graph --oneline
```
## REMOTE
A remote can be added to manage connections with other repositories. After adding a remote, you’ll be able to use ＜name＞ as a convenient shortcut for ＜url＞ in other Git commands.

To show the list of remote repositories use.
```sh
git remote
```
### Add
To create a new connection to a remote repository. 
```sh
git remote add <name> <url>
```
Often you will add remotes via upstream when adding a branch
```sh
git remote add <name> <url>
git branch -u origin new-features
```
### Remove
To remove the connection to the remote repository called ＜name＞.
```sh
git remote rm <name>
```
### Rename
A remote connection can be renamed
```sh
git remote rename <old-name> <new-name>
```

## PUSH
Push a repo branch to the remote origin. To prevent you from overwriting commits, Git won’t let you push when it results in a non-fast-forward merge in the destination repository.
```sh
git push <remote name> <branch>
```

To push all the local branches to the remote repository the `--force` flag can be used.
```sh
git push <remote name> --force
```

Tags are not pushed by default. To push it's.
```sh
git push <remote name> --tags
```

By using the flag `-u` when a push git estabish a follow relation between the two branches (local and remote).
So in future operations such `git push` o `git pull` Git will automatically remember which remote and local branch they belong to.

> [!NOTE]  
> To be able to make push from a local repository into a remote one a key or authorization is required

### Login authorization
When `git push` is executed if git do not detect any other method it will ask to open in the internet a browser a github page in which by login it validate our credentials to materialize the push action.

### Token authorization
> A personal access token need to be generated (PAT)

This can be done in https://github.com/settings/personal-access-tokens/new, it can be specific for one or more repository, or apply to all. A expiration date has to be defined.

And to be able to make a push it needs read and write permissions for:
>Commit statuses, Contents, Metadata

Now when git push it's execute (in VSC for example) can be authorize by passing the user name and the token as the password when the login is required. 

### SSH
When a repo is clone by ssh and we want to push back to the remote the changes. Or we just create a new local repo and want to push the work done into a new repote github repository. SSH can be used, it's a greate way to authenticated the pushes.


We will have to create our SSH rsa key pair, it will ask where the ssh keys will be stored.
```sh
ssh-keygen -t rsa
```
Then copy the public key, getting with.
```sh
cat /your_directory/.ssh/id_rsa.pub
```
Now the public key need to be added into your github account https://github.com/settings/ssh/new, add a title and paste in.

For test our connection run
```sh
ssh -T git@github.com
```

### CLI
Another way to make pushes, is by using github cli.

The first step is install it.
On Windows can be done downloading (and upgrading) it from https://cli.github.com/ or just by using

```sh
winget install --id GitHub.cli	
winget upgrade --id GitHub.cli
```

On linux run
```sh
brew install gh
brew upgrade gh
```
We have to login using the CLI, to authenticated the user it can be done via ssh or token.
```sh
gh auth login
```
The next step is clone the repository via cli, it will allow to push.

```sh
gh repo clone Andresmup/github-fundations
git push
```

## PULL
The `git pull` command is used to fetch and download content from a remote repository and immediately update the local repository to match that content.

Merging remote upstream changes into your local repository is a common task in Git-based collaboration work flows.

> [!NOTE]  
> The git pull command is actually a combination of two other commands, `git fetch` followed by `git merge`.

Fetch the specified remote’s copy of the current branch and immediately merge it into the local copy. 
```sh
git pull <remote name>
```

The `--no-commit` flag fetches the remote content but does not create a new merge commit.
```sh
git pull --no-commit <remote name>
```

To integrate the remote branch with the local one via `git rebase` use.
```sh
git pull --rebase <remote name>
```



## BRANCHES

Branching means you diverge from the main line of development and continue to do work without messing with that main line.

To check the list of branchs can be done by 2 ways.
```sh
git branch
git branch --list
```

To check the list of remotes branchs it's done by using `-a` flag.
```sh
git branch -a
```

Create new branch without checkout the current branch.
```sh
git branch <branch-name>
```

Checkout the branch.
```sh
git checkout <branch-name>
```

Create and checkout a new branch in one line of code by using `-b` flag.
```sh
git checkout -b <branch-name>
```

To rename the current branch it's done by using `-m` flag.
```sh
git branch -m <branch-new-name>
```

**Safe deletion of a branch (can't be done with unmerged changes)** it's done by using `-d` flag.
```sh
git branch -d <branch-new-name>
```

Force deletion (even if it has unmerged changes) can be done with `-D` flag.
> [!WARNING]  
> **This will permanently throw away all of the commits associated with a particular line of development**

```sh
git branch -D <branch-new-name>
```

> [!NOTE]  
> From Git version 2.23 onwards you can use git switch instead of git checkout to:

Switch to an existing branch
```sh
git switch <branch-name>
```

Create a new branch and switch to it, using the `-c` or `-create` flag.
```sh
git switch -c <branch-new-name>
```

Return to your previously checked out branch using the `-`
```sh
git switch -
```

You can give the `-m` flag to the command, which would try a three-way merge.
```sh
git switch -m <branch-name>
```

### Checkout and Switch Branchs comparison

| Difference | git switch | git checkout| 
| --- | --- | --- |
| Versions | Only works with newer Git versions (2.23 and above) | Works with both older and new Git versions |
| Search for a branch in the remote repository if it’s not found in the local repository | :heavy_check_mark: | :x: |
| Capable of doing other things besides switching branches | :x: | :heavy_check_mark: |
| Merge the current branch into another branch and switch to it | :heavy_check_mark: | :x: |

## MERGE
If we want to integrate the work (merge) developed in a branch into another (main) branch we do.

```sh
git checkout main
git merge <branch-name>
```
> [!NOTE]  
> If the two branches you're trying to merge both changed the same part of the same file, Git won't be able to figure out which version to use. The merge stops right before commit so you can resolve the conflicts manually (choosing which version use).

