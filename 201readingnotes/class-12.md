Reading Class 12

# Charts.JS

Charts.js is a JavaScript plugin that uses HTML5;s canvas element to draw the graph on the page.

```<canvas>``` tag is used to create a canvas to draw the chart
then you use the ```<script>``` tag to call the code used to make the chart

you can make line charts, pie charts and bar charts

the usage documentation tells all the ways to use chart.js

## Basic Usage

the ```<canvas>``` tag only has 2 attributes - height and width

* If no height and width are specified the canvas will initially be  300w by 150 high
	

It is always good to specify the ```<id>``` tag because this makes it easier to identify in a script

the ```<canvas>``` element can be styled just like any normal image with margin, border background etc.. 
* These rules do not affect the actual drawing on the canvas
* When no styling is specified the canvas will be transparent
	
the ```<canvas>``` tag requires a closing ```</canvas>``` 

## The Rendering Context

The ```<canvas>``` element creates a fixed-size drawing surface that exposes one or more rendering contexts, which are used to create and manipulate the content shown.

The canvas is initially blank. To display something, a script first needs to access the rendering context and draw on it.

```getContext()``` - is a method used by the ```<canvas>``` element to obtain the rendering context and its drawing functions. 

* it has one paramenter - the type of context
	
## Drawing Rectangles

The ```<canvas>``` element only supports 2 primitive shapes
	1. rectangles
	1. paths ( lists of points connected by lines)
**all other shapes must be created by combining one or more paths.**

*There are 3 functions that draw rectangles on the canvas:*

1.```fillRect(x, y, width, height)``` - draws a filled rectangle
	
2.```strokeRect(x, y, width, height)``` - draws a rectangular outline

3.```clearRect(x, y, width, height)``` - clears the specified rectangular area, making it fully transparent.
	
*x and y specify the position on the canvas relative to the origin of the top left corner of the rectangle. width and height provide the rectangles size*

**All 3 rectangle functions draw immediately to the canvas**

```rect(x, y, width, height)``` - rect(x, y, width, height)

*Before this method is executed, the ```moveTo()``` method is automatically called with the parameters (x,y). In other words, the current pen position is automatically reset to the default coordinates.*

## Drawing Paths

**Path** -  a list of points, connected by segments of lines that can be of different shapes, curved or not, of different width and of different color. A path, or even a subpath, can be closed.

**Making Shapes** - there are 3 steps to make a shape with paths

	1. create the path
	2. using drawing command to draw into the path
	3. stroke, or fill the path to render it
	
I bookmarked the link that showed all the drawing commands

Also the following functions are used to perform these steps:

* ```beginPath()``` - Creates a new path. Once created, future drawing commands are directed into the path and used to build the path up.

* Path methods - methods to set different paths for objects
(see bookmarked link)

* ```closePath()``` - Adds a straight line to the path, going to the start of the current sub-path.

* ```stroke()``` - Draws the shape by stroking its outline.

* ```fill()``` - Draws a solid shape by filling the path's content area.

**The first step to create a path is to call the ```beginPath()```. Internally, paths are stored as a list of sub-paths (lines, arcs, etc) which together form a shape. Every time this method is called, the list is reset and we can start drawing new shapes.**

** When the current path is empty, such as immediately after calling ```beginPath()```, or on a newly created canvas, the first path construction command is always treated as a ```moveTo()```, regardless of what it actually is. For that reason, you will almost always want to specifically set your starting position after resetting a path.**

 **When you call ```fill()```, any open shapes are closed automatically, so you don't have to call ```closePath()```. This is not the case when you call ```stroke().```**
 
 **```moveTo()```** - doesn't actually draw anything but becomes part of the path list described above
	* You can probably best think of this as lifting a pen or pencil from one spot on a piece of paper and placing it on the next.
	
* When the canvas is initialized or ```beginPath()``` is called, you typically will want to use the ```moveTo()``` function to place the starting point somewhere else. We could also use ```moveTo()``` to draw unconnected paths

```lineTo(x,y)``` method - Draws a line from the current drawing position to the position specified by x and y.

**This method takes two arguments, x and y, which are the coordinates of the line's end point. The starting point is dependent on previously drawn paths, where the end point of the previous path is the starting point for the following, etc. The starting point can also be changed by using the ```moveTo()``` method.**

**arcTo method** - there are 2 types of this method

```arc(x, y, radius, startAngle, endAngle, anticlockwise)``` - Draws an arc which is centered at (x, y) position with radius r starting at startAngle and ending at **endAngle** going in the given direction indicated by anticlockwise (defaulting to clockwise).

```arcTo(x1, y1, x2, y2, radius)``` - Draws an arc with the given control points and radius, connected to the previous point by a straight line


 * The ```startAngle``` and ```endAngle``` parameters define the start and end points of the arc in radians, along the curve of the circle. These are measured from the x axis.
 
 * ```anticlockwise``` parameter is a Boolean value which, when true, draws the arc anticlockwise; otherwise, the arc is drawn clockwise.
 
 ## Bezier Curves
 
 * Bezier curve is used to draw complex organic shapes
 
 ```quadraticCurveTo(cp1x, cp1y, x, y)``` - Draws a quadratic Bézier curve from the current pen position to the end point specified by x and y, using the control point specified by cp1x and cp1y.
 
 ```bezierCurveTo(cp1x, cp1y, cp2x, cp2y, x, y)``` - 
 Draws a cubic Bézier curve from the current pen position to the end point specified by x and y, using the control points specified by (cp1x, cp1y) and (cp2x, cp2y).
 
 ** A quadratic Bézier curve has a start and an end point (blue dots) and just one control point (indicated by the red dot) while a cubic Bézier curve uses two control points.**
 
 ## Path2D Objects
 
 ```Path2D()``` - returns a newly instantiated ```Path2D``` object optionally with another path as an argument (creates a copy), or optionally with a string consisting of SVG path data.
 
 All path methods are available on Path2D objects
 
 ```Path2D.addPath(path [, transform])``` - Adds a path to the current path with an optional transformation matrix.
 
 # Applying Styles and colors
 
 ## Colors
 
 There are 2 properties to apply colors
 
 1. ```fillStyle=color``` - sets the syle used when flling shapes
 
 1. ```strokeStyle = color``` - Sets the style for shapes' outlines
 
 **olor is a string representing a CSS <color>, a gradient object, or a pattern object.**
 
 **When you set the strokeStyle and/or fillStyle property, the new value becomes the default for all shapes being drawn from then on. For every shape you want in a different color, you will need to reassign the fillStyle or strokeStyle property.**
 
 
 ## Transparency
 
 Transparancy is acheived by setting the globalAlpha property or by assigning a semi-transparent color to the stroke or fill style.
 
 ```globalAlpha = transparencyValue``` - Applies the specified transparency value to all future shapes drawn on the canvas. The value must be between 0.0 (fully transparent) to 1.0 (fully opaque). This value is 1.0 (fully opaque) by default.
 
 ## Line Styles
 
 The following properties allow us to style lines
 
 ```lineWidth = value``` - Sets the width of lines drawn in the future.
 
 **This property sets the current line thickness. Values must be positive numbers. By default this value is set to 1.0 units.**
 
 ```lineCap = type``` - Sets the appearance of the ends of lines.
 
 **There are three possible values for this property and those are: butt, round and square. By default this property is set to butt.**
	1. butt - ends of line are squared off at the endpoints
	1. round - end of lines are rounded
	1. square - The ends of lines are squared off by adding a box with an equal width and half the height of the line's thickness.
 
 ```lineJoin = type``` - Sets the appearance of the "corners" where lines meet.
 
 **There are three possible values for this property: round, bevel and miter. By default this property is set to miter**
	1. round - Rounds off the corners of a shape by filling an additional sector of disc centered at the common endpoint of connected segments. The radius for these rounded corners is equal to half the line width.
	1. bevel1 - Fills an additional triangular area between the common endpoint of connected segments, and the separate outside rectangular corners of each segment.
	1. miter - Connected segments are joined by extending their outside edges to connect at a single point, with the effect of filling an additional lozenge-shaped area.
	
	
 
 
 
 
 
 ```miterLimit = value``` - Establishes a limit on the miter when two lines join at a sharp angle, to let you control how thick the junction becomes.
 
 ** the miter limit is the maximum allowed ratio of the extension length (in the HTML canvas, it is measured between the outside corner of the joined edges of the line and the common endpoint of connecting segments specified in the path) to half the line width.**
 
 ```getLineDash()``` - Returns the current line dash pattern array containing an even number of non-negative numbers.
 
 ```setLineDash(segments)``` - Sets the current line dash pattern.
 
 ```lineDashOffset = value``` - Specifies where to start a dash array on a line.
 
## Gradients

gradients are created with the ```CanvasGradient``` object
by using one of the following methods.

```createLinearGradient(x1, y1, x2, y2)``` - Creates a linear gradient object with a starting point of (x1, y1) and an end point of (x2, y2).

```createRadialGradient(x1, y1, r1, x2, y2, r2)```  - Creates a radial gradient. The parameters represent two circles, one with its center at (x1, y1) and a radius of r1, and the other with its center at (x2, y2) with a radius of r2.

Once we've created a ```CanvasGradient``` object we can assign colors to it by using the ```addColorStop()``` method.

```gradient.addColorStop(position, color)``` - Creates a new color stop on the gradient object. The position is a number between 0.0 and 1.0 and defines the relative position of the color in the gradient, and the color argument must be a string representing a CSS ```<color>```, indicating the color the gradient should reach at that offset into the transition.

you can add as many color stops to a gradient as you need


## Patterns

Patterns are created using the ```createPattern()``` method

```createPattern(image, type)``` - Creates and returns a new canvas pattern object. image is a CanvasImageSource (that is, an HTMLImageElement, another canvas, a ```<video>```element, or the like. type is a string indicating how to use the image.

The following string values are used in the method
repeat - Tiles the image in both vertical and horizontal directions.

repeat-x - Tiles the image horizontally but not vertically.

repeat-y - Tiles the image vertically but not horizontally.

no-repeat - Doesn't tile the image. It's used only once.

## Shadows

There are four properties used to create shadows

```shadowOffsetX = float``` - Indicates the horizontal distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

```shadowOffsetY = float``` - Indicates the vertical distance the shadow should extend from the object. This value isn't affected by the transformation matrix. The default is 0.

```shadowBlur = float``` - Indicates the size of the blurring effect; this value doesn't correspond to a number of pixels and is not affected by the current transformation matrix. The default value is 0.

```shadowColor = color``` - A standard CSS color value indicating the color of the shadow effect; by default, it is fully-transparent black.

* When using fill (or clip and isPointinPath) you can optionally provide a fill rule algorithm by which to determine if a point is inside or outside a path and thus if it gets filled or not. This is useful when a path intersects itself or is nested.

2 values are used to determine if a point is inside or outside a path

1. "nonzero": The non-zero winding rule, which is the default rule.
1. "evenodd": The even-odd winding rule.

## Drawing Text

There are 2 methods to render text

```fillText(text, x, y [, maxWidth])``` - Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.

```strokeText(text, x, y [, maxWidth])``` - Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.


## Styling text

The following are ways to style text

**font = value** - The current text style being used when drawing text. This string uses the same syntax as the CSS font property. The default font is 10px sans-serif.

**textAlign = value** - Text alignment setting. Possible values: start, end, left, right or center. The default value is start.

**textBaseline = value** - Baseline alignment setting. Possible values: top, hanging, middle, alphabetic, ideographic, bottom. The default value is alphabetic.

**direction = value** - Directionality. Possible values: ltr, rtl, inherit. The default value is inherit.

```measureText()``` - Returns a TextMetrics object containing the width, in pixels, that the specified text will be when drawn in the current text style.


































https://deannaj401.github.io/reading-notes/