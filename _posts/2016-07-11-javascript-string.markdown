---
title: Javascript String
published: false
layout: post
tags:
- string
- javascript
categories:
- javascript
---

<b><u>Declaration</u></b>

{% highlight js %}
var firstName = "Mert";
var lastName = "Karayel";
{% endhighlight %}

<b><u>Escaping Literal Quotes in Strings</u></b>

When your string is "Challengers said, "Mert is learning JavaScript"." How do you define that ?

{% highlight js %}
var sentence = "Challengers said, \"Mert is learning JavaScript.\"."
{% endhighlight %}

When you need a literal quote on your string, you can easily escape from quote by using backslash(\) in front of the quote. 

Another way to do that is changing outer double quote to single quote and thats it so we can easily read this notation. The other way is not easy on the eye for long post so  this way is much better.

{% highlight js %}
var sentence = 'Challengers said, "Mert is learning JavaScript.".'
{% endhighlight %}

<b><u>Escape Sequences in Strings</u></b>

\\' single quote -
\\" double quote -
\\\\ backslash -
\n newline -
\r carriage return -
\t tab -
\b backspace -
\f feed

<b><u>Concatenating Strings with Plus Operator</u></b>

When the + operator is used with a String value, it is called the concatenation operator.

{% highlight js %}
var str = "My name is Mert." + " I am blogging."
{% endhighlight %}

Also I can write it like this.

{% highlight js %}
var str = "My name is Mert.";
str += "I am blogging."
{% endhighlight %}

<b><u>Find the Length of a String</u><b>

{% highlight js %}
"Mert Karayel".length; // 12
{% endhighlight %}

<b><u>Use Bracket Notation to Find the First Character in a String</u></b>

{% highlight js %}
var name = "Mert Karayel"
var firstLetterOfName = name[0] // M
{% endhighlight %}