---
published: true
title: Javascript String
layout: post
tags: [string, javascript]
categories: [Javascirpt]
---
<b><u>Declaration</u></b>

var firstName = "Mert";

var lastName = "Karayel";

<b><u>Escaping Literal Quotes in Strings</u></b>

When your string is "Challengers said, "Mert is learning JavaScript"." How do you define that ?

var sentence = "Challengers said, \"Mert is learning JavaScript.\"."

When you need a literal quote on your string, you can easily escape from quote by using backslash(\) in front of the quote. 

Another way to do that is changing outer double quote to single quote and thats it so we can easily read this notation. The other way is not easy on the eye for long post so  this way is much better.

var sentence = 'Challengers said, "Mert is learning JavaScript.".'

<b><u>Escape Sequences in Strings</u></b>

<table class="table" align="center">
 <tr><td><b>Code</b></td><td><b>Output</b></td></tr>
 <tr><td>\'</td><td>single quote</td></tr>
 <tr><td>\"</td><td>double quote</td></tr>
 <tr><td>\\</td><td>backslash</td></tr>
 <tr><td>\n</td><td>newline</td></tr>
 <tr><td>\r</td><td>carriage return</td></tr>
 <tr><td>\t</td><td>tab</td></tr>
 <tr><td>\b</td><td>backspace</td></tr>
 <tr><td>\f</td><td>form feed</td></tr>
</table>

<b><u>Concatenating Strings with Plus Operator</u></b>

When the + operator is used with a String value, it is called the concatenation operator.

var str = "My name is Mert." + " I am blogging."

Also I can write it like this.

var str = "My name is Mert.";

str += "I am blogging."

<b><u>Find the Length of a String</u><b>

"Mert Karayel".length; // 12

<b><u>Use Bracket Notation to Find the First Character in a String</u></b>

var name = "Mert Karayel"

var firstLetterOfName = name[0] // M