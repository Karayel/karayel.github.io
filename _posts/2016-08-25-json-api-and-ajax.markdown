---
published: true
title: JSON API and AJAX Usage
layout: post
tags: [javascript, json, ajax]
categories: [javascript]
---
We can make basic application with using json api and ajax. We can use some html file as below and JSON file as linked https://www.freecodecamp.com/json/cats.json during the application.

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

After the knowledge, our script will be as follows

{% highlight js %}
$(document).ready(function() {
    $("#getMessage").on("click", function(){
      $.getJSON("/json/cats.json", function(json) {
        $(".message").html(JSON.stringify(json));
      }); 
    });
  });
{% endhighlight %}

<b><u>Convert JSON Data to HTML</u></b>

We know the JSON data and we can use the .forEach() method to loop through our data and modify our HTML elements.
Here's the code that does this:

<%highlight js%>
#json coming from the getJSON method.
json.forEach(function(val) {
  // every json object has a unique key and 
  // according to these key filled out the information about data.
  var keys = Object.keys(val);
  html += "<div class = 'cat'>";
  keys.forEach(function(key) {
    html += "<strong>" + key + "</strong>: " + val[key] + "<br>";
  });
  html += "</div><br>";
});
{% endhighlight %}

At the end of this, our script will be like this

<%highlight js%>
$(document).ready(function() {
    $("#getMessage").on("click", function() {
      $.getJSON("/json/cats.json", function(json) {
        var html = "";
        json.forEach(function(val) {
           var keys = Object.keys(val);
           html += "<div class = 'cat'>";
           keys.forEach(function(key) {
           html += "<strong>" + key + "</strong>: " + val[key] + "<br>";
        });
        html += "</div><br>";
      });
        $(".message").html(html);
      });
    });
  });
{% endhighlight %}

When we click the button, we got JSON object as below:
<%highlight js%>
[  
   {  
      id:0,
      imageLink: https://s3.amazonaws.com/freecodecamp/funny-cat.jpg,
      altText:A white cat wearing a green helmet shaped melon on it's head.,
      codeNames:[  
         Juggernaut,
         Mrs. Wallace,
         Buttercup
      ]
   }
]
{% endhighlight %}

<b><u>Rendering Image From Data Sources</u></b>

We know that JSON object has id, imageLink, altText and codeNames properties. We wanna only use imageLink property for showing image.

Here's the code that does this:

<%highlight js%>
html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";
{% endhighlight %}

After the rendering Image From Data Sources, forEach part will be change a little bit.

<%highlight js%>
 $(document).ready(function() {
    $("#getMessage").on("click", function() {
      $.getJSON("/json/cats.json", function(json) {
        var html = "";
        json.forEach(function(val) {
          html += "<div class = 'cat'>";
          html += "<img src = '" + val.imageLink + "' " + "alt='" + val.altText + "'>";  
          html += "</div>";
        });
        $(".message").html(html);
      });
    });
  });
{% endhighlight %}

<b><u>Prefilter JSON</u></b>

Let's filter out the cat whose "id" key has a value of 1.

Here's the code to do this:

<%highlight js%>
json = json.filter(function(val) {
  return (val.id !== 1);
});
{% endhighlight %}