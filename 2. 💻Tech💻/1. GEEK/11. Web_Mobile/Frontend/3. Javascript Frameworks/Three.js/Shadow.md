To see the shadow , we need to enable shadow map in the renderer
```js
const canvas = document.querySelector(".webgl");

const renderer = new THREE.WebGLRenderer({

  canvas: canvas,

});

renderer.setSize(sizes.width, sizes.height);

renderer.shadowMap.enabled = true;
```

Then we need to let our objects to receive shadows and cast shadows
```js
const cube = new THREE.Mesh(new THREE.BoxGeometry(1, 1, 1, 2, 2, 2), material);
// Cast shadow
cube.castShadow = true;
const torus = new THREE.Mesh(
  new THREE.TorusGeometry(0.5, 0.3, 64, 64),
  material
);
// Cast shadow
torus.castShadow = true;
const sphere = new THREE.Mesh(new THREE.SphereGeometry(0.7, 32, 16), material);
// Cast shadow
sphere.castShadow = true;
const plane = new THREE.Mesh(new THREE.PlaneGeometry(8, 8), material);
// Receive shadow
plane.receiveShadow = true;


const spotLight = new THREE.SpotLight(0xffffff, 0.6);
spotLight.position.set(0, 4, 3);
scene.add(spotLight);
// Cast shadow
spotLight.castShadow = true;
// We can do this to make the Shadow smoother
spotLight.shadow.mapSize.width = 1024 * 20;
spotLight.shadow.mapSize.height = 1024 * 20;
```