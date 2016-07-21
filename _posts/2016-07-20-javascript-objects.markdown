---
published: true
title: Javascript Objects
layout: post
---
<b><u>Creating Object<u></u>

Objects are similar to arrays, except that instead of using indexes to access and modify their data, you access the data in objects through what are called properties.

var cat = {
  "name": "Whiskers",
  "legs": 4,
  "tails": 1,
  "enemies": ["Water", "Dogs"]
};

<b><u>How can I reach the javascript object properties ?</u></b>

This is simple as much as you think. If you know any other programming language, . (dot) provide to access object properties.

cat.name // Whiskers

Javascript have more option about that problem. You can access object properties with using bracket notation. This notation is as simple as dot notation.

var myName = {
  "First Name": "Mert",
  "Las Name": "Karayel"
};

myName["First Name"]; // Mert

If you want to update your object properties.You just use dot or bracket notation for properties and assign another value.

myName["First Name"]="Marry";

<b><u>Add New Properties to Object</u></b>

We can add new properties to objects the same way we would modify them.

myName["age"] = 22;

<b><u>Delete Properties from Object</u></b>

We can also delete properties from objects like this:

delete myName.age;

<b><u>Using Objects for Lookups</u></b>

Objects can be thought of as a key/value storage, like a dictionary. If you have tabular data, you can use an object to "lookup" values rather than a switch statement or an if/else chain. This is most useful when you know that your input data is limited to a certain range.

Here is an example of a simple reverse alphabet lookup:

var alpha = {
  1:"Z",
  2:"Y",
  3:"X",
  4:"W",
  ...
  24:"C",
  25:"B",
  26:"A"
};
alpha[2]; // "Y"
alpha[24]; // "C"

<b><u>Testing Objects for Properties</u></b>
We can use the .hasOwnProperty(propname) method of objects to determine if that object has the given property name. .hasOwnProperty() returns true or false if the property is found or not.

myName.hasOwnProperty("First Name"); // true

<b><u>Manipulating Complex Objects</u></b>

Here's an example of a complex data structure:

var ourMusic = [
  {
    "artist": "Daft Punk",
    "title": "Homework",
    "release_year": 1997,
    "formats": [ 
      "CD", 
      "Cassette", 
      "LP" ],
    "gold": true
  }
];

This is an array which contains one object inside. The object has various pieces of metadata about an album. 

<b><u>Accessing Nested  Objects</u></b>

var ourStorage = {
  "desk": {
    "drawer": "stapler"
  },
  "cabinet": {
    "top drawer": { 
      "folder1": "a file",
      "folder2": "secrets"
    },
    "bottom drawer": "soda"
  }
};

ourStorage.cabiner["top drawer"].folder1; //a file