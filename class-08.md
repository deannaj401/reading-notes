*These are the same notes I took before but I did read the chapter again to refresh my memory*

Ch 15
p358-404
Layout


CSS treats each HTML element as if it is in its own box. This box will either be a block-level box or an inline box.

Block-level elements start on a new line Examples include: ```<h1>``` ```<p>``` ```<ul>``` ```<li>```

inline elements flow in Between surrounding text Examples include: ```<img>``` ```<b>``` ```<i>```

containing elements - if one block level element sits inside another block level element then the outer box is known as the containing or parent element.

```<div>``` is a common block level element

Positioning Schemes

Normal Flow: Every block-level element appears on a new line, causing each item to appear lower down the page than the previous one. Even if you specify the width of the boxes and there is space for two elements to sit side-by-side, they will not appear next to each other. This is the default behavior.

Since this is default behavior you don't need a property to indicate Normal Flow. But if you wanted to the syntax is

position: static;


Relative Positioning: This moves an element from the position it would be in normal flow, shifting it to the top, right, bottom, or left of where it would have been placed. This does not affect the position of surrounding elements; they stay in the position they would be in in normal flow.

position: relative;

Absolute Positioning: This positions the element in relation to its containing element. It is taken out of normal flow, meaning that it does not affect the position of any surrounding elements (as they simply ignore the space it would have taken up). Absolutely positioned elements move as users scroll up and down the page.

position: absolute;

Fixed Positioning: positions the element in relation to the browser window. Therefore, when a user scrolls down the page, it stays in the exact same place.

position: fixed;

You specify the positioning scheme using the position property in CSS.

Float property:  allows you to take an element in normal flow and place it as far to the left or right of the containing element as possible.
Anything else that sits inside the containing element will flow around the element that is floated. This should be used with the Width property to control how wide the floated element will be. 

p{
float: right;
width: 275px;
margin: 5px
padding: 5px

the above CSS makes blocks sit next to each other


z-index: allows you to control which box appears on top when boxes overlap.Its value is a number, and the higher the number the closer that element is to the front. For example, an element with a z-index of 10 will appear over the top of one with a z-index of 5. its sometimes called the stacking context

z-index: 10;}


clear property: allows you to say that no element (within the same containing element) should touch the left or righthand sides of a box. It can take the following values:

left: The left-hand side of the box should not touch any other elements appearing in the same containing element.

right:The right-hand side of the box will not touch elements appearing in the same containing element.

both:Neither the left nor right-hand sides of the box will touch elements appearing in the same containing element.

none: Elements can touch either side.

pages can be set to a fixed width or a liquid layout. Liquid Layouts use percentages so that the page is visible no matter what device you view it on. 

The standard is 960-1000 pixel wide