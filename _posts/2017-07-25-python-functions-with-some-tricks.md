---
title: "Python Functions with some tricks"
layout: post
date: 2017-07-25 10:00
image: false
headerImage: false
tag:
- python
category: blog
author: vicyang
description: 
---

Define functions is one of basic Python skills. I would like to focus on closure and its tricks.


## Metadata

We can add some annotations on function in order to let programmers know how this function should be used.
	
{% gist vrootic/7bfd08c3ee72b954a687c827ce8b2ba9 %}

Python interpreter wouldn't give any semantic meaning on these statement. They are not type checks mechanism. However, they still give other maintainers enough clues to track code.

## If functions have multiple values to return, they are packed in tuple and returned.

## Default value in parameters

{% gist vrootic/07d976384d4310879c6967a1ee42c29f %}

**Indicated default values should always be immutable objects**
Like None, True, False, number or string

## Capture variable in lambda

{% gist vrootic/6b0c50430df61776627ec669d2ff5247 %}


## Using functools.partial

{% gist vrootic/c445cf3afffb1b74f4f65e8a88d6f5cc %}

## Closure

{% gist vrootic/6b33ec2f0f55eacd4dfe3e9c747ab288 %}

### When do we have a closure?

- We must have a nested function (function inside a function).
- The nested function must refer to a value defined in the enclosing function.
- The enclosing function must return the nested function.

### When to use closures?

Closures can avoid the use of global values and provides some form of data hiding. It can also provide an object oriented solution to the problem.

We may want to replace single-method class with closure.

{% gist vrootic/2b7aff3d95f782069f169c9a3f2bb200 %}

We may also want our callback functions to bring additional information

{% gist vrootic/7d1e0902683bff9d05aa9bf5edd6aac1 %}





## Reference

[1] [Python Closures](https://www.programiz.com/python-programming/closure)
[2] Python cookbook 3rd version