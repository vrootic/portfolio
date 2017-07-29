---
title: "Python Crawler Example (1)"
layout: post
date: 2017-07-28 10:00
tag:
- python
- requests
- beautifulsoup
- generator
image: false
headerImage: false
projects: true
description: 
category: blog
author: vicyang
externalLink: false
---

I found **clicking on job posting website** could be automized, so I wrote a script for crawling. Here I used Python, beautifulsoup, requests and generators tricks for practicing.


I used Salesforce Career Page for example.

<img src="{{site.url}}/assets/images/2017-07-28-python-crawler-example-1/1.png">
<figcaption class="caption">Salesforce Career Website</figcaption>
<br/>


## Where should I get started?

I knew Google Chrome has tool to see each request sent from browser, so I used that to see the request I sent from browser. By seeing that, I could know what kind of information I can wrap in code and issue a query.

<img src="{{site.url}}/assets/images/2017-07-28-python-crawler-example-1/2.png">
<figcaption class="caption">Chrome Browser Developer Tool</figcaption>
<br/>

<img src="{{site.url}}/assets/images/2017-07-28-python-crawler-example-1/3.png">
<figcaption class="caption">Curl Example</figcaption>
<br/>

I pasted on editor and saw there was a **GET request** sent to Salesforce server. So, all I need is use requests to send a GET request to that and I can get the result.

{% gist vrootic/3144895face87e21f9616ff797c25f6b %}

Apply this code would receive 403. (HTTP Code 403 - Forbidden)


## What happened then?

Apparently, it's not enough for this request, so I guessed it required header information to send it.

{% gist vrootic/2e5dca03fed4787dea71bb29c7387554 %}

And I received 200. (HTTP Code 200 - OK)

## Start analyzing HTML

I put the response in BeautifulSoup and got parsed HTML. What I really need is the list of jobs. I observed that page from Chrome Developer Tool and found some important CSS tag.

{% gist vrootic/627dddeab82ae6b4617cff301c4638ea %}

<img src="{{site.url}}/assets/images/2017-07-28-python-crawler-example-1/4.png">
<figcaption class="caption">Result Example</figcaption>
<br/>

From this code, I got only 10 jobs listed on my terminal. There must be something wrong, and then I realized I only parsed **one page**.

Next part, I would use generator to generate different url.

## Generate URL by leveraging generators

I composed a <i>get_total_pages</i> function to get total pages. I found it's only 10 jobs listed on one page, so I used the <i>jobnumbers</i> divided by 10 and got the result.

{% gist vrootic/c7b0579e960de9092a0265e7d6fe5e7a %}

The function is the logic of generator.

	def url_cat(total_pages, url):
    	yield url
    	page = 1
    	while page <= total_pages:
        	yield url + str(page)
        	page += 1

I used 2 **yield** statements because the first url has no number concatenated afterward, and then I used the second **yield** to generate urls.

	url_gen = url_cat(total_pages, url)

    for url in url_gen:
        soup = get_soup(url, headers, payload)
        list_jobs(soup)

I applied for-loop to iterate the generator.

Now, I can get a list of information that I really wanted.


===

What's inside?

- Python
- Generators
- Requests
- BeautifulSoup


