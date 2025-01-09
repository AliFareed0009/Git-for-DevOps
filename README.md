# Git-for-DevOps


# This Repository is for Git Version Control System Practice 

This Repository is made to practice Git in and implement daily life scenarios of a Devops Engineer.

## What is version control?
Version control, also known as source control, is the practice of tracking and managing changes to software code. Version control systems are software tools that help software teams manage changes to source code over time. As development environments have accelerated, version control systems help software teams work faster and smarter. They are especially useful for DevOps teams since they help them to reduce development time and increase successful deployments.

Version control software keeps track of every modification to the code in a special kind of database. If a mistake is made, developers can turn back the clock and compare earlier versions of the code to help fix the mistake while minimizing disruption to all team members.

## Introduction
- Git is a fast, scalable, distributed revision control system with an unusually rich command set that provides both high-level operations and full access to internals.

## What is Git?
By far, the most widely used modern version control system in the world today is Git. Git is a mature, actively maintained open source project originally developed in 2005 by Linus Torvalds, the famous creator of the Linux operating system kernel.

## Architecture of Git
 ![Git Architecture](https://github.com/AliFareed0009/Git-for-DevOps/blob/1163be48fd9916ae7f60bdc7ec1aafccc89da824/Images/architecture.jpg)

## Install git

1. From your shell, install Git using apt-get:

```
sudo apt-get update
sudo apt-get install git
```

2. Verify the installation was successful by typing git --version:

``` git --version ```

### Set your basic information
Configure your email
``` git config user.email [your.email@domain.com] ```

Configure your name
``` git config user.name [your-name] ```

## Folders and Files

| Folder Name | Useage | Description |
| ------- | ----------- | ----------- |
| `Core Concepts` | Concepts | Main Concepts Every DevOps Engineer should know |

#### 
Git Commands
============

_A list of my commonly used Git commands_


### Getting & Creating Projects

| Command | Description |
| ------- | ----------- |
| `git init` | Initialize a local Git repository |
| `git clone ssh://git@github.com/[username]/[repository-name].git` | Create a local copy of a remote repository |

### Basic Snapshotting

| Command | Description |
| ------- | ----------- |
| `git status` | Check status |
| `git add [file-name.txt]` | Add a file to the staging area |
| `git add -A` | Add all new and changed files to the staging area |
| `git commit -m "[commit message]"` | Commit changes |
| `git rm -r [file-name.txt]` | Remove a file (or folder) |
| `git remote -v` | View the remote repository of the currently working file or directory |

### Branching & Merging

| Command | Description |
| ------- | ----------- |
| `git branch` | List branches (the asterisk denotes the current branch) |
| `git branch -a` | List all branches (local and remote) |
| `git branch [branch name]` | Create a new branch |
| `git branch -d [branch name]` | Delete a branch |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git checkout -b [branch name]` | Create a new branch and switch to it |
| `git checkout -b [branch name] origin/[branch name]` | Clone a remote branch and switch to it |
| `git branch -m [old branch name] [new branch name]` | Rename a local branch |
| `git checkout [branch name]` | Switch to a branch |
| `git checkout -` | Switch to the branch last checked out |
| `git checkout -- [file-name.txt]` | Discard changes to a file |
| `git merge [branch name]` | Merge a branch into the active branch |
| `git merge [source branch] [target branch]` | Merge a branch into a target branch |
| `git stash` | Stash changes in a dirty working directory |
| `git stash clear` | Remove all stashed entries |
| `git stash pop` | Apply latest stash to working directory |

### Sharing & Updating Projects

| Command | Description |
| ------- | ----------- |
| `git push origin [branch name]` | Push a branch to your remote repository |
| `git push -u origin [branch name]` | Push changes to remote repository (and remember the branch) |
| `git push` | Push changes to remote repository (remembered branch) |
| `git push origin --delete [branch name]` | Delete a remote branch |
| `git pull` | Update local repository to the newest commit |
| `git pull origin [branch name]` | Pull changes from remote repository |
| `git remote add origin ssh://git@github.com/[username]/[repository-name].git` | Add a remote repository |
| `git remote set-url origin ssh://git@github.com/[username]/[repository-name].git` | Set a repository's origin branch to SSH |

### Inspection & Comparison

| Command | Description |
| ------- | ----------- |
| `git log` | View changes |
| `git log --summary` | View changes (detailed) |
| `git log --oneline` | View changes (briefly) |
| `git diff [source branch] [target branch]` | Preview changes before merging |




## Git Branching
  ![Git Branching](https://github.com/AliFareed0009/Git-for-DevOps/blob/1163be48fd9916ae7f60bdc7ec1aafccc89da824/Images/Branch.avif)

### git init
Initializes a new Git repository in the current directory. This command creates a new .git directory, which contains all the necessary metadata and objects for version control.

```
git init
```

### git clone
Creates a copy of an existing Git repository. This command downloads the repository and its history from a remote server to your local machine.

`git clone <repository-url>`

`git clone https://github.com/user/repo.git`


### git status
Shows the current status of the working directory and staging area. It displays which changes have been staged, which are still unstaged, and which files are not being tracked by Git.

`git status`


### git add
Stages changes (new files, modifications, deletions) to be included in the next commit. It tells Git to track these changes.

```
git add <file>
git add index.html

To add all changes:
git add .
```


### git commit
Records the staged changes to the repository’s history. Each commit includes a commit message describing the changes.

`git commit -m "Commit message"`


### git push
Uploads local repository content to a remote repository. It is used to share changes with others and update the remote repository with your commits.

```
git push <remote> <branch>
git push origin main
```


### git pull
Fetches and integrates changes from a remote repository into the local repository. This command is used to update your local branch with changes from the remote branch.

```
git pull <remote> <branch>
git pull origin main
```


### git fetch
Downloads objects and references from a remote repository but does not merge them into the current branch. It is used to see if there are new changes in the remote repository without affecting your local work.

```
git fetch <remote>
git fetch origin
```


### git merge
 Integrates changes from one branch into the current branch. This command is used to combine changes from different branches.

```
git merge <branch>
git merge feature-branch
```


### git branch
Lists, creates, or deletes branches. Branches are used to develop features or fix bugs independently of the main codebase.

```
List branches:
git branch

Create a new branch:
git branch <branch-name>

Delete a branch:
git branch -d <branch-name>
```


### git checkout
Switches between branches or restores working directory files. It is used to move your working directory to a different branch or commit.

```
Switch branches:
git checkout <branch-name>

Restore files:
git checkout -- <file>

```

### git log
Displays the commit history for the current branch. It shows a list of commits, including commit messages, authors, and timestamps.

```
git reset

Soft reset (keeps changes in the working directory):
git reset --soft <commit>

Hard reset (discards changes):
git reset --hard <commit>
```

### git diff
Shows differences between the working directory and the index (staging area) or between commits. It helps in reviewing changes before committing.

```
git diff
```

### git stash
Temporarily saves changes that are not yet ready to be committed. It’s useful when you need to switch branches without committing the current changes.

```
git stash

To apply stashed changes:
git stash apply
```