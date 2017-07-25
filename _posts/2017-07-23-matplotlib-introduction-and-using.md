---
title: "Matplotlib Introduction and Using"
layout: post
date: 2017-07-24 9:00
image: false
headerImage: false
tag:
- python
- matplotlib
- ipython
category: blog
author: vicyang
description: 
---

## Matplotlib Introduction and Using

This slides is made for Taipei.py meetup. In this talk, I gave base knowledge how to use Matplotlib and gave some exercises in order to let readers understand what and why they need to know this knowledge before applying it.

### What is Matplotlib?

Matplotlib is a tool that implemented in Python. The primary target of this tool is another replacement of Matlab. Matplotlib has a convenient command-line interface. You can also trigger IPython to fast plot. You can use OO interface to compose complex figures.

* Pros

	- You can directly use Python to manipulate data and tweak.
	- Multiplot is better in Matplotlib.
	- You can apply LaTex to render plot.

* Cons

	- Because of the two interfaces (OO and GUI) exist, API is more complicated. You would see there are two or more methods to compose the same figures.

	- Official document is hard to read.



<img src="{{site.url}}/assets/images/2017-07-24-matplotlib-introduction-and-using/1.png">
<figcaption class="caption">Practice 1</figcaption>
<br/>

{% gist vrootic/2ad8365e6f24f4e9f9bd0368075d558d %}

<img src="{{site.url}}/assets/images/2017-07-24-matplotlib-introduction-and-using/2.png">
<figcaption class="caption">Practice 2</figcaption>
<br/>

{% gist vrootic/f963a9b2db614eeed18cf15f2d4bcfe3 %}

<img src="{{site.url}}/assets/images/2017-07-24-matplotlib-introduction-and-using/3.png">
<figcaption class="caption">Practice 3</figcaption>
<br/>

{% gist vrootic/f53669058e69124ac14e94e6bbe16e97 %}


<img src="{{site.url}}/assets/images/2017-07-24-matplotlib-introduction-and-using/4.png">
<figcaption class="caption">Compare Between Shell and Jupyter</figcaption>
<br/>

### Summary

In Matplotlib, class is following the rule **Figure -> Axes -> (Line2D, Text, etc)**.
One Figure can contain several Axes. Use Axes in Matplotlib indicates a plotting area.


For more details, you can check my slides.

<iframe src="//www.slideshare.net/slideshow/embed_code/key/xM90AmtXEilGEb" width="595" height="485" frameborder="0" marginwidth="0" marginheight="0" scrolling="no" style="border:1px solid #CCC; border-width:1px; margin-bottom:5px; max-width: 100%;" allowfullscreen> </iframe> 
<div style="margin-bottom:5px"> <strong> <a href="//www.slideshare.net/vrootic/matplotlib-64469117" title="Matplotlib 簡介與使用" target="_blank">Matplotlib 簡介與使用</a> </strong> from <strong><a target="_blank" href="https://www.slideshare.net/vrootic">Vic Yang</a></strong> </div>