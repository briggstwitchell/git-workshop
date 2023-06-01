---
title: git status
layout: default
parent: Basic Commands
nav_order: 2
---

Anytime we want to see what's going on with git, we can run this command:

```bash
git status
```

Output:
```
On branch main

No commits yet

nothing to commit (create/copy files and use "git add" to track)
```

Git status is a very handy command. It tells us:
* where we are 
* what we've done
* some options for what we can do.

***

Let's create a README.md file for our code repository and run `git status` again.

Output:
```
On branch main

No commits yet

Untracked files:
  (use "git add <file>..." to include in what will be committed)
        README.md

nothing added to commit but untracked files present (use "git add" to track)
```

Now git tells us we have an untracked file. What does this mean? Well, git only tracks files that we tell it to keep track of. So far, as far as git is concerned, this is still an empty directory. Until we use our next commmand...