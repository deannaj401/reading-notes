# CSS Transforms

**transform syntax** - the transform property followed by the value. The value specifies the transform type followed by a specific amount inside parentheses

the following is a sample:

```div {```
  ```-webkit-transform: scale(1.5);```
     ```-moz-transform: scale(1.5);```
       ```-o-transform: scale(1.5);```
          ```transform: scale(1.5);```
```}```

## 2D transforms

* Two-dimensional transforms work on the x and y axes, known as horizontal and vertical axes.

### 2D Rotate

**rotate** - provides the ability to rotate an element from 0 to 360 degrees.
	* a positive value will rotate an element clockwise
	* a negative value will rotate an element counterclockwise
	* The default point of rotation is the center of the element, 50% 50%, both horizontally and vertically

Here is the HTML

```<figure class="box-1">Box 1</figure>```
```<figure class="box-2">Box 2</figure>```

Here is the CSS

```.box-1 {```
  ```transform: rotate(20deg);```
}
```.box-2 {```
  ```transform: rotate(-55deg);```
}

### 2D scale

**scale** - allows you to change the appeared size of an element.
	* the default scale value is 1
		* any value between .99 and .01 makes an element appear smaller while any value greater than or equal to 1.01 makes an element appear larger


Here is the HTML

```<figure class="box-1">Box 1</figure>```
```<figure class="box-2">Box 2</figure>```

Here is the CSS

```.box-1 {```
  ```transform: scale(.75);```
}
```.box-2 {```
  ```transform: scale(1.25);```
}

* It is possible to scale only the height or width of an element using the scaleX and scaleY values.
	* The scaleX value will scale the width of an element 
	* the scaleY value will scale the height of an element
	* To scale both the height and width of an element but at different sizes, the x and y axis values may be set simultaneously. To do so, use the scale transform declaring the x axis value first, followed by a comma, and then the y axis value.

HTML

```<figure class="box-1">Box 1</figure>```
```<figure class="box-2">Box 2</figure>```
```<figure class="box-3">Box 3</figure>```

CSS

```.box-1 {```
  ```transform: scaleX(.5);```
}
```.box-2 {```
  ```transform: scaleY(1.15);```
}
```.box-3 {```
  ```transform: scale(.5, 1.15);```
}

### 2D Translate

**translate** - works like relative positioning, pushing and pulling an element in different directions without interrupting the normal flow of the document.

	* translateX - changes the position of an element on the horizontal axis
	* translateY - changes the position of an element on the vertical axis
	* to set both x and y axis values at once use the translate value and declare the x axis value first followed by a comma and then the y axis value.
	
	* The distance values used within the translate value may be any general length measurement, most commonly pixels or percentages
		* Positive values will push an element down and to the right of its default position 
		* Negative values will pull an element up and to the left of its default position.



### 2D Skew

**skew** - used to distort elements on the horizontal axis, vertical axis or both. 
	* skewX value distorts an element on the horizontal axis
	* skewY value distorts an element on the vertical axis
	* To distort an element on both axes the skew value is used, declaring the x axis value first, followed by a comma, and then the y axis value
	* he distance calculation of the skew value is measured in units of degrees NOT pixels or percentages
	


Multiple transforms must be used at once.
	* To combine transforms, list the transform values within the transform property one after the other without the use of commas
	* Using multiple transform declarations will not work, as each declaration will overwrite the one above it.
	


The following is a code to make a cube



### Transform Origin

**transform origin** - dead center of an element both 50% horizontally and 50% vertically. The **transform-orgin** property is used to change this

* The transform-origin property can accept one or two values. When only one value is specified, that value is used for both the horizontal and vertical axes. If two values are specified, the first is used for the horizontal axis and the second is used for the vertical axis.



### Perspective

**perspective value** - applying the perspective property to a parent element transforms a group of element all with the same perspective.



* The perspective value can be set as none or a length measurement
	* The none value turns off any perspective
	* length value will set the depth of the perspective
	
To make an object 3D you use the above transforms but add the z axis
except for skew which cannot be used in 3D
If you don't want to see the back of an object set the backface visibilty to hidden. visible is the default

# Transitions and Animations

for a transition to take place, an element must have a change in state, and different styles must be identified for each state. The easiest way for determining styles for different states is by using the :hover, :focus, :active, and :target pseudo-classes.

There are 4 transition related properties
	1. transition-property
	1. transition-duration
	1. transition-timing-function
	1. transition-delay
	
* The **transition-property** property determines exactly what properties will be altered in conjunction with the other transitional properties. By default, all of the properties within an element’s different states will be altered upon change. However, only the properties identified within the transition-property value will be affected by any transitions.

* If multiple properties need to be transitioned they may be comma separated within the transition-property value. Additionally, the keyword value all may be used to transition all properties of an element.

* not all properties can be transitioned. Only those that have an identifiable halfway point. 
	1. colors, font sizes etc can be transitioned
	1. display property etc can not be 
	
**Transition duration** - The value of this property can be set using general timing values, including seconds (s) and milliseconds (ms). These timing values may also come in fractional measurements

When transitioning multiple properties you can set multiple durations, one for each property. As with the transition-property property value, multiple durations can be declared using comma separated values. The order of these values when identifying individual properties and durations does matter. For example, the first property identified within the transition-property property will match up with the first time identified within the transition-duration property, and so forth.

**Transition-timing**

* The transition-timing-function property is used to set the speed in which a transition will move. 

*keyword values for the transition-timing property**
* linear - identifies a transition moving in a constant speed from one state to another
* ease-in - identifies a transition that starts slowly and speeds up throughout the transition,
* ease-out - dentifies a transition that starts quickly and slows down throughout the transition.
* ease-in-out - identifies a transition that starts slowly, speeds up in the middle, then slows down again before ending.

* Each timing function has a cubic-bezier curve behind it, which can be specifically set using the cubic-bezier(x1, y1, x2, y2) value. Additional values include step-start, step-stop, and a uniquely identified steps(number_of_steps, direction) value.

**Transition Delay** 

sets a time value, seconds or milliseconds, that determines how long a transition should be stalled before executing

To set numerous transitions at once, set each individual group of transition values, then use a comma to separate each additional group of transition values.

### Animations

To set multiple points at which an element should undergo a transition, use the @keyframes rule. The @keyframes rule includes the animation name, any animation breakpoints, and the properties intended to be animated.

*The @keyframes rule must be vendor prefixed, just like all of the other transition and animation properties*

only individual properties may be animated

**animation-name** - the property value used in the @keyframes rule that assigns a name to an element

**animation-duration - sets the length of the animation in seconds**

The other animation properties are
timing function delay

By default, animations run their cycle once from beginning to end and then stop. To have an animation repeat itself numerous times the animation-iteration-count property may be used. Values for the animation-iteration-count property include either an integer or the infinite keyword. Using an integer will repeat the animation as many times as specified, while the infinite keyword will repeat the animation indefinitely in a never ending fashion.

On top of being able to set the number of times an animation repeats, you may also declare the direction an animation completes using the animation-direction property. Values for the animation-direction property include normal, reverse, alternate, and alternate-reverse.


The animation-play-state property allows an animation to be played or paused using the running and paused keyword values respectively. When you play a paused animation, it will resume running from its current state rather than starting from the very beginning again.

he animation-fill-mode property identifies how an element should be styled either before, after, or before and after an animation is run. The animation-fill-mode property accepts four keyword values, including none, forwards, backwards, and both.


























https://deannaj401.github.io/reading-notes/