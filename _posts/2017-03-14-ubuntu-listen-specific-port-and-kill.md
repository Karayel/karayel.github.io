---
title: "Ubuntu Listen Specific Port and Kill"
layout: post
date: 2016-03-14
image: /assets/images/markdown.jpg
headerImage: false
tag:
- ubuntu
category: blog
author: mkarayel
description: Ubuntu Listen Specific Port and Kill
---

{% highlight bash %}
sudo netstat -lpn | grep :4000
tcp        0      0 127.0.0.1:4000          0.0.0.0:*               LISTEN      17028/jekyll serve
kill -9 17028
{% endhighlight %}
