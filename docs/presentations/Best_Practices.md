---
title:
 - Best Practices
subtitle:
 - Version &hash
author:
 - Joe
 - Lee
institute:
 - Concord Robotics Team 1721
description: |
    A guide to best practices.
theme: Dresden
navigation: frame
date: "Build Date: &date"
aspectratio: 169
logo: resources/logo.png
section-titles: false
toc: false
---


# Naming Conventions

## Why do we use naming conventions?

Naming Conventions are important because they
help other team members understand what your code does.

Since switching to python, we get to have extra
flexibility but our approach should generally be the same.

## Example 1, Docstrings

```python
def getTargetAngle(vision_x, vision_y):
    """Returns the vision target angle

    This method returns the relative angle (in radians)
    of the current vision target

    Parameters:
        vision_x (float): A float between -1 and 1
        vision_y (float): A float between -1 and 1

    Returns:
        target_angle (float): Angle of the target in radians
    """

    ... code ...
```


## Example 2, Comments in code

```python
drivetrain.run()  # Runs the drivetrain

coolWheelID = 1    # Updated 1/1/1999
uncoolWheelID = 2  # Updated 1/1/1999

# This makes a long object
my_long_object = object_generator(
    long_obnoxious_subobject,
    another_long_subobject)
```


# Auto Formatting

## Python Black

Configure `black` to be your auto-formatter for python.
This can make staying in compliance with unit tests much
easier, as it will auto format for you if you enable it.

If using vscode, you can do this by setting `black`
under `python.formatting.provider`


# Git

## Git commits

Git commits should be meaningful, and should not be too long.

A good rule of thumb is

> If it cannot be summed up in a commit title,
> it is too much to include in a single commit

There is no need to push every commit as soon as it is created, it can be
good practice to make several commits, especially if you are implementing
a large feature. Ex:

```
Make rio log camera messages (possible fix for #69)
Display camera messages on dashboard
Process camera messages in rio
Images process correctly, this closes #69
```
