---
layout: post
title:  "Separate site on Github pages"
date:   2023-12-17 17:27:52 +0800
categories: Familiarization w SSG
---

# Introduction

This section explain how to set a separate site within Github pages.

By default, github pages hosts your jekyll site at `https://your-username/github.io`.

To do so, you have to name your repository as `your-username/github.io`. See screenshot below for reference:  
![Default Github Pages Repo](/images/TblxHaErU3.png)

### Separate Folder 

However, if you want to host your site at a specified base URL, you must:  
1. Name the repository accordingly
2. Explicitly indicate the base url in the jekyll config file

For example, suppose you want your page to be hosted at `your-username/github.io/test-project`. You will have to name your repository as `test-project`. See screenshot below for reference:  
![Default Github Pages Repo](/images/Xb7MgOrBbL.png)

With this configuration, you must also specify the configuration in your `_config.yml` for the base URL:  

```yml
title: Your awesome title
email: your-email@example.com
description: >- # this means to ignore newlines until "baseurl:"
  This is a site to test creation of a separate repo in github pages
baseurl: "/test-project" # the subpath of your site, e.g. /blog
url: "" # the base hostname & protocol for your site, e.g. http://example.com
twitter_username: jekyllrb
github_username:  jekyll
```

With the above configuration, you would be able to access the site at the following link:  [Test Project Site](https://walakaka77.github.io/test-project/ "Test Project Site!")

Notice that the URL of all the links have the base URL that was specified in the config:  
![Default Github Pages Repo](/images/9S4SPXzyVR.png)