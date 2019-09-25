---
layout: post
title: Build Github Page using Jekyll static site generator
date: 2017-09-12 00:00:00 +0300
description: You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. # Add post description (optional)
img: github-jekyll.jpg # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Github,Jekyll,Ruby] # add tag
---

If you want to build Github Page to create a blog or documentation page this is what you all need to prepare (this tutorial using Windows 10 OS).
* Install Git CLI , Ruby and Jekyll
* Create github page repository
* Code Editor (Sublime or Visual Studio Code)

### Step 1 : Install Git CLI , Ruby and Jekyll

Assume you already have github account, if not sign up now in [here](http://github.com), Then get Installer and install the necessarry app listed below:
* Git CLI [(source)](https://git-scm.com/downloads).
* Ruby Installer for Windows [(source)](https://rubyinstaller.org/downloads/). # get installer with DEVKIT

Now check the version of your ruby app using (the version must be higher than 2.1):
> ruby -v

In my development i'm using ruby version :
> ruby 2.6.4p104 (2019-08-28 revision 67798) [x64-mingw32]

Install bunler and jekyll using gem :
> gem install jekyll bundler


### Step 2 : Create github page repository

To create github page just create new repository and fill repository name using this format "yoursitename.github.io" and click Create repository.

![Create Github Page Repository]({{site.baseurl}}/assets/img/github_page/create-repo.jpg)

Create new repository on your local machine :

> * echo "# yoursitename.github.io" >> README.md
* git init
* git add README.md
* git commit -m "first commit"
* git remote add origin https://github.com/username/yoursitename.github.io.git
* git push -u origin master
{: color=black}

Then open setting and scrool down to "Github Pages" section. Choose the source to "master branch".

![Github Page Setting]({{site.baseurl}}/assets/img/github_page/github-pages-setting.jpg)