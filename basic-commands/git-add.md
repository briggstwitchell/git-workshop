---
title: git add
layout: default
parent: Basic Commands
nav_order: 3
---

# Git add

---


Let's start tracking files with git. We can do this with the add command:

The add command takes this format:
```bash
git add <filename>
```
Let's use it to start tracking the README file we made:

```bash
git add README.md
```

Now what does `git status` tell us?

![add readme](../images/add/add-readme.png)
{: .terminal }

Cool! Git is now actively watching our README.md file for changes. We could commit right now to permanently save our changes to the repository history. This would mean that anytime we wanted, we could have git take us back to this moment in the development of our project. Committing early and often is a good idea, but let's hold off just a little longer. Let's add another line to the file and see what git has to say about it. 
```bash
A website for showcasing my skills.
```
We know that git was tracking README.md for changes, so it should have noticed that the file changed. 

Let's run `git status` again and see if it did:

![changed readme](../images/add/changed-readme.png)
{: .terminal}

Yet another informative message from Git. This is why you should run git status before you do anything else with the Git repository. 

In this message, Git is telling us a few things:
* the old version of README.md can be committed now
* the new version (with the extra line) would not be committed if we made a commit right now
* we could also throw away our new changes by using ```git restore <filename>```

If we want to save the newest version of README.md to the index, we just add the file again:
```bash
git add README.md 
```

---
> Often, we will just want to back up everything we've worked on in the directory. Instead of adding each file individually, we can just add all files with:
> ```bash
> git add .
> ```
> or:
> ```bash
> git add -A
> ```
{: .pro-tip }
