---
title: git init
layout: default
parent: Basic Commands
nav_order: 2
---

# Git init
---

First, let's start a git project in our directory.
open a terminal and type:

```bash
git init
```

So, what did this just do? 

When you run git init, you are setting up a git repository. This means that git is setting up any structures it needs to track your work, and placing them in a special folder called .git. Let's take a look at the contents of our directory now:

__linux/mac__
```bash
ls -a
```
__windows__
```powershell
dir -Force
```
---

> ```bash
> aristotle@aristotle:~/ws-playground$ ls -a
> .  ..  .git
> ```
{: .terminal }

There it is! Our git repository is being maintained in the .git folder. 

---
> .git is a **hidden** folder, so it won't show up in your file system unless you reveal hidden files. We won't be modifying the folder anyway, but it's good to know it is there. 
{: .note}

Since our repository was started in this directory, git will track any files we tell it about in this directory or any subdirectories we create. 

Aside from listing the directory contents, there are some other ways we can find out what is going on with our git repository...