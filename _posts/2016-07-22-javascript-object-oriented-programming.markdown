---
published: true
title: Javascript Object Oriented Programming
layout: post
tags: [javascript, oop ]
categories: [Javascript]
---
<b><u>Constructor</u></b>

{% highlight js %}
var Car = function() {
  this.wheels = 4;
  this.engines = 1;
  this.seats = 5;
};
{% endhighlight %}

<b><u>Make Unique Objects by Passing Parameters to our Constructor</u></b>

{% highlight js %}
var Car = function(wheels, seats, engines) {
  this.wheels = wheels;
  this.seats = seats;
  this.engines = engines;
};

var myCar = new Car(6, 3, 1);
{% endhighlight %}
