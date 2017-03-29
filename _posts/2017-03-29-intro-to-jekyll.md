---
layout: single
title: "First Post: Learning the Ropes to Jekyll"
author_profile: true
modified:
categories: 
excerpt:
tags: [Jekyll, Jekyll setup, formatting dates]
comments: true
image:
  feature:
date: 2017-03-29T04:32:36.834Z
---

I have heard of GitHub's free hosting of static Jekyll pages in the past, but I never bothered learning how to put a Jekyll site together. That was the case until last weekend.  I strapped myself down on my chair and began to build this personal site/blog, which was long overdue.  So, after getting a functional version of the site running, here I am, preaching the gospel of Jekyll and GitHub Pages.
  
> Come small son, let us leverage the powers of free web hosting.
>
> <cite>Eugene Ma</cite>

This post will serve as a guide to the putting together a Jekyll site with the "Minimal Mistakes" theme, as well as creating your first post.  *Very meta...*

First Jekyll Site
---
First of all, what is Jekyll?  Jekyll is an open-source site generator that takes markdown files that you write and converts that into a static website.  It is written in Ruby, so you will need to install [Ruby](https://www.ruby-lang.org) and [RubyGems](https://rubygems.org/) in order for the proceeding commands to work.

To set up your first Jekyll website, you simply followed the instructions on the [Jekyll](https://jekyllrb.com/) website.  I have noted the steps below:  

```
# Install Jekyll and Bundler gems through RubyGems
~ $ gem install jekyll bundler

# Create a new Jekyll site at ./your-site-name
~ $ jekyll new your-site-name

# Change into your new directory
~ $ cd your-site-name

# Build the site on the preview server
~/your-site-name $ bundle exec jekyll serve

# You should be able to see the site now in a web browser at http://localhost:4000
```

This is cool and all, but how do you get it on the world wide web?
For my website, I use GitHub pages to host my site for free.  if you know how git and GitHub works you can skip to the next section. If this is your first time using git, you can install a git client at <https://git-scm.com/>.  You will also need to create an account on [Github](https://github.com).  GitHub is a version control repository service that lets you keep your code on their website.  It also keeps various versions of the code you write, based on the "commits" you create.

Once that is all done, you will need to:
1. Create a repository on GitHub named *username*.github.io, where *username* is your username on GitHub
2. Setting up the remote repository to track your local repository:

```
# Initialize a new git repository if you have not done so already 
~/your-site-name $ git init

# You will need to add all the code in your current directory and make a commit first 
~/your-site-name $ git add .
~/your-site-name $ git commit -m "My first commit"

# Replace your-username with your corresponding username
$ git remote add https://github.com/your-username/your-username.github.io 

# Update the github repository with your site
$ git push origin master

# You will be prompted for your credentials, enter them.
# If all steps were completed without error, you should be able to see your site at your-username.github.io 
```    

But, I want to use Minimal Mistakes theme with GitHub pages!
---
Sorry to say that if you followed the steps of the previous sections, there is no easy way to apply the theme to your new project as of the current date.  If you are really set out to use the theme on GitHub pages (like I was), you will need to follow the proceeding steps:

Note: If you are following through with deleting a repository on GitHub, remember to create a backup copy before you delete it.  There is no way to recover it once it is deleted.  If you goof up a delete, **nobody else but you** will be held liable or responsible.
1. First, rename or delete your repository at https://github.com/your-username/your-username.github.io 
2. You will need to fork [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) on GitHub, this creates a copy of a Jekyll repository with a Minimal Mistakes theme on your GitHub account
3. Rename the repository to your-username.github.io 

By now, you should be able to verify that you have a working copy of Jekyll with the Minimal Mistakes theme on your GitHub page: *your-username.github.io*.

4. Now you will need a local version of the code repository to work with:

```
# To work on it locally, simply clone the repository:
$ git clone https://github.com/your-username/your-username.github.io 
```

Formatting Dates
---
To my understanding, Jekyll takes in ISO 8601 date formats as the date parameter for posts.    

So I needed a way to generate the current date and time for my new post.  My way of generating the date uses the client-side Javascript console (press F12 in your web browser, it should be at the bottom):

The code I used was:
``` javascript
// returns a Date object
d = new Date();

// returns a string of the Date object in ISO 8610 format
d.toISOString()
```

This is documented on Microsoft's [Javascript reference]( https://docs.microsoft.com/en-us/scripting/javascript/reference/toisostring-method-date-javascript).

More sections to come...
---
* This thing called Markdown
* Jekyll basics



            