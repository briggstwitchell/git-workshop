---
title: git init
layout: default
parent: Basic Commands
nav_order: 2
---

first, let's start a git project in our directory.
open a terminal and type:

```bash
git init
```

So, what did this just do? Let's take a look at the contents of our directory:

__linux/mac__
```bash
ls -a
```
__windows__
```powershell
dir -Force
```

There it is! Our git repository is being maintained in the .git folder. 
```bash
aristotle@aristotle:~/ws-playground$ ls -a
.  ..  .git
```
Note, this is a **hidden** folder, so it won't always show up in your file system. Git knows it is there and will use it to track anything that we tell it to in this directory and any subdirectories. Let's see what git is up to...