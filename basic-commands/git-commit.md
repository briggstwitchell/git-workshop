---
title: git commit
layout: default
parent: Basic Commands
nav_order: 4
---

# Git commit
---


Now that we've added a few files for git to track, we can make our first commit. 
```bash
git commit -m "first commit, added README.md and index.html"
```

Notice the -m option. This stands for __message__. 

Any time we make a commit, we want to give it a description that tells us whatever new changes have been made since the last time we committed.

But what is a commit anyway?

Well, if you remember from earlier, commits are like breadcrumbs. So now we have one breadcrumb on our trail. This means that any time we want, we can come back to this version of our project.
This is why descriptive commit messages are important. If we find ourselves trying to figure out where our program went wrong, we need to know what changes happened at each breadcrumb we could go back to.

---
> Adding and committing are different. 
> 
> When we *add* a file, we are placing it in the __index__.
> 
> When we *commit*, we are adding the index to the __object database__.
{: .note }
<br>

!["index vs repo"](../images/git-staging-area.png)
{: .text-center}

The index is also known as the *staging area*. We can add to the index as many times as we want before committing. We can't get back to the state of our project based on adding, though. Only commits let us do that. 

Adding is a good idea if we have reached a good spot in our project, but we're not ready to make a breadcrumb for us to come back to. Adding to the index often is a good idea. 

When we commit a file, we are placing it in the object database, aka our *repository*.

Commits are the breadcrumbs we've been talking about. Once a commit is made to the object database, it becomes a permanent anchor to a particular version of our project.

This means that we can revisit any of our old commits, no matter how far along we get in our project.

---

Let's make a new file called index.html, add it to the index, and commit our changes...