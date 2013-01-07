---
title: a github blog - part two
layout: blogpost
tags: github webdev tutorial
---

In the [last post](http://mariev.net/studiousmarie{{page.previous.url}}), I 
showed you how to set up a github repository to host a website. *A really simple
website with one sad page.* 

In the *gh-pages* branches create the following files:

1. .gitignore		
This will tell github to ignore certain files when performing repo maintenance. 
[My .gitignore](https://github.com/mariev/mariev.github.com/blob/master/.gitignore):

{% highlight r %}
.site/		
~.*		
{% highlight r %}
	
2. 404.html
3. CNAME
4. _config.yml
5. favicon.ico