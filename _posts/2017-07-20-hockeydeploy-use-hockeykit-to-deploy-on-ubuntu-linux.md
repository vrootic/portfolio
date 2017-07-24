---
title: "Hockeydeploy - Use HockeyKit to deploy on Ubuntu/Linux"
layout: post
date: 2017-07-20 10:00
tag:
- django
- javascript
- bootstrap
- css
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

Use HockeyKit to deploy on Ubuntu/Linux server in order to build a testflight-like service.

## Introduction

The project is finished when I was in Zoaks. Before we start the project, we used TestFlight to distribute iOS app to testers. However, we found a project called [HockeyKit](https://github.com/bitstadium/HockeyKit) and decided to extend this project for internal use.

In this project, we could use Django to upload new beta app to automatically generate a responsive website in order to download beta app.

On top of HockeyKit, we could achieve:

* **Over-The-Air app distribution**

  Distribute your applications via an automatically generated, and optimized for each type of client. So your app can be installed directly when invoked from a mobile device, or downloaded if called from a desktop computer.

* **In-App-Updates**

  Optional client to be integrated into your applications. Works similar to the Sparkle framework on the Mac. The app checks if there is an update available from your server and will provide upgrade options. If the operation system does not support OTA updates, the client will still inform the user about available updates.

* **Multiple Application Support**

  Provide multiple applications from one server to multiple clients and testers. Either by providing them all on a single web site, or individual pages per application.

* **Automatically generated web pages**

  Device specific and optimized web pages are automatically generated for each application. So the tester can either install the application directly if loading the web page on a device, or download the files when loading the web page from a desktop computer.

  By default all available applications appear in a single web page, but there is also an option to provide individual pages for each or selected applications.

* **Multiple Version Support**

  Upload multiple version of the same app to the server. Useful with the "Team Management" feature. It also provides you the option to store specific release notes per version.

* **Team Management** (iOS 4.x only, API V2 required)

  Assign devices (and their users) to specific teams and provide them different app versions. Your designer should get the latest unstable version but your clients Q&A testing only gets the most stable ones. This feature requires the apps to include the Hockey client.

* **Device Authentication** (iOS only, API V2 required)

  Add another security level to your applications. If non-authorized persons gets hold of your application, they could re-sign the application with their own certificates. This feature activates device authentication against your own Hockey service and blocks the application from being used if the device is not authorized.

* **Installation statistics** (iOS only)

  See which device is of which type, the installed app version, the system language (API V2 only), the OS version and see the last time the app has been started.

* **Does not require a database, PHP5 sufficient**

  The server only uses the filesystem and PHP5. There are no additional requirements.

* **Easy to setup and use**

  The server component is designed to be managed without any database, it only uses the filesystem to achieve all of its functionalities. This makes it very easy to install and maintain.

## Prerequisite

* Script files in this project must be applied on Linux-based server.
* Python2.7

## Step of building project

- Build Hockey Project
	- Set up [project-name] folder
	- Set up file directory in Apache http.conf to set up server file location on server
	- Target platforms are iOS/Android

- Set up parameter for PROJECT_NAME and PROJECT_PATH in settings.py

- Use pytho hockeyDeploy.py to build folder that required in (Set up [project-name] folder)

======

For more details, you can check [here](https://github.com/vrootic/hockeydeploy)