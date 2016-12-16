---
layout: post
title:  "Undo a failed rebase"
date:   2016-12-16 20:00:00 +0200
categories: git
---

Today, I learn how to : Undo a failed rebase or anything stupid.

It's useful for _coming back on time_, as if something went wrong during a git command.

#### example
 {% highlight shell %}
 # List all git events
 git reflog

 # Go back to a previous' one 
 git reset --hard HEAD@{5}
 {% endhighlight %}
