# PHP tutorial
## What is PHP
* PHP is an acronym for "PHP: Hypertext Preprocessor"
* PHP is a widely-used, open source scripting language
* PHP scripts are executed on the server
* PHP is free to download and use

## What is a PHP File?
* PHP files can contain text, HTML, CSS, JavaScript, and PHP code
* PHP code are executed on the server, and the result is returned to the browser as plain HTML
* PHP files have extension ".php"

## PHP Case Sensitivity
* In php, all keywords (e.g. if,else,while,echo,etc), classes, functions, and user-defined functions are NOT case-sensitive

## Creating (Declaring) PHP Variables
a variable starts with the $ sign, followed by the name of the variable

## PHP is a Loosely Typed Language
PHP automatically converts the variable to the correct data type, depending on its value

### PHP has three different variable scopes
* local 
* global
* static

## PHP Global Variables - superglobals
They are always accessible, regardless of scope
### The PHP superglobal variables are:
* $GLOBALS
* $_SERVER
* $_REQUEST
* $_POST
* $_GET
* $_FILES
* $_ENV
* $_COOKIE
* $_SESSION

## Diff between GET and POST
* Information sent from a form with the GET method is visible to everyone GET also has limits on the amount of 
information to send. because the variable are displayed in the URL, it is possible to bookmark the page
* invisible to others and has no limits on the amount of informatin to send

## Form Validation
![alt text](info.jpg)
* Name: <input type="text" name="name">     [//]: # name is just like id 
* E-mail: <input type="text" name="email">   [//]: # "email" is id
* Website: <input type="text" name="website"> [//]: # "website" is id
* Comment: <textarea name"comment" rows="5" cols="40"></textarea>

## Radio Buttons
Gender:
<input type="radio" name="gender" value="female"> Female
<input type="radio" name="gender" value="male"> Male

## the form element
The HTML code of the form looks like this:
<form method="post" action="<?php echo htmlspecialchars($_SERVER["PHP_SELF"]);?>">
** the $_SERVER["PHP_SELF"] sends the submitted form data to the page itself, instead of jumping to a different page **

## htmlspecialchars() function

## preg_match


# JS Tutorial
## JavaScript can "display" data in different ways:
* Writing into an HTML element, using innerHTML
* Writing into the HTML output using document.write()  only for testing
* Writing into an alert box, using window.alert()
* Writing into the browser console, using console.log()

~5 will not return 10, It will return -6
~00000000000000000000000000000101 will return 11111111111111111111111111111010
substract 1 and bitwise except sign bit

## HTML Events
* An HTML web page has finished loading
* An HTML input field was changed
* An HTML button was clicked

## String function    diff between indexOf() and search
* the search() method cannot take a second start position argument
* the search() method can take much more powerful search values (regualar expressions)

## cannot compare objects

## Every JavaScript object has a prototype The prototype is also an object 
## All JavaScript objects inherit their properties and methods from their prototype

## Object Prototypes
* Creating a Prototype
function Person(first, last, age, eyecolor){
    this.firstName = first;
    this.lastName = last;
    this.age = age;
    this.eyeColor = eyecolor;
}
Example
var myFather = new Person("John", "Doe", 50, "blue");
* Adding a Property to an Object
myFather.nationality = "English";
* Adding a Method to an Object
myFather.name = function () {
    return this.firstName + "" + this.lastName;
}

* Adding Properties to a Prototype
You cannot add a new property to a prototype the same way as you add a new property to an existing object, because the prototype is not an exiting object

* To add a new property to a prototype, you must add it to the constructor function:
function Person(first, last, age, eyecolor){
    this.nationality = "English";
}

* Adding Methods to a Prototype
Your constructor funciton can also define methods
function Person(first, last, age, eyecolor){
    this.name = function() {
        return this.firstName + " " + this.lastName;
    };
}
* Using the prototype Property
Person.prototype.nationality = "English";
* JS prototype property also allows you to add new methods to an exiting prototype
Person.prototype.name = function() {
    return this.firstName + " " + this.lastName;
}

## A function expression can be stored in a variable
var x = function (a,b) {return a * b;};

## The Function() Constructor
Functions can also be defined with a built-in JS function constructor called Function()
var myFunction = new Function("a","b","return a * b");
var x = myFunction (4,3);

## In the DOM all HTML elements are defined as objects
* The programming interface is the properties and methods of each object
* A property is a value that you can get or set
* A method is an action you can do

* The HTML DOM document object is the owner of all other objects in your web page *

## The document object represents your web page
* If you want to access any element in an HTML page, you always start with accessing the document object

## Finding HTML Elements by Tag Name
* var x = document.getElementsByTagName("p");

## Add Many Event Handlers to the same element
* element.addEventListener("click",myFunction);

## The HTML above you can read:
* <html> is the root node
* <html> has no parents
* <html> is the parent of <head> and <body>
* <head> is the first child of <html>
* <body> is the last child of <html>

## DOM Nodes
* var para = document.createElement("p")
* var node = document.createTextNode("This is a new paragraph");
* para.appendChild(node);
* Finally you must append the new element to an exiting element
  var element = document.getElementById("div1")
* element.appendChild(para);

## Here is a common workaround: Find the child you want to remove and use its parentNode property to find the parent

var child = document.getElementById("p1");
child.parentNode.removeChild(child);








































































































































































































































