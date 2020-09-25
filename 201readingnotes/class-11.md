Duckett HTML

Ch 16
p406-427

# Images

 commonly used image sizes are:
*  Small portrait: 220 x 360
* Small landscape: 330 x 210
* Feature photo: 620 x 400

## float property

There are 2 ways to use the float property

1. The float property is added to the class that was created to
represent the size of the image 

1. New classes are created with names such as align-left or
align-right to align the images to the left or right of the page.
These class names are used in addition to classes that indicate
the size of the image.

*It is also common to add a margin to the image to ensure
that the text does not touch their edges.*

## Centering Images with CSS

Images are inline elements by default.

In order to center an image, it should be turned into a blocklevel
element using the **display property** with a value of **block.**

### 2 Common ways to horizontally center an image

1. On the containing element, you can use the text-align property with a value of center.

1. On the image itself, you can use the use the margin property and set the values of the left and right margins to auto.

* You can specify class names that allow any element to be centered, in the same way that you can for the dimensions or alignment of images.

This can also be used for the ```<figure>``` element

## Background Images

```<background-image>```

* The background-image property allows you to place an image behind any HTML
element. This could be the entire page or just part of the page. By default, a background image will repeat to fill the entire box

* The path to the image follows the letters url, and it is put inside parentheses and quotes.

## Repeating Images

```background-repeat```
```background-attachment```

The ```background-repeat``` property can have 4 values:

**repeat** - The background image is repeated both horizontally and vertically

**repeat-x** - The image is repeated horizontally only

**repeat-y** - The image is repeated vertically only

**no-repeat** - The image is only shown once

the ```background-attachment``` property specifies whether a background image should stay in one position or move as the user scrolls up and down the page. It can have one of two values:

**fixed** -the image stays in the same position on the page

**scroll** - The image moves up and down as the user scrolls up and down the page


## Background Position

```background-position```

```background-position``` - specifies where in the browser window the background image should be placed.

* This property usually has a pair of values. The first represents
the horizontal position and the second represents the vertical.

* If you only specify one value, the second value will default to
center.

* you can also use a pair of pixels or percentages. These represent
the distance from the top left corner of the browser window
(or containing box). The top left corner is equal to 0% 0%.


## Shorthand

### background

* The background property acts like a shorthand for all of the other background properties

* The properties must be specified in the following order but you can miss any value if you do not want to specify it

1. background-color
1. background-image
1. background-repeat
1. background-attachment
1. background-position

## Image Rollovers and Sprites

**rollover** - a link or button that changes to a second style when a user moves their mouse over it

* set a background image for the link or button that has 3 different styles of the same button (but only allows enough space to show one of them at a time)

* When the user moves their mouse over the element or clicks on it the position of the background image is moved to show the relevant image. 

page 418 ducket html shows the steps to create a rollover

* To reduce the number of images your browser has to load you can create image sprites

Ch 19 
p476-492

# Practical information

## Search Engine Optimization  (SEO)

**search engine optimization** - the practice of trying to help your site appear nearer the top of search engine results when people look for the topics that your website covers.

**on-page techniques** - the methods you can use on your web pages to improve their rating in search engines.

* There are 7 places where keywords can appear to improve its findability

1. page title
1. url/web address
1. headings
1. text
1. link text
1. image alt text
1. page descriptions



**off-page techniques** - determining how to rank your site by looking at the other sites that link to yours

*Flash is no longer supported but the reading pages were bookmarked just in case.*




https://deannaj401.github.io/reading-notes/