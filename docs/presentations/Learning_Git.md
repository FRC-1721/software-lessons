---
title:
 - Learning Git
subtitle:
 - Version &hash
author:
 - Joe
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
