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

In *gh-pages* create the folder ```feed``` and the file ```index.xml```. This xml file
will be parsed by Jekyll and can use any of the page elements as for the posts or any 
stand-alone pages. The key elements to include are:

1. Suppress layout
	In the YAML front manner, specify ```layout:nil```
2. Specify the xml version and link to the ```css```
3. Designate the rss version	
4. Place content inside the ```<channel>```  &  ```</channel>``` tags	
5. At content start, include:	
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
	<lastBuildDate>{{ site.time | date: "%a, %d %b %Y %H:%M:%S %z" }}</lastBuildDate>
	{% endraw %}	
	{% endhighlight %}
6. In the 





