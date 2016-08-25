---
published: true
title: Javascript Comparison
layout: post
tags: [javascript, comparison]
categories: [javascript]
---
<b><u>Comparison with the Strict Equality Operator</u></b>

Strict equality (===) is the counterpart to the equality operator (==). Unlike the equality operator, strict equality tests both the data type and value of the compared elements.

{% highlight js %}
3 === 3   // true
3 === '3' // false
{% endhighlight %}

<b><u>Comparison with the Strict Inequality Operator</u></b>

The strict inequality operator (!==) is the opposite of the strict equality operator. It means "Strictly Not Equal" and returns false where strict equality would return true and vice versa. Strict inequality will not convert data types.

{% highlight js %}
3 !== 3   // false
3 !== '3' // true
4 !== 3   // true
{% endhighlight %}
