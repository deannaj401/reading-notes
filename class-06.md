Understanding the Problem Domain is the Hardest part of programming

If you take the focus off the problem domain and put on something else like technology then it makes learning a lot easier

Understanding the problem is the most critical piece to the equation

You can make the problem eaier by narrowing your focus to a particular part of the problem or by understanding the problem better

Duckett JavaScript

Ch 3

P100-105

# What Is An Object?

Objects group together a set of variables and functions to create a model of a something you would recognize from the real world

* In an object Variables become known as properties

* In an object functions become known as methods

* In an object properties and methods have a name and a value

The name is called a **key**

* An object cannot have 2 keys with the same name. This is because keys are used to access their corresponding values.

The **value of a property** can be a string, number Boolean, array or even another object

The **value of a method** is always a function

## Creating An Object: Literal Notation

*see page 102 in book for example of object*



objects are stored in curly braces

When setting properties treat the values like you would do for variables:
* strings live in quotes
* arrays live in square brackets

Seperate each key from its value using a colon

Seperate each property and method with a comma but not after the last value


## Accessing an Object and Dot Notation

**Dot Notation** - to access a property or method of an object you use the name of the object, followed by a period, then the name of the property or method you want to access

* the period is known as the member operator. The property of method on its right is a member of the object on its left.

```var hotelName = hotel.name;```
(hotel is the object, period is the member operator, and name is the property or method name)

**Square Bracket Syntax** - the object name is followed by square brackets, and the property name is inside them.

```var hotelName = hotel['name'];```

* this method is commonly used when
	* the name of  property is a number (should be avoided)
	* a variable is being used in place of the property name

If you had two objects on the same page, you would create each one using the same
notation but store them in variables with different names.


Ch 5

p183-242

# Document Object Model

The Document Object Model (DOM) specifies how browsers should create a model of an HTML page and how JavaScript can access and update the contents of a web page while it is in the browser window.

The DOM is neither part of HTML, nor part of JavaScript; it is a separate set of rules. It is implemented by all major browser makers, and covers two primary areas:

1. MAKING A MODEL OF THE HTML PAGE
	* When the browser loads a web page, it creates a model of the page in 	  memory.
	* The DOM specifies the way in which the browser should structure this              model using a DOM tree.
	* The DOM is called an object model because the model (the DOM tree) is
          made of objects.
 	* Each object represents a different part of
	  the page loaded in the browser window.

1. ACCESSING AND CHANGING THE HTML PAGE

	* The DOM also defines methods and properties to access and update each
	object in this model, which in turn updates
	what the user sees in the browser.

	* The DOM states what your script can "ask the browser about the
	current page, and how to tell the browser to update what is being shown 	to the user.



### The 4 nodes of the DOM tree are:

1. Document Node - represents the entire page
1. Element Node - 
1. Attribut Nodes
1. Text Nodes



* Each node is an object with methods and properties.
* Scripts access and update this DOM tree (not the source HTML file).
* Any changes made to the DOM tree are reflected in the browser.

## Accessing and Updating the DOM tree:

###  Access the Elements
 
**Individual Elements**
* There are 3 ways to select an individual element
1. ```getElementById()``` - uses the value of an elements id attribute 
1. ```querySelector()``` - Uses a CSS selector and returns the first matching    element
1. You can also select individual elements by traversing from one element to another within the DOM tree

**Multiple Elements(NODELISTS)**

There are 3 ways to select multiple elements

1. ```getElementsByClassName()``` - Selects all elements that have a specific value 	for their class attribute
* this method has one parameter:the *class* name which is given in quotes within the parenthesis after the method name. 
* This method always returns a NodeList because several elements can have the same value for their class

```el.className = 'cool';```

1. ```getElementsByTagName()``` -   Selects all elements that have the specified tag name
* The element name is specified as a parameter so it is placed inside the parentheses and is contained by quote marks.
* do not include the angled brackets in an HTML tag name. just the letters inside the bracket

```var elements = document.getElementsByTagName('li');```


1.  ```querySelectorAll()``` - Uses a CSS selector to select all matching elements
 * querySelector() returns the first element node that matches the CSS-style selector
* Both methods take a CSS selector as their only parameter

```var el = document.querySelector(li.hot;);```

**Traversing Between Element Nodes

You can move from one element node to a related element node

1. ```parentNode``` - Selects the parent of the current element node(returns 1 element)

1. ```previousSibling/nextSibling``` - Selects the previous or next sibling from 								the DOM tree
1. ```firstChild/lastChild``` - Select the first of last child of the current element  


### to access/update text nodes

```**nodeValue**``` - this property lets you access or update contents of a text node

1. select the ```<li>``` element
1. Use the ```firstChild``` property to get the text node
1. Use the text node's only property (nodeValue)to get the text from the element
	* the text node does not include text inside any child elements

### to work with HTML content
1. ```**innerText**``` - allows access just to text
1. ```**innerHTML**``` - allows access to child elements and text content
* When getting HTML from an element, the innerHTML property will get the content of an
element and return it as one long string, including any markup that the element contains.

1. ```**textContent**``` - allows access just to text content

* When you use these properties to update the content of an element, the new content will
overwrite the entire contents of the element (both text and markup).

1. DOM manipulation - lets you create new nodes, add nodes to a tree and remove nodes from a tree

### to access/update attribute values
1. ```**className/id**``` - lets you get or update the value of the class and id attributes
1. ```**hasAttribute**``` - checks if an attribute exists
1. ```**getAttribute**``` - gets an attributes value
1. ```**setAttribute**``` - updates the attribute value
1. ```**removeAttribute**``` - removes an attribute

## Caching DOM queries

**DOM Queries** - Methods that find elements in the DOM tree
	* when you need to work with an element more than once you should use a variable tostore the result of this query

* When a script selects an element to access or update the interpreter must find the element(s) in the DOM tree
* Once it has found the node that represents the elements you can work with that node, its parent or any children

## Accessing Elements

**NodeList** - collection of nodes. Each node is given an index number(A number that starts at zero just like an array

* If a method can return more than one node, it will always return a Nodelist

**live NodeList** - when your script updates the page the NodeList is updated at the same time. 
**static NodeList** - when your script updates the page the NodeList is not updated to reflect the changes made by the script

when you have a NodeList you can loop through each node in the collection and apply the same statements to each using a for loop


### Selecting an Element from a Nodelist

**item method** - returns an individual node from the NodeList
* You specify the index number of the element you want as a parameter of the method inside parentheses

**Array Syntax**- preferred over the item() method because it is faster
* You can access individual nodes using a square bracket syntax similar to that used toacess individual items from an array by specifying the index number of the element you want inside square brackets that follow the Node List.


### Methods that return a single element node

* getElementById('id') - Selects an individual element given the value of its id attribute .
The HTML must have an id attribute in order for it to be selectable. the value is placed inside quote marks because it is a string.
 	* the quickest and most efficient way to access an element because no 2 elements canshare the same value for their id attribute


* querySelector('css selector') - Uses CSS selector syntax that would select one or more element s .
This method returns only the first of the matching elements.
	* not supported by older browsers. Can be used to accurately target many more elements

### Methods that return one or more elements as a NodeList

```getElementsByClassName('class')``` - Selects one or more elements given the value of their cl ass attribute. The HTML must have a class attribu te for it to be selectable. This method is faster than querySe1ectorA11().

```getElementsByTagName('tagName')``` - Selects all elements on the page with the specified tag name.
This method is faster than querySe1ectorA11().

```querySelectorAll('css selector')``` - Uses CSS selector syntax to select one or more elements and returns all of those that match.

## How to Get/Update Element Content

To work with the content of elements you can:
* **Navigate to the text nodes*. This works best when the element contains only text, no other
elements.
* **Work with the containing element**. This allows you to access its text nodes and child elements.
It works better when an element has text nodes and child elements that are siblings.

## Adding Elements Using DOM Manipulation

```**createElement()**``` - Creates a new node. This element is stored in a variable. When the element node is created it is not yet part of the DOM tree. 

```**createTextNode()**``` - creates a new text node. It is also stored in a variable. It can be added to the element node using ```appendChild()``` method. This provides content for the element. If you want to attach an empty element then skip this step

```**appendChild()**``` - used to add an element to the DOM tree. Allows you to specify which element you want this node added to, as a child of it.

```**InsertBefore()**``` - used to add anew element before the selected DOM node.

## Removing Elements via DOM manipulation
1. store the element to be removed in a variable
1. store the parent of that element in a variable using the parentNode property
1. Remove the element from its containing element using the removeChild() method. 
	* the 	```*remvoveChild()*``` method takes one parameter which is the reference to the element that you no longer want

## Cross-Site Scripting (XSS) Attacks

XSS involves an attacker placing malicious code into a site. 

**untrusted data** - data you don't have complete control over

XSS can give the attacker access to information in the DOM , the website cookies, or session tokens

**session tokens** - information that identifies you from other users when you log into a site

### Defending Against Cross-Site Scripting

**validation** - only letting visitors input the kind of characters they need to when supplying information. 

Double check validation on the server before displaying user content/storing it in a database

Escape all dangerous characters when data leaves the database
see book page 231 for list of characters that need to be escaped

**encodeURIComponent() method** - encodes the following characters:

, I ? : @ & = + $ #


## Attribute Nodes

2 steps to accessing and updating attributes

1. select the element node that carries the attribute and follow it with a period symbol
1. Use one of the following methods:

```getAttribute```: gets the value of an attribute
```hasAttribute```: checks if element node has a specified attribute. The attribute name is given as argument in the parentheses
```setAttribute```: sets the value of an attribute. 
```removeAttribute```: removes an attribute from an element node. first select the element then call the removeAttribute()

Or one of the following properties
className: gets or sets the value of the class attribute. If the attribute does not exist it will be created and given the specified value. 
id: gets or sets the value of the id attribute

https://deannaj401.github.io/reading-notes/.

