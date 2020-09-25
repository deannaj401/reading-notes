Duckett HTML 
Ch2 40-61

# TEXT

HTML has six "levels" of headings:
# ```<h1>```is the biggest 
```<h6>``` is the smallest

```<p>``` is the paragraph tag

By default, a browser will show each paragraph on a new line
with some space between it and any subsequent paragraphs

<b>```<b>``` is the bold tag

<i>```<i>``` is the italic tag

The <sup>```<sup>``` element is used to contain characters that
should be superscript such as the suffixes of dates or
mathematical concepts like raising a number to a power 

The <sub> ```<sub>``` element is used to contain characters that should
be subscript. It is commonly used with foot notes or chemical
formulas such as H<sub>2</sub>0.

### white space collapsing: 
When a browser comes across 2 or more spaces next to each other and only displays one space. Or if it comes across a line break it treats it as a single space.

```<br />``` (Line Break) and

```<hr />```(Horizontal Rule break ) are
empty elements because they only have one tag and a space and a forward slash.

Visual editors often resemble word processors. Although
each editor will differ slightly,there are some features that
are common to most editors that allow you to control the
presentation of text.

●● Headings are created by
highlighting text then using
a drop-down box to select a
heading.

●● Bold and italic text are
created by highlighting some
text and pressing a b or i
button.

●● New paragraphs are created
using the return or the enter
key.

●● Line breaks are created by
pressing the shift key and the
return key at the same time.

●● Horizontal rules are created
using a button with a straight
line on it.

When copying  text from a program like Word into a visual editor first paste into Notepad to prevent it adding extra Markup

Code views show you the code created by the visual editor so
you can manually edit it, or so you can just enter new code
yourself. It is often activated using a button with an icon
that says HTML or has angled brackets. White space may be
added to the code by the editor to make the code easier to read.

## Semantic Markup - does not affect the structure of the web page but does add extra information to the page

```<strong>``` indicates the content has strong importance
by default browsers will show this is bold

```<em>``` indicates emphasis that subtly changes the meaning of a sentence. by default a browser will show this in italics

The ```<blockquote>``` <blockquote> element is used for longer quotes that take
up an entire paragraph.

The ```<p>``` element is still used inside the ```<blockquote>``` element. Usually a browser will indent a ```<blockquote>```



```<q>``` is used for shorter quotes that sit within a paragraph. Browsers are supposed to put quotes around the ```<q>``` element but Internet Explorer does not so its not recommended.

```<abbr>``` used on abbreviations or acronyms. Used with a title attribute in the opening tag:

```<p><abbr title="Professor">Prof</abbr>```

```<cite>``` references a piece of work like a book or film

```<dfn>``` indicates the defining instance of a new term

```<address>``` to contain contact info of the author of the page like physical address email or phone number

<ins> ```<ins>``` shows content that was added to the page. Usually underlined

<del>```<del>``` shows content that was deleted from page. Usually crossed out

```<s>``` indicated something that is no longer relevant but should not be deleted. Usually shows up crossed out. 
Example.
<s> Was $999 </s> now
 only $5.

# Ch 10
226-245

## Intro to CSS

CSS is what adds styling to an HTML page

CSS treats each HTML element as if it appears inside
its own box and uses rules to indicate how that
element should look.

CSS works by associating rules with HTML elements. These rules govern how the content of specified elements should be displayed.
 A CSS rule contains two parts:
 a selector and a declaration.  

1. Selectors indicate which element the rule applies to.
The same rule can apply to more than one element if you
separate the element names with commas.

1. Declarations indicate how the elements referred to in
the selector should be styled.
Declarations are split into two parts (a property and a value), and are separated by a colon.

* CSS declarations sit inside curly brackets and each is made up of two parts: a property and a value, separated by a colon. You can specify several properties in one declaration, each separated by a semi-colon.

* Properties indicate the aspects of the element you want to
change. For example, color, font, width, height and border.

Values specify the settings you want to use for the chosen
properties. For example, if you want to specify a color property then the value is the color you want the text in these elements 

## External CSS

```<link>``` element is an empty element that is in the ```<head>``` element. used to tell the browser where to find the CSS file used to style the page
It uses 3 attributes:

1. href -  specifies the path to the CSS file (which is often placed in a folder called css or styles).

1. type -  specifies the type of document being linked to. the value should be text/css

1. rel - specifies the relationship between the HTML page and the file it is linked to. The value should be stylesheet when linking to a CSS file.

Sometimes there are multiple CSS files in a HTML page. for example one used for fonts and colors and another to control layout. 

Internal CSS

```<style>``` sits in the ```<head>``` element and gives CSS rules. Usually only used if an HTML page only has 1 page

If you use external CSS you can change an element across all the pages from one place and keeps the content easier to manage.

## CSS Selectors

CSS selectors are case sensitive and must match element names and attribute values exactly

The following are common selectors:

* Universal - applies to all elements in the document
example -  *{}

* Type - Matches element names 

  example -  h1 h2 h3 {}

* Class - Matches an element whose class attribute has a value that matches the one specified after the period symbol

example -  .note{} (targets any element whose clase attribute is has a value of note.)

p.note{} (targets only ```<p>``` elements whose class attribute has a value of note)

* ID - Matches an element whose id attribute has a value that matches the one specified after the pound or hash symbol

example -  #introduction {} (Targets the element whose id attribute has a value of introduction)

* Child - Matches an element that is a direct child of another
example li>a{} (Targets any``` <a>``` elements are children of an ```<li>``` element but not other ```<a>``` elements in the page)

* Descendant - Matches an element that is a descendent of another specified element(not just a direct child of that element)

example -  p a {} (targets any ```<a>``` elements that sit inside a ```<p>``` element even if there are other elements nested between them.)

Adjacent Sibling  - Matches an element that is the next sibling of another
example h1+p {} ( Targets the first ```<p>``` element after any ```<h1>``` element but not other ```<p>``` elements

*General Sibling - Matches an element that is a sibling of another although it does not hae to be the directly preceding element

example h1~p {} If you had 2 ```<p>``` elements that are siblings of an ```<h1>``` element, this rule would apply to both.

## CSS Rules Cascade

If 2 or more rules apply to the same element then there are rules as to which will take precedence

**LAST RULE** - 
If the two selectors are identical, the latter of the two will take precedence.


**SPECIFICITY** - 
If one selector is more specific than the others, the more
specific rule will take precedence over more general ones.

example:
h1 is more specific than *

You can add !important after any property value to indicate
that it should be considered more important than other rules
that apply to the same element.

### Inheritance

If you specify the font-family or color properties on the ```<body>``` element they will apply to most child elements because the value of the font-family property is inherited by child elements.

background-color or border properties are not inherited. 
If they were the page would look messy

You can force a lot of properties to inherit values from their parent elements by using inherit for the value of the
properties.


## Duckett JavaScript

Ch 2 53-84

# Basic JavaScript Instructions

A script is a series of instructions that a computer can follow one-by-one.
Each individual instruction or step is known as a statement.
Statements should end with a semicolon.

JavaScript is case sensitive

Code blocks are statements surrounded by curly braces. There is no semicolon at the end

## Comments

comments help explain what the code does and helps you and others who read your code

* Multi-line comments - start and end with /* and */. Anything between these characters is not processed by the JavaScript interpreter

* Single-line comment - // used for short descriptions of code. 

* camelCase - first word is all lowercase and any subsequent words have their first letter capitalized

3 data types

1. Numeric Data handles numbers including negative numbers and decimals

1. String Data consists of letters and special characters. It is enclosed within a pair of quotes

1. Boolean Data - can have one of two values...either true or false

when declaring a variable in JavaScript, you do not need to specify what type of data it will hold.

* escaping - using a backwards slash before any type of quote mark that appears within a string. Good for using in contractions (won't didn't etc)

## ARRAYS

Array- special type of variable that stores a list of values and you do not need to specify how many values it will hold. Values in arrays are seperated by commas

an array is named like any other variable
(var followed by name of the array)

The values are assigned to the array inside a pair of square brackets, and each value is separated by a comma.

The values in the array do not need to be the same data type, so you can store a string, a number and a Boolean all in the same array.

Values in an array are accessed as if they are in a numbered list. It is important to know that the numbering of this list starts at zero (not one).

example of Array

var colors;
colors ['white', 'black', ' custom '];

Each item in an array is automatically given a number
called an index. This can be used to access specific items in the array. 
example:

var colors;
colors= ['white' ,'black' ,' custom'];

* index values start at 0 (not 1), so the following table
shows items from the array and their corresponding index values:

INDEX VALUE

o 'white '

1 'black'

2 'custom'

To retrieve the third item on the list, the array name is specified along with the index number in square brackets.

example:

var itemThree;

itemThree = colors [2];

* Each array has a property called length, which holds the number of items in the array.

example 

var numColors ;
numColors =colors. length;

## Expressions

An expression (results in) a single value.
some expressions just assign a value to a variable like a color or number
some expressions perform operations like 
var area = 3 * 2
the value is now 6
or joining together strings of words

JavaScript uses the following math operators

Addition + 

Subtraction - 

Division /

Multiplication *

Increment ++ ( adds 1 to the current number)

Decrement -- (subtracts 1 from the current number)

Modulus % (divides 2 values and returns the remainder 
eg 10 % 3  1)


NaN means not a number and happens when you try to add strings instead of numbers

## Ch4 
145-162

# Decisions and Loops

Evaluations: analyzes values in your scripts to determine whether or not they match expected results

Decisions: Decides which path your script should go down

Loops: used to perform the same set of steps repeatedly

FLOWCHART:

flowcharts help plan decisions on where code should be run next In order to determine which path to take you set a condition
If the condition returns true you take one path if it is false you take another path

Comparison operators allow you to compare values and test whether a condition is met or not.
examples are > (greater than) < (less than) and == which checks whether 2 values are the same

2 components of a decision
1. an expression is evaluated which returns a value
2. a conditional statement says what to do in a given situation.

Evaluation: Checks the current status of the script by comparing 2 values using a comparison operator which returns a value of true or false

Conditional statement: based on a concept of if/then/else

example:
if a condition is met then your code executes one or more statements, else your code does something else or skips the step

You can also use multiple conditions by combining 2 or more comparison operators

example: checking whether 2 conditions are both met or if just one of several conditions is met

Types of comparison operators


* == (is equal to)
compares 2 values (numbers strings or Booleans) to see if they are the same

* != (is not equal to) 
compares 2 values (numbers strings or Booleans) to see if they are not the same

* === (Strict equal to) 
compares 2 values to check that both the data type and value are the same

'3' === 3 returns false because they are not the same data type or value

* !== (Strict not equal to)
compares 2 values to check that both the data type and value are not the same

'3' !== 3 returns true because they are not the same data type or value

### Its usually preferable to use the strict method

In any condition, there is usually 1 operator and 2 operands. The operands are placed on each side of the operator. They can be values or variables. Expressions are enclosed in brackets.

The operand does not have to ba a single value or variable name. An operand can be an expression because each expression evaluates into a single value

Comparison operators usually return single values of true or false.
Logical operators allow you to compare the results of more than one comparison operator

## Logical operators

* Logical And: &&  tests more than one condition. 

true && true returns true

true && false returns false

false && true returns false

false && false returns false


* Logical Or : || tests at least one condition

true || true returns true

true || false returns true

false || true returns true

false || false returns false


* Logical Not: ! takes a single Boolean value and inverts it. Reverses the expression

!true returns false

!false returns true

Logical expressions are evaluated left to right. If the 1st condition can provide enough information to get the answer then there is no need to evaluate the second condition

false && anything

it has found a false so there is no point to determine the other result as they cannot both be true

true || anything

There is no point continuing because at least one of the values is true

## IF statements

The if statement evaluates a condition. If the condition evaluates to true, any statements in the subsequent code block are executed. If the condition evaluates to false the statements in the code block are not run and the script moves to the next block.

## IF...Else

the if...else statement checks a condition. If it resolves to true the first code block is executed. if the condition resolves to false the second code block is run instead.

The statements inside an if statement should be followed by a semicolon but not after the curly brace of the code block.

An if statement only runs a set of statements if the
condition is true:

An if ... else statement runs one set of code if the
condition is true or a different set if it is false:

https://deannaj401.github.io/reading-notes/.

