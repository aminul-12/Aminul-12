<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Aminul Islam | Professional Portfolio</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link href="https://fonts.googleapis.com/css2?family=Fira+Code&display=swap" rel="stylesheet" />
  <style>
    body {
      margin: 0;
      font-family: 'Fira Code', monospace;
      background: linear-gradient(to right, #0f0f0f, #1a1a1a);
      color: #eee;
      display: flex;
      flex-direction: column;
      align-items: center;
      overflow-x: hidden;
    }

    header {
      padding: 40px 20px;
      text-align: center;
      position: relative;
    }

    .typing-text {
      font-size: 1.5em;
      white-space: nowrap;
      overflow: hidden;
      border-right: 2px solid #36BCF7;
      width: 0;
      animation: typing 4s steps(50, end), blink 0.6s step-end infinite;
    }

    @keyframes typing {
      from { width: 0 }
      to { width: 100% }
    }

    @keyframes blink {
      50% { border-color: transparent }
    }

    img.profile {
      width: 180px;
      border-radius: 50%;
      box-shadow: 0 0 15px #00ffd599;
      margin-top: 30px;
    }

    .confetti {
      position: fixed;
      top: -20px;
      width: 100%;
      height: 100%;
      pointer-events: none;
      z-index: 999;
      animation: drop 3s ease-out forwards;
    }

    @keyframes drop {
      0% { transform: translateY(-100%) rotate(0deg); opacity: 0; }
      100% { transform: translateY(100vh) rotate(360deg); opacity: 1; }
    }

    .link-btn {
      background: #36BCF7;
      color: #111;
      padding: 10px 20px;
      margin-top: 25px;
      text-decoration: none;
      font-weight: bold;
      border-radius: 6px;
      display: inline-block;
    }

    .project-card {
      background-color: #222;
      border-radius: 12px;
      padding: 20px;
      max-width: 700px;
      margin: 30px auto;
      box-shadow: 0 0 10px #00ffd544;
    }

    .project-card h3 {
      color: #00ffd5;
      margin-bottom: 10px;
    }

    footer {
      margin-top: 60px;
      padding: 20px;
      color: #aaa;
      font-size: 0.9em;
    }
  </style>
</head>
<body>

  <!-- 🎊 Confetti Congratulations -->
  <div class="confetti">🎉🎉🎉 Congratulations Aminul! 🎉🎉🎉</div>

  <header>
    <div class="typing-text">Hi 👋, I'm Aminul Islam | Frontend Developer</div>
    <img src="your-photo.jpg" alt="Aminul Islam" class="profile" />
    <a href="https://linkedin.com/in/aminul-islam-97282b25a" class="link-btn">🔗 Connect on LinkedIn</a>
    <a href="https://aminul-port.netlify.app/" class="link-btn">📂 Visit Portfolio</a>
  </header>

  <!-- 🎓 Project Showcase -->
  <section class="project-card">
    <h3>🧪 Chemical Adventure Project</h3>
    <p>A web-based interactive chemistry playground built with educational intent, powered by animations and reaction simulations.</p>
    <a href="https://chemicaladventure.netlify.app/" target="_blank" class="link-btn">🔗 Explore Project</a>
  </section>

  <section class="project-card">
    <h3>📘 About This Site</h3>
    <p>This portfolio is built with HTML/CSS and vanilla JS enhancements including typing animation, animated confetti drop, and responsive layout — designed to reflect both professionalism and creativity. Firebase Auth, PDF previews, and analytics integration are available inside the full portfolio.</p>
  </section>

  <footer>
    &copy; <span id="year"></span> Aminul Islam — Passionate about frontend development, secure design, and creative interfaces.
  </footer>

  <script>
    document.getElementById('year').textContent = new Date().getFullYear();
  </script>
</body>
</html>
