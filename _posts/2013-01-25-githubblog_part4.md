---
date: 3013-01-25
title: a github blog - part four
layout: blogpost
tags: github webdev tutorial
---

By now you should have a site with one or more each of static pages, blog posts, 
and templates. You know how to start a Jekyll server to view local draft posts. And
you understand the filename nomenclature for scheduling posts.

But blogging is all about an easy conversation, no? I visit your RSS reader, you post
a reply, and so forth. Really, if you can master css, this will be a walk in the park.

### Enabling the RSS feed
In *gh-pages* create the folder ```feed``` and within that, the file ```index.xml```. 
This xml file
will be parsed by Jekyll and can use any of the page elements as for the posts or any 
stand-alone pages. The key elements to include are:

##### Suppress layout in the YAML front matter
{% highlight xml %}
---
layout: nil
---
{% endhighlight %}
##### Specify the xml version and link to the stylesheet

{% highlight xml %}{% raw %}<?xml version="1.0"?>
<?xml-stylesheet type="text/css" 
	href="http://mariev.net/media/css/rss.css" ?>
{% endraw %}
{% endhighlight %}
##### Designate the rss version	
{% highlight xml %}
{% raw %}
<rss version="2.0" xmlns:atom="http://www.w3.org/2005/Atom">
{% endraw %}
{% endhighlight %}
##### Place content inside the ```<channel>```  &  ```</channel>``` tags	
At content start, include:	

- title	
- link to landing page	
- description	
- language encoding	
- publication date	
- last build date	

{% highlight xml %}{% raw %}
<title>studiousmarie</title>
<link>http://mariev.net/studiousmarie</link>
<atom:link href="http://mariev.net/studiousmarie/feed/index.xml" 
	rel="self" type="application/rss+xml" />
<description>feed for blog studiousmarie</description>
<language>en-us</language>
<pubDate>{{ site.time | date: "%a, %d %b %Y %H:%M:%S %z" }}</pubDate>
<lastBuildDate>{{ site.time | date: 
	"%a, %d %b %Y %H:%M:%S %z" }}</lastBuildDate>
{% endraw %}	
{% endhighlight %}

> It may be valuable to present only a snippet of the full content 
> for viewing via RSS. Two popular reasons:
>
> 1. Driving traffic to the host site 
> 2. To prevent 'scraping' of copyrighted material

##### Enable feed discovery
Between ```<head>``` and ```</head>``` of the layout template files, include a 
link to the feed

{% highlight html %}
<link rel="alternate" type="application/rss+xml" 
	title="RSS Feed for studiousmarie" 
	href="http://mariev.net/studiousmarie/feed" />
{% endhighlight %}

### Adding comment plugin
The instructions here use the [Disqus](http://disqus.com) platform, which
offers free comment hosting independent of your site host. This separation 
is important, because it allows migration of your site in the future without 
losing valuable conversations. 

When you register your site, Disqus will prompt to select a platform. Choose 
"universal". Follow the directions to paste code into the relevant layout
template file.




