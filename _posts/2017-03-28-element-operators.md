---
title: Element Operators
published: false
layout: post
tags:
- mongodb
- operator
categories:
- mongodb
---

* **$exists**   Matches documents that have the specified field.
* **$type**	Selects documents if a field is of the specified type.

**Examples**

{% highlight bash %}
db.collectionName.find({ "title": { $exists: true } })
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ "title": { $exists: false } })
{% endhighlight %}

{% highlight bash %}
db.CollectionName.find({ _id: { $type: "string" } })
{% endhighlight %}