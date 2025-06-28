<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Natural Resources</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html, body {
      height: 100%;
      overflow: hidden;
      font-family: 'Segoe UI', sans-serif;
      color: #2d2d2a; /* Bark brown */
      background-color: #edf6f9; /* Soft pale mint */
    }

    header {
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      background-color: #0e883ba7; /* Deep forest green */
      color: white;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem 2rem;
      z-index: 1000;
    }

    .logo {
      font-size: 1.5rem;
      font-weight: bold;
    }

    nav {
      display: flex;
      align-items: center;
    }

    nav ul {
      list-style: none;
      display: flex;
      gap: 2rem;
    }

    nav a {
      color: white;
      text-decoration: none;
      font-weight: 500;
      transition: color 0.3s;
      cursor: pointer;
    }

    nav a:hover {
      color: #95d5b2; /* Light fern green */
    }

    .hamburger {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }

    .hamburger div {
      width: 25px;
      height: 3px;
      background: white;
      margin: 4px 0;
    }

    @media (max-width: 768px) {
      nav ul {
        flex-direction: column;
        position: absolute;
        top: 70px;
        left: 0;
        right: 0;
        background-color: #0c451ede;
        display: none;
        text-align: center;
        padding: 1rem 0;
      }

      nav ul.active {
        display: flex;
      }

      .hamburger {
        display: flex;
      }
    }

    section {
      display: none;
      justify-content: center;
      align-items: center;
      text-align: center;
      height: 100vh;
      width: 100vw;
      padding: 80px 20px 20px;
      opacity: 0;
      transition: opacity 0.5s ease;
    }

    section.show {
      display: flex;
      opacity: 1;
    }

    h1 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    p {
      max-width: 800px;
      margin: 0 auto 1rem;
      font-size: 1.1rem;
    }

    #home {
        background: linear-gradient(90deg, #22d3ee, #818cf8, #f472b6);
      color: #0a0b0b;
      position: relative;
      flex-direction: column;
    }

    #about.show {
      background-color: #b6f3cb;
    }

    #types.show {
      background-color: #63d1d5;
    }

    #importance.show {
      background-color: #d2bbdf;
    }

    #contact.show {
      background-color: #fefae0;
    }

    .emoji {
      position: absolute;
      font-size: 2rem;
      animation: float 4s infinite ease-in-out;
    }

    @keyframes float {
      0% { transform: translateY(0) rotate(0deg); }
      50% { transform: translateY(-20px) rotate(180deg); }
      100% { transform: translateY(0) rotate(360deg); }
    }
  </style>
</head>
<body>

<header>
  <div class="logo">🌿 Resources</div>
  <div class="hamburger" id="hamburger">
    <div></div>
    <div></div>
    <div></div>
  </div>
  <nav>
    <ul id="nav-menu">
      <li><a data-target="home">Home</a></li>
      <li><a data-target="about">About</a></li>
      <li><a data-target="types">Types</a></li>
      <li><a data-target="importance">Importance</a></li>
      <li><a data-target="contact">Contact</a></li>
    </ul>
  </nav>
</header>

<section id="home" class="show">
  <h1>Welcome to Natural Resources</h1>
  <p>Explore the richness of Earth’s resources—learn, protect, and preserve for future generations.</p>
</section>

<section id="about">
  <div>
    <h1>About Natural Resources</h1>
    <p>Natural resources are materials from Earth used to support life and meet human needs. They include air, water, soil, plants, animals, minerals, and fossil fuels.</p>
  </div>
</section>

<section id="types">
  <div>
    <h1>Types of Natural Resources</h1>
    <p><strong>Renewable:</strong> Resources that regenerate (e.g., sunlight, wind, water, forests).</p>
    <p><strong>Non-Renewable:</strong> Finite resources (e.g., coal, oil, natural gas, minerals).</p>
    <p><strong>Biotic:</strong> Living or once-living resources (e.g., animals, plants).</p>
    <p><strong>Abiotic:</strong> Non-living resources (e.g., land, air, water, metals).</p>
  </div>
</section>

<section id="importance">
  <div>
    <h1>Importance of Natural Resources</h1>
    <p>They provide food, shelter, energy, and raw materials. Responsible use ensures sustainable development, supports ecosystems, and helps combat climate change.</p>
  </div>
</section>

<section id="contact">
  <div>
    <h1>Contact</h1>
    <p>
      🌱 Email: sustainability@earth.org<br>
      📞 Phone: +1 345 678 9012<br>
      📍 Address: 123 Green Street, Eco City, Earth
    </p>
  </div>
</section>

<script>
  const sections = document.querySelectorAll('section');
  const links = document.querySelectorAll('nav a');
  const hamburger = document.getElementById('hamburger');
  const navMenu = document.getElementById('nav-menu');

  hamburger.addEventListener("click", () => {
    navMenu.classList.toggle("active");
  });

  links.forEach(link => {
    link.addEventListener('click', () => {
      const target = document.getElementById(link.dataset.target);
      sections.forEach(section => {
        section.classList.remove('show');
        section.style.display = 'none';
      });
      setTimeout(() => {
        target.style.display = 'flex';
        setTimeout(() => target.classList.add('show'), 10);
      }, 100);
      navMenu.classList.remove("active");
    });
  });

  const home = document.getElementById("home");
  const emojis = ['🌿','💧','🌞','🌍','🪨','🔥'];
  for (let i = 0; i < 15; i++) {
    const emoji = document.createElement("div");
    emoji.classList.add("emoji");
    emoji.innerText = emojis[Math.floor(Math.random() * emojis.length)];
    emoji.style.top = Math.random() * 90 + "%";
    emoji.style.left = Math.random() * 90 + "%";
    emoji.style.animationDuration = (3 + Math.random() * 4) + "s";
    home.appendChild(emoji);
  }
</script>

</body>
</html>
