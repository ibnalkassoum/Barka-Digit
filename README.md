 <!DOCTYPE html>  
<html lang="fr">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1.0">  
  <title>Barka Digit - Le digital au service de l'Afrique</title>  
  {{ content_for_header }}  
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@300;400;500;600;700;800;900&display=swap" rel="stylesheet">  
  <style>  
    :root {  
      --primary-dark: #0A2A66;  
      --accent-orange: #FF8C00;  
      --light-gray: #f8f9fa;  
      --text-dark: #212529;  
      --text-light: #6c757d;  
      --white: #ffffff;  
      --shadow-sm: 0 2px 10px rgba(0,0,0,0.08);  
      --shadow-md: 0 4px 20px rgba(0,0,0,0.12);  
      --shadow-lg: 0 8px 30px rgba(0,0,0,0.15);  
      --transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);  
    }  
  
    * {  
      margin: 0;  
      padding: 0;  
      box-sizing: border-box;  
    }  
  
    body {  
      font-family: 'Montserrat', sans-serif;  
      color: var(--text-dark);  
      line-height: 1.6;  
      background-color: var(--white);  
      overflow-x: hidden;  
    }  
  
    h1, h2, h3, h4, h5, h6 {  
      font-weight: 800;  
      line-height: 1.3;  
      color: var(--primary-dark);  
      margin-bottom: 1rem;  
    }  
  
    h1 {  
      font-size: clamp(2.2rem, 5vw, 3.5rem);  
    }  
  
    h2 {  
      font-size: clamp(1.8rem, 4vw, 2.5rem);  
      text-align: center;  
      position: relative;  
      padding-bottom: 1rem;  
    }  
  
    h2:after {  
      content: '';  
      position: absolute;  
      bottom: 0;  
      left: 50%;  
      transform: translateX(-50%);  
      width: 60px;  
      height: 3px;  
      background: var(--accent-orange);  
    }  
  
    p {  
      margin-bottom: 1rem;  
      color: var(--text-light);  
    }  
  
    a {  
      text-decoration: none;  
      color: inherit;  
      transition: var(--transition);  
    }  
  
    .container {  
      width: 100%;  
      max-width: 1200px;  
      margin: 0 auto;  
      padding: 0 1.5rem;  
    }  
  
    .btn {  
      display: inline-block;  
      padding: 1rem 2rem;  
      background: linear-gradient(135deg, var(--accent-orange), #e67e00);  
      color: var(--white);  
      border: none;  
      border-radius: 50px;  
      font-weight: 600;  
      font-size: 1rem;  
      text-transform: uppercase;  
      letter-spacing: 0.5px;  
      cursor: pointer;  
      transition: var(--transition);  
      box-shadow: var(--shadow-md);  
    }  
  
    .btn:hover {  
      transform: translateY(-3px);  
      box-shadow: var(--shadow-lg);  
    }  
  
    section {  
      padding: 5rem 0;  
    }  
  
    /* Header */  
    header {  
      background-color: rgba(255, 255, 255, 0.95);  
      backdrop-filter: blur(10px);  
      position: fixed;  
      top: 0;  
      width: 100%;  
      z-index: 1000;  
      box-shadow: var(--shadow-sm);  
      padding: 1rem 0;  
    }  
  
    .navbar {  
      display: flex;  
      justify-content: space-between;  
      align-items: center;  
    }  
  
    .logo {  
      font-size: 1.8rem;  
      font-weight: 900;  
      background: linear-gradient(135deg, var(--primary-dark), var(--accent-orange));  
      -webkit-background-clip: text;  
      -webkit-text-fill-color: transparent;  
      background-clip: text;  
    }  
  
    .nav-links {  
      display: flex;  
      gap: 2rem;  
    }  
  
    .nav-links a {  
      font-weight: 600;  
      position: relative;  
    }  
  
    .nav-links a:after {  
      content: '';  
      position: absolute;  
      bottom: -5px;  
      left: 0;  
      width: 0;  
      height: 2px;  
      background: var(--accent-orange);  
      transition: var(--transition);  
    }  
  
    .nav-links a:hover:after {  
      width: 100%;  
    }  
  
    .mobile-toggle {  
      display: none;  
      font-size: 1.5rem;  
      cursor: pointer;  
    }  
  
    /* Hero */  
    #hero {  
      background: linear-gradient(135deg, var(--primary-dark), #1a3a8f);  
      color: var(--white);  
      padding: 10rem 0 6rem;  
      position: relative;  
      overflow: hidden;  
    }  
  
    .hero-content {  
      max-width: 700px;  
      position: relative;  
      z-index: 2;  
    }  
  
    .hero-content p {  
      font-size: 1.2rem;  
      margin-bottom: 2rem;  
      color: rgba(255, 255, 255, 0.9);  
    }  
  
    /* About */  
    #about {  
      background-color: var(--light-gray);  
    }  
  
    .about-content {  
      display: grid;  
      grid-template-columns: 1fr 1fr;  
      gap: 3rem;  
      align-items: center;  
    }  
  
    .about-text ul {  
      margin: 1.5rem 0;  
      padding-left: 1.5rem;  
    }  
  
    .about-text li {  
      margin-bottom: 0.8rem;  
      position: relative;  
    }  
  
    .about-text li:before {  
      content: '✓';  
      color: var(--accent-orange);  
      font-weight: bold;  
      position: absolute;  
      left: -1.5rem;  
    }  
  
    /* Services */  
    .services-grid {  
      display: grid;  
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));  
      gap: 2rem;  
    }  
  
    .service-card {  
      background: var(--white);  
      border-radius: 15px;  
      padding: 2rem;  
      box-shadow: var(--shadow-md);  
      transition: var(--transition);  
      border-top: 3px solid var(--accent-orange);  
    }  
  
    .service-card:hover {  
      transform: translateY(-10px);  
      box-shadow: var(--shadow-lg);  
    }  
  
    .service-icon {  
      font-size: 2.5rem;  
      margin-bottom: 1rem;  
      background: linear-gradient(135deg, var(--primary-dark), var(--accent-orange));  
      -webkit-background-clip: text;  
      -webkit-text-fill-color: transparent;  
      background-clip: text;  
    }  
  
    /* Contact */  
    .contact-container {  
      display: grid;  
      grid-template-columns: 1fr 1fr;  
      gap: 3rem;  
    }  
  
    .contact-form .form-group {  
      margin-bottom: 1.5rem;  
    }  
  
    .contact-form label {  
      display: block;  
      margin-bottom: 0.5rem;  
      font-weight: 600;  
    }  
  
    .contact-form input,  
    .contact-form textarea {  
      width: 100%;  
      padding: 0.8rem;  
      border: 1px solid #ddd;  
      border-radius: 8px;  
      font-family: 'Montserrat', sans-serif;  
    }  
  
    .contact-form textarea {  
      height: 120px;  
      resize: vertical;  
    }  
  
    .contact-item {  
      display: flex;  
      align-items: flex-start;  
      gap: 1rem;  
      margin-bottom: 1.5rem;  
    }  
  
    .contact-icon {  
      background: var(--primary-dark);  
      color: var(--white);  
      width: 45px;  
      height: 45px;  
      border-radius: 50%;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      flex-shrink: 0;  
      font-weight: bold;  
    }  
  
    /* Footer */  
    footer {  
      background-color: var(--primary-dark);  
      color: var(--white);  
      padding: 4rem 0 2rem;  
    }  
  
    .footer-content {  
      display: grid;  
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));  
      gap: 2rem;  
      margin-bottom: 2rem;  
    }  
  
    .footer-column h3 {  
      font-size: 1.3rem;  
      margin-bottom: 1.5rem;  
      color: var(--accent-orange);  
    }  
  
    .footer-links li {  
      margin-bottom: 0.8rem;  
    }  
  
    .footer-links a {  
      color: rgba(255, 255, 255, 0.7);  
    }  
  
    .footer-links a:hover {  
      color: var(--accent-orange);  
      padding-left: 5px;  
    }  
  
    .social-links {  
      display: flex;  
      gap: 1rem;  
      margin-top: 1rem;  
    }  
  
    .social-links a {  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      width: 40px;  
      height: 40px;  
      background: rgba(255, 255, 255, 0.1);  
      border-radius: 50%;  
    }  
  
    .social-links a:hover {  
      background: var(--accent-orange);  
      transform: translateY(-3px);  
    }  
  
    .copyright {  
      text-align: center;  
      padding-top: 2rem;  
      border-top: 1px solid rgba(255, 255, 255, 0.1);  
      color: rgba(255, 255, 255, 0.6);  
      font-size: 0.9rem;  
    }  
  
    /* Responsive */  
    @media (max-width: 992px) {  
      .about-content,  
      .contact-container {  
        grid-template-columns: 1fr;  
        gap: 2rem;  
      }  
    }  
  
    @media (max-width: 768px) {  
      .nav-links {  
        display: none;  
        position: absolute;  
        top: 100%;  
        left: 0;  
        width: 100%;  
        background: var(--white);  
        flex-direction: column;  
        gap: 1rem;  
        padding: 1rem;  
        box-shadow: var(--shadow-md);  
      }  
  
      .mobile-toggle {  
        display: block;  
      }  
  
      h2:after {  
        width: 40px;  
      }  
    }  
  </style>  
</head>  
<body>  
  {{ content_for_layout }}  
  
  <!-- Header -->  
  <header>  
    <div class="container">  
      <nav class="navbar">  
        <div class="logo">Barka Digit</div>  
        <ul class="nav-links">  
          <li><a href="#hero">Accueil</a></li>  
          <li><a href="#about">À propos</a></li>  
          <li><a href="#services">Services</a></li>  
          <li><a href="#contact">Contact</a></li>  
        </ul>  
        <div class="mobile-toggle">☰</div>  
      </nav>  
    </div>  
  </header>  
  
  <!-- Hero Section -->  
  <section id="hero">  
    <div class="container">  
      <div class="hero-content">  
        <h1>Barka Digit</h1>  
        <p>Le digital au service de l'Afrique</p>  
        <a href="https://wa.me/22798174737" target="_blank" class="btn">Discutons de votre projet</a>  
      </div>  
    </div>  
  </section>  
  
  <!-- About Section -->  
  <section id="about">  
    <div class="container">  
      <div class="about-content">  
        <div>  
          <h2>À propos de nous</h2>  
          <p>Barka Digit est un groupe digital basé à Niamey, au Niger. Notre bureau se situe à Bobiel, Station Sahara, sur la voie qui mène vers le CEG35.</p>  
          <p>Voici nos domaines d'expertise :</p>  
          <ul>  
            <li>E-commerce : création et gestion de boutiques en ligne</li>  
            <li>Publicité digitale : campagnes Facebook</li>  
            <li>Création de vidéos publicitaires</li>  
            <li>Formations : e-commerce, marketing digital, montage</li>  
            <li>Placement de marketeurs qualifiés</li>  
            <li>Vente de produits numériques (guides, outils, services)</li>  
          </ul>  
        </div>  
        <div>  
          <div style="background: linear-gradient(45deg, #0A2A66, #FF8C00); height: 350px; border-radius: 15px;"></div>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <!-- Services Section -->  
  <section id="services">  
    <div class="container">  
      <h2>Nos Services</h2>  
      <div class="services-grid">  
        <div class="service-card">  
          <div class="service-icon">[E]</div>  
          <h3>E-commerce</h3>  
          <p>Création et gestion complète de boutiques en ligne performantes avec solutions de paiement sécurisées.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">[P]</div>  
          <h3>Publicité Digitale</h3>  
          <p>Campagnes publicitaires ciblées sur Facebook et Instagram pour maximiser votre retour sur investissement.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">[V]</div>  
          <h3>Création de Vidéos</h3>  
          <p>Production de vidéos publicitaires professionnelles pour valoriser votre marque et vos produits.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">[F]</div>  
          <h3>Formations</h3>  
          <p>Programmes de formation pratique en e-commerce, marketing digital et montage vidéo pour entrepreneurs.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">[M]</div>  
          <h3>Placement</h3>  
          <p>Mise en relation avec des marketeurs qualifiés pour renforcer vos équipes et booster vos ventes.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">[D]</div>  
          <h3>Produits Numériques</h3>  
          <p>Vente de guides, outils et services numériques conçus pour accélérer la croissance de votre business.</p>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <!-- Contact Section -->  
  <section id="contact">  
    <div class="container">  
      <h2>Contactez-nous</h2>  
      <div class="contact-container">  
        <div class="contact-form">  
          <form id="contactForm">  
            <div class="form-group">  
              <label for="name">Nom</label>  
              <input type="text" id="name" required>  
            </div>  
            <div class="form-group">  
              <label for="email">Email</label>  
              <input type="email" id="email" required>  
            </div>  
            <div class="form-group">  
              <label for="message">Message</label>  
              <textarea id="message" required></textarea>  
            </div>  
            <button type="submit" class="btn">Envoyer</button>  
          </form>  
        </div>  
        <div class="contact-info">  
          <h3>Coordonnées</h3>  
          <div class="contact-item">  
            <div class="contact-icon">[T]</div>  
            <div>  
              <strong>WhatsApp</strong><br>  
              <a href="https://wa.me/22798174737" target="_blank">+227 98 17 47 37</a>  
            </div>  
          </div>  
          <div class="contact-item">  
            <div class="contact-icon">[M]</div>  
            <div>  
              <strong>Email</strong><br>  
              <a href="mailto:contactbarkadigit@gmail.com">contactbarkadigit@gmail.com</a>  
            </div>  
          </div>  
          <div class="contact-item">  
            <div class="contact-icon">[L]</div>  
            <div>  
              <strong>Adresse</strong><br>  
              Bobiel, Station Sahara, vers CEG35, Niamey  
            </div>  
          </div>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <!-- Footer -->  
  <footer>  
    <div class="container">  
      <div class="footer-content">  
        <div class="footer-column">  
          <h3>Barka Digit</h3>  
          <p>Le digital au service de l'Afrique</p>  
          <div class="social-links">  
            <a href="https://www.facebook.com/share/1JBq9FrcDF/" target="_blank">f</a>  
            <a href="https://wa.me/22798174737" target="_blank">w</a>  
          </div>  
        </div>  
        <div class="footer-column">  
          <h3>Liens rapides</h3>  
          <ul class="footer-links">  
            <li><a href="#hero">Accueil</a></li>  
            <li><a href="#about">À propos</a></li>  
            <li><a href="#services">Services</a></li>  
            <li><a href="#contact">Contact</a></li>  
          </ul>  
        </div>  
      </div>  
      <div class="copyright">  
        © Barka Digit 2025 – Tous droits réservés  
      </div>  
    </div>  
  </footer>  
  
  <script>  
    // Mobile menu toggle  
    document.querySelector('.mobile-toggle').addEventListener('click', function() {  
      const navLinks = document.querySelector('.nav-links');  
      navLinks.style.display = navLinks.style.display === 'flex' ? 'none' : 'flex';  
    });  
  
    // Form submission  
    document.getElementById('contactForm').addEventListener('submit', function(e) {  
      e.preventDefault();  
      alert('Merci pour votre message ! Nous vous répondrons dans les plus brefs délais.');  
      this.reset();  
    });  
  
    // Smooth scrolling  
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {  
      anchor.addEventListener('click', function(e) {  
        e.preventDefault();  
        const target = document.querySelector(this.getAttribute('href'));  
        if (target) {  
          window.scrollTo({  
            top: target.offsetTop - 80,  
            behavior: 'smooth'  
          });  
        }  
      });  
    });  
  </script>  
</body>  
</html>  
  
  
  
  
  
  
<!DOCTYPE html>  
<html lang="fr">  
<head>  
  <meta charset="UTF-8">  
  <meta name="viewport" content="width=device-width, initial-scale=1">  
  <title>Barka Digit – Le digital au service de l’Afrique</title>  
  {{ content_for_header }}  
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&display=swap" rel="stylesheet">  
  <style>  
    :root {  
      --primary: #0A2A66;  
      --accent: #FF8C00;  
      --white: #ffffff;  
      --light: #f9f9f9;  
      --dark: #333333;  
      --gray: #666666;  
    }  
  
    * {  
      margin: 0;  
      padding: 0;  
      box-sizing: border-box;  
    }  
  
    body {  
      font-family: 'Poppins', sans-serif;  
      color: var(--dark);  
      line-height: 1.6;  
      background-color: var(--white);  
      overflow-x: hidden;  
    }  
  
    a {  
      text-decoration: none;  
      color: inherit;  
    }  
  
    ul {  
      list-style: none;  
    }  
  
    .container {  
      width: 90%;  
      max-width: 1200px;  
      margin: auto;  
    }  
  
    .btn {  
      display: inline-block;  
      background-color: var(--accent);  
      color: var(--white);  
      padding: 14px 28px;  
      border-radius: 4px;  
      font-weight: 600;  
      transition: background 0.3s ease;  
      border: none;  
      cursor: pointer;  
    }  
  
    .btn:hover {  
      background-color: #e07a00;  
    }  
  
    /* Header */  
    header {  
      background-color: var(--white);  
      padding: 20px 0;  
      position: sticky;  
      top: 0;  
      z-index: 1000;  
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);  
    }  
  
    .header-content {  
      display: flex;  
      justify-content: space-between;  
      align-items: center;  
    }  
  
    .logo {  
      font-size: 24px;  
      font-weight: 700;  
      color: var(--primary);  
    }  
  
    nav ul {  
      display: flex;  
      gap: 25px;  
    }  
  
    nav a {  
      font-weight: 500;  
      color: var(--dark);  
      transition: color 0.3s ease;  
    }  
  
    nav a:hover {  
      color: var(--accent);  
    }  
  
    /* Hero */  
    .hero {  
      background: linear-gradient(135deg, var(--primary), #0d3b8e);  
      color: var(--white);  
      padding: 100px 0;  
      text-align: center;  
    }  
  
    .hero h1 {  
      font-size: 2.8rem;  
      margin-bottom: 20px;  
    }  
  
    .hero p {  
      font-size: 1.2rem;  
      margin-bottom: 30px;  
      max-width: 700px;  
      margin-left: auto;  
      margin-right: auto;  
    }  
  
    /* Section */  
    section {  
      padding: 80px 0;  
    }  
  
    .section-title {  
      text-align: center;  
      margin-bottom: 50px;  
      font-size: 2rem;  
      color: var(--primary);  
    }  
  
    /* About */  
    .about-content {  
      max-width: 800px;  
      margin: auto;  
      text-align: center;  
      font-size: 1.1rem;  
    }  
  
    .expertise {  
      display: grid;  
      grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));  
      gap: 30px;  
      margin-top: 40px;  
    }  
  
    .expertise-item {  
      background: var(--light);  
      padding: 25px;  
      border-radius: 8px;  
      text-align: center;  
      transition: transform 0.3s ease;  
    }  
  
    .expertise-item:hover {  
      transform: translateY(-5px);  
    }  
  
    .expertise-item h3 {  
      margin: 15px 0;  
      color: var(--primary);  
    }  
  
    /* Services */  
    .services-grid {  
      display: grid;  
      grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));  
      gap: 30px;  
    }  
  
    .service-card {  
      background: var(--white);  
      border-radius: 8px;  
      padding: 30px;  
      box-shadow: 0 5px 15px rgba(0,0,0,0.05);  
      transition: box-shadow 0.3s ease;  
      text-align: center;  
    }  
  
    .service-card:hover {  
      box-shadow: 0 8px 25px rgba(0,0,0,0.1);  
    }  
  
    .service-icon {  
      font-size: 2.5rem;  
      color: var(--accent);  
      margin-bottom: 20px;  
    }  
  
    /* Contact */  
    .contact-wrapper {  
      display: flex;  
      flex-wrap: wrap;  
      gap: 40px;  
    }  
  
    .contact-form {  
      flex: 1;  
      min-width: 300px;  
    }  
  
    .contact-info {  
      flex: 1;  
      min-width: 300px;  
    }  
  
    .form-group {  
      margin-bottom: 20px;  
    }  
  
    .form-group input,  
    .form-group textarea {  
      width: 100%;  
      padding: 14px;  
      border: 1px solid #ddd;  
      border-radius: 4px;  
      font-family: inherit;  
    }  
  
    .contact-details {  
      background: var(--light);  
      padding: 25px;  
      border-radius: 8px;  
    }  
  
    .contact-details ul li {  
      margin-bottom: 15px;  
      display: flex;  
      align-items: center;  
    }  
  
    .contact-details ul li svg {  
      margin-right: 10px;  
      fill: var(--accent);  
      width: 20px;  
      height: 20px;  
    }  
  
    /* Footer */  
    footer {  
      background: var(--primary);  
      color: var(--white);  
      padding: 50px 0 20px;  
    }  
  
    .footer-content {  
      display: flex;  
      flex-wrap: wrap;  
      justify-content: space-between;  
      gap: 30px;  
      margin-bottom: 30px;  
    }  
  
    .footer-links h4,  
    .social h4 {  
      margin-bottom: 20px;  
      font-size: 1.2rem;  
    }  
  
    .footer-links ul li {  
      margin-bottom: 10px;  
    }  
  
    .social ul {  
      display: flex;  
      gap: 15px;  
    }  
  
    .social ul li a {  
      display: block;  
      width: 40px;  
      height: 40px;  
      background: rgba(255,255,255,0.1);  
      border-radius: 50%;  
      display: flex;  
      align-items: center;  
      justify-content: center;  
      transition: background 0.3s ease;  
    }  
  
    .social ul li a:hover {  
      background: var(--accent);  
    }  
  
    .copyright {  
      text-align: center;  
      padding-top: 20px;  
      border-top: 1px solid rgba(255,255,255,0.1);  
      font-size: 0.9rem;  
      opacity: 0.8;  
    }  
  
    /* Responsive */  
    @media(max-width: 768px) {  
      .hero h1 {  
        font-size: 2rem;  
      }  
  
      nav ul {  
        flex-direction: column;  
        gap: 10px;  
      }  
  
      .section-title {  
        font-size: 1.7rem;  
      }  
    }  
  </style>  
</head>  
<body>  
  
  <header>  
    <div class="container header-content">  
      <div class="logo">Barka Digit</div>  
      <nav>  
        <ul>  
          <li><a href="#accueil">Accueil</a></li>  
          <li><a href="#apropos">À propos</a></li>  
          <li><a href="#services">Services</a></li>  
          <li><a href="#contact">Contact</a></li>  
        </ul>  
      </nav>  
    </div>  
  </header>  
  
  <section class="hero" id="accueil">  
    <div class="container">  
      <h1>Le digital au service de l’Afrique</h1>  
      <p>Barka Digit conçoit des solutions numériques puissantes pour propulser votre entreprise vers l’avenir.</p>  
      <a href="https://wa.me/22798174737" target="_blank" class="btn">Discutons de votre projet</a>  
    </div>  
  </section>  
  
  <section id="apropos">  
    <div class="container">  
      <h2 class="section-title">À propos de nous</h2>  
      <div class="about-content">  
        <p>Barka Digit est un groupe digital basé à Niamey, au Niger.<br>  
        Notre bureau se situe à Bobiel, Station Sahara, sur la voie qui mène vers le CEG35.</p>  
  
        <div class="expertise">  
          <div class="expertise-item">  
            <strong>E-commerce</strong>  
            <p>Création et gestion de boutiques en ligne performantes</p>  
          </div>  
          <div class="expertise-item">  
            <strong>Publicité digitale</strong>  
            <p>Campagnes ciblées sur Facebook et réseaux sociaux</p>  
          </div>  
          <div class="expertise-item">  
            <strong>Vidéo publicitaire</strong>  
            <p>Production de contenus vidéo percutants</p>  
          </div>  
          <div class="expertise-item">  
            <strong>Formations</strong>  
            <p>E-commerce, marketing digital, montage vidéo</p>  
          </div>  
          <div class="expertise-item">  
            <strong>Marketplace</strong>  
            <p>Placement de marketeurs qualifiés</p>  
          </div>  
          <div class="expertise-item">  
            <strong>Produits numériques</strong>  
            <p>Vente de guides, outils et services digitaux</p>  
          </div>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <section id="services" style="background-color: #f5f7fa;">  
    <div class="container">  
      <h2 class="section-title">Nos Services</h2>  
      <div class="services-grid">  
        <div class="service-card">  
          <div class="service-icon">🛒</div>  
          <h3>E-commerce</h3>  
          <p>Conception et gestion de boutiques en ligne sur mesure pour vendre 24h/24.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">📣</div>  
          <h3>Publicité Digitale</h3>  
          <p>Campagnes optimisées pour toucher votre audience cible sur Facebook et Instagram.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">🎥</div>  
          <h3>Vidéo Publicitaire</h3>  
          <p>Création de vidéos impactantes pour promouvoir vos produits et services.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">🎓</div>  
          <h3>Formations</h3>  
          <p>Programmes complets pour maîtriser l’e-commerce, le marketing digital et le montage.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">👥</div>  
          <h3>Talents Marketeurs</h3>  
          <p>Mise en relation avec des professionnels qualifiés pour booster vos projets.</p>  
        </div>  
        <div class="service-card">  
          <div class="service-icon">📦</div>  
          <h3>Produits Numériques</h3>  
          <p>Vente de guides, outils et services digitaux pour entrepreneurs africains.</p>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <section id="contact">  
    <div class="container">  
      <h2 class="section-title">Contactez-nous</h2>  
      <div class="contact-wrapper">  
        <div class="contact-form">  
          <form>  
            <div class="form-group">  
              <input type="text" placeholder="Votre nom" required>  
            </div>  
            <div class="form-group">  
              <input type="email" placeholder="Votre email" required>  
            </div>  
            <div class="form-group">  
              <textarea rows="5" placeholder="Votre message" required></textarea>  
            </div>  
            <button type="submit" class="btn">Envoyer</button>  
          </form>  
        </div>  
        <div class="contact-info">  
          <div class="contact-details">  
            <ul>  
              <li>  
                <svg viewBox="0 0 24 24"><path d="M20.01 15.38c-1.23 0-2.42-.2-3.53-.56-.35-.12-.74-.03-1.01.24l-1.57 1.97c-2.83-1.35-5.48-3.9-6.89-6.83l1.95-1.66c.27-.28.35-.67.24-1.02-.37-1.11-.56-2.3-.56-3.53 0-.54-.45-.99-.99-.99H4.19C3.65 3 3 3.24 3 3.99 3 13.28 10.73 21 20.01 21c.71 0 .99-.63.99-1.18v-3.45c0-.54-.45-.99-.99-.99z"/></svg>  
                <a href="https://wa.me/22798174737" target="_blank">+227 98 17 47 37 (WhatsApp)</a>  
              </li>  
              <li>  
                <svg viewBox="0 0 24 24"><path d="M20 4H4c-1.1 0-1.99.9-1.99 2L2 18c0 1.1.9 2 2 2h16c1.1 0 2-.9 2-2V6c0-1.1-.9-2-2-2zm0 4l-8 5-8-5V6l8 5 8-5v2z"/></svg>  
                <a href="mailto:contactbarkadigit@gmail.com">contactbarkadigit@gmail.com</a>  
              </li>  
              <li>  
                <svg viewBox="0 0 24 24"><path d="M12 2C8.13 2 5 5.13 5 9c0 5.25 7 13 7 13s7-7.75 7-13c0-3.87-3.13-7-7-7zm0 9.5a2.5 2.5 0 0 1 0-5 2.5 2.5 0 0 1 0 5z"/></svg>  
                Bobiel, Station Sahara, vers CEG35, Niamey  
              </li>  
            </ul>  
          </div>  
        </div>  
      </div>  
    </div>  
  </section>  
  
  <footer>  
    <div class="container">  
      <div class="footer-content">  
        <div class="footer-links">  
          <h4>Liens rapides</h4>  
          <ul>  
            <li><a href="#accueil">Accueil</a></li>  
            <li><a href="#services">Services</a></li>  
            <li><a href="#contact">Contact</a></li>  
          </ul>  
        </div>  
        <div class="social">  
          <h4>Suivez-nous</h4>  
          <ul>  
            <li><a href="https://www.facebook.com/share/1JBq9FrcDF/" target="_blank">f</a></li>  
            <li><a href="https://wa.me/22798174737" target="_blank">w</a></li>  
          </ul>  
        </div>  
      </div>  
      <div class="copyright">  
        © Barka Digit 2025 – Tous droits réservés  
      </div>  
    </div>  
  </footer>  
  
  {{ content_for_layout }}  
  
</body>  
</html>

Dis moi quel code choisir entre ces deux qu'il a généré 
