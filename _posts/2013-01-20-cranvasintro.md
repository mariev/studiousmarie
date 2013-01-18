---
date: 3013-01-20
title: installing cranvas on Mountain Lion (Mac OSX 10.8.2)
layout: blogpost
tags: cranvas tutorial R
---

Cranvas is an `R` package providing interactive statistical plots. 
Find the [code on github](https://github.com/ggobi/cranvas). See the
[Interface 2012 talk](https://github.com/downloads/yihui/yihui.github.com/cranvas-Houston-2012.pdf);
[Examples from UseR!2012](http://yihui.name/slides/2012-useR-cranvas-demo.R).

The following is what works on my system, and attempts to buffer against
breaks due to development changes.

###### My system

Mac OSX (10.8.2)	
R 2.15.2	
qtbase 1.0.6	
qtpaint 0.9.0	
cranvas 0.8.2	
RStudio 0.97.237	
Qt 4.6.4	

###### Steps
This assumes that R and RStudio is up and running

1. Download and install [Qt](http://qt-project.org/downloads). Select 4.6.4 (Cocoa), 
	both libraries and debug libraries
	
	*Note: the default on Mountain Lion is 4.8.3. It is possible to have both versions running*
2. On github, fork [cranvas](https://github.com/ggobi/cranvas), [qtbase](https://github.com/ggobi/qtbase)
	and [qtpaint](https://github.com/ggobi/qtbase)	

3. In an active R session install packages from the local directory using ```install.packges```.
	If there are errors indicating that the Qt dynamic library cannot be found, try:

	{% highlight r %}
	install.packages('package_name', repos = NULL, type = 'source', 
                 INSTALL_opts = '--no-multiarch'){% endhighlight %}
                 
*Note: any packages that depend on this package will also have to be installed using ```INSTALL_opts = '--no-multiarch'```*