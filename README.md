<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Agence Web Dynamique</title>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    * { margin: 0; padding: 0; box-sizing: border-box; font-family: 'Inter', sans-serif; }
    body { color: #333; line-height: 1.6; scroll-behavior: smooth; }
    a { text-decoration: none; color: inherit; }
    section { padding: 80px 20px; min-height: 100vh; display: flex; align-items: center; justify-content: center; flex-direction: column; opacity: 0; transform: translateY(50px); transition: all 1s ease; }
    .container { max-width: 1200px; margin: 0 auto; width: 100%; text-align: center; }

    /* Navbar */
    header { position: fixed; top:0; width: 100%; background: rgba(255,255,255,0.95); backdrop-filter: blur(10px); z-index: 1000; box-shadow: 0 2px 10px rgba(0,0,0,0.05); }
    nav { display: flex; justify-content: space-between; align-items: center; padding: 15px 20px; }
    .logo { font-weight: 700; font-size: 1.5rem; color: #4CAF50; }
    .nav-links { display: flex; gap: 20px; }
    .nav-links a { font-weight: 600; transition: color 0.3s; }
    .nav-links a:hover { color: #4CAF50; }

    /* Hero Section Parallax */
    #hero { background: linear-gradient(135deg, #4CAF50, #67D0A3); color: white; height: 100vh; display: flex; flex-direction: column; justify-content: center; align-items: center; background-attachment: fixed; background-size: cover; }
    #hero h1 { font-size: 3rem; margin-bottom: 20px; }
    #hero p { font-size: 1.2rem; margin-bottom: 30px; }
    .btn-primary { background: white; color: #4CAF50; padding: 15px 30px; border-radius: 50px; font-weight: bold; transition: transform 0.3s; }
    .btn-primary:hover { transform: scale(1.1); }

    /* Sections */
    h2 { font-size: 2rem; margin-bottom: 20px; }
    p { max-width: 700px; margin: 0 auto 20px; }

    /* About */
    #about { background: #f9f9f9; flex-direction: row; gap: 40px; flex-wrap: wrap; }
    #about img { max-width: 400px; border-radius: 15px; box-shadow: 0 10px 30px rgba(0,0,0,0.1); }

    /* Services */
    #services .cards { display: flex; flex-wrap: wrap; justify-content: center; gap: 30px; margin-top: 40px; }
    .card { background: white; padding: 30px; border-radius: 15px; width: 280px; box-shadow: 0 10px 25px rgba(0,0,0,0.08); transition: transform 0.3s, box-shadow 0.3s; cursor: pointer; }
    .card:hover { transform: translateY(-10px) scale(1.05); box-shadow: 0 15px 30px rgba(0,0,0,0.15); }
    .card h3 { margin-bottom: 15px; color: #4CAF50; }

    /* Contact Form */
    #contact form { max-width: 500px; margin: 0 auto; display: flex; flex-direction: column; gap: 20px; }
    input, textarea { padding: 15px; border: 1px solid #ccc; border-radius: 10px; width: 100%; transition: border-color 0.3s, transform 0.3s; }
    input:focus, textarea:focus { border-color: #4CAF50; outline: none; transform: scale(1.02); }
    button { padding: 15px; border: none; background: #4CAF50; color: white; font-weight: bold; border-radius: 50px; cursor: pointer; transition: background 0.3s, transform 0.3s; }
    button:hover { background: #45a049; transform: scale(1.05); }

    /* Footer */
    footer { background: #333; color: white; text-align: center; padding: 30px; margin-top: 40px; }

    /* Responsive */
    @media(max-width: 768px){
      #about { flex-direction: column; }
      #services .cards { flex-direction: column; align-items: center; }
    }

    /* Visible class pour scroll */
    .visible { opacity: 1; transform: translateY(0); }
  </style>
</head>
<body>

  <!-- Navbar -->
  <header>
    <nav class="container">
      <div class="logo">AgenceWeb</div>
      <div class="nav-links">
        <a href="#hero">Accueil</a>
        <a href="#about">À propos</a>
        <a href="#services">Services</a>
        <a href="#contact">Contact</a>
      </div>
    </nav>
  </header>

  <!-- Hero Section -->
  <section id="hero">
    <h1>Créons des sites web modernes</h1>
    <p>Design élégant, expérience utilisateur optimale, visibilité maximale.</p>
    <a href="#contact" class="btn-primary">Commencez maintenant</a>
  </section>

  <!-- About Section -->
  <section id="about">
    <img src="https://via.placeholder.com/400x300.png?text=À+propos" alt="À propos">
    <div>
      <h2>À propos de nous</h2>
      <p>Nous sommes une équipe de passionnés du web, spécialisés en développement, design et stratégie digitale pour vous aider à réussir en ligne.</p>
    </div>
  </section>

  <!-- Services Section -->
  <section id="services">
    <h2>Nos Services</h2>
    <div class="cards">
      <div class="card">
        <h3>Design UX/UI</h3>
        <p>Des interfaces modernes et intuitives qui captivent vos utilisateurs.</p>
      </div>
      <div class="card">
        <h3>Développement Web</h3>
        <p>Sites web performants, responsives et sécurisés, adaptés à vos besoins.</p>
      </div>
      <div class="card">
        <h3>SEO & Marketing</h3>
        <p>Augmentez votre visibilité et votre impact grâce à nos stratégies marketing.</p>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact">
    <h2>Contactez-nous</h2>
    <form>
      <input type="text" placeholder="Votre nom" required>
      <input type="email" placeholder="Votre email" required>
      <textarea rows="5" placeholder="Votre message" required></textarea>
      <button type="submit">Envoyer</button>
    </form>
  </section>

  <!-- Footer -->
  <footer>
    <p>&copy; 2025 Agence Web Dynamique. Tous droits réservés.</p>
  </footer>

  <!-- Script pour animations au scroll -->
  <script>
    const sections = document.querySelectorAll('section');
    const observer = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if(entry.isIntersecting){
          entry.target.classList.add('visible');
        }
      });
    }, { threshold: 0.2 });
    sections.forEach(section => observer.observe(section));
  </script>

</body>
</html>
