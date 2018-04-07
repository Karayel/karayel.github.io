---
title: "Ubuntu Add Alias"
layout: post
date: 2016-02-24 22:48
image: /assets/images/markdown.jpg
headerImage: false
tag:
- ubuntu
category: blog
author: mkarayel
description: Ubuntu Add Alias
---

{% highlight bash %}
mkdir /usr/bin/Bash
cp YourBash.sh /usr/bin/Bash
gedit ~/.bashrc
alias youralias = 'sh /usr/bin/Bash/YourBash.sh'
source ~/.bashrc
youralias
{% endhighlight %}