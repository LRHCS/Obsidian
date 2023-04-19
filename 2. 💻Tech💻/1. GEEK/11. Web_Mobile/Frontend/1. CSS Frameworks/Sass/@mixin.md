The `@mixin` directive lets you create CSS code that is to be reused throughout the website. 
```scss
@mixin important-text {
  color: red;
  font-size: 25px;
  font-weight: bold;
  border: 1px solid blue;
}

.danger {
  @include important-text;
  background-color: green;
}                  
```
@mixin is like a function of a css code
```scss
@mixin transform($property) {  -webkit-transform: $property;  
  -ms-transform: $property;  
  transform: $property;}  
  
.myBox {  @include transform(rotate(20deg));}
```