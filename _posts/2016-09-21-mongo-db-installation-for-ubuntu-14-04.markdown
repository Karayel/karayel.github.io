---
title: "Mongo DB Installation for Ubuntu 14.04"
layout: post
date: 2016-02-24 22:48
image: /assets/images/markdown.jpg
headerImage: false
tag:
- mongo
category: blog
author: mkarayel
description: Mongo DB Installation for Ubuntu 14.04
---

<b><u>Import the public key used by the package management system</b></u>

{% highlight bash %}
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 7F0CEB10
{% endhighlight %}
	
<b><u>Create a list file for MongoDB</b></u>

{% highlight bash %}
echo "deb http://repo.mongodb.org/apt/ubuntu trusty/mongodb-org/3.0 multiverse" | sudo tee /etc/apt/sources.list.d/mongodb-org-3.0.list
{% endhighlight %}

<b><u>Reload local package database.</b></u>

{% highlight bash %}
sudo apt-get update
{% endhighlight %}

<b><u>Install the MongoDB packages</b></u>

{% highlight bash %}
sudo apt-get install -y mongodb-org
{% endhighlight %}

{% highlight bash %}
Start sudo service mongod start
Stop sudo service mongod stop
Restart sudo service mongod restart
{% endhighlight %}

<b><u>Mongo db log file location</b></u>

{% highlight bash %}
/var/log/mongodb/mongod.log
{% endhighlight %}

<b><u>Remove mongodb </b></u>

{% highlight bash %}
sudo apt-get purge mongodb-org*
{% endhighlight %}

<b><u>Remove data and log files</b></u>

{% highlight bash %}
sudo rm -r /var/log/mongodb
sudo rm -r /var/lib/mongodb
{% endhighlight %}

If you want to see more details. Please look at the following url
<a href="https://docs.mongodb.com/manual/installation/" target="_blank">Mongo DB Installation </a>
