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

{% highlight ruby %}ruby -v {% endhighlight %}

In my development i'm using ruby version :
{% highlight ruby %}ruby 2.6.4p104 (2019-08-28 revision 67798) [x64-mingw32] {% endhighlight %}

Install bunler and jekyll using gem :
{% highlight ruby %}gem install jekyll bundler {% endhighlight %}

### Step 2 : Create Jekyll Blog on your local Machine

There is many option to create new jekyll blog on your local machine.

#1. Create new jekyll blog with default template using command :

{% highlight ruby %}jekyll new yournewblogname {% endhighlight %}

#2. You can either download or clone the template from [(jekyll template)](https://jekyllthemes.io/).

Then run your jekyll on your local machine to make sure everything work.

{% highlight ruby %}jekyll serve {% endhighlight %}

And you will get url to your jekyll (usually on localhost:4000) like this :

![Github Page Setting]({{site.baseurl}}/assets/img/github_page/jekyll-serve.jpg)

Now check jekyll on your browser.

Let’s me explain a litte about jekyll structure and how tou can edit them.

* _posts: This is the folder that has all your blog posts. Each of these posts should be a markdown file and should be included within this folder for it to be listed in your blog.
* _site: This files in this folder are responsible for compiling your blog. You basically have different blog posts, images, pages lying in different folders. The files in _sites folder bring them together and publish it as a website.
* _config.yml: This file contains your site’s variables such as title, your usernames, urls etc.
* about.md: This is just a markdown file that contains data to be published in your about section
* gemfile: gemfile contains all the dependencies for this site. Meaning you are using jekyll. And within jekyll, you are using it’s default theme called ‘Minima’. The gem file specifies such info.
* index.md: contains info that is visible in the home page of your blog.

### Step 3 : Create github page repository

To create github page just create new repository and fill repository name using this format "yoursitename.github.io" and click Create repository.

![Create Github Page Repository]({{site.baseurl}}/assets/img/github_page/create-repo.jpg)

Go to your jekyll root folder and init new repository on your local machine and push your jekyll :

{% highlight ruby %}
* git init
* git add .
* git commit -m "first commit"
* git remote add origin https://github.com/username/yoursitename.github.io.git
* git push origin master
{% endhighlight %}

Then open setting and scrool down to "Github Pages" section. Choose the source to "master branch".

![Github Page Setting]({{site.baseurl}}/assets/img/github_page/github-pages-setting.jpg)

And now open "yoursitename.github.io" and your blog is ready to go.
