---
title: "Git Command Cheat Sheet (1)"
layout: post
date: 2017-07-22 22:00
image: false
headerImage: false
tag:
- git
category: blog
author: vicyang
description: 
---

Git basic commands for my reference


## Initialize
```
git init .
```

## Stage
```
git add .
```

## Commit
```
git commit -m 'msg' 							
```

## Open editor to check this commit
```
git commit												 
```

## Unstage
```
git reset           							
```

## Return to the nearest commit
```
git reset --hard <sha key>
```

## Return to specific version and commit (Not recommend)
```
git revert <sha key>
```

## List branches
```
git branch
```

## Change version
```
git checkout <sha key>
```

## Open a branch and ride on it
```
git checkout -b <branchname> 
```

## Branch commit
```
git checkout <sha key>
git checkout -b <branchname>
```

## Change master branch
```
git checkout new-master
git branch -m master old-master
git branch -m new-master master
```