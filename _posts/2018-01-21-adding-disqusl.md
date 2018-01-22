---
layout: single
title: "Adding Disqus Support"
author_profile: true
modified:
categories: 
excerpt:
tags: [Jekyll, Jekyll setup, disqus]
comments: true
image:
  feature:
date: 2018-01-22T00:05:01.513Z
---

Since making my personal website, I have always been meaning to add comment functionality to it.  I've slacked on this part due to my last semester scramble and then the ensuing job search scramble.  But finally, I go around to doing it, and decided to just summarize the process in this post.

This is going to be a relatively short post since the Minimal Mistakes theme makes it very low friction to adding Disqus.  Note that your experience might be different if you are rolling with another Jekyll theme or are building a custom theme.

Without further ado, here are the steps to adding disqus comments to your Minimal Mistakes Jekyll site:

Disqus: 

First you need to actually register with Disqus and add a website.

1. Register at <https://disqus.com/profile/signup/>
2. Create a website at <https://disqus.com/admin/create/>
- Fill in `Website Name`, which will be your shortname. This is used in configurations later on Jekyll
3. Set up Disqus settings:
    1. Select Plan => Subscribe Now, under Basic
    2. Install Disqus => Select Jekyll => Configure
    3. Configure Disqus => Type in Website URL => Complete Setup

Jekyll:

I added `comments: true` to the YAML front matter (at the top of your post markdown files) for all of my posts.

Then I changed the following in _config.yml in the base Jekyll directory:

```
comments:
  provider               : "disqus"
  disqus:   
    shortname            : "your-disqus-shortname"
```

And there you have it.  Once you run `jekyll serve`, you should be able to be able to see your changes locally.  Once you commit and push to github, and you are gucci!

Now all your friends on the interwebs can throw shade at you on your fancy disqus-enabled Jekyll blog!