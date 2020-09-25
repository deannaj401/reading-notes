Duckett HTML
Ch 3
62-73

# Lists

Browsers indent lists by default

Ordered lists are lists where each item in the list is
numbered.
It is created with the ```<ol>``` element

Each item in the list is placed between an opening ```<li>``` tag and a closing ```</li>``` tag. (The li stands for list item.)

Unordered lists are lists that begin with a bullet point
It is created with the ```<ul>```element and also uses ```<li>``` element like an ordered list


Definition lists are made up of a set of terms along with the definitions for each of those terms.

It is created with the ```<dl>``` 


Definition lists usually contain
   
   ``` <dl>  ```  and ```<dt>``` elements


```<dt>```    used to contain the term being defined

	
```<dd>``` - used to contain the definition

You can put a second list inside an ```<li>``` element to create a sublist or nested list Browsers display nested lists indented further than parent lists. In unordered lists Browsers will usually change the style of the bullet point too.




Ch13
Boxes
p300-329

## Box Dimensions

* height and width properties are used to set the box siz 

3 ways to specify siz
pixels
percentages
ems

1. pixels are the most popular method to specify the size because you can accurately control the size

1. percentages are the size of the box relative to the size of the browser window

1. ems are the size of the box based on the size of the tet within it

## Limiting Width

- min-width - the smallest size a box can be displayed at when the browser window is narrow

- max-width - the maximum width a box can stretch to when the browser window is wide

## Limiting Height

- min-height - the smallest size a box can be displayed at then the browser window is short

- max-height - the maximum height a box can stretch to when the browser window is long

Overflow property tells the browser what to do if the content contained within a box is larger than the box itself.

It has 1 of 2 values:

1. hidden: hides any extra content that doesn't fit

1. scroll: adds a scrollbar to the box so users can scroll down


## Border Margin & Padding

3 properties that can be adjusted to control the appearance of a box:

1. Border - Every box has a border even if its not visible. It seperates the edge of one box from another

1. Margin- sit outside the edge of the border. the width of the margin controls the gap between the borders of 2 boxes

1. Padding - the space between the border of a box and any content contained within it

If you specify a width for a box, then the borders, margin, and padding are added to its width and height.

## White Space & Vertical Margin

white space - the space between items on a page

If the bottom margin of any box touches the top margin of
another, the browser will only show the larger of the two margins. If both margins are the same size, it will
only show one.

## Border Width

The border-width property is used to control the width
of a border. The value of this property can either be given
in pixels or using one of the following values:

* thin
* medium
* thick

(You cannot use percentages with this property.)

You can control the individual size of borders using four
separate properties:

* border-top-width
* border-right-width
* border-bottom-width
* border-left-width

You can specify all four values in one property:

border-width: 2px 1px 1px 2px;

the values appear in clockwise order: top, right, bottom, left.

## Border Style

border-style - controls style of the border
it uses the following values:

*solid* -  a single solid line

*dotted* -  a series of square dots

*dashed* - a series of short lines

*double* -  two solid lines

*groove* -  appears to be carved into the page

*ridge*  - appears to stick out from the page

*inset* - appears embedded into the page

*outset* - looks like it is coming out of the screen

*hidden / none*  - no border is shown

You can individually change the
styles of different borders using:

border-top-style
border-left-style
border-right-style
border-bottom-style


## Border Color

Colors can be specified using RGB values, hex codes or CSS color names

It is possible to individually
control the colors of the borders
on different sides of a box using:
border-top-color

border-right-color

border-bottom-color

border-left-color


Or you can control the color of the border using one property

*border-color: darkcyan deeppink darkcyan deeppink;*

The values appear clockwise: top, right, bottom, left

### The border property allows you to specify the width, style and color of a border in one property in that specific order

## Padding

The padding property allows you to specify how much space
should appear between the content of an element and its
border.

Most often this property is specified in pixels
If a width is specified for a box, padding is
added onto the width of the box.

You can specify different values
for each side of a box using:

padding-top

padding-right

padding-bottom

padding-left


Or you can control the color of the border using one property
the values appear clockwise: top, right, bottom, left

**padding: 10px 5px 3px 1px;*

The value of the padding property is not inherited by child elements in the same way that the color value of the font-family property is; so you need to specify the padding for every element that needs to use it.

## Margin Property

The margin property controls the gap between boxes. Its value
is commonly given in pixels

If one box sits on top of another margins are collapsed , which means the larger of the two margins will be used and the smaller will be disregarded.

If the width of a box is specified then the margin is
added to the width of the box.

You can specify values for each
side of a box using:

margin-top

margin-right

margin-bottom

margin-left

Or you can control the color of the border using one property
the values appear clockwise: top, right, bottom, left

*margin: 1px 2px 3px 4px;*

 another way to write it is

*margin: 10px 20 px;*

* which means the left and right margins should be 10 pixels and the top and bottom should be 20 pixels

The value of the margin property is not inherited by child elements in the same way that the color value of the font-family property is, so you need to specify the margin for every element that needs to use it.

## Centering Content

If you want to center a box on the page (or center it inside
the element that it sits in), you can set the left-margin and
right-margin to auto.

In order to center a box on the page, you need to set a width
for the box (otherwise it will take up the full width of the page).

Once you have specified the width of the box, setting the left and right margins to auto will make the browser put an equal gap on each side of the box. This centers the box on the page (or within the element that the box sits inside).

The text-align property is inherited by child elements. You
therefore also need to specify the text-align property on the
centered box if you do not want the text inside it to be centered

## Change Inline/Block 

display property - allows you to turn an inline element into a block-level element or vice versa. also can be used to hide an element from the page

This property uses the following values:

- inline - causes a block-level element to act like an inline element

- block - causes an inline element to act like a block-level element

- inline-block - causes a block-level element to flow like an inline element, while retaining other features of a block-level element.

- none - hides an element from the page by acting as though it is not on the page at all

## Hiding Boxes

*visibility property* - allows you to hide boxes from users
but It leaves a space where the element would have been.

This property uses the following values:

1. hidden which hides the element
If the visibility of an element is set to hidden, a blank space will appear in its place.
If you do not want a blank space to appear, then you should use the display property with a value of none instead


1. visible which shows the element




Duckett JavaScript

ch 4
Decisions and Loops
162-182

## IF...ELSE Statements

The if...else statement checks a condition. If it resolves to true the first code block is executed. If the condition resolves to false the second code block is run instead.

statements inside an if statement should be followed by a semicolon, but there is no need to place one
after the closing curly brace of the code blocks.


## Switch Statements

a *switch statement* starts with a variable called the switch value. Each case indicates a possible value for this variable and the code that should run if the variable matches that value

At the end of each case is the *break* keyword. It tells
the JavaScript interpreter that it has finished with
this switch statement and to proceed to run any
subsequent code that appears after it.


JavaScript can convert data types behind the scenes to
complete an operation. This is known as *type coercion.*

JavaScript is said to use *weak typing* because the data type
for a value can change.

## Truthy & Falsy values

Due to type coercion, every value in JavaScript can be treated as if it were true or false

## Loops

* For - used to run a code a specific number 
of times. the condition is usually a counter
which is used to tell how many times the loop should
run.

* While the code continues to loop for as long as the 
condition is true

* Do While - always run the statements inside the 
curly braces at least once even if the condition 
evaluates to false


https://deannaj401.github.io/reading-notes/.