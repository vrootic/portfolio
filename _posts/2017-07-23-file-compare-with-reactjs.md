---
title: "File Compare with ReactJS"
layout: post
date: 2017-07-23 10:10
tag:
- javascript
- reactjs
- bootstrap
- electron
image: false
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: 
category: project
author: vicyang
externalLink: false
---


## File Compare with ReactJS

Summary: A simple file compare tool with ReactJS


### FileCompare
Compare two Excel files

### What can it do for us?
1. Compare two Excel file (.xls or .xlsx) by selecting common attributes. If there are some different rows or duplicate rows, this program will show them for you.
2. The different rows can be exported as .csv file.

### How does the comparing process take action?
1. In the beginning, we preselect the "authentication ID" as the primary field, 
  and the program would check whether the given fields are the same based on the primary field.
2. In the next version, the program will choose which field can be the primary field.

### How can we use the program?
1. Install Electron http://electron.atom.io
2. Clone this respository to local machine
<pre><code>git clone https://github.com/vrootic/FileCompare.git</code></pre>
3. Execute it.
<pre><code>electron FileCompare</code></pre>


<img src="{{site.url}}/assets/images/2017-07-23-file-compare-with-reactjs/1.png">
<figcaption class="caption">Screenshot 1</figcaption>
<br/>

<img src="{{site.url}}/assets/images/2017-07-23-file-compare-with-reactjs/2.png">
<figcaption class="caption">Screenshot 2</figcaption>
<br/>

--

What has inside?

- Electron
- ReactJS
- Bootstrap

--

Check it out [here](https://github.com/vrootic/FileCompare)
