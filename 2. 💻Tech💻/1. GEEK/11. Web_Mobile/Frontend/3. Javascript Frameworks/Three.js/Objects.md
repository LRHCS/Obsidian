# Init a Object
```js
const cube1 = new THREE.Mesh(
  new THREE.BoxGeometry(1, 1, 1, 2, 2, 2),
  new THREE.MeshBasicMaterial({ color: 'red' })
);

// or

const Geometry =  new THREE.BoxGeometry(1, 1, 1, 2, 2, 2);
const Material = new THREE.MeshBasicMaterial({ color: 'red' })
const cube1 = new THREE.Mesh(Geometry, Material)
```


# Position
```js
cube1.position.set(1.5, 0, 0);

// =

cube1.position.x = 1.5
cube1.position.y = 0
cube1.position.z = 0

```


# Scale
```js
// Increase the size
mesh.scale.set(2, 0.5, 0.5);
```

# Rotation

```js
// Rotation
mesh.rotation.reorder("XYZ");
mesh.rotation.set(1, 2, 3);
```

# Group
```js
// Init a new group and add objects in there, the changes on the group will affect all objects in there
const group = new THREE.Group();
scene.add(group);

  

group.add(cube1);
group.add(cube2);
group.add(cube3);
```

# Animate
```js
const clock = new THREE.Clock();
function animate() {

  const elaspedTime = clock.getElapsedTime();

  cube1.rotation.x += 0.01;

  cube1.position.y = Math.sin(elaspedTime);

  cube2.rotation.y += 0.01;

  cube2.position.y = Math.cos(elaspedTime);

  cube3.rotation.z += 0.01;

  cube3.position.y = Math.sin(elaspedTime);

  
  // render the scence
  renderer.render(scene, camera);
  // Capture each frame
  requestAnimationFrame(animate);

}
  

animate();
```

# Controlls
```js
const controls = new OrbitControls(camera, canvas);
```