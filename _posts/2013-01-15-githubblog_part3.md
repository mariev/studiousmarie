---
title: a github blog - part three
layout: blogpost
tags: github webdev tutorial
---

In the [last post](http://mariev.net/studiousmarie{{page.previous.url}}), I 
showed you how to organize your website to find the github host via a custom 
domain and some basic infrastructure.

Now the fun part: generating content!

In the *gh-pages* branch create the following folders:

__media__	
Store all ```css``` and ```js``` files here

__p__	
Stand-alone pages (e.g. 'About Me' or 'Contact') go in this folder. These
will be .md files.

__\_layouts__	
Html files for use as templates for the various page types (e.g. 'blog post' or 
'default'). Use {{content}}  as a placeholder for the unique portion of the page. 

__\_posts__		
Markdown files for each post. Publication
date and permalink are determined by the name of your post file. The format is: 
YYYY-MM-DD-post\_title.md. Thus ```2013-01-15-githubblog_part3.md```
posts on January 15, 2013 with the permalink 
```http://mariev.net/studiousmarie/2013/01/15/githubblog_part3.html```. To write
posts for future publication (e.g. while on vacation or during finals crunch), 
simply name the file with the publication date. Github publishes only up to current
date. Syntax resources:
[Markdown](http://daringfireball.net/projects/markdown/syntax); 
page elements using [liquid extensions](https://github.com/shopify/liquid/wiki/liquid-for-designers)
 and [jekyll additions](https://github.com/mojombo/jekyll/wiki/Liquid-Extensions)

###### Previewing content

Once these files are populated and updated to github, the servers will automatically
build the site by parsing markdown files using Jekyll and Liquid. Unless you can write
perfect code on the first try (not me!), it makes sense to preview the files before they
go live. 

View the site locally by:

1. Open a command prompt [windows] or terminal window [mac, linux]
2. Navigate to your repository folder (e.g. ```studiousmarie```)
3. Type: ``` jekyll --server --future```
4. In your favorite browser, navigate to: ```localhost:4000```

When you're satisfied with the appearance, simply update the github repo as normal.

###### Front matter
Each page, whether a stand-alone or post, will include a few lines of front matter. 
These values tell Jekyll what template to use and instantiates variables. Each value
occupies a single line in the form ```variable name: value```. Front matter is separated
from content by a line of three hyphens on a separate line above and below. For example,
the front matter for this post is:

{% highlight r %}
---
title: a github blog - part three
layout: blogpost
tags: github webdev tutorial
---
{% endhighlight %}

You should now have enough information to create a complex blog, with all content pages in 
markdown, hosted by github and accessible via a custom domain. Next, I will give pointers
on integrating social media tools: RSS, commenting.


> **power users**     
> In the front matter, change the date to waaaay future for drafts that should
> not see the light of day until you explicitly say so. For example, this post in 
> draft state had a extra line:
>
> ```date: 3013-01-15```. 