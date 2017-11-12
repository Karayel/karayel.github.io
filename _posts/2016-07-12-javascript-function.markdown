---
title: Javascript Function
published: false
layout: post
tags:
- javascript
- comparasion
categories:
- javascript
---

<b><u>Write Reusable JavaScript with Functions</u></b>

Example function 

{% highlight js %}
function functionName() {
  console.log("Hello World");
}
{% endhighlight %}

You can invoke this function by using its name.

functionName();

<b><u>Passing Values to Functions with Arguments</u></b>

Example function

{% highlight js %}
function functionWithParameter(param1, param2) {
  console.log(param1, param2);
}
{% endhighlight %}

Then we can call functionWithParameter:

{% highlight js %}
functionWithParameter("Hello", "World");
{% endhighlight %}

<b><u>Global Scope</u></b>

Variables which are defined outside of a function block have Global scope.This means, they can be seen everywhere in your JavaScript code.Variables which are used without the var keyword are automatically created in the global scope. 

<b><u>Local Scope</u></b>

Variables which are declared within a function, as well as the function parameters have local scope. That means, they are only visible within that function.

<b><u>Return a Value from a Function with Return</u></b>

{% highlight js %}
function plusThree(num) {
  return num + 3;
}

var answer = plusThree(5); // 8
{% endhighlight %}