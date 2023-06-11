#CSS #programming_lang r    

# CSS
3 ways to add in the html
-   **Inline** - by using the `style` attribute inside HTML elements
-   **Internal** - by using a `<style>` element in the `<head>` section
-   **External** - by using a `<link>` element to link to an external CSS file

## background color
```Html
<body style="background-color:powderblue;">  
  
<h1>This is a heading</h1>  
<p>This is a paragraph.</p>  
  
</body>
```

## Text color
```html
<h1 style="color:blue;">This is a heading</h1>  
<p style="color:red;">This is a paragraph.</p>
```

## Fonts
```html
<h1 style="font-family:verdana;">This is a heading</h1>  
<p style="font-family:courier;">This is a paragraph.</p>
```

## Text size
```html
<h1 style="font-size:300%;">This is a heading</h1>  
<p style="font-size:160%;">This is a paragraph.</p>
```
## Text Alignment
```html
<h1 style="text-align:center;">Centered Heading</h1>  
<p style="text-align:center;">Centered paragraph.</p>
```

##  Border
css defines a border around the html element
```css
p {  
	border: 2px solid powderblue;
}
```

##  Padding
space between the text and the border

```css
p {  
	border: 2px solid powderblue;  
	padding: 30px;
  }
```

##  Margin
  
space outside the border.

```css
p {  
	border: 2px solid powderblue;  
	margin: 50px;
}
```