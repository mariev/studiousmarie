---
date: 3013-01-10
title: a github blog - part two
layout: blogpost
tags: github webdev tutorial
---

In the [last post](http://mariev.net/studiousmarie{{page.previous.url}}), I 
showed you how to set up a github repository to host a website. *A really simple
website with one sad page.* 

In the *gh-pages* branch create the following files:

__.gitignore__ 


This will tell github to ignore certain files when performing repo maintenance. At minimum,
you will want to ignore local builds of the site (_more later_) and temporary files generated
via routine system operations. [My .gitignore](https://github.com/mariev/mariev.github.com/blob/master/.gitignore):
{% highlight r %}_site/
*~
{% endhighlight %}	

__404.html__

This is the page people will see if they click a broken link or type the wrong address.
As a general rule, the page should both be informative and help visitors find their way.
A short message, contact info and link back to the home page is sufficient. 

__CNAME__

For sites that have a custom domain name. No need for `http://` or `www`

___config.yml__

Any arguments to pass to jekyll. This is really useful if you want to use code 
highlighting syntax besides maruku, for example rDiscount. A complete list of 
options see [here](https://github.com/mojombo/jekyll/wiki/Configuration).

__favicon.ico__
What's the icon you want people to associate with your site? Typically this will be
displayed on the tab of the visitor's web browser. This should be a file of 32 x 32 
for compliance with newer retina-type displays.



Okay, now you know how to point people to your github hosting from a custom domain, support
lost visitors, keep your repo from collecting unnecessary files, and you've thought about
what syntax engine you want to use. Next, we'll go about pushing content.