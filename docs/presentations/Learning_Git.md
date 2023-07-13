---
title:
 - Learning Git
subtitle:
 - Version &hash
author:
 - Joe
 - Keegan
institute:
 - Concord Robotics Team 1721
description: |
    A tutorial on how to git
    started with git.
theme: Dresden
navigation: frame
date: "Build Date: &date"
aspectratio: 1610
logo: resources/logo.png
section-titles: false
toc: false
fontsize: 8pt
---


# Introduction to Version Control Software

## What is Version Control

Version Control Software allows software developers
(Yes, you) to manage and _work together_ when developing
large, complex codebases.

Working as a team is one of the most difficult parts of
software development, actually learning the code is difficult
too but any project is much harder if you are the only one working
on it.

## Examples of Version Control Software

 - Git
 - SVN
 - Subversion

## Why we use Git

Tools like git allow us to document _changes in code_, it
also enables us to work together, document bugs, changes
and all aspects of a complex and changing codebase.


# Using Git

## The git commit

A git commit is the fundamental component in a git project.

Unlike tools such as google drive, git does not store code
as files, instead, a git repo, is simply a collection of
_git diffs_,

Lets use this file as an example. lets say we modified this
very presentation.

```shell
...Make some modifications...
$ git add Learning_Git.md
$ git commit -m "Change something in Learning_Git.md"
```

## Git diffs

Lets look at what the git diff looks like after a change like that, we can use the `git diff`
command for this.

```diff
diff --git a/docs/presentations/Learning_Git.md b/docs/presentations/Learning_Git.md
index 39cda71..da0d71f 100644
--- a/docs/presentations/Learning_Git.md
+++ b/docs/presentations/Learning_Git.md
@@ -55,3 +55,5 @@ A git commit is the fundamental component in a git repo.
 Unlike tools such as google drive, git does not store code
 as files, instead, a git repo, is simply a collection of
 _git diffs_, 
+
+Lets use this file as an example. lets say we modified this very presentation.
```

Git tells us where in the file we modified the data (`@@ -55,3 +55,5 @@`) and whether
it was an addition `+` or a deletion `-`


## Git diffs

### Note {.alertblock}
You don't need to manually view the diff every time. But its handy to know that git is not tracking actual
files, but the differences between files. This will be helpful later on when we talk about branching.


## Git Blame

Using a feature of git called blaming, `git blame`` we can look back on the history
of any piece of code in the repo, find out when it was changed,
and by who.

```
74631165 (KenwoodFox        2021-12-03 15:58:40 -0500 24) # Introduction to Version Control Software
fceb20ea (KenwoodFox        2021-12-03 15:42:26 -0500 25) 
74631165 (KenwoodFox        2021-12-03 15:58:40 -0500 26) ## What is Version Control
fceb20ea (KenwoodFox        2021-12-03 15:42:26 -0500 27) 
74631165 (KenwoodFox        2021-12-03 15:58:40 -0500 28) Version Control Software allows software...
```

This is a very useful feature if we want to find a specific change that introduced a new bug, and check
any and all code that was introduced at that time.


## Git branching

One of the most important code collaboration issues arises when we want to edit the same file, or tree
of files together without stepping on each others toes.

You'll recall back that git only tracks the diffs between files, and not actual files.

Lets say we have a very simple repo with this single file:

```md
# Hello world!

This is a markdown file.

Please add some text here!
```


## A quick example

You're working with mechanical team to implement a new feature on the bot, a robot arm, the rest of the code
team has already left and is working on other things.

Before you get started, you might want to `git checkout main` and `git fetch` to make sure you're
up to date with the latest code from the repo. If you're behind, you can `git pull` to retreive commits
upstream`

Now you can `git checkout -b layout-robot-arm`, the -b option lets you create a new branch and its automatically
based off the branch you're currently on. Its good to base yourself off `main` as this is the latest fully
tested code.

## A quick example

Now you can start coding! Make small steps, little changes at a time.

```
Create arm.py with methods for controlling the bot manually
Integrate arm.py with robot.py
Create method for controlling the bot with a wii remote
Refactor arm.py for new arm design
```

Your commit messages should be short and generally in the afermative tense something like `Create new feature`
instead of `I created a new feature`. The prior makes reading git logs easier but there are no strict rules,
if its helpful to you, feel free to write what you think is most relevant.

There are no rules on the commit description (any line past the first is the description) feel free to write notes,
link issues (ex: #69) or @ other code team members (ex: This might conflict with what @khanMan is working on).

Finally, when you're all done, feel satisfied and `git push`!


# Installing git

## Instalation on GNU/Linux

### Ubuntu/Deb

```shell
$ sudo apt install git
```

### Arch Linux

```shell
# pacman -S git
```


# example tutorial

## initalize a new git repo

follow theses steps to make a empty git repo in temp folder

```shell
/tmp$ cd /tmp
/tmp$ mkdir git_lesson
/tmp$ cd git_lesson/
/tmp/git_lesson$ git init
Initialized empty Git repository in /tmp/git_lesson/.git/
```

## commit some changes

```shell
$ cd /tmp/git_lesson
/tmp/git_lesson$ nano README.md
/tmp/git_lesson$ git add README.md
/tmp/git_lesson$ git commit -m "make a readme.md"
[master (root-commit) 0ea961e] make a readme.md
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```
