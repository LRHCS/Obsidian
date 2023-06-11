#Web  #html  

# Document
```html
<!DOCTYPE html>  
<html lang="en">  
<body>  
  
<h1>My First Heading</h1>  
<p>My first paragraph.</p>  
  
</body>  
</html>
```

# Heading
```html
<h1>hello</h1>
<h2>hello</h2>
<h3>hello</h3>
```
with  `style="font-size:1000px"` the heading will be bigger

# Paragraph
```html
<p>This is a paragraph.</p>  
<p>This is another paragraph.</p>
```

# Link
```html
<a href="https://www.w3schools.com">This is a link</a>
```

# Image
``` html
<img src="w3schools.jpg" alt="W3Schools.com" width="104" height="142">
```
src is the source file of the image, alt is when the file is broken, then it will show alt on the screen
## Absolute Link
it's like a url
> src="https://www.w3schools.com/images/img_girl.jpg"
## Relative Link
it's like a data source
>src="/images/img_girl.jpg".
# <br> Line break
with<br>
```html
<p>This is a <br> paragraph with a line break.</p>
```

# Style(normal with #CSS)
```html
<p style="color:red;">This is a red paragraph.</p>
```

# Title
the title with show when you hover the text
```html
<h2 title="I'm a header">The title Attribute</h2>

<p title="I'm a tooltip">Mouse over this paragraph, to display the title attribute as a tooltip.</p>
```

# <hr> Horizontal break
<hr> is a horizontal break.


# preformatived text
with pre it shows preformatted text, with `<p>` the html will delete the whitespace automaticlly

```html
<pre>  
  My Bonnie lies over the ocean.  
  
  My Bonnie lies over the sea.  
  
  My Bonnie lies over the ocean.  
  
  Oh, bring back my Bonnie to me.  
</pre>
```

# Some Text Formatting
-   `<b>` - Bold text
-   `<strong>` - Important text
-   `<i>` - Italic text
-   `<em>` - Emphasized text
-   `<mark>` - Marked text
-   `<small>` - Smaller text
-   `<del>` - Deleted text
-   `<ins>` - Inserted text
-   `<sub>` - Subscript text
-   `<sup>` - Superscript text
# Comment
```html
<!-- Write your comments here -->
```
with multiple lines
```html
<!--  
<p>Look at this cool image:</p>  
<img border="0" src="pic_trulli.jpg" alt="Trulli">  
-->
```

# Links
## Target attribute
-   `_self` - Default. Opens the document in the same window/tab as it was clicked
-   `_blank` - Opens the document in a new window or tab
-   `_parent` - Opens the document in the parent frame
-   `_top` - Opens the document in the full body of the window
```html
<a href="https://www.w3schools.com/" target="_blank">Visit W3Schools!</a>
```

## Image as links
```html
<a href="default.asp">  
<img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">  
</a>
```

## button as link
```html
<button onclick="document.location='https://www.w3schools.com/'">HTML Tutorial</button>
```
Here, an unvisited link will be green with no underline. A visited link will be pink with no underline. An active link will be yellow and underlined. In addition, when mousing over a link (a:hover) it will become red and underlined:
```html
<style>  
a:link {  
	color: green;  
	background-color: transparent;  
	text-decoration: none;
	}  


a:visited {  
	color: pink;  
	background-color: transparent;  
	text-decoration: none;
	}  


a:hover {  
	color: red;  
	background-color: transparent;  
	text-decoration: underline;
}  
  
a:active {  
	color: yellow;  
	background-color: transparent;  
	text-decoration: underline;
}  
</style>
```

## jump in the html
```html
<!DOCTYPE html>
<html>
<body>

<p><a href="#C4">Jump to Chapter 4</a></p>
<p><a href="#C10">Jump to Chapter 10</a></p>
<p><a href="#C1">Jump to Chapter 1</a></p>
<p><a href="#C23">Jump to 23</a><p>
<h2 id="#C1">Chapter 1</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 2</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 3</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C4">Chapter 4</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 5</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 6</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 7</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 8</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 9</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C10">Chapter 10</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 11</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 12</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 13</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 14</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 15</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 16</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 17</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 18</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 19</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 20</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 21</h2>
<p>This chapter explains ba bla bla</p>

<h2>Chapter 22</h2>
<p>This chapter explains ba bla bla</p>

<h2 id="C23">Chapter 23</h2>
<p>This chapter explains ba bla bla</p>

</body>
</html>
```
we use the id to create a bookmark

# Image
## Map
```html
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">  
  
<map name="workmap">  
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">  
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">  
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">  
</map>
```

## Background
```html
<style>  
body {  background-image: url('img_girl.jpg');}  
</style>
```
if you dont want it to repeat, write `background-repeat: no-repeat;`
```html
<style>  
body {  background-image: url('example_img_girl.jpg');  
  background-repeat: no-repeat;}  
</style>
```
cover will cover the entire element, fixed mean that the background dont move
```html
<style>  
body {  background-image: url('img_girl.jpg');  
  background-repeat: no-repeat;  
  background-attachment: fixed;  
  background-size: cover;}  
</style>
```

# Favicon
```html
<!DOCTYPE html>  
<html>  
<head>  
  <title>My Page Title</title>  
  <link rel="icon" type="image/x-icon" href="/images/favicon.ico">  
</head>  
<body>  
  
<h1>This is a Heading</h1>  
<p>This is a paragraph.</p>  
  
</body>  
</html>
```
it's the link behind title

# Tables
```html
<table>  
  <tr>  
    <th>Company</th>  
    <th>Contact</th>  
    <th>Country</th>  
  </tr>  
  <tr>  
    <td>Alfreds Futterkiste</td>  
    <td>Maria Anders</td>  
    <td>Germany</td>  
  </tr>  
  <tr>  
    <td>Centro comercial Moctezuma</td>  
    <td>Francisco Chang</td>  
    <td>Mexico</td>  
  </tr>  
</table>
```

colspan, the header will span over 2 or more cells
```html
<table>  
  <tr>  
    <th colspan="2">Name</th>  
    <th>Age</th>  
  </tr>  
  <tr>  
    <td>Jill</td>  
    <td>Smith</td>  
    <td>50</td>  
  </tr>  
  <tr>  
    <td>Eve</td>  
    <td>Jackson</td>  
    <td>94</td>  
  </tr>  
</table>
```

there is also rowspan
```html
<table>  
  <tr>  
    <th>Name</th>  
    <td>Jill</td>  
  </tr>  
  <tr>  
    <th rowspan="2">Phone</th>  
    <td>555-1234</td>  
  </tr>  
  <tr>  
    <td>555-8745</td>  
</tr>  
</table>
```

colgroup define the style of a group
```html
  
<table>  
  <colgroup>  
    <col span="2" style="background-color: #D6EEEE">  
  </colgroup>  
  <tr>  
    <th>MON</th>  
    <th>TUE</th>  
    <th>WED</th>  
    <th>THU</th>  
...
```


# List
## Unorded List
this is with dot, unorded List
```html
<ul style="list-style-type:disc;">  
  <li>Coffee</li>  
  <li>Tea</li>  
  <li>Milk</li>  
</ul>
```
there are some different list styles of unorded List
- disc
- circle
- square
- none
### Navbar
```html
<!DOCTYPE html>  
<html>  
<head>  
<style>  
ul {  list-style-type: none;  
  margin: 0;  
  padding: 0;  
  overflow: hidden;  
  background-color: #333333;}  
  
li {  float: left;}  
  
li a {  display: block;  
  color: white;  
  text-align: center;  
  padding: 16px;  
  text-decoration: none;}  
  
li a:hover {  background-color: #111111;}  
</style>  
</head>  
<body>  
  
<ul>  
  <li><a href="#home">Home</a></li>  
  <li><a href="#news">News</a></li>  
  <li><a href="#contact">Contact</a></li>  
  <li><a href="#about">About</a></li>  
</ul>  
  
</body>  
</html>
```
## Orded List
this is with number, orded List
```html
<ol>  
  <li>Coffee</li>  
  <li>Tea</li>  
  <li>Milk</li>  
</ol>
```
# Div
The `<div>` element is often used as a container for other HTML elements.
The `<div>` element has no required attributes, but `style`, `class` and `id` are common.
When used together with CSS, the `<div>` element can be used to style blocks of content:
```html
<div style="background-color:black;color:white;padding:20px;">  
  <h2>London</h2>  
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>  
</div>
```
defines a section in document(Block-Level)
# Span
```html
<p>My mother has <span style="color:blue;font-weight:bold">blue</span> eyes and my father has <span style="color:darkolivegreen;font-weight:bold">dark green</span> eyes.</p>
```
The `<span>` element is an inline container used to mark up a part of a text, or a part of a document.
The `<span>` element has no required attributes, but `style`, `class` and `id` are common.
When used together with CSS, the `<span>` element can be used to style parts of the text:
defines section in document(inline)

# Class
-   The HTML `class` attribute specifies one or more class names for an element
-   Classes are used by CSS and JavaScript to select and access specific elements
-   The `class` attribute can be used on any HTML element
-   The class name is case sensitive
-   Different HTML elements can point to the same class name
-   JavaScript can access elements with a specific class name with the `getElementsByClassName()` method

# Id
-     
    The `id` attribute is used to specify a unique id for an HTML element
-   The value of the `id` attribute must be unique within the HTML document
-   The `id` attribute is used by CSS and JavaScript to style/select a specific element
-   The value of the `id` attribute is case sensitive
-   The `id` attribute is also used to create HTML bookmarks
-   JavaScript can access an element with a specific id with the `getElementById()` method
# Head Element
in head contains metadata such as: title, style, meta, link, script...

title defines the title of the document

style is used for the css code

with link you can link your css stylesheet or the javascript code with you html

with meta you can define many things: character set, page description, keywords, author of the document, and viewport settings.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

# Layout