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

> ```
> On branch main
> 
> No commits yet
> 
> Changes to be committed:
>   (use "git rm --cached <file>..." to unstage)
> 	new file:   README.md
> ```
{: .terminal }

Cool! Git is now actively watching our README.md file for changes. We could commit right now to permanently save our changes to the repository history. This would mean that anytime we wanted, we could have git take us back to this moment in the development of our project. Committing early and often is a good idea, but let's hold off just a little longer. Let's add another line to the file and see what git has to say about it. 
```bash
echo "this website is going to be awesome" >> README.md
```
We know that git was tracking README.md for changes, so it should have noticed that the file changed. 

Let's run `git status` again and see if it did:

> ```
> On branch main
> 
> No commits yet
> 
> Changes to be committed:
>   (use "git rm --cached <file>..." to unstage)
> 	new file:   README.md
> 
> Changes not staged for commit:
>   (use "git add <file>..." to update what will be committed)
>   (use "git restore <file>..." to discard changes in working directory)
> 	modified:   README.md
> ```
{: .terminal}

Yet another informative message from git. This is why you should run git status before you do anything else with the git repository. 

In this message, git is telling us a few things:
* the old version of README.md can be committed now
* the new version (with the extra line) would not be committed if we made a commit right now
* we could also throw away our new changes by using git restore

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
