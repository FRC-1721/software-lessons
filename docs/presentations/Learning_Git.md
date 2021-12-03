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
aspectratio: 169
logo: resources/logo.png
section-titles: false
toc: false
---


# Introduction to Version Control Software

## What is Version Control

Version Control Software allows software developers
(Yes, you) to manage and _work together_ when developing
large, complex codebases.

## Examples of Version Control Software

 - Git
 - SVN
 - Subversion

## Why we use Git

Tools like git allow us to document _changes in code_, it
also enables us to work together, document bugs, changes
and all aspects of a complex and changing codebase.


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


# Using Git

## The git commit

A git commit is the fundamental component in a git repo.

Unlike tools such as google drive, git does not store code
as files, instead, a git repo, is simply a collection of
_git diffs_, 

```shell
$ git add -A
$ git commit -m "Change something..."
```

## Git diffs

_diffs_ are descriptions of what changes are done on a file, for example:

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
+_diffs_ are descriptions of what changes are done on a file, for example:
```

## Git Blame

Using a tool like _git blame_ we can look back on the history
of any piece of code in the repo, find out when it was changed,
and by who.

```
74631165 (KenwoodFox        2021-12-03 15:58:40 -0500 24) # Introduction to Version Control Software
fceb20ea (KenwoodFox        2021-12-03 15:42:26 -0500 25) 
74631165 (KenwoodFox        2021-12-03 15:58:40 -0500 26) ## What is Version Control
fceb20ea (KenwoodFox        2021-12-03 15:42:26 -0500 27) 
74631165 (KenwoodFox        2021-12-03 15:58:40 -0500 28) Version Control Software allows software developers
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

``shell
~$ cd /tmp/git_lesson
/tmp/git_lesson$ nano README.md
/tmp/git_lesson$ git add README.md
/tmp/git_lesson$ git commit -m "make a readme.md"
[master (root-commit) 0ea961e] make a readme.md
 1 file changed, 1 insertion(+)
 create mode 100644 README.md
```
