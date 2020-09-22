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
> Graphic design - print, Visual designer - UI, and Web designer is a 
<!--stackedit_data:
eyJoaXN0b3J5IjpbNzg0NDg1NjEzLDYyOTgxOTUxMCw1MDE0Nj
cyMTgsLTMxMjkyMzk4MCwxNDA3Njg4OTg0LDczODQ4MzY5Niwt
MTY4Nzg2ODI0MywxNDEwNzQ1OTkzLC05OTY2OTUwNzMsLTU5Mz
MzNzY3NF19
-->