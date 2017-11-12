---
title: Regex Operator
published: false
layout: post
tags:
- mongodb
- operator
categories:
- mongodb
---

**$regex**	Selects documents where values match a specified regular expression

**Example**

{% highlight bash %}
db.collectionName.find({ "title": { $regex: /^Mo.*/ } }).pretty()
{% endhighlight %}