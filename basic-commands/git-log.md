---
title: git log
layout: default
parent: Basic Commands
nav_order: 5
---

# Git log

---
Now that we have made a few commits, we should take a look at the history of our repository. Git has another command for this:

```bash
git log
```

Git log shows us each commit in our repository history, along with the hash of the commit. We will learn a little more about these hashes later, but just know that git uses a commit's hash to uniquely identify it.

> ```bash
> commit c6694de0f0de86a4656a311b1ee21c8ad379e3f4 (HEAD -> main)
> Author: tonyburwinkel <burwinkel.a@northeastern.edu>
> Date:   Tue Jun 6 21:01:26 2023 -0400
> 
>     added index.html
> 
> commit 6f86afaab8b138a62831651b306cc3cbf1ae6781
> Author: tonyburwinkel <burwinkel.a@northeastern.edu>
> Date:   Tue Jun 6 20:37:13 2023 -0400
> 
>     first commit, added README
> ```
{: .terminal}

Git log uses a pager to display our commit history, so you can use your up and down arrow keys to move up and down once the history gets long. 

Git log also has some useful options we can use to make our history easier to look at:

```bash
git log --oneline
```

> ```bash
> c6694de (HEAD -> main) added index.html
> 6f86afa first commit, added README
> ```
{: .terminal}

When you've got a lot of commits and are looking for one in particular, ```--oneline``` comes in handy. 

The shortened commit hashes can also be used to go back to earlier commits.