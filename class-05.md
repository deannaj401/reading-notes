Duckett HTML

Ch 5

P94 - 125

# Images

Images should...
* Be relevant    
* Convey information    
* Convey the right mood 
* Be instantly recognisable   
* Fit the color palette

The following are sites to get stock photos

```www.istockphoto.com```
```www.gettyimages.com```
```www.veer.com```
```www.sxc.hu```
```www.fotolia.com```

Create a folder for all the images the site use

```<img>``` is the element to add an image. This is an empty element with no closing tag. It must contain:

* ```<src>``` - this tells the browser where to find the image file

* ```<alt>``` - provides a text description of the image which describes the image if you cannot see it


```<title>``` - can also be used with the ```<img>``` element. it provides additional information about the image when a user hovers over the image.  


other attributes used in an ```<img>``` element are:

*height* - specifies height in pixels

*width* - specifies width in pixels

## Where to Place Images in code:

This is what happens when you place images in the following areas

1. **Before a paragraph**: The paragraph starts on a new line after the image.

1. **InsIde the start of a paragraph**: The first row of text aligns with the bottom of the image.

1. **In the mIddle of a paragraph**: The image is placed between the words of the paragraph that it appears in.

Block elements always appear on a new line. Examples of block elements include the ```<h1>``` and ```<p>``` elements.

Inline elements sit within a block level element and do not start on a new line

## Image Dimensions

The images you use on your website should be saved at the same width and height that you want them to appear on the page.

Images created for the web should be saved at a resolution of 72 ppi. The higher the resolution of the image, the larger the size of the file.


```<figure>``` contains images and their caption so that the two are associated
You can have more than one image inside the ```<figure>``` element as long as they all share the same caption.

```<figcaption>``` - allows to add a caption to an image

Photographs are best saved as JPEGS and vectors are best saved as Gifs

Ch 11

p246-263

# Color

* The color property allows you to specify the color of text inside an element. You can specify any color in CSS in one of three ways:

1. RGB values
1. Hex Codes
1. Color names

**background-color** - specifies the background color using the same 3 methods as above.

If you do not specify a background color then it is transparent

the default color is white but if you want to be sure to make it white, use the background - color property on the ```<body>``` element

**opacity** property - allows to specify the opacity of an element and any of its child elements

**hue** is expressed as an angle between 0 and 360 degrees

**saturation** is expressed asa percentage

**Lightness** is expressed as a percentage with 0% being white, 50% being normal and 100% being black

**alpha** - expressed as a number between 0 and 1.0 
(eg. .5 = 50% transparency)

Ch 12

p264-299

# Text

### Types of text:

1. **Serif** - Serif fonts have extra details on the ends of the main strokes of the letters. These details are known as serifs.

1. **Sans-Serif** - Sans-serif fonts have straight ends to letters, and therefore have a much cleaner design.

**Monospace** - Every letter in a monospace (or fixed-width) font is the same width. (Non-monospace fonts have different widths.)

* Browsers will only display a font if it is installed on the users computer

**font stack** - to specify more than one typeface and create an order of preference (in case the user does not have your first choice of typeface installed


### Font-Family property

**font-family property** - The font-family property allows you to specify the typeface that should be used for any text inside the element(s) to which a CSS rule applies.

The value of this property is the name of the typeface you want to use

If a font name is made up of more than one word, it should be put in double quotes.

* you should not use more than 3 typefaces on a page

### Font elements

**font-size property** - enables you to specify a size for the font.

the most common ways of specifying size are:

* Pixels
* Percentages
* Ems - (equivalent to the width of a letter m)

**@font-face** - allows you to use a font, even if it is not installed on the computer of the person browsing, by allowing you to specify a path to a copy of the font, which will be downloaded if it is not on the user's machine.

places to get free fonts:

1. www.foxsquirrel.com
1. www.fontex.org
1. www.openfontlibrary.org
1. www.typekit.com
1. www.kernest.com
1. www.fontspring.com

Google also provides open source fonts. Rather than adding the @font-face rule to your own style sheet, you link to a CSS file and font files on their servers: www.google.com/webfonts

**font-weight** - allows you to create bold text. There are two values that this property commonly takes:

1. normal - causes text to appear at a normal weight

1. bold - causes text to appear bold

**font-style** - makes text italic. The property can take 3 values:

1. normal
1. normal
1. oblique

**text-transform** - used to change the case of text giving it one of the following values:

1. uppercase 
1. lowercase 
1. capitalize


**text-decoration** - specifies the following values

1. none - removes any decoration already applied
1. underline
1. overline
1. line-through
1. blink

**line-height** - specifies line height or leading

**letter-spacing**
**word-spacing** -  specifies kerning

**text-align** -  allows you to control the alignment of text. The property can take one of four values:

1. left
1. right
1. center
1. justify

**vertical-align** - used with inline elements such as ```<img>```, ```<em>```, or ```<strong>``` elements. 
it performs a task very similar to the HTML align attribute used on the ```<img>``` element

it can take the following values:

1. baseline
1. sub super
1. top 
1. text-top 
1. middle 
1. bottom 
1. text-bottom


* It can also take a length (usually specified in pixels or ems) or a percentage of the line height

***text-indent*** - allows you to indent the first line of text within an element. The amount you want the line indented by can be specified in a number of ways but is usually given in pixels or ems.

psuedo classes change the style of an element when a user hovers over or clicks on text or when they have visited a link


https://deannaj401.github.io/reading-notes/.






 



