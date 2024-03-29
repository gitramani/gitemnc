// Define colors
const colors = [
  0xff0000, // Red
  0x00ff00, // Green
  0x0000ff, // Blue
  0xffff00, // Yellow
  0xff00ff, // Magenta
  0x00ffff  // Cyan
];

// Initialize variables
let currentColorIndex = 0;
let scene, camera, renderer, mesh;

// Initialize Three.js scene
init();

function init() {
  // Create scene
  scene = new THREE.Scene();

  // Create camera
  camera = new THREE.PerspectiveCamera(75, window.innerWidth / window.innerHeight, 0.1, 1000);
  camera.position.z = 5;

  // Create geometry
  const geometry = new THREE.BoxGeometry();

  // Create material
  const material = new THREE.MeshBasicMaterial({ color: colors[currentColorIndex] });

  // Create mesh
  mesh = new THREE.Mesh(geometry, material);
  scene.add(mesh);

  // Create renderer
  renderer = new THREE.WebGLRenderer();
  renderer.setSize(window.innerWidth, window.innerHeight);
  document.body.appendChild(renderer.domElement);

  // Add event listener for color switch
  window.addEventListener('click', switchColor);

  // Render scene
  animate();
}

// Animation loop
function animate() {
  requestAnimationFrame(animate);
  renderer.render(scene, camera);
}

// Function to switch color
function switchColor() {
  currentColorIndex = (currentColorIndex + 1) % colors.length;
  mesh.material.color.setHex(colors[currentColorIndex]);
}
