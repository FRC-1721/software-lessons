---
title:
 - Getting Started With Linux
subtitle:
 - Version &hash
author:
 - Joe
institute:
 - Concord Robotics Team 1721
description: |
    An introduction for
    team members new to
    linux.
theme: Dresden
navigation: frame
date: "Build Date: &date"
aspectratio: 169
logo: resources/logo.png
section-titles: false
toc: false
---


# Welcome To Linux

## Welcome to linux

Welcome to linux! If you're reading this you're likely  
new to linux entirely!

In the following sections, we'll go over a few differences  
between OS's you may be familer with, Such as _Microsoft Windows_  
or Apple's _macOS_.


# Coming from _Microsoft Windows_

## Introduction

If you're familer with Windows, then many things in linux will  
feel very odd! Windows and linux share nearly no common  
ancestry, and everything under the hood is built very different.

## Installing Software (Using a Package Manager)

One of the biggest differences will be the **Package Manager**.  
Nearly every linux **distro** will ship with a package manager,  
a tool for installing software via package **repositories**,  
installing software from a .exe or .msi dosent happen in linux!  
If you want some software, try this:

```console
$ sudo apt install <name of package>
```

### Arch

```console
# pacman -S <name of package>
```
