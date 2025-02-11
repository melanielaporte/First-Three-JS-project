<h1 align="center">First ThreeJS Project</h1>

This README.md file contains starter files and folders.
![shapePinkGif](https://github.com/user-attachments/assets/fd7d3781-bf27-424e-9563-b15c578ebf78)

 
# Step 1: create the environment
1. Install [Node.js](https://nodejs.org/)
2. In terminal/bash, install three.js and [Vite](https://vitejs.dev/) build tool in your project folder
3. In terminal, run then should see http://localhost:5173
    npx vite
4.Open the url to see your web app.

# Step 2: Build tool or use a local server with a CDN and import maps.
- scene, camera and renderer

**main.js**

*import * as THREE from 'three';*

*const scene = new THREE.Scene();*
*const camera = new THREE* *PerspectiveCamera( 75, window.*
*innerWidth / window.innerHeight, *0.1, 1000 );*

*const renderer = new THREE.*
*WebGLRenderer();*
*renderer.setSize( window.*
*innerWidth, window.innerHeight )*
*document.body.appendChild(*
*renderer.domElement );*

# Step 3: create a scene
const geometry = new THREE.BoxGeometry( 1, 1, 1 );
const material = new THREE.MeshBasicMaterial( { color: 0x00ff00 } );
const cube = new THREE.Mesh( geometry, material );
scene.add( cube );

camera.position.z = 5;

# Step 4: Rendering the scene
function animate() {
	renderer.render( scene, camera );
}
renderer.setAnimationLoop( animate );


# Step 5: Animating the cube

cube.rotation.x += 0.01;
cube.rotation.y += 0.01;

# Step 6: The result
**index.html**

<!DOCTYPE html>
<html lang="en">
	<head>
		<meta charset="utf-8">
		<title>My first three.js app</title>
		<style>
			body { margin: 0; }
		</style>
	</head>
	<body>
		<script type="module" src="/main.js"></script>
	</body>
</html>

**main.js**

import * as THREE from 'three';

const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera( 75, window.innerWidth / window.innerHeight, 0.1, 1000 );

const renderer = new THREE.WebGLRenderer();
renderer.setSize( window.innerWidth, window.innerHeight );
renderer.setAnimationLoop( animate );
document.body.appendChild( renderer.domElement );

const geometry = new THREE.BoxGeometry( 1, 1, 1 );
const material = new THREE.MeshBasicMaterial( { color: 0x00ff00 } );
const cube = new THREE.Mesh( geometry, material );
scene.add( cube );

camera.position.z = 5;

function animate() {

	cube.rotation.x += 0.01;
	cube.rotation.y += 0.01;

	renderer.render( scene, camera );




https://threejs.org/docs/#manual/en/introduction/Installation
