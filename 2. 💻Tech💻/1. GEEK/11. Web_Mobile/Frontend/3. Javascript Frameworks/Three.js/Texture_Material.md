# Types of Textures
## Color(Albedo)
- Applied on the geometry
- Most simple one

## Alpha
- Grayscale Image
- White is visible
- Black invisible

## Height
- Grayscale Image
- Move the verticies to create some relief
- Need enough subdivisions

## Normal
- add details(about light)
- Doesn't need subdivisions
- verticies won't move
- Better Performence

## Ambient Occulusion
- Grayscale
- Fake shadowNot physically accurate
- Helps to create contrast

## Metallic
- Reflection
- White is metall, black not

## Roughness
- Grayscale image
- White is rough, black not

## Using


```js
const image = new Image();
const texture = new THREE.Texture(image);
image.onload = () => {
  texture.needsUpdate = true;
};

image.src = "/textures/color.jpg";

const cube1 = new THREE.Mesh(
  new THREE.BoxGeometry(1, 1, 1, 2, 2, 2),
  new THREE.MeshBasicMaterial({ map: texture })
);

// easier version
const textureLoader = new THREE.TextureLoader();
const texture = textureLoader.load(
  "./textures/color.jpg",
  () => {
    console.log("Loading");
  },
  () => {
    console.log("Progress");
  },
  () => {
    console.log("error");
  }
);
const cube1 = new THREE.Mesh(
  new THREE.BoxGeometry(1, 1, 1, 2, 2, 2),
  new THREE.MeshBasicMaterial({ map: texture })
);
```


# Materials

## MeshBasicMaterial
```js
const material = new THREE.MeshBasicMaterial();
material.wireframe = true;
material.map = colorTexture;
material.color = new THREE.Color("green");
material.transparent = true;
material.opacity = 0.5;
material.alphaMap = alphaTexture;
material.side = THREE.DoubleSide;
```

## MeshNormalMaterial
```js
const material = new THREE.MeshNormalMaterial();

material.flatShading = true;
```

## MeshDepthMaterial

```js
const material = new THREE.MeshDepthMaterial();
```


## MeshLambertMaterial
```js
const material = new THREE.MeshLambertMaterial();
```

## MeshPhongMaterial
```js
const material = new THREE.MeshPhongMaterial();
material.shininess = 100;
material.specular = new THREE.Color(0x1188ff);
```

## MeshToonMaterial
```js
const material = new THREE.MeshToonMaterial();
```

## !MeshStandardMaterial(Here you can apply all of the textures)
```js
const material = new THREE.MeshStandardMaterial();
material.metalness = 0;
material.roughness = 1;
material.map = colorTexture;
material.aoMap = ambientOcculusionTexture;
material.aoMapIntensity = 1;
material.displacementMap = heightTexture;
material.displacementScale = 0.05;
material.metalnessMap = metalnessTexture;
material.roughnessMap = roughnessTexture;
material.normalMap = normalTexture;
material.normalScale.set(0.5, 0.5);
material.transparent = true;
material.alphaMap = alphaTexture;
```