Duckett HTML 
Ch 4 p74-93

# Links

## Linking To Other Sites


Links are created using the ```<a>``` element which has an attribute called _href_
The value of the _href_ attribute is where the link goes when the user clicks on it.

The link should also tell the user where the link goes if possible

*absolute URL* - the full web address for a site in a link

*URL* - Uniform Resource Locator

## Linking To Other Pages on the Same Site

A page within the same site can be linked to with a _relative URL_

*relative URL* - shorthand version of absolute URLs because they do not specify the domain name.

### Directory Structure

top level folder is called the _root_  folder and contains all of the other files and folders for a website. it also contains the index.html file for the entire site

*relationships* - the directory structure uses  
* parent
* child 
* grandparent 
* grandchild 
  
  for relationships between files and folders


### Relative Link types

**same folder** - just use the file name

**child folder** - the name of the child folder, followed by a forward slash, then the file name.

**grandchild folder** -  Use the name of the child folder, followed by a forward slash, then the name of the grandchild folder, followed by another forward slash, then the file name.

**parent folder** - Use ../ to indicate the folder above the current one, then follow it with the file name.

**grandparent folder** - Repeat the ../ to indicate that you want to go up two folders (rather than one), then follow it with the file name.

* when a website is uploaded to a webserver a forward slash will return the homepage for the entire site, and a forward slash followed by a file name will return that file providing it is in the root directory.

## Email link

an example of a link to the users email program. It opens a new email message and addresses it to the person specified

```<a href="mailto:jon@example.org">Email Jon</a>```

## Opening Links in a New Window

example of a link to open up a link in a new window

```<a href="http://www.imdb.com" target="_blank">``` 

* this link uses the target attribute on the opening ```<a>``` tag

## Linking To A Specific Part of the Same Page

example of a link to a specific part of the same page

```<a href="#arc_shot">Arc Shot</a><br /> ```

* the above link would take you to the section called Arc Shot. It uses an id tag in the link. The heading Arc Shot on the page needs to use an id tag as well 

```<h2 id="arc_shot">Arc Shot</h2>```

* You can link to a specific part of a page on another website  by putting in the absolute URL after href followed by a ```#``` symbol, followed by the element you are linking to. The other website must use id attributes that identify specific parts of the page.

example:

```<a href="http:/www. htmlandcssbookcom/ #bottom">```

Ch 15
p358-404

## Layout


CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.

*Block-level elements* -  start on a new line Examples include: ```<h1>``` ```<p>``` ```<ul>``` ```<li>```

*inline elements* -  flow in Between surrounding text Examples include: ```<img>``` ```<b>``` ```<i>```

*containing elements* - if one block level element sits inside another block level element then the outer box is known as the containing or parent element.

```<div>``` is a common block level element

## Positioning Schemes

**Normal Flow**: Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-by-side, they will not appear next to each other. This is the default behavior.

* Since this is default behavior you don't need a property to indicate Normal Flow. But if you wanted to the syntax is

*position: static;*



**Relative Positioning**: This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.

*position: relative;*

**Absolute Positioning**: This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

*position: absolute;*

**Fixed Positioning**: positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place.

*position: fixed;*

* You specify the positioning scheme using the position property in CSS.

**Float property**:  allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.
Anything else that sits inside the containing element will flow around the element that is floated. This should be used with the Width property to control how wide the floated element will be. 

*p{
float: right;

width: 275px;

margin: 5px

padding: 5px*

* the above CSS makes blocks sit next to each other


**z-index**: allows you to control which box appears on top when boxes overlap.Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10 will appear over the top of one with a z-index of 5. its sometimes called the stacking context

*z-index: 10;}*


**clear property**: allows you to say that no element (within the same containing element) should touch the left or righthand sides of a box. It can take the following values:

* *left*: The left-hand side of the box should not touch any other elements appearing in the same containing element.

* *right*:The right-hand side of the box will not touch elements appearing in the same containing element.

* *both*:Neither the left nor right-hand sides of the box will touch elements appearing in the same containing element.

* *none*: Elements can touch either side.

pages can be set to a fixed width or a liquid layout. Liquid Layouts use percentages so that the page is visible no matter what device you view it on. 

The standard is 960-1000 pixel wide

Duckett JavaScript
Ch 3 86-99

# Functions Methods & Objects

**Functions**: let you group a series of statements together to perform a specific task. If different parts of a script repeat the same task, you can reuse the function (rather than repeating the same set of statements). 
You can also store the steps needed for a task since functions are not always executed when a page loads

*function declaration*: giving the function a name and then writing the statements needed to achieve its task inside the curly braces.

example of a function:

function sayHello() {
 document.write('Hello!');

**calling a function**: executing all of the statements between the curly braces with one line of code. 

example of calling a function:

sayHello();

**parameters**: information the function needs to work..(width height..etc). The paramenters act like variables

example of paramenters

function getArea(width, height) {
 return width * height;

* width and height are the parameters in the above example

**arguments**: the values a function should use in the parentheses that follow its name. They can be values or variables

example:

getArea(3, 5);

* the arguments are values

wallWidth = 3;
wallHeight = 5;
getArea(wallWidth, wallHeight);

* the arguments are the variables wallWidth and wallHeight

**return keyword**: used to return a value to the code that called the function. When return is used the interpreter leaves the function . It goes back to the statement that called it. 

functions return more than one value using an Array

*variable scope* : if you declare a variable within a function it can only be used within that function

**Local Variable**: a variable that can only be used in the function where it was created. 

**Global variable**: a variable that is created outside a function and can be used anywhere within the script


https://deannaj401.github.io/reading-notes/.