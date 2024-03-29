<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Portfolio with Resume</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <header>
    <h1>My Portfolio</h1>
  </header>
  
  <nav>
    <ul>
      <li><a href="#home">Home</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#projects">Projects</a></li>
      <li><a href="#contact">Contact</a></li>
      <li><a href="resume.pdf" target="_blank">Resume</a></li> <!-- Link to PDF resume -->
    </ul>
  </nav>
  
  <div class="background-container">
    <div class="background"></div>
  </div>

  <section id="home">
    <h2>Home</h2>
    <p>Welcome to my portfolio!</p>
  </section>
  
  <section id="about">
    <h2>About</h2>
    <p>About me goes here...</p>
  </section>
  
  <section id="projects">
    <h2>Projects</h2>
    <div class="project">
      <h3>Project 1</h3>
      <p>Description of project 1</p>
    </div>
    <div class="project">
      <h3>Project 2</h3>
      <p>Description of project 2</p>
    </div>
  </section>
  
  <section id="contact">
    <h2>Contact</h2>
    <p>Contact information goes here...</p>
  </section>
  
  <footer>
    <p>&copy; 2024 My Portfolio</p>
  </footer>

  <script src="https://cdnjs.cloudflare.com/ajax/libs/jquery/3.6.0/jquery.min.js"></script>
  <script src="script.js"></script>
</body>
</html>


