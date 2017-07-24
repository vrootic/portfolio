---
title: "Realtime Twitter Streaming Render"
layout: post
date: 2017-07-19 10:00
tag:
- javascript
- flask
- socketio
- eventlet
image: false
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: 
category: project
author: vicyang
externalLink: false
---

## Realtime Twitter Streaming Render

This is one of my Flask project. I tried to render tweets by using asynchronous method that socketio provides. After set up Twitter API key, I can render tweets that contains keyword to browser asynchronously.

<img src="{{site.url}}/assets/images/2017-07-19-realtime-twitter-streaming-render/1.png">
<figcaption class="caption">Screenshot 1</figcaption>
<br/>

For core code,

{% gist vrootic/76c78793722bb49ffb432e930462f105 %}

===

For more details, you can check [here](https://github.com/vrootic/realtime-twitter-streaming-render/tree/master)


