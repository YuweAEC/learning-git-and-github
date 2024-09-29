# Git and GitHub Guide

## INDEX
1. [Introduction](#introduction)
   - [What is Git](#what-is-git)
   - [Why Git](#why-git)
   - [Features of Git](#features-of-git)
   - [What is GitHub](#what-is-github)
2. [Configuring Git for the First Time](#configuring-git-for-the-first-time)
3. [General Git Features](#general-git-features)
   - [Initializing Git](#initializing-git)
   - [Staging Files](#staging-files)
   - [Making a Commit](#making-a-commit)
   - [Status of Files and Log](#status-of-files-and-log)
4. [Git Help](#git-help)
5. [Git Branching](#git-branching)
   - [Making a New Git Branch](#making-a-new-git-branch)
   - [Checking All Available Branches](#checking-all-available-branches)
   - [Switching to Other Branches](#switching-to-other-branches)
   - [Making a New Branch and Directly Switching to It](#making-a-new-branch-and-directly-switching-to-it)
   - [Deleting a Branch](#deleting-a-branch)
   - [Merging Two Branches](#merging-two-branches)
6. [Working with GitHub](#working-with-github)
   - [Push Local Repo to GitHub](#push-local-repo-to-github)
   - [Pull Local Repo from GitHub](#pull-local-repo-from-github)
   - [Pull Branch from GitHub](#pull-branch-from-github)
   - [Push Branch to GitHub](#push-branch-to-github)
   - [Git Clone from GitHub](#git-clone-from-github)
7. [Git Undo](#git-undo)
   - [Git Revert](#git-revert)
   - [Git Reset](#git-reset)
   - [Git Amend](#git-amend)

---

## Introduction

### What is Git
Git is a version control system that helps you keep track of code changes and collaborate on code with other developers.

### Why Git
- Git is widely used by over 70% of developers.
- Developers can work together from anywhere in the world.
- Git allows you to see the full history of the project.
- Git helps developers revert to earlier versions of a project.

### Features of Git
- When a file is changed, added, or deleted, it is considered modified.
- Modified files can be staged and then committed to store a permanent snapshot.
- Git allows you to see the full history of every commit.
- You can revert back to any previous commit.
- Git keeps track of changes in each commit rather than storing a separate copy of every file.

### What is GitHub
- GitHub is a platform that provides tools to use Git effectively.
- It is the largest host of source code in the world, owned by Microsoft since 2018.
- GitHub allows developers to collaborate on projects remotely.

---

## Configuring Git for the First Time

To set up your Git for the first time:

```sh
$ git config --global user.name "<Enter your username here>"
$ git config --global user.email "<Enter your email here>"
```

---

## General Git Features

### Initializing Git
Git will start tracking changes in the current folder:

```sh
$ git init
```

### Staging Files

Staging individual files:

```sh
$ git add <filename with extension>
```

Staging all files in a folder:

```sh
$ git add --all
$ git add -A
```

### Making a Commit

Adding commits helps keep track of progress and changes:

```sh
$ git commit -m "<Enter your message here>"
```

Committing without staging first:

```sh
$ git commit -a -m "<Enter your message here>"
```

### Status of Files and Log

View the status of files:

```sh
$ git status
$ git status --short  # Compact view
```

View commit history:

```sh
$ git log
$ git log --oneline
```

---

## Git Help

View help for specific commands:

```sh
$ git <command> -help
```

See all available options:

```sh
$ git help --all
```

To exit list view, press `SHIFT + G` to jump to the end and `q` to exit.

---

## Git Branching

Branches allow working on different parts of a project without impacting the main branch. Once work is complete, branches can be merged back.

### Making a New Git Branch

```sh
$ git branch <name of branch>
```

### Checking All Available Branches

```sh
$ git branch
```

### Switching to Other Branches

```sh
$ git checkout <branch name>
```

### Making a New Branch and Directly Switching to It

```sh
$ git checkout -b <branch name>
```

### Deleting a Branch

```sh
$ git branch -d <branch name>
```

### Merging Two Branches

It’s preferred to switch to the master branch before merging:

```sh
$ git merge <branch name>
```

---

## Working with GitHub

### Push Local Repo to GitHub

Add a remote repository:

```sh
$ git remote add origin <paste copied URL here>
```

Push the master branch to GitHub and set it as default:

```sh
$ git push --set-upstream origin master
```

Push changes to GitHub after the initial setup:

```sh
$ git push origin
```

### Pull Local Repo from GitHub

Pull changes from a remote repository:

```sh
$ git pull origin
```

### Pull Branch from GitHub

List all branches:

```sh
$ git branch -a  # All branches
$ git branch -r  # Only remote branches
```

Checkout and pull a branch:

```sh
$ git checkout <branch name>
$ git pull
```

### Push Branch to GitHub

Create a new branch and push it to GitHub:

```sh
$ git checkout -b <branch name>
$ git commit -a -m "<Message>"
$ git push origin <branch name>
```

### Git Clone from GitHub

Clone a repository:

```sh
$ git clone <copied URL>
```

Clone to a specific folder:

```sh
$ git clone <copied URL> <folder name>
```

---

## Git Undo

### Git Revert

Revert to a previous commit:

```sh
$ git log --oneline  # Find commit hash
$ git revert HEAD --no-edit  # Revert the latest commit
```

Revert to an earlier commit:

```sh
$ git revert HEAD~<x>  # 'x' represents the number of commits back
```

### Git Reset

Reset the repository to a previous commit:

```sh
$ git reset <commithash>
```

Undo reset (reset back to a specific commit):

```sh
$ git reset <commithash>
```

### Git Amend

Modify the most recent commit:

```sh
$ git commit --amend -m "<Commit Message>"
```

Amend files:

1. Stage the changes.
2. Amend with:

```sh
$ git commit --amend
```

---

Thanks for reading!
```

This `README.md` file provides a structured and easy-to-read guide for using Git and GitHub, organized in a logical manner with clear explanations of each topic.
