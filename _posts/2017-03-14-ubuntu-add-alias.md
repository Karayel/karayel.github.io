---
title: Ubuntu Add Alias
published: 'true'
layout: post
tags:
- linux
categories: linux
---

{% highlight bash %}
mkdir /usr/bin/Bash

cp YourBash.sh /usr/bin/Bash

gedit ~/.bashrc

alias youralias='sh /usr/bin/Bash/YourBash.sh'

source ~/.bashrc

youralias
{% endhighlight %}