---
layout: post
title:  "Run a bash command in background"
date:   2016-12-15 20:00:00 +0200
categories: bash
---

Today, I learn how to : Run a bash command in background.

It's useful on server I can be disconnected, so I can follow the command on an output file. by using the command **nohup** at the beginning and **&** at the end, I'll be able to see the file _nohup.out_ with the command execution.

#### example
 {% highlight shell %}
 nohup composer install &

 # To follow the execution
 tail -f nohup.out
 {% endhighlight %}
