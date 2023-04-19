```js
const sizes = {

  width: window.innerWidth,

  height: window.innerHeight,

};

const camera = new THREE.PerspectiveCamera(
// fov
  80,
// size
  sizes.width / sizes.height,
// near
  0.1,
// far
  100

);

scene.add(camera);
camera.position.set(0, 0, 3);
camera.lookAt(mesh.position);
```