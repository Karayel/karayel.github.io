---
published: true
title: Javascript Regular Expression
layout: post
tags: [javascript, regular, expression]
categories: [javascript]
---
<b><u>Sift through Text with Regular Expressions</u></b>

Regular expressions are used to find certain words or patterns inside of strings.

Some basic rules for regular expression:

<b>/ </b> is the start of the regular expression.

<b>the</b> is the pattern we want to match.

<b>/</b> is the end of the regular expression.

<b>g</b> means global, which causes the pattern to return all matches in the string, not just the first one.

<b>i</b>  means that we want to ignore the case (uppercase or lowercase) when searching for the pattern.

<b>\d</b>  which is used to retrieve one digit (e.g. numbers 0 to 9) in a string.

<b>\s</b> to select all the whitespace characters in the sentence string.

<b>\r</b> for the carriage return

<b>\n</b> for the newline

<b>\t</b> for the tab
 
<b>\f</b>  for the form feed

<b>Important Note:</b> You can invert any match by using the uppercase version of the regular expression selector.
 
{% highlight js %}
// Setup
var testString = "Ada Lovelace and Charles Babbage designed the first computer and the software that would have run on it.";

// Example
var expressionToGetSoftware = /software/gi;
var softwareCount = testString.match(expressionToGetSoftware).length;
{% endhighlight %}
