#jquery
With jQuery you select (query) HTML elements and perform "actions" on them.

---

## jQuery Syntax

The jQuery syntax is tailor-made for **selecting** HTML elements and performing some **action** on the element(s).

Basic syntax is: **$(_selector_)._action_()**

-   A $ sign to define/access jQuery
-   A (_selector_) to "query (or find)" HTML elements
-   A jQuery _action_() to be performed on the element(s)

Examples:

`$(this).hide()` - hides the current element.

`$("p").hide()` - hides all p elements.

`$(".test").hide()` - hides all elements with class="test".

`$("#test").hide()` - hides the element with id="test".

## The Document Ready Event

You might have noticed that all jQuery methods in our examples, are inside a document ready event:
```javascript
$(document).ready(function(){  
  
  _// jQuery methods go here..._  
  
});

```


This is to prevent any jQuery code from running before the document is finished loading (is ready).

It is good practice to wait for the document to be fully loaded and ready before working with it. This also allows you to have your JavaScript code before the body of your document, in the head section.

Here are some examples of actions that can fail if methods are run before the document is fully loaded:

-   Trying to hide an element that is not created yet
-   Trying to get the size of an image that is not loaded yet

**Tip:** The jQuery team has also created an even shorter method for the document ready event:
```javascript
$(function(){  
  
  _// jQuery methods go here..._  
  
});
```

Use the syntax you prefer. We think that the document ready event is easier to understand when reading the code.