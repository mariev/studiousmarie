---
title: studiousmarie | Marie Vendettuoli
layout: default
section: blog

---
<div id = "archive">

<!--- For displaying future posts on local server -->
<ul>
{% for post in site.posts %}
{% capture myyear %}{{post.date | date: "%Y" }}{% endcapture %}

{% if "3013" == {{myyear}} %}
<li><span id = "date">{{post.date | date: "%b %d" }}</span> &raquo; 
	<a href = "http://localhost:4000{{post.url}}">{{post.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
<!--- end future -->

<h3>2013</h3>
<ul>
{% for post in site.posts %}
{% capture myyear %}{{post.date | date: "%Y" }}{% endcapture %}

{% if "2013" == {{myyear}} %}
<li><span id = "date">{{post.date | date: "%b %d" }}</span> &raquo; 
	<a href = "http://mariev.net/studiousmarie{{post.url}}">{{post.title}}</a></li>
{% endif %}
{% endfor %}
</ul>
