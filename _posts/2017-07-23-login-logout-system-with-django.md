---
title: "Login/Logout System with Django"
layout: post
date: 2017-07-23 11:20
tag:
- django
- bootstrap
- cookiecutter-django
image: false
headerImage: false
projects: true
hidden: true # don't count this post in blog pagination
description: 
category: project
author: vicyang
externalLink: false
---


## Summary

Just a simple demo for login/logout system with Email verification.

Also, deploy for [Live Demo on Heroku](https://i2x-challenge-demo.herokuapp.com/)


## Prerequisites

```
Python3
PostgreSQL>=9.4
Mac/Linux
```

## Use virtualenv

```
python -m venv ENV
source ENV/bin/activate
```

## Clone this repository

```
git clone https://github.com/vrootic/i2x_challenge.git
```

## Install packages

```
cd i2x_challenge
pip install -r requirements
```

## Initialize DB

```
createdb i2x_challenge
python manage.py migrate
```

## Create Superuser

```
python manage.py createsuperuser
```

## Start Dev Server

```
python manage.py runserver
```

Deployment instructions
===========================
## Install Heroku Toolbelt
First, [sign up to Heroku](https://signup.heroku.com/)
Then, install [Heroku toolbelt](https://toolbelt.heroku.com/)

```
heroku login
```

## Create Heroku app

```
heroku create [your_app_name]
```

## Set environment variables

```
heroku addons:create heroku-postgresql:hobby-dev
heroku config:set DJANGO_SECRET_KEY='[your secret key]'
heroku config:set DJANGO_SETTINGS_MODULE='config.settings.production'
heroku config:set DJANGO_ALLOWED_HOSTS='.herokuapp.com'
```

## Push to deploy

```
git push heroku master
```
## Migrate the DB

```
heroku run python manage.py migrate
```

Finish!



Link to live demo on Heroku
===========================

[Live Demo on Heroku](https://i2x-challenge-demo.herokuapp.com/)