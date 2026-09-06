```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>Sanket Chalwadi | Developer Portfolio</title>

  <meta name="description"
        content="Sanket Chalwadi - Developer Portfolio. Explore my projects, skills, education and GitHub journey.">

  <meta name="author" content="Sanket Chalwadi">

  <!-- Google Font -->
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>

  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&family=JetBrains+Mono:wght@400;500;600&display=swap"
        rel="stylesheet">

  <!-- Font Awesome -->
  <link rel="stylesheet"
        href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.2/css/all.min.css">

  <style>

    /* =========================================================
       GLOBAL
    ========================================================= */

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      scroll-behavior: smooth;
    }

    :root {
      --bg: #05070d;
      --bg2: #080c14;
      --card: rgba(13, 18, 30, 0.78);
      --border: rgba(0, 229, 255, 0.15);

      --cyan: #00e5ff;
      --blue: #147eff;
      --purple: #7c3cff;

      --text: #f5f7ff;
      --muted: #9ca8ba;

      --shadow:
        0 0 30px rgba(0, 229, 255, 0.08);
    }

    body {
      font-family: "Inter", sans-serif;
      background:
        radial-gradient(
          circle at 20% 10%,
          rgba(0, 229, 255, 0.08),
          transparent 30%
        ),
        radial-gradient(
          circle at 80% 20%,
          rgba(124, 60, 255, 0.08),
          transparent 30%
        ),
        var(--bg);

      color: var(--text);
      line-height: 1.6;
      overflow-x: hidden;
    }

    a {
      text-decoration: none;
      color: inherit;
    }

    img {
      max-width: 100%;
    }

    .container {
      width: min(1120px, 92%);
      margin: auto;
    }

    /* =========================================================
       BACKGROUND GRID
    ========================================================= */

    body::before {
      content: "";
      position: fixed;
      inset: 0;

      background-image:
        linear-gradient(
          rgba(255,255,255,0.025) 1px,
          transparent 1px
        ),
        linear-gradient(
          90deg,
          rgba(255,255,255,0.025) 1px,
          transparent 1px
        );

      background-size: 45px 45px;
      pointer-events: none;
      z-index: -2;
    }

    body::after {
      content: "";
      position: fixed;
      width: 500px;
      height: 500px;

      background: rgba(0, 229, 255, 0.05);

      filter: blur(120px);
      border-radius: 50%;

      top: -200px;
      left: -200px;

      pointer-events: none;
      z-index: -1;
    }

    /* =========================================================
       NAVBAR
    ========================================================= */

    header {
      position: fixed;
      width: 100%;
      top: 0;
      z-index: 1000;

      backdrop-filter: blur(18px);
      background: rgba(5, 7, 13, 0.72);

      border-bottom: 1px solid rgba(255,255,255,0.05);
    }

    nav {
      height: 75px;

      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-family: "JetBrains Mono", monospace;
      font-size: 20px;
      font-weight: 700;
      color: white;
    }

    .logo span {
      color: var(--cyan);
    }

    .nav-links {
      display: flex;
      gap: 30px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-size: 14px;
      font-weight: 500;

      transition: 0.3s;
    }

    .nav-links a:hover {
      color: var(--cyan);
    }

    .menu-btn {
      display: none;

      font-size: 24px;
      color: var(--cyan);
      cursor: pointer;
    }

    /* =========================================================
       HERO
    ========================================================= */

    #home {
      min-height: 100vh;

      display: flex;
      align-items: center;

      padding-top: 75px;
    }

    .hero {
      display: grid;
      grid-template-columns: 1.3fr 0.7fr;

      gap: 70px;
      align-items: center;
    }

    .terminal {
      display: inline-flex;
      align-items: center;
      gap: 10px;

      padding: 8px 14px;

      border: 1px solid var(--border);
      border-radius: 50px;

      background: rgba(0,229,255,0.04);

      color: var(--cyan);

      font-family: "JetBrains Mono", monospace;
      font-size: 13px;

      margin-bottom: 22px;
    }

    .terminal-dot {
      width: 8px;
      height: 8px;

      background: #00ff9d;
      border-radius: 50%;

      box-shadow: 0 0 10px #00ff9d;
    }

    .hero h1 {
      font-size: clamp(45px, 7vw, 78px);
      line-height: 1.05;
      letter-spacing: -3px;
      margin-bottom: 20px;
    }

    .hero h1 span {
      background: linear-gradient(
        90deg,
        var(--cyan),
        #7ab8ff,
        #a87cff
      );

      -webkit-background-clip: text;
      -webkit-text-fill-color: transparent;
    }

    .hero h2 {
      font-family: "JetBrains Mono", monospace;
      color: var(--muted);

      font-size: clamp(18px, 2vw, 25px);
      margin-bottom: 20px;
    }

    .hero p {
      max-width: 650px;

      color: var(--muted);
      font-size: 17px;

      margin-bottom: 30px;
    }

    .hero-buttons {
      display: flex;
      gap: 14px;
      flex-wrap: wrap;
    }

    .btn {
      display: inline-flex;
      align-items: center;
      gap: 9px;

      padding: 12px 20px;

      border-radius: 9px;

      font-size: 14px;
      font-weight: 600;

      transition: 0.3s;
    }

    .btn-primary {
      background: linear-gradient(
        135deg,
        var(--cyan),
        var(--blue)
      );

      color: #001018;

      box-shadow:
        0 0 25px rgba(0,229,255,0.2);
    }

    .btn-primary:hover {
      transform: translateY(-3px);

      box-shadow:
        0 0 35px rgba(0,229,255,0.35);
    }

    .btn-outline {
      border: 1px solid rgba(255,255,255,0.12);
      color: white;
    }

    .btn-outline:hover {
      border-color: var(--cyan);
      color: var(--cyan);
      transform: translateY(-3px);
    }

    /* =========================================================
       PROFILE CARD
    ========================================================= */

    .profile-wrap {
      display: flex;
      justify-content: center;
    }

    .profile-card {
      position: relative;

      width: 290px;
      height: 290px;

      border-radius: 30px;

      background:
        linear-gradient(
          145deg,
          rgba(0,229,255,0.08),
          rgba(124,60,255,0.06)
        );

      border: 1px solid var(--border);

      display: flex;
      align-items: center;
      justify-content: center;

      box-shadow: var(--shadow);

      transform: rotate(3deg);
    }

    .profile-inner {
      width: 245px;
      height: 245px;

      border-radius: 25px;

      border: 1px solid rgba(0,229,255,0.2);

      display: flex;
      flex-direction: column;

      align-items: center;
      justify-content: center;

      background: rgba(0,0,0,0.25);

      transform: rotate(-3deg);
    }

    .avatar {
      width: 100px;
      height: 100px;

      border-radius: 50%;

      display: flex;
      align-items: center;
      justify-content: center;

      font-size: 38px;
      font-weight: 800;

      background:
        linear-gradient(
          135deg,
          var(--cyan),
          var(--purple)
        );

      color: #02050a;

      margin-bottom: 15px;

      box-shadow:
        0 0 35px rgba(0,229,255,0.25);
    }

    .profile-inner h3 {
      font-size: 18px;
    }

    .profile-inner p {
      color: var(--muted);
      font-size: 13px;
    }

    /* =========================================================
       SECTION
    ========================================================= */

    section {
      padding: 100px 0;
    }

    .section-title {
      margin-bottom: 50px;
    }

    .section-title span {
      color: var(--cyan);

      font-family: "JetBrains Mono", monospace;
      font-size: 13px;
    }

    .section-title h2 {
      font-size: 38px;
      margin-top: 7px;
    }

    .section-title p {
      color: var(--muted);
      margin-top: 10px;
    }

    /* =========================================================
       ABOUT
    ========================================================= */

    .about-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;

      gap: 25px;
    }

    .card {
      background: var(--card);

      border: 1px solid rgba(255,255,255,0.06);

      border-radius: 15px;

      padding: 28px;

      box-shadow: var(--shadow);

      backdrop-filter: blur(12px);

      transition: 0.3s;
    }

    .card:hover {
      transform: translateY(-5px);
      border-color: var(--border);
    }

    .card h3 {
      margin-bottom: 14px;
    }

    .card p {
      color: var(--muted);
      font-size: 15px;
    }

    .info-list {
      list-style: none;
      margin-top: 15px;
    }

    .info-list li {
      display: flex;
      justify-content: space-between;

      padding: 10px 0;

      border-bottom: 1px solid rgba(255,255,255,0.05);

      color: var(--muted);
    }

    .info-list strong {
      color: white;
    }

    /* =========================================================
       SKILLS
    ========================================================= */

    .skills-grid {
      display: grid;

      grid-template-columns:
        repeat(4, 1fr);

      gap: 15px;
    }

    .skill {
      padding: 20px;

      border: 1px solid rgba(255,255,255,0.06);

      background: rgba(13,18,30,0.65);

      border-radius: 13px;

      text-align: center;

      transition: 0.3s;
    }

    .skill i {
      font-size: 30px;

      color: var(--cyan);

      margin-bottom: 10px;
    }

    .skill h4 {
      font-size: 14px;
    }

    .skill:hover {
      transform: translateY(-6px);

      border-color: rgba(0,229,255,0.3);

      box-shadow:
        0 0 25px rgba(0,229,255,0.08);
    }

    /* =========================================================
       PROJECTS
    ========================================================= */

    .projects-grid {
      display: grid;

      grid-template-columns:
        repeat(3, 1fr);

      gap: 20px;
    }

    .project {
      position: relative;

      padding: 25px;

      min-height: 300px;

      display: flex;
      flex-direction: column;
    }

    .project-top {
      display: flex;
      justify-content: space-between;

      margin-bottom: 20px;
    }

    .folder {
      font-size: 30px;
      color: var(--cyan);
    }

    .project-links {
      display: flex;
      gap: 15px;
    }

    .project-links a {
      color: var(--muted);
      font-size: 18px;
    }

    .project-links a:hover {
      color: var(--cyan);
    }

    .project h3 {
      margin-bottom: 10px;
    }

    .project p {
      color: var(--muted);

      font-size: 14px;

      flex-grow: 1;
    }

    .tags {
      display: flex;
      gap: 7px;

      flex-wrap: wrap;

      margin-top: 20px;
    }

    .tag {
      padding: 5px 9px;

      border-radius: 5px;

      background: rgba(0,229,255,0.06);

      border: 1px solid rgba(0,229,255,0.1);

      color: #9edff0;

      font-family: "JetBrains Mono", monospace;

      font-size: 11px;
    }

    /* =========================================================
       GITHUB
    ========================================================= */

    .github-card {
      text-align: center;

      padding: 40px 25px;
    }

    .github-card i {
      font-size: 50px;

      margin-bottom: 20px;
    }

    .github-card h3 {
      font-size: 25px;
      margin-bottom: 10px;
    }

    .github-card p {
      max-width: 600px;
      margin: auto auto 25px;
    }

    .github-stats {
      margin-top: 30px;

      display: grid;

      grid-template-columns:
        repeat(4, 1fr);

      gap: 15px;
    }

    .stat {
      padding: 20px;

      background: rgba(255,255,255,0.025);

      border: 1px solid rgba(255,255,255,0.05);

      border-radius: 10px;
    }

    .stat strong {
      display: block;

      font-size: 25px;

      color: var(--cyan);
    }

    .stat span {
      color: var(--muted);

      font-size: 12px;
    }

    /* =========================================================
       EDUCATION
    ========================================================= */

    .timeline {
      position: relative;

      max-width: 850px;

      margin: auto;
    }

    .timeline::before {
      content: "";

      position: absolute;

      left: 10px;
      top: 0;
      bottom: 0;

      width: 1px;

      background:
        linear-gradient(
          var(--cyan),
          transparent
        );
    }

    .timeline-item {
      position: relative;

      padding-left: 45px;

      margin-bottom: 35px;
    }

    .timeline-dot {
      position: absolute;

      left: 3px;
      top: 7px;

      width: 15px;
      height: 15px;

      border-radius: 50%;

      background: var(--cyan);

      box-shadow:
        0 0 15px rgba(0,229,255,0.6);
    }

    .timeline-item h3 {
      margin-bottom: 5px;
    }

    .timeline-item .date {
      color: var(--cyan);

      font-family: "JetBrains Mono", monospace;

      font-size: 12px;

      margin-bottom: 8px;
    }

    .timeline-item p {
      color: var(--muted);
    }

    /* =========================================================
       CONTACT
    ========================================================= */

    .contact-grid {
      display: grid;

      grid-template-columns: 1fr 1fr;

      gap: 25px;
    }

    .contact-item {
      display: flex;

      align-items: center;

      gap: 15px;

      padding: 18px;

      border: 1px solid rgba(255,255,255,0.05);

      border-radius: 10px;

      margin-bottom: 12px;

      transition: 0.3s;
    }

    .contact-item i {
      width: 42px;
      height: 42px;

      display: flex;

      align-items: center;
      justify-content: center;

      border-radius: 10px;

      background: rgba(0,229,255,0.07);

      color: var(--cyan);
    }

    .contact-item:hover {
      border-color: rgba(0,229,255,0.2);
    }

    .contact-item span {
      display: block;

      color: var(--muted);

      font-size: 12px;
    }

    .contact-item strong {
      font-size: 14px;
    }

    /* =========================================================
       FOOTER
    ========================================================= */

    footer {
      border-top: 1px solid rgba(255,255,255,0.05);

      padding: 30px 0;

      text-align: center;

      color: var(--muted);

      font-size: 13px;
    }

    footer span {
      color: var(--cyan);
    }

    /* =========================================================
       REVEAL ANIMATION
    ========================================================= */

    .reveal {
      opacity: 0;

      transform: translateY(30px);

      transition:
        opacity 0.7s ease,
        transform 0.7s ease;
    }

    .reveal.active {
      opacity: 1;

      transform: translateY(0);
    }

    /* =========================================================
       RESPONSIVE
    ========================================================= */

    @media (max-width: 900px) {

      .hero {
        grid-template-columns: 1fr;

        text-align: center;
      }

      .hero p {
        margin-left: auto;
        margin-right: auto;
      }

      .hero-buttons {
        justify-content: center;
      }

      .profile-wrap {
        order: -1;
      }

      .profile-card {
        width: 230px;
        height: 230px;
      }

      .profile-inner {
        width: 195px;
        height: 195px;
      }

      .avatar {
        width: 75px;
        height: 75px;

        font-size: 28px;
      }

      .about-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .projects-grid {
        grid-template-columns:
          repeat(2, 1fr);
      }

      .skills-grid {
        grid-template-columns:
          repeat(3, 1fr);
      }
    }

    @media (max-width: 650px) {

      .nav-links {
        position: absolute;

        top: 75px;
        left: 0;

        width: 100%;

        flex-direction: column;

        background: rgba(5,7,13,0.97);

        padding: 20px;

        display: none;

        text-align: center;
      }

      .nav-links.active {
        display: flex;
      }

      .menu-btn {
        display: block;
      }

      .hero h1 {
        letter-spacing: -2px;
      }

      .projects-grid {
        grid-template-columns: 1fr;
      }

      .skills-grid {
        grid-template-columns:
          repeat(2, 1fr);
      }

      .github-stats {
        grid-template-columns:
          repeat(2, 1fr);
      }

      section {
        padding: 75px 0;
      }

      .section-title h2 {
        font-size: 30px;
      }
    }

  </style>
</head>


<body>

  <!-- =======================================================
       NAVIGATION
  ======================================================== -->

  <header>

    <div class="container">

      <nav>

        <a href="#home" class="logo">
          &lt;<span>Sanket</span>/&gt;
        </a>

        <ul class="nav-links" id="navLinks">

          <li>
            <a href="#home">Home</a>
          </li>

          <li>
            <a href="#about">About</a>
          </li>

          <li>
            <a href="#skills">Skills</a>
          </li>

          <li>
            <a href="#projects">Projects</a>
          </li>

          <li>
            <a href="#github">GitHub</a>
          </li>

          <li>
            <a href="#education">Education</a>
          </li>

          <li>
            <a href="#contact">Contact</a>
          </li>

        </ul>

        <div class="menu-btn" id="menuBtn">
          <i class="fa-solid fa-bars"></i>
        </div>

      </nav>

    </div>

  </header>


  <!-- =======================================================
       HERO
  ======================================================== -->

  <main>

    <section id="home">

      <div class="container">

        <div class="hero">

          <div class="hero-content reveal">

            <div class="terminal">

              <span class="terminal-dot"></span>

              <span>
                Available for opportunities
              </span>

            </div>

            <h1>
              Hi, I'm <span>Sanket</span>.
            </h1>

            <h2>
              &gt; Developer &amp; Tech Enthusiast
            </h2>

            <p>
              I’m a passionate developer who enjoys building
              modern digital experiences, learning new technologies,
              solving problems and turning ideas into real-world
              projects.
            </p>

            <div class="hero-buttons">

              <!-- CHANGE THIS GITHUB LINK -->
              <a
                href="https://github.com/"
                target="_blank"
                class="btn btn-primary"
              >
                <i class="fa-brands fa-github"></i>
                GitHub
              </a>

              <a
                href="#projects"
                class="btn btn-outline"
              >
                <i class="fa-solid fa-code"></i>
                View Projects
              </a>

            </div>

          </div>


          <div class="profile-wrap reveal">

            <div class="profile-card">

              <div class="profile-inner">

                <div class="avatar">
                  SC
                </div>

                <h3>
                  Sanket Chalwadi
                </h3>

                <p>
                  Developer
                </p>

              </div>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         ABOUT
    ====================================================== -->

    <section id="about">

      <div class="container">

        <div class="section-title reveal">

          <span>01 / ABOUT</span>

          <h2>
            About Me
          </h2>

          <p>
            A little about who I am and what I do.
          </p>

        </div>


        <div class="about-grid">

          <div class="card reveal">

            <h3>
              Who I Am
            </h3>

            <p>
              Hello! I'm Sanket Chalwadi, a technology enthusiast
              interested in software development, programming and
              building useful digital solutions.
            </p>

            <br>

            <p>
              I enjoy experimenting with new technologies,
              improving my coding skills and creating projects
              that help me learn by doing.
            </p>

          </div>


          <div class="card reveal">

            <h3>
              Quick Info
            </h3>

            <ul class="info-list">

              <li>
                <span>Name</span>
                <strong>Sanket Chalwadi</strong>
              </li>

              <li>
                <span>Role</span>
                <strong>Developer</strong>
              </li>

              <li>
                <span>Focus</span>
                <strong>Software &amp; Web Development</strong>
              </li>

              <li>
                <span>Learning</span>
                <strong>DSA &amp; Modern Technologies</strong>
              </li>

              <li>
                <span>Location</span>
                <strong>India</strong>
              </li>

            </ul>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         SKILLS
    ====================================================== -->

    <section id="skills">

      <div class="container">

        <div class="section-title reveal">

          <span>02 / SKILLS</span>

          <h2>
            My Tech Stack
          </h2>

          <p>
            Technologies and tools I work with.
          </p>

        </div>


        <div class="skills-grid">

          <div class="skill reveal">
            <i class="fa-brands fa-html5"></i>
            <h4>HTML5</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-brands fa-css3-alt"></i>
            <h4>CSS3</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-brands fa-js"></i>
            <h4>JavaScript</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-brands fa-python"></i>
            <h4>Python</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-brands fa-java"></i>
            <h4>Java</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-solid fa-database"></i>
            <h4>SQL</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-brands fa-git-alt"></i>
            <h4>Git</h4>
          </div>

          <div class="skill reveal">
            <i class="fa-brands fa-github"></i>
            <h4>GitHub</h4>
          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         PROJECTS
    ====================================================== -->

    <section id="projects">

      <div class="container">

        <div class="section-title reveal">

          <span>03 / PROJECTS</span>

          <h2>
            Featured Projects
          </h2>

          <p>
            Some of the things I've built and experimented with.
          </p>

        </div>


        <div class="projects-grid">


          <!-- PROJECT 1 -->

          <div class="card project reveal">

            <div class="project-top">

              <i class="fa-regular fa-folder folder"></i>

              <div class="project-links">

                <a
                  href="https://github.com/"
                  target="_blank"
                >
                  <i class="fa-brands fa-github"></i>
                </a>

                <a href="#">
                  <i class="fa-solid fa-arrow-up-right-from-square"></i>
                </a>

              </div>

            </div>

            <h3>
              Portfolio Website
            </h3>

            <p>
              A modern responsive developer portfolio designed
              to showcase my skills, projects, education and
              professional journey.
            </p>

            <div class="tags">

              <span class="tag">
                HTML
              </span>

              <span class="tag">
                CSS
              </span>

              <span class="tag">
                JavaScript
              </span>

            </div>

          </div>


          <!-- PROJECT 2 -->

          <div class="card project reveal">

            <div class="project-top">

              <i class="fa-regular fa-folder folder"></i>

              <div class="project-links">

                <a
                  href="https://github.com/"
                  target="_blank"
                >
                  <i class="fa-brands fa-github"></i>
                </a>

                <a href="#">
                  <i class="fa-solid fa-arrow-up-right-from-square"></i>
                </a>

              </div>

            </div>

            <h3>
              Student Management System
            </h3>

            <p>
              A project designed to manage student information,
              records and academic data using programming and
              database concepts.
            </p>

            <div class="tags">

              <span class="tag">
                Java
              </span>

              <span class="tag">
                SQL
              </span>

              <span class="tag">
                Database
              </span>

            </div>

          </div>


          <!-- PROJECT 3 -->

          <div class="card project reveal">

            <div class="project-top">

              <i class="fa-regular fa-folder folder"></i>

              <div class="project-links">

                <a
                  href="https://github.com/"
                  target="_blank"
                >
                  <i class="fa-brands fa-github"></i>
                </a>

                <a href="#">
                  <i class="fa-solid fa-arrow-up-right-from-square"></i>
                </a>

              </div>

            </div>

            <h3>
              Web Application
            </h3>

            <p>
              A responsive web application created to practice
              frontend development, user interfaces and
              JavaScript functionality.
            </p>

            <div class="tags">

              <span class="tag">
                HTML
              </span>

              <span class="tag">
                CSS
              </span>

              <span class="tag">
                JavaScript
              </span>

            </div>

          </div>


        </div>

      </div>

    </section>


    <!-- =====================================================
         GITHUB
    ====================================================== -->

    <section id="github">

      <div class="container">

        <div class="section-title reveal">

          <span>04 / GITHUB</span>

          <h2>
            My GitHub Journey
          </h2>

          <p>
            Explore my repositories and coding activity.
          </p>

        </div>


        <div class="card github-card reveal">

          <i class="fa-brands fa-github"></i>

          <h3>
            Let's Build Something!
          </h3>

          <p>
            Check out my GitHub profile to see my repositories,
            experiments, projects and contributions.
          </p>

          <!-- CHANGE YOUR GITHUB USERNAME HERE -->

          <a
            href="https://github.com/"
            target="_blank"
            class="btn btn-primary"
          >

            <i class="fa-brands fa-github"></i>

            Visit GitHub

          </a>


          <div class="github-stats">

            <div class="stat">

              <strong>--</strong>

              <span>
                Repositories
              </span>

            </div>

            <div class="stat">

              <strong>--</strong>

              <span>
                Contributions
              </span>

            </div>

            <div class="stat">

              <strong>--</strong>

              <span>
                Followers
              </span>

            </div>

            <div class="stat">

              <strong>∞</strong>

              <span>
                Learning
              </span>

            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =====================================================
         EDUCATION
    ====================================================== -->

    <section id="education">

      <div class="container">

        <div class="section-title reveal">

          <span>05 / EDUCATION</span>

          <h2>
            Education
          </h2>

          <p>
            My academic journey.
          </p>

        </div>


        <div class="timeline">


          <div class="timeline-item reveal">

            <div class="timeline-dot"></div>

            <div class="card">

              <div class="date">
                CURRENT
              </div>

              <h3>
                Bachelor of Technology
              </h3>

              <p>
                Computer Engineering
              </p>

              <p>
                Currently developing my knowledge in
                software engineering, computer science,
                programming and modern technologies.
              </p>

            </div>

          </div>


          <div class="timeline-item reveal">

            <div class="timeline-dot"></div>

            <div class="card">

              <div class="date">
                COMPLETED
              </div>

              <h3>
                Diploma in Computer Engineering
              </h3>

              <p>
                Computer Engineering
              </p>

              <p>
                Built a foundation in programming,
                databases, computer networks,
                web development and software engineering.
              </p>

            </div>

          </div>


        </div>

      </div>

    </section>


    <!-- =====================================================
         CONTACT
    ====================================================== -->

    <section id="contact">

      <div class="container">

        <div class="section-title reveal">

          <span>06 / CONTACT</span>

          <h2>
            Let's Connect
          </h2>

          <p>
            Have an idea, opportunity or project?
            Let's talk.
          </p>

        </div>


        <div class="contact-grid">


          <div class="card reveal">

            <h3>
              Get In Touch
            </h3>

            <p>
              I'm always interested in learning,
              collaborating and working on interesting
              technology projects.
            </p>

            <br>


            <!-- CHANGE EMAIL -->

            <a
              href="mailto:your.email@example.com"
              class="contact-item"
            >

              <i class="fa-solid fa-envelope"></i>

              <div>

                <span>Email</span>

                <strong>
                  your.email@example.com
                </strong>

              </div>

            </a>


            <!-- CHANGE GITHUB -->

            <a
              href="https://github.com/"
              target="_blank"
              class="contact-item"
            >

              <i class="fa-brands fa-github"></i>

              <div>

                <span>GitHub</span>

                <strong>
                  github.com/yourusername
                </strong>

              </div>

            </a>


            <!-- CHANGE LINKEDIN -->

            <a
              href="https://www.linkedin.com/"
              target="_blank"
              class="contact-item"
            >

              <i class="fa-brands fa-linkedin"></i>

              <div>

                <span>LinkedIn</span>

                <strong>
                  LinkedIn Profile
                </strong>

              </div>

            </a>

          </div>


          <div class="card reveal">

            <h3>
              Currently
            </h3>

            <br>

            <p>
              🚀 Building projects
            </p>

            <p>
              💻 Improving programming skills
            </p>

            <p>
              📚 Learning new technologies
            </p>

            <p>
              🧠 Practicing problem solving
            </p>

            <p>
              🌱 Growing every day
            </p>

            <br>

            <a
              href="mailto:your.email@example.com"
              class="btn btn-primary"
            >

              <i class="fa-solid fa-paper-plane"></i>

              Say Hello

            </a>

          </div>


        </div>

      </div>

    </section>

  </main>


  <!-- =======================================================
       FOOTER
  ======================================================== -->

  <footer>

    <div class="container">

      <p>

        Designed &amp; Built by

        <span>
          Sanket Chalwadi
        </span>

        •

        <span>
          &lt;/&gt;
        </span>

      </p>

      <p style="margin-top:6px;">

        © <span id="year"></span>
        Sanket Chalwadi. All rights reserved.

      </p>

    </div>

  </footer>


  <!-- =======================================================
       JAVASCRIPT
  ======================================================== -->

  <script>

    /* =====================================================
       MOBILE MENU
    ====================================================== */

    const menuBtn =
      document.getElementById("menuBtn");

    const navLinks =
      document.getElementById("navLinks");


    menuBtn.addEventListener("click", () => {

      navLinks.classList.toggle("active");

    });


    /* Close menu after clicking */

    document
      .querySelectorAll(".nav-links a")
      .forEach(link => {

        link.addEventListener("click", () => {

          navLinks.classList.remove("active");

        });

      });


    /* =====================================================
       SCROLL REVEAL
    ====================================================== */

    const revealElements =
      document.querySelectorAll(".reveal");


    const observer =
      new IntersectionObserver(

        entries => {

          entries.forEach(entry => {

            if (entry.isIntersecting) {

              entry.target.classList.add("active");

            }

          });

        },

        {
          threshold: 0.12
        }

      );


    revealElements.forEach(element => {

      observer.observe(element);

    });


    /* =====================================================
       CURRENT YEAR
    ====================================================== */

    document.getElementById("year").textContent =
      new Date().getFullYear();


    /* =====================================================
       ACTIVE NAVIGATION
    ====================================================== */

    const sections =
      document.querySelectorAll("section");

    const navItems =
      document.querySelectorAll(".nav-links a");


    window.addEventListener("scroll", () => {

      let current = "";

      sections.forEach(section => {

        const sectionTop =
          section.offsetTop - 120;

        if (
          window.scrollY >= sectionTop
        ) {

          current = section.getAttribute("id");

        }

      });


      navItems.forEach(link => {

        link.style.color = "";

        if (
          link.getAttribute("href") ===
          "#" + current
        ) {

          link.style.color =
            "var(--cyan)";

        }

      });

    });

  </script>

</body>
</html>
```
