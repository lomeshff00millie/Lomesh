<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1.0" />
  <title>Student Portfolio</title>

  <!-- External CSS/JS -->
  <link rel="stylesheet" href="style.css" />
  <script defer src="script.js"></script>

  <!-- EmailJS SDK -->
  <script type="text/javascript" src="https://cdn.emailjs.com/dist/email.min.js"></script>
  <script>
    (function () {
      emailjs.init("YOUR_PUBLIC_KEY"); // Replace with your EmailJS Public Key
    })();
  </script>

  <style>
    /* === Base Styles === */
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      background-color: #f9f9f9;
      color: #333;
    }
    header, section, footer { padding: 20px; }
    a { text-decoration: none; color: inherit; }

    /* === Navbar === */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #333;
      padding: 15px 20px;
      color: white;
    }
    .nav-links {
      display: flex;
      gap: 15px;
      list-style: none;
    }
    .nav-links a { color: white; font-weight: bold; }
    .menu-toggle { display: none; cursor: pointer; }

    /* === Hero Section === */
    .hero {
      background: #eee;
      text-align: center;
      padding: 60px 20px;
    }
    .hero h1 span { color: #007bff; }
    .btn {
      display: inline-block;
      margin-top: 15px;
      padding: 10px 20px;
      background: #007bff;
      color: white;
      border-radius: 5px;
    }

    /* === About === */
    .about-content {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
      align-items: center;
    }
    .about-content img {
      max-width: 200px;
      border-radius: 8px;
    }

    /* === Projects === */
    .project-grid {
      display: flex;
      gap: 20px;
      flex-wrap: wrap;
    }
    .project-card {
      background: white;
      padding: 15px;
      border-radius: 8px;
      flex: 1;
      min-width: 200px;
      box-shadow: 0 0 5px rgba(0,0,0,0.1);
    }

    /* === Quiz Section === */
    .quiz-container {
      background-color: white;
      padding: 20px;
      border-radius: 8px;
      max-width: 700px;
      margin: auto;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    .quiz-container h1 { text-align: center; }
    .question { margin-bottom: 20px; }
    .question h2 { font-size: 18px; }
    .options label { display: block; margin: 5px 0; }
    .answer { margin-top: 5px; font-weight: bold; color: green; }

    /* === Blog Section === */
    .post {
      background: white;
      padding: 15px;
      margin-bottom: 20px;
      border-radius: 8px;
      box-shadow: 0 0 5px rgba(0,0,0,0.1);
    }
    .post h2 { margin: 0 0 10px; }
    .post small { color: gray; font-size: 12px; }

    /* === Contact Form === */
    form { display: flex; flex-direction: column; gap: 10px; }
    input, textarea { padding: 10px; font-size: 16px; }
    button {
      padding: 10px;
      background: #007bff;
      color: white;
      border: none;
      border-radius: 5px;
    }

    /* Responsive Nav */
    @media (max-width: 768px) {
      .nav-links { display: none; flex-direction: column; background: #333; }
      .nav-links.active { display: flex; }
      .menu-toggle { display: block; }
    }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="navbar">
      <div class="logo">MyPortfolio</div>
      <ul class="nav-links" id="nav-links">
        <li><a href="#home">Home</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#projects">Projects</a></li>
        <li><a href="#quiz">Quiz</a></li>
        <li><a href="#blog">Blog</a></li>
        <li><a href="#contact">Contact</a></li>
      </ul>
      <div class="menu-toggle" id="menu-toggle">&#9776;</div>
    </nav>
  </header>

  <!-- Hero -->
  <section id="home" class="hero">
    <div class="hero-content">
      <h1>Hello, I'm <span>MR__ LOMESH</span></h1>
      <p>I am the student</p>
      <a href="#projects" class="btn">View My Work</a>
    </div>
  </section>

  <!-- About -->
  <section id="about" class="about">
    <h2>About Me</h2>
    <div class="about-content">
      <img src="IMG_20250910_122708.jpg" alt="Profile Photo" />
      <p>
        I am a student enthusiastic about technology and design. 
        I love building interactive, user-friendly web applications 
        and exploring new tools in the tech world.
      </p>
    </div>
  </section>

  <!-- Projects -->
  <section id="projects" class="projects">
    <h2>My Projects</h2>
    <div class="project-grid">
      <div class="project-card">
        <h3>Project 1</h3>
        <p>A simple responsive website.</p>
      </div>
      <div class="project-card">
        <h3>Project 2</h3>
        <p>JavaScript-based quiz app.</p>
      </div>
      <div class="project-card">
        <h3>Project 3</h3>
        <p>Personal blog with CMS.</p>
      </div>
    </div>
  </section>

  <!-- Quiz Section -->
  <section id="quiz" class="quiz">
    <div class="quiz-container">
      <h1>HTML Quiz</h1>

      <div class="question">
        <h2>1. What is the correct HTML element for the largest heading?</h2>
        <div class="options">
          <label>A. &lt;heading&gt;</label>
          <label>B. &lt;h6&gt;</label>
          <label>C. &lt;h1&gt;</label>
          <label>D. &lt;head&gt;</label>
        </div>
        <div class="answer">Correct Answer: C. &lt;h1&gt;</div>
      </div>

      <div class="question">
        <h2>2. Which HTML tag is used to define a hyperlink?</h2>
        <div class="options">
          <label>A. &lt;href&gt;</label>
          <label>B. &lt;link&gt;</label>
          <label>C. &lt;a&gt;</label>
          <label>D. &lt;hyperlink&gt;</label>
        </div>
        <div class="answer">Correct Answer: C. &lt;a&gt;</div>
      </div>

      <div class="question">
        <h2>3. What is the correct HTML element to display an image?</h2>
        <div class="options">
          <label>A. &lt;img href="image.jpg"&gt;</label>
          <label>B. &lt;image src="image.jpg"&gt;</label>
          <label>C. &lt;img src="image.jpg"&gt;</label>
          <label>D. &lt;src img="image.jpg"&gt;</label>
        </div>
        <div class="answer">Correct Answer: C. &lt;img src="image.jpg"&gt;</div>
      </div>
    </div>
  </section>

  <!-- Blog Section -->
  <section id="blog" class="blog">
    <h2>My Blog</h2>
    <div class="container" id="postsContainer"></div>
  </section>

  <!-- Contact -->
  <section id="contact" class="contact">
    <h2>Contact Me</h2>
    <form id="contact-form">
      <input type="text" id="name" name="user_name" placeholder="Your Name" required>
      <input type="email" id="email" name="user_email" placeholder="Your Email" required>
      <textarea id="message" name="message" placeholder="Your Message" required></textarea>
      <button type="submit">Send</button>
    </form>
    <p id="form-status"></p>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 MR__ LOMESH | All rights reserved</p>
  </footer>

  <!-- Blog Script -->
  <script>
    function loadPosts() {
      const postsContainer = document.getElementById("postsContainer");
      const posts = JSON.parse(localStorage.getItem("blogPosts")) || [];
      postsContainer.innerHTML = "";
      posts.reverse().forEach(post => {
        const postEl = document.createElement("div");
        postEl.classList.add("post");
        postEl.innerHTML = `
          <h2>${post.title}</h2>
          <small>${new Date(post.date).toLocaleString()}</small>
          <p>${post.content}</p>
        `;
        postsContainer.appendChild(postEl);
      });
    }
    loadPosts();
  </script>
</body>
</html>
