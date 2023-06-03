---
title: git add
layout: default
parent: Basic Commands
nav_order: 3
---

Let's start tracking files with git. We can do this with the add command:

```bash
git add README.md
```

Now what does `git status` tell us?

Output:
```
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   README.md
```

Cool! Git is now actively watching our README.md file for changes. Let's add another line to the file and see what git has to say about it.

```bash
echo "this website is going to be awesome" >> README.md
```
Let's run `git status` again:
Output:
```
On branch main

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)
	new file:   README.md

Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
	modified:   README.md
```

So as we can see, now that README.md has been added, git is watching it for changes. If we want to save these changes to the index, we just add the file again:
```bash
git add README.md 
git status
```
