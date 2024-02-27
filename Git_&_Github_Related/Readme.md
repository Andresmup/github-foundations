# **GIT w/GITHUB BASICS**

## Git Config
The first step when using git after installing it, is to set up email and username. This values are storage in a local file named git configfile

The gitconfig file is what stores your global configurations for git such an email, name, editor and more

Showing the contents of .gitconfig file
```
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

## Git Hidden Folder
It's posible to check if there is git repository in a project, folder project o local path.
If there is a hidden folder called `.git` it's tells your that this project is a git repo.

## Start Git
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
git clone git@github.com:AndresMPaws/GithubDemo.git
cd GithubDemo
```

#### CLI

```sh
gh repo clone AndresMPaws/GithubDemo    
```
## Status
Git status shows you what files will or not be commited

```sh
git status
```


## Add
To stage changes that will be included in the commit. Files that are track and untrack.

Can staged all with ```add .```

Can staged a specific file with ```add Readme.md```


## Reset 
Reset allows to move Staged changes to be unstaged.
This is a useful to revert all files,for not to be commited.

```sh
git add .
git reset
```
>git reset will revert a git add

## Commits
To commit code we can write git commit which will open up the commit edit message in editor of choice. 
Make commit and commit messages without opening an editor
```sh 
git commmit -m "Message"
```
To make the commit and open the editor to complite the info required
```
git commit
```

There is a way to add and commit in the same command by using -a flag.

The -a stands for all. This option automatically stages all modified files to be committed. If new files are added the -a option will not stage those new files. Only files that the Git repository is aware of will be committed.
```
git commit -a -m "Message"
```

## Log
Show recent git commits to the git tree, with some info like commit hash, author name, author email, branch, date, commit message
```
git log
```

