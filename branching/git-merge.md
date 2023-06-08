---
title: git merge
layout: default
parent: Branching
nav_order: 3
---
# Git merge
---

Once we're happy with the work we've done on our feature branch, the next thing we want to do is __integrate__ it into main. Git has a special command for this called __merge__.

Before we merge, we should do a few things:
* run ```git status``` to make sure our changes are committed
* Commit any outstanding changes on the feature branch
* Switch to the branch we want to merge into

Running ```git status```:
```bash
> On branch add-styles
> nothing to commit, working tree clean
```
{: .terminal}

Looks like all of our work is committed. 

Let's switch back to our main branch:
```bash
git switch main
```

Now let's run the merge command. The syntax for the merge command is ```git merge <target-branch>```. Running this brings any changes from the target-branch into the branch we are on now. Let's try it:

```bash
git merge add-styles
```

> ```bash
> Updating 8828696..5cbef78
> Fast-forward
>  style.css | 4 ++++
>  1 file changed, 4 insertions(+)
>  create mode 100644 style.css
>  ```
{: .terminal}

Okay great, seems like it worked. 

Let's take a look at ```git log --oneline``` again.

> ```bash
> 5cbef78 (HEAD -> main, add-styles) added stylesheet
> 8828696 added index.html
> c750089 first commit, added README.md
> ```
{: .terminal}

Now HEAD is pointing at main again. This means we are on the main branch. We can see that now add-styles is on the same line as main. Main and add-styles are on the same commit, which is to say, their contents are identical now. 

## Delete Your Branches
---

This may seem strange, but the best thing to do now is to delete our feature branch. Don't worry, this won't remove anything important, and is considered a best practice. 

To delete a branch, we use the ```git branch``` command with the ```-d``` option. The format for the commane is ```git branch -d <target-branchname>```

Let's try it on our add-styles branch:

```bash
git branch -d add-styles
```
When we run the command, git gives us a little info:

> ```bash
> Deleted branch add-styles (was 5cbef78).
> ```
{: .terminal}

Note that this is the same as our current commit hash. This is because branches aren't really structural features in git. Branches are just labels for the last commit on a certain path in the git graph. All git is telling us here is that it has removed the label from our current commit. Both branches, main and add-styles, were pointing to the same commit. Now only the main pointer remains, but nothing has materially changed.

## Git is a graph

Specifically, it's a Directed Acyclic Graph. 
