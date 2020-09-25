# Responsive Web design

### Basic HTML and HTML5
- h1, h2, h3, .. => Different __levels__ of headings
- HTML5 introduces more descriptive tags - main, header, footrt, nav, article, section, video, etc. These also help with __SEO__
- img tag is __self closing__
- We can use anchor tag to create __internal links__ as well. We use __href="#id"__ in that case
- __href ="#"__ creates a dead link
- _required_ is a __boolean attribute__
-  Forms:
	- _for_ of the label should match with the _id_ of the input. Also, using same 	_name_ attribute creates a __radio group__
	- Radio buttons are generally used for single answer and checkboxes for multi correct questions
	- _name, value_ get submitted at the end. The default value is _on_. We generally use the lowercase version of label as value
	- _checked_ boolean attribute can be used to have inputs checked by default
- div => division element 
---
### Basic CSS

> The idea behind CSS is that you can use a selector to target an HTML element in the DOM and then apply a variety of attributes to that element to change the way it is displayed on the page.
- It is a good practice to end inline style declarations with a "__;__"
- font family names should be wrapped in quotes if they contain space
- fonts __degrade/fallback__ in the order from left to right. 
- All html elements are essentially little rectangles.
- margins can also be negative!
- __[attr=value]__ : attribute selector
- Relative Units:
	- __%__ : generally corresponds to respective parent attribute. For example, if you set an element's font-size as a percentage it will be a percentage of the font-size of the element's parent. If you use a percentage for a width value, it will be a percentage of the width of the parent
	- __em__ : Font size of the parent, in the case of typographical properties like font-size, and font size of the element itself, in the case of other properties like width
	- __rem__ : Font size of the root element
	- __vw__ : 1% of the viewport's width
	- __vh__ : 1% of the viewport's height
- !important syntax :  __attr: value !important;__
- Declaring variables: __- -name: value;__ Using them: __attr: var(- -name, fallback-value);__
- To make use of variable inheritance, CSS variables are often defined in the __:root__ element. It is a pseudo-class selector that matches the root element of the document, usually the html element
---
### Applied Visual Design
> Graphic design - print, Visual designer - UI, and Web design is a subset of visual design.
- __text-align: justify;__ => causes all lines of text except the last line to meet the left and right edges of the line box.
-  With the __strong tag__, the browser applies the CSS of __font-weight: bold;__ to the element.
- With the __u tag__, the browser applies the CSS of __text-decoration: underline;__ to the element.
-  With the __s tag__, the browser applies the CSS of __text-decoration: line-through;__ to the element.
- The __box-shadow__ CSS property adds shadow effects around an element's frame. You can set multiple effects separated by commas. A box shadow is described by X and Y offsets relative to the element, blur and spread radius, and color.
- The __line-height__ CSS property sets the height of a line box. It's commonly used to set the distance between lines of text.
- __positioning elements__:
	- __position: relative__: Doesnot take it out of flow. Relative to it's current position in the normal flow
	
	![GIF showing the CSS offsets](https://cdn-media-1.freecodecamp.org/imgr/eWWi3gZ.gif)
	- __position: absolute__: Remove the element from normal flow. Element will be locked relative to its closest _positioned_ ancestor. So, generally the parent is made _relative_
	- __position: fixed__: One key difference between the fixed and absolute positions is that an element with a fixed position won't move when the user scrolls
	- __Floating elements__ are removed from the normal flow of a document and pushed to either the left or right of their containing parent element. It's commonly used with the __width__ property to specify how much horizontal space the floated element requires
	- __z-index__ property can specify the order of how elements are stacked on top of one another. It must be an integer, and higher values for the z-index property of an element move it higher in the stack than those with lower values
	- __margin: auto__ works only for block level elements. So to center images, we have to first use __display: block;__
- __Color Theory__:
	> The color wheel is a useful tool to visualize how colors relate to each other - it's a circle where similar hues are neighbors and different hues are farther apart. When two colors are opposite each other on the wheel, they are called complementary colors. They have the characteristic that if they are combined, they "cancel" each other out and create a gray color. However, when placed side-by-side, these colors appear more vibrant and produce a strong visual contrast
	
	- __Tertiary colors__ are the result of combining a primary color with one of its secondary color neighbors
	- __Hue__ is what people generally think of as 'color'. If you picture a spectrum of colors starting with red on the left, moving through green in the middle, and blue on right, the hue is where a color fits along this line. In hsl(), hue uses a color wheel concept instead of the spectrum, where the angle of the color on the circle is given as a value between 0 and 360.
	- __Saturation__ is the amount of gray in a color. A fully saturated color has no gray in it, and a minimally saturated color is almost completely gray. This is given as a percentage with 100% being fully saturated
	- __Lightness__ is the amount of white or black in a color. A percentage is given ranging from 0% (black) to 100% (white), where 50% is the normal color
	- __background: linear-gradient(gradient_direction, color 1, color 2, color 3, ...);__ - The first argument specifies the direction from which color transition starts - it can be stated as a degree, where 90deg makes a vertical gradient and 45deg is angled like a backslash. The following arguments specify the order of colors used in the gradient.
- __Transform, Transition, and Animations__:
	- Applying a transform to a div element will also affect any child elements contained in the div
	- The __animation properties__ control how the animation should behave and the __@keyframes__ rule controls what happens during that animation. @keyframes is how to specify exactly what happens within the animation over the duration. This is done by giving CSS properties for specific "frames" during the animation, with percentages ranging from 0% to 100%
	- __animation-fill-mode: forwards;__ - The animation-fill-mode specifies the style applied to an element when the animation has finished
	- __animation-iteration-count: infinite__ - Animate elements continually
	- __animation-timing-function__ - The default value is ease, which starts slow, speeds up in the middle, and then slows down again in the end. Other options include ease-out, which is quick in the beginning then slows down, ease-in, which is slow in the beginning, then speeds up at the end, or linear, which applies a constant animation speed throughout
	- __animation-timing-function: cubic-bezier(x1, y1, x2, y2)__ - The cubic-bezier function consists of four main points that sit on this 1 by 1 grid: p0, p1, p2, and p3. p0 and p3 are set for you - they are the beginning and end points which are always located respectively at the origin (0, 0) and (1, 1). You set the x and y values for the other two points, and where you place them in the grid dictates the shape of the curve for the animation to follow. This is done in CSS by declaring the x and y values of the p1 and p2 "anchor" points in the form: (x1, y1, x2, y2)