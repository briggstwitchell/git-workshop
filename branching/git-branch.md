---
title: git branch
layout: default
parent: Branching
nav_order: 1
---
# Git branch
---

Let's add another file to our project:

```bash
touch style.css
echo "body {background-color: gray}" > style.css
git add . 
git commit -m "added styles"
```

We are at a point now where we might think about different ways we could develop our website. Suppose we wanted to see how our website looked with a yellow background, but we didn't want to lose the current state of our website. 

This is where __branching__ becomes useful. Obviously, this website is very simple, but if we were considering making major changes to the site, or adding a new feature, we would want to make a branch to work on these changes before we committed them to our working website. Let's make a new branch with the branch command:

```bash 
git branch yellow-bg
```

Let's see what that did by running ```git log --oneline``` again:

> ```bash
> 8a36368 (HEAD -> main) added styles
> c6694de (yellow-bg) added index.html
> 6f86afa first commit, added README
> ```
{: .terminal}

We can see our new branch, yellow-bg. 
We've created the branch, but we haven't actually switched to it yet. 
We know this because of the line that says HEAD -> main. 
HEAD is just a variable that git uses to tell us where we are in the repository structure. Most git repositories have at least one __integration branch__, like main. 

When we want to make changes to the integration branch, we make other branches, like yellow-bg, so we don't muddy up our integration branch with changes we haven't tested or fully implemented yet. 

This is an essential part of software development known as CI/CD, or continuous integration/continuous development. Version control systems like git make CI/CD possible. This is how you can have a live website that multiple developers work on concurrently. 

Any time we want to make a change to our project, we should develop and test it on a __feature__ branche before finally deciding to incorporate our changes into the main __integration__ branch.