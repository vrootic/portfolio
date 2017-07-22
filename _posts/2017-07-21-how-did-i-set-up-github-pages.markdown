---
title: "How did I set up GitHub Pages"
layout: post
date: 2017-07-21 22:00
image: false
headerImage: false
tag:
- jekyll
- github
category: blog
author: vicyang
description: 
---



# How did I set up GitHub Pages

There are a lot of tutorials out there and I just want to contribute one today. There is a [StaticGen](https://www.staticgen.com) that tells you which static site generator is the most used. In 2015, I have tried [Hugo](http://gohugo.io/) in the first place. It was really nice, and there are a lot of blogs that tell you why they changed from Jekyll to Hugo or other static site generator. I'm not here to tell you which one is better, I just want to tell you how I set up Jekyll. If you tried to deploy on GitHub, I think Jekyll is still a good static site generator to use.

### Prerequisite

- Ruby (because you need to use gem install)
- Git (just basic knowledge)
- GitHub account (you need an account before you can deploy blog on it)

### Install

	~$ gem install jekyll
	
Next, you can use Jekyll to initiate a project
	
	~$ jekyll new my-new-site
	~$ cd my-new-site
	~/my-new-site$ jekyll serve

Then, open your browser and go to [http://127.0.0.1:4000](http://127.0.0.1:4000) and you can see your default theme serving on local.

### Deploy to GitHub

Remember we already have our GitHub account. If you don't have this, go to GitHub and sign up for one.

At this point, you can decide what kind of url does your website have?

- Use GitHub default url **https://username.github.io**
- Apply custom domain **https://example.com**

#### Use GitHub default url

Before proceeding, you have to make sure you have created a repository named **<i>username.github.io</i>** where username is your username (or organization name) on GitHub.

For more details, you can look [here](https://pages.github.com).

	~/my-new-site$ git init .
	~/my-new-site$ git add .
	~/my-new-site$ git commit -m 'init git'
	
	git remote add origin https://github.com/username/username.github.io.git
	git push -u origin master

After you push repo to GitHub, it will automatically build the website on **master** branch.

#### Apply custom domain

In this case, you have to set your branch to **gh-pages** and add a CNAME file in this repository, which contains the domain you bought from [GoDaddy](https://godaddy.com) or other provider.

* Take GoDaddy for example, please specify A to **192.30.252.153** and **192.30.252.154** and CNAME to **username.github.io**. 
Just like the following picture.
<img src="{{site.url}}/assets/images/2017-07-21-how-did-i-set-up-github-pages-in-2017/1.png">
<figcaption class="caption">Godaddy DNS settings</figcaption>
<br/>

* Back to local, we can start pushing repository to GitHub.
	
		~/my-new-site$ git init .
		~/my-new-site$ git checkout -b gh-pages
		~/my-new-site$ git add .
		~/my-new-site$ git commit -m 'init git'
	
		git remote add origin https://github.com/username/username.github.io.git
		git push -u origin gh-pages


* Go to GitHub repository settings page to check GitHub Pages Settings:
<img  src="{{site.url}}/assets/images/2017-07-21-how-did-i-set-up-github-pages-in-2017/2.png">
<figcaption class="caption">GitHub Repository Settings Tab</figcaption>
<br/>

* Please make sure **source** points to **gh-pages** branch and **custom domain** points to the domain you bought.
<img src="{{site.url}}/assets/images/2017-07-21-how-did-i-set-up-github-pages-in-2017/3.png">
<figcaption class="caption">GitHub Pages Settings Area</figcaption>
<br/>

* Then you can go to your domain and see the result.

### Reference

[1] [GitHub Pages](https://pages.github.com)

[2] [利用Jekyll與Github Page建立自己的Dev-Blog](http://seans.tw/2016/make-own-blog-with-jekyll-and-github-page/)

[3] [Github Pages + Jekyll 快速架站](http://lywdev.space/2016/08/30/create-website-with-github-and-jekyll/)

[4] [Setting up GitHub Pages with Jekyll](http://www.stephaniehicks.com/githubPages_tutorial/pages/githubpages-jekyll.html)

[5] [Jekyll x Github x Blog 系列](https://rhadow.github.io/2015/02/18/Jekyll-x-Github-x-Blog-Part1/)