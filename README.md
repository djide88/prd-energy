# prd-energy
<!DOCTYPE html>
<html lang="fr">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>PRD ENERGY | Solutions énergétiques</title>

  <style>
    :root {
      --green: #1d6b57;
      --light-green: #e9f5ef;
      --dark: #102a2a;
      --text: #5d6c6c;
      --white: #ffffff;
      --yellow: #d9ec67;
    }

    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
    }

    body {
      font-family: Arial, Helvetica, sans-serif;
      color: var(--dark);
      background: #ffffff;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    .container {
      width: 90%;
      max-width: 1180px;
      margin: auto;
    }

    header {
      position: sticky;
      top: 0;
      z-index: 10;
      background: rgba(255, 255, 255, 0.96);
      border-bottom: 1px solid #edf1ef;
    }

    .navbar {
      height: 78px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      color: var(--green);
      font-size: 24px;
      font-weight: 800;
      letter-spacing: 1px;
    }

    .logo span {
      color: var(--dark);
    }

    .nav-links {
      display: flex;
      gap: 30px;
      align-items: center;
      list-style: none;
      font-size: 14px;
      font-weight: bold;
    }

    .nav-links a:hover {
      color: var(--green);
    }

    .nav-button,
    .button {
      display: inline-block;
      border: none;
      cursor: pointer;
      font-weight: bold;
      border-radius: 30px;
      padding: 14px 22px;
    }

    .nav-button,
    .button-primary {
      color: white;
      background: var(--green);
    }

    .button-primary:hover {
      background: #155341;
    }

    .button-light {
      color: var(--dark);
      background: white;
    }

    .hero {
      color: white;
      padding: 125px 0;
      background:
        linear-gradient(110deg, rgba(16, 42, 42, 0.94), rgba(29, 107, 87, 0.72)),
        url("https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=1800&q=85")
        center/cover;
    }

    .hero-content {
      max-width: 720px;
    }

    .tag {
      display: inline-block;
      color: var(--yellow);
      background: rgba(217, 236, 103, 0.18);
      padding: 8px 15px;
      border-radius: 30px;
      font-size: 13px;
      font-weight: bold;
      margin-bottom: 22px;
    }

    .hero h1 {
      font-size: clamp(42px, 6vw, 76px);
      line-height: 1.05;
      margin-bottom: 25px;
    }

    .hero h1 span {
      color: var(--yellow);
    }

    .hero p {
      max-width: 590px;
      color: #e2eeee;
      font-size: 18px;
      margin-bottom: 35px;
    }

    .hero-buttons {
      display: flex;
      gap: 15px;
      flex-wrap: wrap;
    }

    section {
      padding: 90px 0;
    }

    .section-title {
      max-width: 650px;
      margin-bottom: 45px;
    }

    .section-title small {
      color: var(--green);
      font-weight: bold;
      text-transform: uppercase;
      letter-spacing: 2px;
    }

    .section-title h2 {
      font-size: 42px;
      line-height: 1.15;
      margin: 12px 0 18px;
    }

    .section-title p {
      color: var(--text);
    }

    .services {
      background: var(--light-green);
    }

    .service-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 22px;
    }

    .service-card {
      padding: 30px;
      background: white;
      border-radius: 18px;
      border: 1px solid #e0eee7;
    }

    .service-card .icon {
      color: var(--green);
      font-size: 34px;
      margin-bottom: 18px;
    }

    .service-card h3 {
      margin-bottom: 12px;
    }

    .service-card p {
      color: var(--text);
      font-size: 15px;
    }

    .about-wrapper {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 60px;
      align-items: center;
    }

    .about-image {
      min-height: 430px;
      border-radius: 22px;
      background:
        linear-gradient(rgba(29, 107, 87, 0.12), rgba(29, 107, 87, 0.12)),
        url("https://images.unsplash.com/photo-1621905251189-08b45d6a269e?auto=format&fit=crop&w=1000&q=85")
        center/cover;
    }

    .about-text p {
      color: var(--text);
      margin-bottom: 20px;
    }

    .about-list {
      list-style: none;
      margin: 25px 0;
    }

    .about-list li {
      margin-bottom: 12px;
      font-weight: bold;
    }

    .about-list li::before {
      content: "✓";
      color: var(--green);
      margin-right: 10px;
    }

    .contact {
      background: #f7faf8;
    }

    .contact-wrapper {
      display: grid;
      grid-template-columns: 0.9fr 1.1fr;
      gap: 70px;
      align-items: start;
    }

    .contact-info {
      display: grid;
      gap: 18px;
    }

    .contact-info div {
      padding: 18px;
      border-left: 4px solid var(--green);
      background: white;
      border-radius: 8px;
    }

    .contact-info strong {
      display: block;
      margin-bottom: 5px;
    }

    .contact-info a {
      color: var(--green);
    }

    form {
      display: grid;
      gap: 15px;
      padding: 35px;
      background: white;
      border-radius: 18px;
      box-shadow: 0 8px 30px rgba(16, 42, 42, 0.08);
    }

    form h3 {
      font-size: 26px;
      margin-bottom: 8px;
    }

    .form-grid {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 15px;
    }

    input,
    select,
    textarea {
      width: 100%;
      border: 1px solid #d9e4df;
      border-radius: 8px;
      padding: 14px;
      font: inherit;
      outline: none;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: var(--green);
    }

    textarea {
      min-height: 140px;
      resize: vertical;
    }

    footer {
      padding: 25px 0;
      color: #d9e8e2;
      background: var(--dark);
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      gap: 20px;
      font-size: 14px;
    }

    @media (max-width: 800px) {
      .nav-links {
        display: none;
      }

      .service-grid,
      .about-wrapper,
      .contact-wrapper {
        grid-template-columns: 1fr;
      }

      .hero {
        padding: 90px 0;
      }

      .section-title h2 {
        font-size: 34px;
      }

      .form-grid {
        grid-template-columns: 1fr;
      }

      .footer-content {
        flex-direction: column;
      }
    }
  </style>
</head>

<body>

  <header>
    <div class="container navbar">
      <a href="#" class="logo">PRD <span>ENERGY</span></a>

      <nav>
        <ul class="nav-links">
          <li><a href="#services">Services</a></li>
          <li><a href="#entreprise">Entreprise</a></li>
          <li><a href="#contact">Contact</a></li>
          <li>
            <a href="#contact" class="nav-button">Demander un devis</a>
          </li>
        </ul>
      </nav>
    </div>
  </header>

  <main>

    <section class="hero">
      <div class="container">
        <div class="hero-content">
          <span class="tag">FROID • CLIMATISATION • CVC</span>

          <h1>
            Des solutions fiables pour votre
            <span>confort énergétique.</span>
          </h1>

          <p>
            PRD ENERGY accompagne les professionnels et les particuliers
            dans leurs projets de froid, climatisation, chauffage,
            ventilation et performance énergétique.
          </p>

          <div class="hero-buttons">
            <a href="#contact" class="button button-light">
              Parlons de votre projet
            </a>

            <a href="#services" class="button button-primary">
              Découvrir nos services
            </a>
          </div>
        </div>
      </div>
    </section>

    <section class="services" id="services">
      <div class="container">
        <div class="section-title">
          <small>Nos expertises</small>
          <h2>Des solutions CVC adaptées à vos besoins.</h2>
          <p>
            Une approche professionnelle pour améliorer le confort,
            la performance et la maîtrise de vos installations.
          </p>
        </div>

        <div class="service-grid">
          <article class="service-card">
            <div class="icon">❄</div>
            <h3>Froid industriel</h3>
            <p>
              Étude et accompagnement de vos installations frigorifiques
              professionnelles et industrielles.
            </p>
          </article>

          <article class="service-card">
            <div class="icon">✦</div>
            <h3>Climatisation</h3>
            <p>
              Des solutions de climatisation efficaces pour vos locaux,
              bureaux, commerces et habitations.
            </p>
          </article>

          <article class="service-card">
            <div class="icon">♨</div>
            <h3>Chauffage & ventilation</h3>
            <p>
              Optimisation du chauffage et de la qualité de l'air
              grâce à des systèmes adaptés.
            </p>
          </article>
        </div>
      </div>
    </section>

    <section id="entreprise">
      <div class="container about-wrapper">
        <div class="about-image"></div>

        <div class="about-text">
          <div class="section-title">
            <small>PRD ENERGY</small>
            <h2>Votre partenaire technique en énergie.</h2>
          </div>

          <p>
            Nous vous accompagnons dans l'étude, l'analyse et l'amélioration
            de vos installations de froid, climatisation et CVC.
          </p>

          <p>
            Notre objectif est de vous proposer des solutions fiables,
            performantes et adaptées à votre activité.
          </p>

          <ul class="about-list">
            <li>Conseils personnalisés</li>
            <li>Solutions adaptées à vos besoins</li>
            <li>Accompagnement professionnel</li>
            <li>Étude de vos projets énergétiques</li>
          </ul>

          <a href="#contact" class="button button-primary">
            Échanger sur votre projet
          </a>
        </div>
      </div>
    </section>

    <section class="contact" id="contact">
      <div class="container contact-wrapper">

        <div>
          <div class="section-title">
            <small>Contact</small>
            <h2>Un projet ? Parlons-en.</h2>
            <p>
              Contactez PRD ENERGY pour obtenir des informations
              ou demander un devis personnalisé.
            </p>
          </div>

          <div class="contact-info">
            <div>
              <strong>Téléphone</strong>
              <a href="tel:+33648882646">06 48 88 26 46</a>
            </div>

            <div>
              <strong>Email</strong>
              <a href="mailto:parfaitdjino@yahoo.fr">
                parfaitdjino@yahoo.fr
              </a>
            </div>

            <div>
              <strong>Adresse</strong>
              30 rue de la 8ème, 60200 Compiègne
            </div>
          </div>
        </div>

        <form action="mailto:parfaitdjino@yahoo.fr" method="post" enctype="text/plain">
          <h3>Demander un devis</h3>

          <div class="form-grid">
            <input
              type="text"
              name="Nom"
              placeholder="Votre nom"
              required
            >

            <input
              type="email"
              name="Email"
              placeholder="Votre adresse e-mail"
              required
            >
          </div>

          <input
            type="text"
            name="Entreprise"
            placeholder="Nom de votre entreprise"
          >

          <select name="Service" required>
            <option value="">Sélectionnez un service</option>
            <option>Froid industriel</option>
            <option>Climatisation</option>
            <option>Chauffage</option>
            <option>Ventilation</option>
            <option>Performance énergétique</option>
            <option>Autre demande</option>
          </select>

          <textarea
            name="Message"
            placeholder="Décrivez votre projet..."
            required
          ></textarea>

          <button type="submit" class="button button-primary">
            Envoyer ma demande
          </button>
        </form>

      </div>
    </section>

  </main>

  <footer>
    <div class="container footer-content">
      <div>© 2026 PRD ENERGY</div>
      <div>Froid · Climatisation · CVC · Énergie</div>
    </div>
  </footer>

</body>
</html>
