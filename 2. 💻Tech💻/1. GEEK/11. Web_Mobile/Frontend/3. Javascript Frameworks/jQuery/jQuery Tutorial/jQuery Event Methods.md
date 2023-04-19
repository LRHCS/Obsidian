#jquery
jQuery is tailor-made to respond to events in an HTML page.

---

## What are Events?

All the different visitors' actions that a web page can respond to are called events.

An event represents the precise moment when something happens.

Examples:

-   moving a mouse over an element
-   selecting a radio button
-   clicking on an element

The term **"fires/fired"** is often used with events. Example: "The keypress event is fired, the moment you press a key".

Here are some common DOM events:

![[Pasted image 20220214213257.png]]

## jQuery Syntax For Event Methods

In jQuery, most DOM events have an equivalent jQuery method.

To assign a click event to all paragraphs on a page, you can do this:
```javascript
$("p").click();
```


The next step is to define what should happen when the event fires. You must pass a function to the event:
```javascript
$("p").click(function(){  
  // action goes here!!  
});
```

  

---

---

## Commonly Used jQuery Event Methods

**$(document).ready()**

The `$(document).ready()` method allows us to execute a function when the document is fully loaded. This event is already explained in the [jQuery Syntax](https://www.w3schools.com/jquery/jquery_syntax.asp) chapter.

**click()**

The `click()` method attaches an event handler function to an HTML element.

The function is executed when the user clicks on the HTML element.

The following example says: When a click event fires on a `<p>` element; hide the current `<p>` element:

### Example
```javascript
$("p").click(function(){  
  $(this).hide();  
});
```
**dblclick()**

The `dblclick()` method attaches an event handler function to an HTML element.

The function is executed when the user double-clicks on the HTML element:

### Example

$("p").dblclick(function(){  
  $(this).hide();  
});

**mouseenter()**

The `mouseenter()` method attaches an event handler function to an HTML element.

The function is executed when the mouse pointer enters the HTML element:

### Example

$("#p1").mouseenter(function(){  
  alert("You entered p1!");  
});


**mouseleave()**

The `mouseleave()` method attaches an event handler function to an HTML element.

The function is executed when the mouse pointer leaves the HTML element:

### Example

$("#p1").mouseleave(function(){  
  alert("Bye! You now leave p1!");  
});

**mousedown()**

The `mousedown()` method attaches an event handler function to an HTML element.

The function is executed, when the left, middle or right mouse button is pressed down, while the mouse is over the HTML element:

### Example

$("#p1").mousedown(function(){  
  alert("Mouse down over p1!");  
});

**mouseup()**

The `mouseup()` method attaches an event handler function to an HTML element.

The function is executed, when the left, middle or right mouse button is released, while the mouse is over the HTML element:

### Example

$("#p1").mouseup(function(){  
  alert("Mouse up over p1!");  
});

**hover()**

The `hover()` method takes two functions and is a combination of the `mouseenter()` and `mouseleave()` methods.

The first function is executed when the mouse enters the HTML element, and the second function is executed when the mouse leaves the HTML element:

### Example

$("#p1").hover(function(){  
  alert("You entered p1!");  
},  
function(){  
  alert("Bye! You now leave p1!");  
});

**focus()**

The `focus()` method attaches an event handler function to an HTML form field.

The function is executed when the form field gets focus:

### Example

$("input").focus(function(){  
  $(this).css("background-color", "#cccccc");  
});



**blur()**

The `blur()` method attaches an event handler function to an HTML form field.

The function is executed when the form field loses focus:

### Example

$("input").blur(function(){  
  $(this).css("background-color", "#ffffff");  
});

## The on() Method

The `on()` method attaches one or more event handlers for the selected elements.

Attach a click event to a `<p>` element:

### Example

$("p").on("click", function(){  
  $(this).hide();  
});

Attach multiple event handlers to a `<p>` element:

### Example

$("p").on({  
  mouseenter: function(){  
    $(this).css("background-color", "lightgray");  
  },  
  mouseleave: function(){  
    $(this).css("background-color", "lightblue");  
  },  
  click: function(){  
    $(this).css("background-color", "yellow");  
  }  
});

Note: in the () can also write slow
![[Pasted image 20220214214216.png]]