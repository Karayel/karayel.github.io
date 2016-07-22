---
published: true
title: Javascript Object Oriented Programming
layout: post
---
<b><u>Constructor</u></b>

var Car = function() {
  this.wheels = 4;
  this.engines = 1;
  this.seats = 5;
};

<b><u>Make Unique Objects by Passing Parameters to our Constructor</u></b>

var Car = function(wheels, seats, engines) {
  this.wheels = wheels;
  this.seats = seats;
  this.engines = engines;
};

var myCar = new Car(6, 3, 1);