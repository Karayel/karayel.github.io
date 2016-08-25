---
published: true
title: Javascript Array
layout: post
tags: [javascript, array]
categories: [javascript]
---
<b><u>Array</u></b>

We can store several pieces of data in one place with using array.

{% highlight js %}
var myInfo = ["Mert Karayel", "22",""Software Engineering"];
{% endhighlight %}

<b><u>Multi Dimensional Array</u></b>

{% highlight js %}
var userInfo = [["Mert Karayel", "22",""Software Engineering"],["James Gosling","61","Java"]];
{% endhighlight %}

<b><u>Access Array Data  </u></b>

{% highlight js %}
var myArray = [1,2,3,4,5];
var data = array[1];  // equals 2 Basically arrayName[index]
{% endhighlight %}

<b><u>Access Multi Dimensional Array Data</u></b>

{% highlight js %}
var myArray = [[1,2,3], [4,5,6], [7,8,9], [[10,11,12], 13, 14]];
var myData = myArray[2][1]; // 8
{% endhighlight %}

<b><u>Manipulate Arrays With push</u></b>

{% highlight js %}
var arr = [1,2,3];
arr.push(4); // new array 1,2,3,4
{% endhighlight %}

<b><u>Manipulate Arrays With pop</u></b>

pop() always removes the last element of an array. 

{% highlight js %}
var arr = [1,2,3];
arr.pop(); // 3
{% endhighlight %}

<b><u>Manipulate Arrays With shift</u></b>

push() always removes the first element of an array. 

{% highlight js %}
var arr = [1,2,3];
arr.shift(); // 1
{% endhighlight %}

<b><u>Manipulate Arrays With unshift</u></b>

{% highlight js %}
var myArray = [["John", 23], ["dog", 3]];
myArray.shift(); // ["dog",3]
myArray.unshift(["Paul",35]); // ["Paul",35],["dog",3]
{% endhighlight %}