---
title:
 - Jack's Python Tutorial
subtitle:
 - Version &hash
author:
 - sheen#2961
institute:
 - Concord Robotics Team 1721
description: |
    A guide to best practices.
theme: Dresden
navigation: frame
date: "Build Date: &date"
aspectratio: 169
logo: ../resources/logo.png
section-titles: false
toc: false
---


# Importing modules

importing packages gives you access to premade methods to make coding easier.

```python
import wheel
```

when importing variables like this you do not need to call the package before the method

```python
from random import *
```

# Declare some variables

declaring variables in python is simple, you don't have 
to specify variable type, and no semicolons needed.

```python
myVar = 5
```

you can modify variables by using modifiers like +=, -=, *=, /=, etc.

```python
myVar += 1
```

# Logic

if statements check variable states and will run the commands inside of it if the variable check returns true

```python
if myVar == 6:
    print("my variable is 6")
```

a variable can be set to a method imported from a package

```python
randVar = randint(1, 10)
```
