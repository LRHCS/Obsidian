```js
// Search in the HTML file webgl class
const canvas = document.querySelector(".webgl");

const renderer = new THREE.WebGLRenderer({

  canvas: canvas,

});

renderer.setSize(sizes.width, sizes.height);
```