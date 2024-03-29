<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>3D Booklet Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div id="canvas-container"></div>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script src="script.js"></script>
</body>
</html>
body, html {
  margin: 0;
  padding: 0;
  overflow: hidden;
}
#canvas-container {
  width: 100%;
  height: 100%;
}
// Set up Three.js scene
const scene = new THREE.Scene();
const camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
const renderer = new THREE.WebGLRenderer();
renderer.setSize(window.innerWidth, window.innerHeight);
document.getElementById('canvas-container').appendChild(renderer.domElement);

// Create booklet geometry
const geometry = new THREE.BoxGeometry(1, 1, 0.1);
const material = new THREE.MeshBasicMaterial({ color: 0x00ff00 });
const booklet = new THREE.Mesh(geometry, material);
scene.add(booklet);

// Set camera position
camera.position.z = 5;

// Animate function
function animate() {
  requestAnimationFrame(animate);
  booklet.rotation.x += 0.01;
  booklet.rotation.y += 0.01;
  renderer.render(scene, camera);
}

// Resize event listener
window.addEventListener('resize', function() {
  const width = window.innerWidth;
  const height = window.innerHeight;
  renderer.setSize(width, height);
  camera.aspect = width / height;
  camera.updateProjectionMatrix();
});

// Start animation
animate();

