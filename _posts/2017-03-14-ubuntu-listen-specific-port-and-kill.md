---
title: Ubuntu Listen Specific Port and Kill
published: 'true'
layout: post
tag:
- linux
- network
categories: linux
---

{% highlight bash %}
sudo netstat -lpn | grep :4000
tcp        0      0 127.0.0.1:4000          0.0.0.0:*               LISTEN      17028/jekyll serve
kill -9 17028
{% endhighlight %}
