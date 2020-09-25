# Class 1 reading notes

## Ducket HTML

### Introduction p2-11

**Ch 1
12-39**

## Structure

* Headings are used to break up a document to make it easier to read
HTML describes the structure of pages

* HTML code is made up of characters that live inside angled
brackets — these are called HTML elements. Elements are usually made up of two tags: an opening tag and a closing tag. (The closing tag has an extra forward slash in it.) Each HTML element tells the browser something about the information that sits between its opening and closing tags.

## Attributes

* Attributes provide additional information about the contents of an element. They appear on the opening tag of the element and are made up of two parts: a name and a value,
separated by an equals sign.

``` <p lang="en-us">Paragraph in English</p> ```

1.  Here an attribute called lang is used to indicate the language used in this element. 
1. The value of this attribute on this page specifies it is in US English.

* The attribute name indicates what kind of extra information
you are supplying about the element's content. It should be
written in lowercase.

* The majority of attributes can only be used on certain elements, although a few attributes (such as lang)
can appear on any element.

* The value is the information or setting for the attribute. It
should be placed in double quotes. Different attributes can
have different values.

## Ch 8 176-199
### Extra Markup

* each web page should begin with a DOCTYPE declaration to tell a browser which version of HTML the page is using

* If you want to add a comment to your code that will not be
visible in the user's browser, you can add the text between these characters:

``` <!-- comment goes here --> ```

* Comments are a good idea in case you have to go back and look at your page or if someone else needs to work on your page.

* The ID attribute is used to uniquely identify that element
from other elements on the page. Its value should start with
a letter or an underscore (not a number or any other  character). It is important that no two elements on the same page have the same value for their id attributes (otherwise the value is no longer unique).

* The id attribute is known as a global attribute because it can be used on any element.

* The class attribute identifies several elements as being different from the other elements on the page. The class attribute on any element can share the same value.
1. By default, using these attributes does not affect the presentation of an element. It will only change their appearance if there is a CSS rule that indicates it should be
displayed differently.
1. If you would like to indicate that
an element belongs to several classes, you can separate class
names with a space

* block level elements always appear to start on a new line in the browser window.

*Examples of block elements are:*

``` <h1> <p>, <ul>, and <li>. ```

Some elements will always appear to continue on the
same line as their neighbouring elements. These are known as
inline elements.

*Examples of inline elements are:*

``` <a>, <b>, <em>, and <img>. ```

* The div element allows you to group a set of elements together in one block-level box.
Using a id or class attribute on the div element lets you create CSS style rules to indicate how much space the div element occupies on the screen and change the appearance of all the elements contained within it.

* The span element is used as an inline equivalent of the dive tag when you have a number of inline elements

* an iframe cuts a window into your page. Common use is embedding a google map. attributes used with an iframe are src height and width

* The meta element lives inside the head element and
contains information about that web page. The meta element is an empty element so it does not have a closing tag. It uses attributes to carry the information.

* Escape characters are for using characters that are normally found in code or special characters.

*List of Escape characters is in Duckett HTML page 194*



## Ch 17 428-451 
### HTML5 Layout

* The header and footer elements can be used for:

1.  The main header or footer that appears at the top or
bottom of every page on the site.

1.  A header or footer for an individual article or
section within the page.

* The nav element is used to contain the major navigational
blocks on the site such as the primary site navigation.

* The article element acts as a container for any section of a page that could stand alone and potentially be syndicated.
article elements can be nested

* The aside element has two purposes, depending on whether
it is inside an article element or not.
1.  When the  aside  element is used inside an article element, it should contain
information that is related to the article but not essential to its overall meaning. For example, a pullquote or glossary might be considered as an aside to the article it relates to.

1. When the aside element is used outside of an article element, it acts as a container for content that is related to the entire page. For example, it might contain links to other sections of the site, a list of recent posts, a search box, or recent tweets by the author.

* The section element groups related content together, and
typically each section would have its own heading.Because the section element groups related items together, it may contain several distinct article elements that have a common theme or purpose. if you have a page with a long article, the section element can be used to split the article up into
separate sections

* The purpose of the hgroup element is to group together a
set of one or more h1 through h6 elements so that they are
treated as one single heading.


## CH 18 452-475
### Process & Design

* a site map is a diagram of the pages that will be used to structure the site

*Example of a site map Ducket HTML page 462*

* card sorting is placing each piece of information that a
visitor might need to know on a separate piece of paper and
then organizing the related information into groups.

* A wireframe is a simple sketch of the key information that needs to go on each page of a site. It shows the hierarchy of the information and how much space it might require.
You should not include the color scheme, font choices,
backgrounds or images for the website in the wireframe.
It should focus on what information needs to be on
each page and create a visual hierarchy to indicate the most
important parts of each page.

*Example wireframe page 464 Duckett HTML*


## Ducket JavaScript

## ch 1 ABC of Programming

* A script is a series of instructions that the computer
can follow in order to achieve a goal.

* To approach writing a script, break down your goal into
a series of tasks and then work out each step needed
to complete that task (a flowchart can help).

 https://deannaj401.github.io/reading-notes/.