---
title: git status
layout: default
parent: Basic Commands
nav_order: 2
---

# Git status
---

Anytime we want to see what's going on with git, we can run this command:

```bash
git status
```

> ```
> On branch main
> 
> No commits yet
> 
> nothing to commit (create/copy files and use "git add" to track)
> ```
{: .terminal }

Git status is a very handy command. It tells us:
* where we are - right now, we're on the main branch
* what we've done - we haven't committed anything yet
* what we can do - we can add files to start tracking them

***

Let's create a README.md file for our code repository and run `git status` again.

> ```
> On branch main
> 
> No commits yet
> 
> Untracked files:
>   (use "git add <file>..." to include in what will be committed)
>         README.md
> 
> nothing added to commit but untracked files present (use "git add" to track)
> ```
{: .terminal }

Now git tells us we have an untracked file. What does this mean? Well, git only tracks files that we tell it to keep track of. So far, as far as git is concerned, this is still an empty directory. Until we use our next commmand...