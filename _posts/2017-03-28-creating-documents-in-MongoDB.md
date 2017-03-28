---
published: true
title: Creating Documents in MongoDB
layout: post
tags: [mongodb, create]
categories: [mongodb] 
---

**Insert One**

{% highlight bash %}
db.collectionName.insertOne(object in json format);
{% endhighlight %}

***Example***
{% highlight bash %}
db.blog.insertOne({"blogger":"Mert KARAYEL","subject":"MongoDB"});
{% endhighlight %}

**Insert Many Ordered**

{% highlight bash %}
db.collectionName.insertMany(
    [
       objects in json format
    ]
);
{% endhighlight %}

insertMany commands take array as a parameter and array contains many object value.
In this command, when any take exception occured, its stop the process and show the result.

**Insert Many Unordered**

{% highlight bash %}
db.collectionName.insertMany(
    [
       objects in json format
		],
    {
        "ordered": false 
    }
   }
	 {% endhighlight %}
