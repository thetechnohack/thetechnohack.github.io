---
date: 2021-01-24 08:43:12
layout: post
title: Google Cloud Shell
subtitle: Getting started with cloud shell environment.
description: This post is all about how you can use a cloud based environment for your projects. We have talked about Google Cloud Shell, its features and limitations.
image: https://res.cloudinary.com/morphy/image/upload/v1611416944/cloud%20shell/GCP_logo.png
optimized_image: https://res.cloudinary.com/morphy/image/upload/h_399,w_760,c_scale/v1611416944/cloud%20shell/GCP_logo.png
category: cloud computing
tags:
  - google
  - cloud
  - terminal
author: sumitpatidar
---

If you always hesitate with installing different software packages on your local system — this blog is for you.

Yes, the best solution to this problem is a cloud based environment.

The cloud computing market is pretty huge but we are going to talk about Google Cloud Platform(GCP), more specifically about Google Cloud Shell.

GCP is a very big deal that's why we are just learning about cloud shell for now.

## What is Google Cloud Shell ?
Cloud Shell is an online development environment based on Google Cloud Platform (GCP).

It runs on a Debian-Based virtual machine, that can be accessed with any browser, it makes it easy to manage your projects and resources without having to install them on your local system.

## Cloud Shell Console
Cloud Shell provides you a console with two main utilities:

### 1.Cloud Shell Terminal
![terminal image](https://lh3.googleusercontent.com/bADt-LplQDbOD3LLXc8nB4zC5GUjV0MCieIWXOUd7j7gaHL2uDuPuZt3kYdl_KoclG4OHTQp26k=e14-w3004)

Cloud Shell Terminal is a linux-based command-line tool for accessing your VM instances.

It supports multiple terminal sessions and full **tmux** support.

It comes with tonnes of pre-installed tool & google cloud sdk.

you have full root privileges on your allocated VM and can even run sudo commands, if you need to.

### 2.Cloud Shell Editor
![editor image](https://lh3.googleusercontent.com/WhS3gyjmk-B3XGdOYtPsnCN6XWkbJPNk4WiTm6wF2RjjANdXcmKjzsPf6WPnvIYlWP_emz55lMYB=e14-w3004)

Cloud Shell Editor has a GUI environment where you can develop, build, debug & deploy your apps and projects

It also supports some useful extensions.

It has an built-in git client. You can easily preview and commit to your repo.

## Features
#### Online development
Access Cloud Console from any web browser. No need to do anything locally.

#### Free storage
It comes with free 5GB of persistent storage as $HOME directory.

#### Pre-installed tools
It comes with many pre-installed tools such as python, java, mysql, nano, vim, emacs, gcloud SDK etc.

#### Up-to-date
All the pre-installed tools always stay up-to-date.

#### Built-in git client
Cloud Shell Editor has a built-in git client. You can manage your repository and project easily.

## Limitations & restrictions
#### Custom packages
You can only install custom packages in $HOME directory. All the packages outside $HOME directory will lost after an hour of inactivity.

#### VS code extensions
You can not install any additional vs code extension on cloud shell editor but it comes with all essential extensions.

#### Private browsing & disabled third-party cookies
You can not use cloud console if you are using private browser or third-party cookies are disabled in your browser 

#### Coin mining & network scanning
Coin mining and network scanning using Cloud Shell are strictly prohibited. If you do such things your account may be disabled forever.

#### Weekly usage limit
Cloud Shell also has a weekly usage limit. If you reach your usage limit, you'll have to wait.

#### Cloud shell inactivity
If you do not access Cloud Shell for 120 days, your home disk will be deleted. You will be informed with email before resetting your $HOME directory.

That's all for now. In the next post we will talk about how to access Cloud Shell Terminal form your local terminal.
