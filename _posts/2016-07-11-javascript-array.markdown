---
title: Javascript Array
published: false
layout: post
tags:
- javascript
- array
categories:
- javascript
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


<b><u>Iterate over Arrays with map</b></u>

The map method will iterate through every element of the array, creating a new array with values that have been modified by the callback function, and return it. Note that it does not modify the original array.

{% highlight js %}
var oldArray = [1,2,3,4,5];
var newArray = oldArray.map(function(value){
  return value+3;
});
console.log(oldArray); // [1,2,3,4,5]
console.log(newArray); // [4,5,6,7,8]
{% endhighlight %}

<b><u>Condense arrays with reduce</u></b>

The array method reduce is used to iterate through an array and condense it into one value.

reduce has an optional second argument which can be used to set the initial value of the accumulator. If no initial value is specified it will be the first array element and currentVal will start with the second array element.

{% highlight js %}
var array = [4,5,6,7,8];
var singleVal = 0;
singleVal = array.reduce(function(previousVal,currentVal){
  return previousVal + currentVal;
},0); // 30
{% endhighlight %}

<b><u>Filter Arrays with filter</u></b>

The filter method is used to iterate through an array and filter out elements where a given condition is not true.

{% highlight js %}
var oldArray = [1,2,3,4,5,6,7,8,9,10];
var newArray = oldArray.filter(function(value){
  return value < 6;
}); // [1,2,3,4,5]
{% endhighlight %}

<b><u>Sort Arrays with sort</u></b>

You can use the method sort to easily sort the values in an array alphabetically or numerically.

{% highlight js%}
var array = [1, 12, 21, 2];
array.sort(function(a,b){
  return b > a;
}); // [21,12,2,1]
{% endhighlight %}

<b><u>Reverse Arrays with reverse</u></b>

You can use the reverse method to reverse the elements of an array.

{% highlight js%}
var array = [1,2,3,4,5,6,7];
var newArray = [];
newArray = array.reverse(); // [7,6,5,4,3,2,1]
{% endhighlight %}

<b><u>Concatenate Arrays with concat</u></b>

concat can be used to merge the contents of two arrays into one.

{% highlight js%}
var oldArray = [1,2,3];
var newArray = [];
var concatMe = [4,5,6];
newArray = oldArray.concat(concatMe); // [1,2,3,4,5,6]
{% endhighlight %}

<b><u>Split Strings with split</u></b>

You can use the split method to split a string into an array.

{% highlight js%}
var string = "Split me into an array";
var array = [];
array = string.split(" "); // [Split,me,into,an,array]
{% endhighlight %}

<b><u>Join Strings with join</u></b>

You can use the join method to join each element of an array into a string separated by whatever delimiter you provide as an argument.

{% highlight js%}
var joinMe = ["Split","me","into","an","array"];
var joinedString = '';
joinedString = joinMe.join(" "); // Split me into an array
{% endhighlight %}