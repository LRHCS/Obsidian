#jquery
 jQuery selectors are one of the most important parts of the jQuery library.

---

## jQuery Selectors

jQuery selectors allow you to select and manipulate HTML element(s).

jQuery selectors are used to "find" (or select) HTML elements based on their name, id, classes, types, attributes, values of attributes and much more. It's based on the existing [CSS Selectors](https://www.w3schools.com/cssref/css_selectors.asp), and in addition, it has some own custom selectors.

All selectors in jQuery start with the dollar sign and parentheses: $().

---

## The element Selector

The jQuery element selector selects elements based on the element name.

You can select all `<p>` elements on a page like this:

$("p")

**Example**

When a user clicks on a button, all `<p>` elements will be hidden:

### Example
```javascript
$(document).ready(function(){  
  $("button").click(function(){  
    $("p").hide();  
  });  
});
```

## The id Selector

The jQuery `#_id_` selector uses the id attribute of an HTML tag to find the specific element.

An id should be unique within a page, so you should use the id selector when you want to find a single, unique element.

To find an element with a specific id, write a hash character, followed by the id of the HTML element:

$("#test")

**Example**

When a user clicks on a button, the element with id="test" will be hidden:

### Example
```javascript
$(document).ready(function(){  
  $("button").click(function(){  
    $("#test").hide();  
  });  
});
```

## The .class Selector

The jQuery `_.class_` selector finds elements with a specific class.

To find elements with a specific class, write a period character, followed by the name of the class:

$(".test")

**Example**

When a user clicks on a button, the elements with class="test" will be hidden:

### Example
```javascript
$(document).ready(function(){  
  $("button").click(function(){  
    $(".test").hide();  
  });  
});
```
![[Pasted image 20220214213051.png]]