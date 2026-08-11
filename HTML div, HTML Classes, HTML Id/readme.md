# Div
 The <div> Element
The <div> element is by default a block element, meaning that it takes all available width, and comes with line breaks before and after.

Example
A <div> element takes up all available width:

Lorem Ipsum <div>I am a div</div> dolor sit amet.
Result
Lorem Ipsum
I am a div
dolor sit amet.

The <div> element has no required attributes, but style, class and id are common.

<div> as a container
The <div> element is often used to group sections of a web page together.

Example
A <div> element with HTML elements:

<div>
  <h2>London</h2>
  <p>London is the capital city of England.</p>
  <p>London has over 9 million inhabitants.</p>
</div>
Result
London
London is the capital city of England.

London has over 9 million inhabitants.
# class
HTML class Attribute
The HTML class attribute is used to specify a class for an HTML element.

Multiple HTML elements can share the same class.

The class Attribute
The class attribute is often used to point to a class name in a style sheet. It can also be used by JavaScript to access and manipulate elements with the specific class name.

In the following example we have three <div> elements with a class attribute with the value of "city". All of the three <div> elements will be styled equally according to the .city style definition in the head section:

Example
<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  border: 2px solid black;
  margin: 20px;
  padding: 20px;
}
</style>
</head>
<body>

<div class="city">
  <h2>London</h2>
  <p>London is the capital of England.</p>
</div>

<div class="city">
  <h2>Paris</h2>
  <p>Paris is the capital of France.</p>
</div>

<div class="city">
  <h2>Tokyo</h2>
  <p>Tokyo is the capital of Japan.</p>
</div>

</body>
</html>
In the following example we have two <span> elements with a class attribute with the value of "note". Both <span> elements will be styled equally according to the .note style definition in the head section:

Example
<!DOCTYPE html>
<html>
<head>
<style>
.note {
  font-size: 120%;
  color: red;
}
</style>
</head>
<body>

<h1>My <span class="note">Important</span> Heading</h1>
<p>This is some <span class="note">important</span> text.</p>

</body>
</html>
Tip: The class attribute can be used on any HTML element.

Note: The class name is case sensitive!

Tip: You can learn much more about CSS in our CSS Tutorial.

REMOVE ADS

The Syntax For Class
To create a class; write a period (.) character, followed by a class name. Then, define the CSS properties within curly braces {}:

Example
Create a class named "city":

<!DOCTYPE html>
<html>
<head>
<style>
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
</style>
</head>
<body>

<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>

</body>
</html>
Multiple Classes
HTML elements can belong to more than one class.

To define multiple classes, separate the class names with a space, e.g. <div class="city main">. The element will be styled according to all the classes specified.

In the following example, the first <h2> element belongs to both the city class and also to the main class, and will get the CSS styles from both of the classes: 

Example
<h2 class="city main">London</h2>
<h2 class="city">Paris</h2>
<h2 class="city">Tokyo</h2>
Different Elements Can Share Same Class
Different HTML elements can point to the same class name.

In the following example, both <h2> and <p> point to the "city" class and will share the same style:

Example
<h2 class="city">Paris</h2>
<p class="city">Paris is the capital of France</p>
REMOVE ADS

Use of the class Attribute in JavaScript
The class name can also be used by JavaScript to perform certain tasks for specific elements.

JavaScript can access elements with a specific class name with the getElementsByClassName() method:

Example
Click on a button to hide all elements with the class name "city":

<script>
function myFunction() {
  var x = document.getElementsByClassName("city");
  for (var i = 0; i < x.length; i++) {
    x[i].style.display = "none";
  }
}
</script>
Don't worry if you don't understand the code in the example above.

You will learn more about JavaScript in our HTML JavaScript chapter, or you can study our JavaScript Tutorial.

Chapter Summary
The HTML class attribute specifies one or more class names for an element
Classes are used by CSS and JavaScript to select and access specific elements
The class attribute can be used on any HTML element
The class name is case sensitive
Different HTML elements can point to the same class name
JavaScript can access elements with a specific class name with the getElementsByClassName() method


# id
HTML id Attribute
The HTML id attribute is used to specify a unique id for an HTML element.

You cannot have more than one element with the same id in an HTML document.

The id Attribute
The id attribute specifies a unique id for an HTML element. The value of the id attribute must be unique within the HTML document.

The id attribute is used to point to a specific style declaration in a style sheet. It is also used by JavaScript to access and manipulate the element with the specific id.

The syntax for id is: write a hash character (#), followed by an id name. Then, define the CSS properties within curly braces {}.

In the following example we have an <h1> element that points to the id name "myHeader". This <h1> element will be styled according to the #myHeader style definition in the head section:

Example
<!DOCTYPE html>
<html>
<head>
<style>
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}
</style>
</head>
<body>

<h1 id="myHeader">My Header</h1>

</body>
</html>
Note: The id name is case sensitive!

Note: The id name must contain at least one character, cannot start with a number, and must not contain whitespaces (spaces, tabs, etc.).

Difference Between Class and ID
A class name can be used by multiple HTML elements, while an id name must only be used by one HTML element within the page:

Example
<style>
/* Style the element with the id "myHeader" */
#myHeader {
  background-color: lightblue;
  color: black;
  padding: 40px;
  text-align: center;
}

/* Style all elements with the class name "city" */
.city {
  background-color: tomato;
  color: white;
  padding: 10px;
}
</style>

<!-- An element with a unique id -->
<h1 id="myHeader">My Cities</h1>

<!-- Multiple elements with same class -->
<h2 class="city">London</h2>
<p>London is the capital of England.</p>

<h2 class="city">Paris</h2>
<p>Paris is the capital of France.</p>

<h2 class="city">Tokyo</h2>
<p>Tokyo is the capital of Japan.</p>
Tip: You can learn much more about CSS in our CSS Tutorial.

REMOVE ADS

HTML Bookmarks with ID and Links
HTML bookmarks are used to allow readers to jump to specific parts of a webpage.

Bookmarks can be useful if your page is very long.

To use a bookmark, you must first create it, and then add a link to it.

Then, when the link is clicked, the page will scroll to the location with the bookmark.

Example
First, create a bookmark with the id attribute:

<h2 id="C4">Chapter 4</h2>
Then, add a link to the bookmark ("Jump to Chapter 4"), from within the same page:

Example
<a href="#C4">Jump to Chapter 4</a>
Or, add a link to the bookmark ("Jump to Chapter 4"), from another page:

<a href="html_demo.html#C4">Jump to Chapter 4</a>
Using the id Attribute in JavaScript
The id attribute can also be used by JavaScript to perform some tasks for that specific element.

JavaScript can access an element with a specific id with the getElementById() method:

Example
Use the id attribute to manipulate text with JavaScript:

<script>
function displayResult() {
  document.getElementById("myHeader").innerHTML = "Have a nice day!";
}
</script>
Tip: Study JavaScript in the HTML JavaScript chapter, or in our JavaScript Tutorial.

Chapter Summary
The id attribute is used to specify a unique id for an HTML element
The value of the id attribute must be unique within the HTML document
The id attribute is used by CSS and JavaScript to style/select a specific element
The value of the id attribute is case sensitive
The id attribute is also used to create HTML bookmarks
JavaScript can access an element with a specific id with the getElementById() method
