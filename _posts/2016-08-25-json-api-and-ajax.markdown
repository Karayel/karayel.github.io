---
published: false
title: JSON API and AJAX
layout: post
---
We can make basic application with using json api and ajax. We can use some html file as below during the application.

{% highlight html %}
<div class="container-fluid">
  <div class = "row text-center">
    <h2>Cat Photo Finder</h2>
  </div>
  <div class = "row text-center">
    <div class = "col-xs-12 well message">
      The message will go here
    </div>
  </div>
  <div class = "row text-center">
    <div class = "col-xs-12">
      <button id = "getMessage" class = "btn btn-primary">
        Get Message
      </button>
    </div>
  </div>
</div>
{% endhighlight %}

<b><u>Trigger Click Events with jQuery</u><b>

<b><i>$(document).ready() function</i></b>

This function runs such that all of the code inside of it executes only once our page has finished loading.