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

![log long](../images/log/log-long.png)
{: .terminal}

Git log uses a pager to display our commit history, so you can use your up and down arrow keys to move up and down once the history gets long. 

Git log also has some useful options we can use to make our history easier to look at:

```bash
git log --oneline
```

![log oneline](../images/log/log-oneline.png)
{: .terminal}

When you've got a lot of commits and are looking for one in particular, ```--oneline``` comes in handy. 

The shortened commit hashes can also be used to go back to earlier commits.

---
# What is HEAD?
---

In the terminal output above, we can see that HEAD is pointing to main ```(HEAD -> main)```.

Whenever we use git log, it shows us the history of our repository and __where we are__ relative to that history. Right now, our head is pointing to the second commit in the repository, our most recent commit. 

If we wanted to go back to the state our repo was in when we made our first commit, we could use the git checkout command.

Git checkout can accept either a relative position or an absolute one. 