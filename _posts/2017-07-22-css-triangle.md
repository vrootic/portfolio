---
title: "CSS Triangle"
layout: post
date: 2017-07-22 23:00
image: false
headerImage: false
tag:
- css
category: blog
author: vicyang
description: 
---

I saw a blog which talked about how to make a css triangle.
Through simple box model, we could build css triangle.

Here is my note.

{% highlight css %}
.css-initial-box {
  width: 100px;
  height: 100px;
  padding: 16px;
  border: 12px solid transparent;
  border-top-color: red;
  border-right-color: green;
  border-bottom-color: blue;
  border-left-color: purple;
}

.css-square {
  width: 0px;
  height: 0px;
  border: 112px solid transparent;
  border-top-color: red;
  border-right-color: green;
  border-bottom-color: blue;
  border-left-color: purple;  
}

.css-bottom-triangle {
  width: 0px
  height: 0px;
  border-bottom: 112px solid blue;
  border-left: 112px solid transparent;
  border-right: 112px solid transparent;
}
{% endhighlight %}