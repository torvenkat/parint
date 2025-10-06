---
date: 2025-09-05
tags:
  - macos
title: Ignore .DS-Store Files in Git
---
MacOS creates `.DS_Store` files every time you run `git status`.  This gets committed to git every time.  To avoid .DS_Store files getting committed, do the following 

## Create a Global .gitignore file

You need to create a global `.gitignore` file **if you don’t already have one**.

```
git config --global core.excludesfile ~/.gitignore_global
```

## Edit the global .gitignore file

Now add the `.DS_Stor`e to your global `.gitignore` file. 

```
echo .DS_Store >> ~/.gitignore_global
```

That't it!