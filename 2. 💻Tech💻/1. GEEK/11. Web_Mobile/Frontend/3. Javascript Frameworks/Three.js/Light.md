**The Lights cost a lot of performences, so use the *baking* in 3D-Software instead**
# AmbientLight
```js
const ambientLight = new THREE.AmbientLight(0xffffff, 0.5);

scene.add(ambientLight);
```

# DirectionalLight
- sun like 
```js
const directionalLight = new THREE.DirectionalLight(0x00fffc, 0.3);

scene.add(directionalLight);

// change the direction of the light

directionalLight.position.set(1,0.25,0);
	```

# HemisphereLight
- The Light of the first color is coming from up(*skyColor*), the second value from the downside(*groundColor*)
- In between there are mix color
```js
const hemisphereLight = new THREE.HemisphereLight(0xff0000, 0x0000ff, 0.3);

scene.add(hemisphereLight);
```

# PointLight
```js
// the third value is the distance of the light, fourth is the time it will decay
const pointLight = new THREE.PointLight(0xff9000, 0.5,100,1);

scene.add(pointLight);

// position
pointLight.position.set(1, -0.5, 1);
```

# RectAreaLight
```js
// The Third value is width and the forth height 
const rectAreaLight = new THREE.RectAreaLight(0x4e00ff, 2, 1, 3);

scene.add(rectAreaLight);
```

# SpotLight

```js
const spotLight = new THREE.SpotLight(
0x78ff00,
0.5,
// distance
10,
// angle
Math.PI * 0.1
,
// penumbra
0.25,
// decay
1
);

spotLight.position.set(0, 2, 3);

scene.add(spotLight);
```

# Helper

```js
const hemisphereLightHelper = new THREE.HemisphereLightHelper(

  hemisphereLight,

  0.2

);

scene.add(hemisphereLightHelper);
```