```js
// Init
const gui = new dat.GUI({ closed: false, width: 400 });
// Create a Folder
const cube1Folder = gui.addFolder("Cube1");

//  add in this Folder some debug thing(Position, visible, wireframe...)
cube1Folder

  .add(cube1.position, "x")

  .min(-1.5)

  .max(3)

  .step(0.01)

  .name("change x");

cube1Folder.add(cube1.position, "y").min(-3).max(3).step(0.01).name("change y");

cube1Folder.add(cube1.position, "z").min(-3).max(3).step(0.01).name("change z");

cube1Folder.add(cube1, "visible");

cube1Folder.add(cube1.material, "wireframe");
```