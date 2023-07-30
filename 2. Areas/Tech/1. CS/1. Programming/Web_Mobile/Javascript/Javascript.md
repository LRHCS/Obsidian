# Basic
```javascript
let name = prompt("What's your name", "LUL");

let flag = confirm("So your name is this");

let res = flag ? alert(`Hello ${name}`) : prompt("What's your name", "LUL");

// Infinite Loop
for (;;){
	// some code
}

// Default Parameter, the another parameter can also be a function
function showMessage(from = "Annonymus", text = "no text given") {

  alert(from + ": " + text);

}

// Object
for(let key in obj){
	alert(key);
	alert(obj[key])
}

// Numbers----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
alert( parseInt('100px') ); // 100 
alert( parseFloat('12.5em') ); // 12.5 
alert( parseInt('12.3') ); // 12, only the integer part is returned 
alert( parseFloat('12.3.4') ); // 12.3, the second point stops the reading
let num = 12.36; 
alert( num.toFixed(1) ); // "12.4"
alert(Math.round(num));
alert(isFinite(num));
// Strings----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
// only works for ``
let guestList = `Guests: 
* John 
* Pete 
* Mary `;
// is the same as
let guestList = "Guests:\n * John\n * Pete\n * Mary";

```
![[Pasted image 20230324202825.png]]
```javascript
// the first character 
alert( str[0] ); // H 
alert( str.at(0) ); // H 
// the last character 
alert( str[str.length - 1] ); // o
alert( str.at(-1) );
for (let char of "Hello") { 
	alert(char); // H,e,l,l,o (char becomes "H", then "e", then "l" etc) 
}
// find substring in a string
let str = "As sly as a fox, as strong as an ox"; let target = "as"; _let pos = -1; while ((pos = str.indexOf(target, pos + 1)) != -1) { alert( pos ); }_

let arr = ["Apple", "Orange", "Pear"];

for (let key in arr) {
  alert( arr[key] ); // Apple, Orange, Pear
}
// iterates over array elements
for (let fruit of fruits) {
  alert( fruit );
}
let arr = ["I", "study", "JavaScript"];

arr.splice(1, 1); // from index 1 remove 1 element

alert( arr ); // ["I", "JavaScript"]
// remove 2 first elements
let removed = arr.splice(0, 2);

alert( removed ); // "I", "study" <-- array of removed elements

let arr = [1, 2];

// create an array from: arr and [3,4]
alert( arr.concat([3, 4]) ); // 1,2,3,4

// create an array from: arr and [3,4] and [5,6]
alert( arr.concat([3, 4], [5, 6]) ); // 1,2,3,4,5,6

// create an array from: arr and [3,4], then add values 5 and 6
alert( arr.concat([3, 4], 5, 6) ); // 1,2,3,4,5,6

arr.forEach(function(item, index, array) {
  // ... do something with item
});

let result = arr.map(function(item, index, array) {
  // returns the new value instead of item
});
let names = 'Bilbo, Gandalf, Nazgul';

let arr = names.split(', ');

for (let name of arr) {
  alert( `A message to ${name}.` ); // A message to Bilbo  (and other names)
}

// Rest parameters, ...args should be at the last position at the argument
function sumAll(...args) { // args is the name for the array
  let sum = 0;

  for (let arg of args) sum += arg;

  return sum;
}

// Spread expression
let arr = [3, 5, 1];
let arr2 = [8, 9, 15];

let merged = [0, ...arr, 2, ...arr2];

function camelize(str) {
  return str
    .split('-') // splits 'my-long-word' into array ['my', 'long', 'word']
    .map(
      // capitalizes first letters of all array items except the first one
      // converts ['my', 'long', 'word'] into ['my', 'Long', 'Word']
      (word, index) => index == 0 ? word : word[0].toUpperCase() + word.slice(1)
    )
    .join(''); // joins ['my', 'Long', 'Word'] into 'myLongWord'
}
```
![[Pasted image 20230327205903.png]]
![[Pasted image 20230327205911.png]]


---
# Dom
## Document
```javascript
for (let node of document.body.childNodes) {
  alert(node); // shows all nodes from the collection
}

let elem = document.getElementById('elem');_ 
// make its background red 
elem.style.background = 'red';
let elements = document.querySelectorAll('ul > li:last-child');
for (let elem of elements) { 
	alert(elem.innerHTML); // "test", "passed" 
}
for (let elem of document.body.children) { 
	if (elem.matches('a[href$="zip"]')) {
		alert("The archive reference: " + elem.href ); 
	} 
}
// Pure Text Content
alert(news.textContent);
// Insertion
<ol id="ol"><li>0</li><li>1</li><li>2</li></ol>
<script>
  ol.before('before'); // insert string "before" before <ol>
  ol.after('after'); // insert string "after" after <ol>

  let liFirst = document.createElement('li');
  liFirst.innerHTML = 'prepend';
  ol.prepend(liFirst); // insert liFirst at the beginning of <ol>

  let liLast = document.createElement('li');
  liLast.innerHTML = 'append';
  ol.append(liLast); // insert liLast at the end of <ol>
</script>
```
![[Pasted image 20230327220414.png]]
```javascript
// CSS Property
document.body.style.margin = '20px';
document.body.style.color
// Sizes
// With Scrollbar
window.innerWidth/innerHeight
// Without
document.documentElement.clientWidth/clientHeight
// Scroll
alert('Current scroll from the top: ' + window.pageYOffset); 
alert('Current scroll from the left: ' + window.pageXOffset);
```

## Events
