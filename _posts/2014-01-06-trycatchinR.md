---
title: tryCatch in R
layout: blogpost
tags: R
date: 2014-01-06
---

<div id = "statement">
As a graduate of Iowa State's HCI Program, I should know better. When it comes 
to usability and error handling, one must first [[obviously]] catch the error. Then
one must provide informative/helpful error messages - preferably one that directs
the user to appropriate action. Finally, display the error 
message in a manner that catches the user's attention.

When writing functions in R, it is easy to be lazy. I like to think that the 
vast majority of useRs are highly skilled at interpreting the cryptic messages
that are generated. You know, gems such as:

{% highlight r %}
$ operator is invalid for atomic vectors
{% endhighlight %}
</div>