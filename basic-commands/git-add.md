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

Cool! Git is now actively watching our README.md file for changes. Let's add another line to the file and see what git has to say about it.
```bash
echo "this website is going to be awesome" >> README.md
```
Let's run `git status` again:

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

So as we can see, now that README.md has been added, git is watching it for changes. If we want to save these changes to the index, we just add the file again:
```bash
git add README.md 
git status
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
