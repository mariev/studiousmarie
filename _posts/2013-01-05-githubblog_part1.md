---
title: a github blog - part 1
layout: blogpost
tags: github webdev tutorial
---

This site is hosted via github pages. In a nutshell: easier, faster, 
free. Who doesn't like free?

One downfall of this system is it seems that documentation is spread 
out - github, jekyll, liquid, plus navigating the various plugins and 
a custom domain. I'm documenting the adventure here in hopes that my
experience will make life easier for someone else. At the very least, 
a resource for troubleshooting.

1. Repo set up
	* If you don't already have a github account, [sign up](http://github.com). 
	There is [minimal] software to [download, and some set up](https://help.github.com/articles/set-up-git).
	* Create a new repo. Name it : *your-github-username*.github.com
	* In the repo, create a branch named *gh-pages* as an [orphan](https://help.github.com/articles/creating-project-pages-manually). 
2. [Install Jekyll](https://github.com/mojombo/jekyll/wiki/install). 
I also use RDiscount and Pygments.
3. Sign up for a comment manager (optional). I use [Disqus](http://disqus.com/)
4. Create the landing page. In gh-pages branch of the repo from step 1, you will need 
index.html 
	

> http://*your-github-username*.github.com should direct to the code from index.html

> **power users**     
> Set up ophan *gh-pages* for each project repo. Each project is accessed via:		
> http://*your-github-username*.github.com/*repo-name*
>

