# **GIT w/GITHUB BASICS**

## GIT CONFIG
The first step when using git after installing it, is to set up email and username. This values are storage in a local file named git configfile

The gitconfig file is what stores your global configurations for git such an email, name, editor and more

Showing the contents of .gitconfig file
```sh
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email.
```sh
git config --config user.name "AndresMP"
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
 - > git init
 - Creating a local copy from a github repository including the history, using: 
 - > git clone

### Git Init 

Some steps to create a new repository by using `git init` can be:
```sh
mkdir /workspaces/tmp/new-project #Create a new folder for the project
cd /worspaces/tmp/new-project #Move into the new folder
git init #Start a new git repository
touch Readme.md #Create a markdown file Readme.md
code Readne.md #Open the Readme.md file and writte something
git status #Uses git status to see what files (if there are) are track and untrack
git add . #Track the changes to all files
git add Readme.md #Track the changes to Readme.md only
git commit -m "Add Readme.md files" #Create a commit, which is a saved snapshot of the tracked files. This contains a message.
```


### Git Clone
Can be using via HTTPS, SSH or GitHub CLI. For publics repo there is no key or authorization required.

#### HTTPS
```sh
mkdir tmp
cd /workspaces/tmp
```

```sh
git clone https://github.com/Andresmup/github-fundations.git
cd github-fundations
```

#### SSH

```sh
git clone git@github.com:Andresmup/github-fundations.git
cd github-fundations
```

#### CLI

```sh
gh repo clone Andresmup/github-fundations    
```
## STATUS
Git status shows you what files will or not be commited

```sh
git status
```


## ADD
To stage changes that will be included in the commit. Files that are track and untrack.

Can staged all with ```add .```

Can staged a specific file with ```add Readme.md```


## RESET
Reset allows to move Staged changes to be unstaged.
This is a useful to revert all files,for not to be commited.

```sh
git add .
git reset
```
>git reset will revert a git add

## COMMIT
To commit code we can write git commit which will open up the commit edit message in editor of choice. 
Make commit and commit messages without opening an editor
```sh 
git commmit -m "Message"
```
To make the commit and open the editor to complite the info required
```sh
git commit
```

There is a way to add and commit in the same command by using -a flag.

The -a stands for all. This option automatically stages all modified files to be committed. If new files are added the -a option will not stage those new files. Only files that the Git repository is aware of will be committed.
```sh
git commit -a -m "Message"
```
## AMMEND
There is a way to make minor changes to the last commit using the flag `--amend`.

**If it has not been pusheed yet**

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

## LOG
Show recent git commits to the git tree, with some info like commit hash, author name, author email, branch, date, commit message
```sh
git log
```
The commit info can be compressed with
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
