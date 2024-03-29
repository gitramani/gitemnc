<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Ramanidevi R - Portfolio</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1 id="name" class="animate__animated animate__bounceIn">Ramanidevi R</h1>
    <p id="profile" class="animate__animated animate__fadeInLeft">Data Analytics | Data Science | SQL | Python</p>
  </header>
  
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="resume.pdf" target="_blank">Resume</a></li>
    </ul>
  </nav>
  
  <section id="home">
    <div class="container">
      <h2 id="about-heading" class="animate__animated animate__fadeInDown">Profile</h2>
      <p id="about-text" class="animate__animated animate__fadeInLeft">As a final year postgraduate, I'm passionate about data analytics, data science, SQL, and Python. My objective is to apply my skills and mindset to contribute effectively in a dynamic professional environment. I aim to solve real-world problems, extract insights from complex datasets, and drive informed decision-making.</p>
    </div>
  </section>

  <section id="projects">
    <div class="container">
      <h2 id="projects-heading" class="animate__animated animate__fadeInDown">Projects</h2>
      <div class="project animate__animated animate__fadeInLeft">
        <h3>Northwind Traders using Tableau</h3>
        <p>Data visualization project using Tableau for Northwind Traders.</p>
        <div class="project-view">
          <a href="northwind_traders_view.html" target="_blank">View Project</a>
        </div>
      </div>
      <div class="project animate__animated animate__fadeInLeft">
        <h3>Heart Disease Data USING Tableau</h3>
        <p>Data visualization project using Tableau for Heart Disease Data.</p>
        <div class="project-view">
          <a href="heart_disease_view.html" target="_blank">View Project</a>
        </div>
      </div>
      <!-- Add more projects similarly -->
    </div>
  </section>
  
  <section id="contact">
    <div class="container">
      <h2 id="contact-heading" class="animate__animated animate__fadeInDown">Contact</h2>
      <p id="contact-text" class="animate__animated animate__fadeInLeft">
        Phone: +91 634532578<br>
        Email: RRDESAGUY43@MAIL.COM<br>
        LinkedIn: <a href="#" target="_blank">HVHFKJHKG</a><br>
        Location: Virudhunagar, Tamil Nadu
      </p>
    </div>
  </section>
  
  <footer>
    <p>&copy; 2024 Ramanidevi R</p>
  </footer>
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

  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/three.js/r128/three.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/tween.js/18.6.4/Tween.min.js"></script>
  <script src="script.js"></script>
</body>
</html>
