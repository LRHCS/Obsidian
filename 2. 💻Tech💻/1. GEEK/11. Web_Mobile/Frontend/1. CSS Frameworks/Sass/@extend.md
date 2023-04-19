The `@extend` directive lets you share a set of CSS properties from one selector to another.
```SCSS
.button-basic  {  border: none;  
  padding: 15px 30px;  
  text-align: center;  
  font-size: 16px;  
  cursor: pointer;}  
  
.button-report  {  @extend .button-basic;  
  background-color: red;}  
  
.button-submit  {  @extend .button-basic;  
  background-color: green;  
  color: white;}
	```