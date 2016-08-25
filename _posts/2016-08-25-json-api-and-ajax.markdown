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

<b><i>$(document).read() function</i></b>

This function runs such that all of the code inside of it executes only once our page has finished loading.

Now, we know that how $(document).read() function works. Let's move on next step. We have to implement a click event handler inside the document function.

{% highlight js %}
  $(document).ready(function() {
    //it is coming from the html file and it is a button for trigger.
    $("#getMessage").on("click", function(){

    });
  });
{% endhighlight %}

<b><u>Change Text with Click Events </u><b>

We can change the text with using jquery. Its 

{% highlight js %}
  $(document).ready(function() {
    $("#getMessage").on("click", function(){
         #div that is classed with message will be changed after the button triggered. 
         $(".message").html("Here is the message");
    });
  });
{% endhighlight %}

<b><u>Get JSON with the jQuery getJSON Method</u></b>

We can get JSON data with getJSON method in the jquery.

jQuery.getJSON( url [, data ] [, success ] )

<b>url</b>: A string containing the URL to which the request is sent.
<b>data</b>: A plain object or string that is sent to the server with the request.
<b>success</b>:A callback function that is executed if the request succeeds.

We can use this method like that
{% highlight js %}
//API url is /json/cats.json and its return json data
$.getJSON("/json/cats.json", function(json) {
   //stringify() method converts a JavaScript value to a JSON string.
  $(".message").html(JSON.stringify(json));
});
{% endhighlight %}



{% highlight js %}
$(document).ready(function() {
    $("#getMessage").on("click", function(){
      $.getJSON("/json/cats.json", function(json) {
        $(".message").html(JSON.stringify(json));
      }); 
    });
  });
{% endhighlight %}