<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Responsive Portfolio</title>
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
    </ul>
  </nav>
  
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
</body>
</html>
 
/* Global Styles */
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
}

header {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 20px 0;
}

nav {
  background-color: #444;
  text-align: center;
}

nav ul {
  list-style-type: none;
  padding: 0;
}

nav ul li {
  display: inline;
  margin-right: 20px;
}

nav ul li a {
  color: #fff;
  text-decoration: none;
}

/* Sections */
section {
  padding: 20px;
}

/* Projects */
.project {
  margin-bottom: 20px;
  border: 1px solid #ccc;
  padding: 10px;
}

/* Footer */
footer {
  background-color: #333;
  color: #fff;
  text-align: center;
  padding: 10px 0;
}
