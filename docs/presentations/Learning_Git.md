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
