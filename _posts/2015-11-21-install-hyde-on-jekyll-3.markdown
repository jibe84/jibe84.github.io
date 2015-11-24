---
layout: post
title:  "Install hyde template on Jekyll >3.0"
date:   2015-11-21 18:00:00 +0200
categories:
---
As you may notice on my blog, I'm using [Jekyll](http://jekyllrb.com/) with [Hyde](http://hyde.getpoole.com/) template. The installation on paper is quite simple, first install Jekyll's gem, then fork Hyde, and finally enjoy on your server.

During the installation, I faced an **incompatibility** between Jekyll 3 and Hyde template, as the last one has been made using Jekyll 2. When I was trying to install it, this message shows up :
{% highlight bash %}
Deprecation: You appear to have pagination turned on, but you haven t included the `jekyll-paginate` gem. Ensure you have `gems: [jekyll-paginate]` in your configuration file.

Deprecation: Starting in 2.0, permalinks for pages in subfolders must be relative to the site source directory, not the parent directory.
{% endhighlight %}

So the solution was to edit `_config.yml` and :

    * Add `gems:[ jekyll-paginate]` to the Dependencies section
    * Remove `relative_permalinks: true`

This fix the issue!

Source: Thanks to [ItachiSan](https://github.com/ItachiSan/itachisan.github.io/commit/0fa0e1f282daadf526065de4a3f89179ed4c901a)
