---
layout: post
title:  "Perform a regular expression match"
date:   2016-12-22 20:00:00 +0200
categories: php
---

Today, I learn how to : Perform a regular expression match.

If matches is provided, then it is filled with the results of search. $matches[0] will contain the text that matched the full pattern, $matches[1] will have the text that matched the first captured parenthesized subpattern, and so on.

#### example
 {% highlight php %}
 $str = "This is amazing test for 'dogs' and 'cats'.";
 {% endhighlight %}
 
By using the 3rd parameter of preg_match..
 {% highlight php %}
 preg_match("/This is amazing test for '(\w+)' and '(\w+)'./", $str, $matches);
 {% endhighlight %}
 
I can select matches:
 {% highlight php %}
 $matches = [
     "This is amazing test for 'dogs' and 'cats'.", 
     "dogs",
     "cats",
 ]
 {% endhighlight %}

[official doc](http://php.net/manual/en/function.preg-match.php)

[live example](http://sandbox.onlinephpfunctions.com/code/a2305e01bbd6994f9e6e553db0fd7d90b9f30607)
