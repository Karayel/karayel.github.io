---
title: Docker Images Run Command
layout: post
published: true
tags:
- docker
categories:
- docker
---

# RabbitMQ

* docker pull rabbitmq:3-management
* docker run -d -p 15672:15672 -p 5672:5672 rabbitmq:3-management

# Hazelcast
* mkdir Hazelcast
* cd Hazelcast
* vi Dockerfile
* Paste the following code 
{% highlight bash %}

FROM hazelcast/hazelcast:latest

ADD hazelcast.xml $HZ_HOME

CMD ./server.sh
{% endhighlight %}

* vi hazelcast.xml
* Copy hazelcast.xml from [https://github.com/hazelcast/hazelcast/blob/master/hazelcast/src/main/resources/hazelcast-default.xml](https://github.com/hazelcast/hazelcast/blob/master/hazelcast/src/main/resources/hazelcast-default.xml)
* docker build -t hazelcast/hazelcast:config -f Dockerfile . (Creating image from docker file,   dot is required for the command.)
* docker run -d -p 5701:5701 hazelcast/hazelcast:config
* docker run -d -p 8080:8080 hazelcast/management-center:latest  
* Go to [http://localhost:8080/mancenter/ ](http://localhost:8080/mancenter/ )in your browser