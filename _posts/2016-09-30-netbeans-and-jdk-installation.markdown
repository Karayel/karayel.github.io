---
title: "Netbeans and JDK Installation"
layout: post
date: 2016-02-24 22:48
image: /assets/images/markdown.jpg
headerImage: false
tag:
- linux
- java
category: blog
author: mkarayel
description: Netbeans and JDK Installation
---

1) Dowloand JDK xxxx with NetBeans 8.x from Oracle.
2) Open terminal Ctrl + Alt + T
3) Move to dowloaded file folder.
{% highlight bash %}
$ cd /Downloads
$ chmod +x jdk-7u80-nb-8_0_2-linux-x64.sh
$ ./jdk-7u80-nb-8_0_2-linux-x64.sh
{% endhighlight %}

Now, you can see the installation screeen. Install JDK and Netbeans by your specification

<b><u>How to set JAVA_HOME environment in Ubuntu?</u></b>

1) Open Terminal.Type the below code in terminal and hit enter.
sudo gedit /etc/environment
2) Find your JDK Path and write it.  
JAVA_HOME ="JDK Path" 
3) Reload the system environment and then echo JAVA_HOME environment.
{% highlight bash %}
source /etc/environment
echo $JAVA_HOME
{% endhighlight %}
4) That's it.