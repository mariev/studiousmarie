---
title: studiousmarie | Marie Vendettuoli
layout: default
section: blog

---
<div id = "archive">
<h3>2013</h3>
<ul>
{% for post in site.posts %}
{% capture myyear %}{{post.date | date: "%Y" }}{% endcapture %}

{% if "2013" == {{myyear}} %}
<li>{{post.date | date: "%b %d" }} &raquo; 
	<a href = "http://mariev.net/studiousmarie{{post.url}}">{{post.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
<h3>2012</h3>
<ul>
{% for post in site.posts %}
{% capture myyear %}{{post.date | date: "%Y" }}{% endcapture %}

{% if "2012" == {{myyear}} %}
<li>{{post.date | date: "%b %d" }} &raquo; 
	<a href = "http://mariev.net/studiousmarie{{post.url}}">{{post.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
</div>
