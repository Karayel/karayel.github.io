---
title: Mongo Basics
layout: post
date: 2016-03-28
image: "/assets/images/markdown.jpg"
tag:
- mongo
category: blog
author: mkarayel
description: Mongo Basics
---

# The _id field in MongoDB 

![_id field]({{site.baseurl}}/static/img/id-and-ObjectIds-in-MongoDB-2.png)

# Creating Documents

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

## Operators
# Element Operators

* **$exists**  Matches documents that have the specified field.
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

# Comparison Operators

* **$eq**	Matches values that are equal to a specified value.
* **$gt**	Matches values that are greater than a specified value.
* **$gte**	Matches values that are greater than or equal to a specified value.
* **$lt** Matches values that are less than a specified value.
* **$lte**	Matches values that are less than or equal to a specified value.
* **$ne** Matches all values that are not equal to a specified value.
* **$in**	Matches any of the values specified in an array.
* **$nin**	Matches none of the values specified in an array.

**Examples**
{% highlight bash %}
db.collectionName.find({ runtime: { $gt: 90 } }).count()
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ runtime: { $gt: 90, $lt: 120 } }).count()
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ "tomato.meter": { $gte: 95 }, runtime: { $gt: 180 } })
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ rated: { $ne: "UNRATED" } }).count()
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ rated: { $in: ["G", "PG"] } }).pretty()
{% endhighlight %}

# Logical Operators

* **$or**	Joins query clauses with a logical OR returns all documents that match the conditions of either clause.
* **$and**	Joins query clauses with a logical AND returns all documents that match the conditions of both clauses.
* **$no**t	Inverts the effect of a query expression and returns documents that do not match the query expression.
* **$nor**	Joins query clauses with a logical NOR returns all documents that fail to match both clauses.

**Examples**

{% highlight bash %}
db.collectionName.find({ $or : [ { "tomato.meter": { $gt: 99 } },{ "metacritic": { $gt: 95 } } ] })
{% endhighlight %}

{% highlight bash %}
db.collectionName.find({ $and : [ { "metacritic": { $ne: 100 } },{ "metacritic" { $exists: true } } ] })
{% endhighlight %}


# Regex Operators

* **$regex**	Selects documents where values match a specified regular expression

**Example**

{% highlight bash %}
db.collectionName.find({ "title": { $regex: /^Mo.*/ } }).pretty()
{% endhighlight %}