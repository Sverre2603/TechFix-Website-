<!DOCTYPE html>
<html lang="de">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <title>TechFix Fleckeby | Handy- & PC-Hilfe</title>

  <meta
    name="description"
    content="TechFix in Fleckeby – persönliche Hilfe bei Handy-, PC- und Technikproblemen."
  >

  <style>
    :root {
      --blue: #2563eb;
      --blue-dark: #1d4ed8;
      --dark: #0f172a;
      --text: #334155;
      --muted: #64748b;
      --light: #f8fafc;
      --border: #e2e8f0;
      --white: #ffffff;
      --green: #16a34a;
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
      color: var(--text);
      background: var(--white);
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    button,
    input,
    textarea {
      font: inherit;
    }

    .container {
      width: min(1120px, 92%);
      margin: 0 auto;
    }

    /* =========================
       NAVIGATION
    ========================= */

    header {
      position: sticky;
      top: 0;
      z-index: 1000;
      background: rgba(255,255,255,.92);
      backdrop-filter: blur(14px);
      border-bottom: 1px solid rgba(226,232,240,.8);
    }

    nav {
      min-height: 74px;
      display: flex;
      align-items: center;
      justify-content: space-between;
    }

    .logo {
      font-size: 1.55rem;
      font-weight: 900;
      letter-spacing: -1px;
    }

    .logo span {
      color: var(--blue);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 28px;
      list-style: none;
    }

    .nav-links a {
      color: var(--muted);
      font-weight: 700;
      font-size: .95rem;
      transition: .2s;
    }

    .nav-links a:hover {
      color: var(--blue);
    }

    .nav-cta {
      background: var(--blue);
      color: white !important;
      padding: 11px 18px;
      border-radius: 10px;
    }

    .nav-cta:hover {
      background: var(--blue-dark);
    }

    .menu-button {
      display: none;
      background: transparent;
      border: 0;
      font-size: 1.7rem;
      cursor: pointer;
    }

    /* =========================
       HERO
    ========================= */

    .hero {
      overflow: hidden;
      padding: 105px 0 90px;
      background:
        radial-gradient(
          circle at 80% 15%,
          rgba(37,99,235,.16),
          transparent 32%
        ),
        linear-gradient(180deg, #fff 0%, #f8fafc 100%);
    }

    .hero-grid {
      display: grid;
      grid-template-columns: 1.1fr .9fr;
      align-items: center;
      gap: 70px;
    }

    .badge {
      display: inline-flex;
      align-items: center;
      gap: 7px;
      padding: 7px 13px;
      border-radius: 999px;
      background: #eff6ff;
      color: var(--blue);
      font-size: .85rem;
      font-weight: 800;
      margin-bottom: 22px;
    }

    h1 {
      color: var(--dark);
      font-size: clamp(2.8rem, 6vw, 5rem);
      line-height: 1.02;
      letter-spacing: -3px;
      margin-bottom: 25px;
    }

    h1 span {
      color: var(--blue);
    }

    .hero-text {
      max-width: 650px;
      color: var(--muted);
      font-size: 1.15rem;
      margin-bottom: 32px;
    }

    .buttons {
      display: flex;
      flex-wrap: wrap;
      gap: 13px;
    }

    .button {
      display: inline-flex;
      justify-content: center;
      align-items: center;
      gap: 8px;
      padding: 14px 21px;
      border-radius: 11px;
      font-weight: 800;
      transition: .2s;
      cursor: pointer;
    }

    .button-primary {
      background: var(--blue);
      color: white;
      box-shadow: 0 10px 25px rgba(37,99,235,.2);
    }

    .button-primary:hover {
      background: var(--blue-dark);
      transform: translateY(-2px);
    }

    .button-secondary {
      background: white;
      color: var(--dark);
      border: 1px solid var(--border);
    }

    .button-secondary:hover {
      border-color: var(--blue);
      color: var(--blue);
    }

    .hero-card {
      position: relative;
      background: var(--dark);
      color: white;
      padding: 38px;
      border-radius: 28px;
      box-shadow: 0 30px 70px rgba(15,23,42,.18);
    }

    .hero-card::before {
      content: "";
      position: absolute;
      width: 100px;
      height: 100px;
      border-radius: 50%;
      background: rgba(37,99,235,.35);
      filter: blur(35px);
      right: 20px;
      top: 20px;
    }

    .hero-icon {
      position: relative;
      font-size: 3rem;
      margin-bottom: 20px;
    }

    .hero-card h2,
    .hero-card p,
    .check-list {
      position: relative;
    }

    .hero-card h2 {
      font-size: 1.8rem;
      margin-bottom: 10px;
    }

    .hero-card p {
      color: #cbd5e1;
      margin-bottom: 24px;
    }

    .check {
      display: flex;
      gap: 10px;
      margin: 11px 0;
      color: #e2e8f0;
    }

    .check span {
      color: #60a5fa;
      font-weight: 900;
    }

    /* =========================
       GENERAL SECTIONS
    ========================= */

    section {
      padding: 90px 0;
    }

    .section-heading {
      max-width: 680px;
      text-align: center;
      margin: 0 auto 50px;
    }

    .section-heading h2 {
      color: var(--dark);
      font-size: clamp(2rem, 4vw, 3rem);
      letter-spacing: -1.5px;
      margin-bottom: 12px;
    }

    .section-heading p {
      color: var(--muted);
      font-size: 1.05rem;
    }

    /* =========================
       SERVICES
    ========================= */

    .services {
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 20px;
    }

    .service-card {
      padding: 30px;
      border: 1px solid var(--border);
      border-radius: 20px;
      background: white;
      transition: .25s;
    }

    .service-card:hover {
      transform: translateY(-5px);
      box-shadow: 0 20px 45px rgba(15,23,42,.08);
      border-color: #bfdbfe;
    }

    .service-icon {
      width: 54px;
      height: 54px;
      display: grid;
      place-items: center;
      background: #eff6ff;
      border-radius: 14px;
      font-size: 1.5rem;
      margin-bottom: 18px;
    }

    .service-card h3 {
      color: var(--dark);
      margin-bottom: 8px;
      font-size: 1.25rem;
    }

    .service-card p {
      color: var(--muted);
    }

    /* =========================
       PRICES
    ========================= */

    .pricing {
      background: var(--light);
    }

    .price-grid {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 20px;
    }

    .price-card {
      position: relative;
      background: white;
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 32px;
    }

    .price-card.featured {
      border: 2px solid var(--blue);
      transform: translateY(-7px);
      box-shadow: 0 20px 45px rgba(37,99,235,.1);
    }

    .popular {
      position: absolute;
      top: -14px;
      left: 24px;
      background: var(--blue);
      color: white;
      padding: 5px 12px;
      border-radius: 999px;
      font-size: .75rem;
      font-weight: 800;
    }

    .price-card h3 {
      color: var(--dark);
      margin-bottom: 10px;
      font-size: 1.3rem;
    }

    .price {
      color: var(--dark);
      font-size: 2.3rem;
      font-weight: 900;
      margin-bottom: 20px;
    }

    .price small {
      color: var(--muted);
      font-size: .85rem;
      font-weight: 500;
    }

    .features {
      list-style: none;
      margin-bottom: 25px;
      color: var(--muted);
    }

    .features li {
      margin: 9px 0;
    }

    /* =========================
       ABOUT
    ========================= */

    .about {
      background: white;
    }

    .about-grid {
      display: grid;
      grid-template-columns: .9fr 1.1fr;
      gap: 60px;
      align-items: center;
    }

    .about-box {
      background: var(--dark);
      color: white;
      padding: 45px;
      border-radius: 25px;
    }

    .about-box .big-icon {
      font-size: 3.5rem;
      margin-bottom: 15px;
    }

    .about-box h3 {
      font-size: 1.7rem;
      margin-bottom: 10px;
    }

    .about-box p {
      color: #cbd5e1;
    }

    .about-text h2 {
      color: var(--dark);
      font-size: 2.5rem;
      line-height: 1.1;
      margin-bottom: 18px;
    }

    .about-text p {
      color: var(--muted);
      margin-bottom: 15px;
    }

    /* =========================
       CONTACT
    ========================= */

    .contact {
      background: var(--light);
    }

    .contact-grid {
      display: grid;
      grid-template-columns: .8fr 1.2fr;
      gap: 55px;
      align-items: start;
    }

    .contact-info h2 {
      color: var(--dark);
      font-size: 2.5rem;
      line-height: 1.1;
      margin-bottom: 15px;
    }

    .contact-info > p {
      color: var(--muted);
      margin-bottom: 28px;
    }

    .contact-item {
      display: flex;
      gap: 14px;
      margin: 20px 0;
    }

    .contact-icon {
      width: 45px;
      height: 45px;
      flex-shrink: 0;
      display: grid;
      place-items: center;
      background: #dbeafe;
      border-radius: 12px;
    }

    .contact-item strong {
      display: block;
      color: var(--dark);
    }

    .contact-item p {
      color: var(--muted);
    }

    form {
      background: white;
      border: 1px solid var(--border);
      border-radius: 22px;
      padding: 32px;
      box-shadow: 0 15px 40px rgba(15,23,42,.06);
    }

    .form-group {
      margin-bottom: 17px;
    }

    label {
      display: block;
      color: var(--dark);
      font-weight: 800;
      font-size: .9rem;
      margin-bottom: 7px;
    }

    input,
    textarea {
      width: 100%;
      border: 1px solid var(--border);
      border-radius: 10px;
      padding: 13px 14px;
      outline: none;
      transition: .2s;
      background: white;
    }

    input:focus,
    textarea:focus {
      border-color: var(--blue);
      box-shadow: 0 0 0 3px rgba(37,99,235,.1);
    }

    textarea {
      min-height: 130px;
      resize: vertical;
    }

    form button {
      width: 100%;
      border: 0;
    }

    /* =========================
       WHATSAPP BUTTON
    ========================= */

    .whatsapp {
      position: fixed;
      right: 22px;
      bottom: 22px;
      z-index: 999;
      display: flex;
      align-items: center;
      gap: 8px;
      background: var(--green);
      color: white;
      padding: 13px 17px;
      border-radius: 999px;
      font-weight: 800;
      box-shadow: 0 10px 30px rgba(22,163,74,.3);
      transition: .2s;
    }

    .whatsapp:hover {
      transform: translateY(-3px);
      background: #15803d;
    }

    /* =========================
       FOOTER
    ========================= */

    footer {
      background: var(--dark);
      color: white;
      padding: 35px 0;
    }

    .footer-content {
      display: flex;
      justify-content: space-between;
      align-items: center;
      gap: 20px;
    }

    footer p {
      color: #94a3b8;
      font-size: .9rem;
    }

    /* =========================
       MOBILE
    ========================= */

    @media (max-width: 850px) {

      .menu-button {
        display: block;
      }

      .nav-links {
        display: none;
        position: absolute;
        top: 74px;
        left: 0;
        width: 100%;
        padding: 20px;
        background: white;
        border-bottom: 1px solid var(--border);
        flex-direction: column;
        gap: 18px;
      }

      .nav-links.active {
        display: flex;
      }

      .hero {
        padding: 75px 0;
      }

      .hero-grid,
      .about-grid,
      .contact-grid {
        grid-template-columns: 1fr;
      }

      .services {
        grid-template-columns: 1fr;
      }

      .price-grid {
        grid-template-columns: 1fr;
      }

      .price-card.featured {
        transform: none;
      }

      .about-grid {
        gap: 35px;
      }
    }

    @media (max-width: 550px) {

      section {
        padding: 65px 0;
      }

      h1 {
        letter-spacing: -2px;
      }

      .buttons {
        flex-direction: column;
      }

      .button {
        width: 100%;
      }

      .hero-card,
      .about-box,
      form {
        padding: 26px;
      }

      .whatsapp {
        right: 14px;
        bottom: 14px;
      }

      .footer-content {
        flex-direction: column;
        text-align: center;
      }
    }
  </style>
</head>

<body>

  <!-- =========================
       NAVIGATION
  ========================== -->

  <header>
    <div class="container">

      <nav>

        <a href="#" class="logo">
          Tech<span>Fix</span>
        </a>

        <button
          class="menu-button"
          id="menuButton"
          aria-label="Menü öffnen"
        >
          ☰
        </button>

        <ul class="nav-links" id="navLinks">
          <li><a href="#leistungen">Leistungen</a></li>
          <li><a href="#preise">Preise</a></li>
          <li><a href="#ueber-uns">Über uns</a></li>
          <li>
            <a href="#kontakt" class="nav-cta">
              Kontakt
            </a>
          </li>
        </ul>

      </nav>

    </div>
  </header>


  <!-- =========================
       HERO
  ========================== -->

  <main>

    <section class="hero">

      <div class="container hero-grid">

        <div>

          <div class="badge">
            📍 Fleckeby & Umgebung
          </div>

          <h1>
            Technik, die
            <span>einfach funktioniert.</span>
          </h1>

          <p class="hero-text">
            Persönliche Hilfe bei Handy- und PC-Problemen.
            Verständlich erklärt, fair kalkuliert und ohne
            unnötiges Fachchinesisch.
          </p>

          <div class="buttons">

            <a
              href="#kontakt"
              class="button button-primary"
            >
              Anfrage senden →
            </a>

            <a
              href="#leistungen"
              class="button button-secondary"
            >
              Leistungen ansehen
            </a>

          </div>

        </div>


        <div class="hero-card">

          <div class="hero-icon">
            💻📱
          </div>

          <h2>
            TechFix
          </h2>

          <p>
            Deine persönliche Technik-Hilfe in
            Fleckeby und Umgebung.
          </p>

          <div class="check-list">

            <div class="check">
              <span>✓</span>
              Handy einrichten
            </div>

            <div class="check">
              <span>✓</span>
              PC-Probleme lösen
            </div>

            <div class="check">
              <span>✓</span>
              Daten übertragen
            </div>

            <div class="check">
              <span>✓</span>
              WLAN & Technik
            </div>

          </div>

        </div>

      </div>

    </section>


    <!-- =========================
         LEISTUNGEN
    ========================== -->

    <section id="leistungen">

      <div class="container">

        <div class="section-heading">

          <h2>
            Was ich für dich erledige
          </h2>

          <p>
            Schnelle und verständliche Unterstützung
            rund um Smartphone und Computer.
          </p>

        </div>


        <div class="services">

          <article class="service-card">

            <div class="service-icon">
              📱
            </div>

            <h3>
              Handy-Hilfe
            </h3>

            <p>
              Neues Smartphone einrichten, Apps installieren,
              Einstellungen erklären und bei Problemen helfen.
            </p>

          </article>


          <article class="service-card">

            <div class="service-icon">
              💻
            </div>

            <h3>
              PC-Hilfe
            </h3>

            <p>
              Unterstützung bei Windows, Programmen,
              Dateien, Druckern und allgemeinen PC-Problemen.
            </p>

          </article>


          <article class="service-card">

            <div class="service-icon">
              🔄
            </div>

            <h3>
              Datenübertragung
            </h3>

            <p>
              Fotos, Kontakte und wichtige Dateien
              auf ein neues Gerät übertragen.
            </p>

          </article>


          <article class="service-card">

            <div class="service-icon">
              📶
            </div>

            <h3>
              WLAN & Internet
            </h3>

            <p>
              Hilfe bei Verbindungsproblemen und
              bei der Einrichtung deiner Geräte.
            </p>

          </article>

        </div>

      </div>

    </section>


    <!-- =========================
         PREISE
    ========================== -->

    <section id="preise" class="pricing">

      <div class="container">

        <div class="section-heading">

          <h2>
            Faire & einfache Preise
          </h2>

          <p>
            Klare Preise ohne komplizierte Pakete.
          </p>

        </div>


        <div class="price-grid">

          <article class="price-card">

            <h3>
              Quick-Hilfe
            </h3>

            <div class="price">
              15 €
              <small>/ 30 Min.</small>
            </div>

            <ul class="features">
              <li>✓ Kleine Probleme</li>
              <li>✓ Einstellungen</li>
              <li>✓ Kurze Beratung</li>
            </ul>

            <a
              href="#kontakt"
              class="button button-secondary"
            >
              Anfrage senden
            </a>

          </article>


          <article class="price-card featured">

            <div class="popular">
              BELIEBT
            </div>

            <h3>
              Technik-Hilfe
            </h3>

            <div class="price">
              20 €
              <small>/ Stunde</small>
            </div>

            <ul class="features">
              <li>✓ Handy-Hilfe</li>
              <li>✓ PC-Hilfe</li>
              <li>✓ WLAN-Probleme</li>
              <li>✓ Persönliche Erklärung</li>
            </ul>

            <a
              href="#kontakt"
              class="button button-primary"
            >
              Termin anfragen
            </a>

          </article>


          <article class="price-card">

            <h3>
              Komplett-Service
            </h3>

            <div class="price">
              ab 30 €
            </div>

            <ul class="features">
              <li>✓ Neues Handy einrichten</li>
              <li>✓ Datenübertragung</li>
              <li>✓ Apps & Einstellungen</li>
              <li>✓ Grundlegende Einweisung</li>
            </ul>

            <a
              href="#kontakt"
              class="button button-secondary"
            >
              Anfrage senden
            </a>

          </article>

        </div>

      </div>

    </section>


    <!-- =========================
         ÜBER UNS
    ========================== -->

    <section id="ueber-uns" class="about">

      <div class="container about-grid">

        <div class="about-box">

          <div class="big-icon">
            🛠️
          </div>

          <h3>
            Einfach statt kompliziert.
          </h3>

          <p>
            Bei TechFix steht verständliche Technik-Hilfe
            im Mittelpunkt.
          </p>

        </div>


        <div class="about-text">

          <h2>
            Technik-Hilfe aus Fleckeby.
          </h2>

          <p>
            Du hast ein Problem mit deinem Handy oder PC?
            Dann bist du bei TechFix richtig.
          </p>

          <p>
            Egal ob neues Smartphone, langsamer Computer,
            Probleme mit Apps oder eine Frage zur Bedienung –
            ich helfe dir Schritt für Schritt.
          </p>

          <p>
            <strong>
              Persönlich. Verständlich. Fair.
            </strong>
          </p>

        </div>

      </div>

    </section>


    <!-- =========================
         KONTAKT
    ========================== -->

    <section id="kontakt" class="contact">

      <div class="container contact-grid">

        <div class="contact-info">

          <h2>
            Lass uns dein Technikproblem lösen.
          </h2>

          <p>
            Schreib mir kurz, wobei du Hilfe brauchst.
          </p>


          <div class="contact-item">

            <div class="contact-icon">
              📞
            </div>

            <div>

              <strong>
                Telefon
              </strong>

              <p>
                <a href="tel:+4915259463737">
                  01525 9463737
                </a>
              </p>

            </div>

          </div>


          <div class="contact-item">

            <div class="contact-icon">
              ✉️
            </div>

            <div>

              <strong>
                E-Mail
              </strong>

              <p>
                <a href="mailto:sverre.lausen2011@icloud.com">
                  sverre.lausen2011@icloud.com
                </a>
              </p>

            </div>

          </div>


          <div class="contact-item">

            <div class="contact-icon">
              📍
            </div>

            <div>

              <strong>
                Servicegebiet
              </strong>

              <p>
                Fleckeby & Umgebung
              </p>

            </div>

          </div>

        </div>


        <!-- KONTAKTFORMULAR -->

        <form id="contactForm">

          <div class="form-group">

            <label for="name">
              Name
            </label>

            <input
              type="text"
              id="name"
              name="name"
              placeholder="Dein Name"
              required
            >

          </div>


          <div class="form-group">

            <label for="email">
              E-Mail
            </label>

            <input
              type="email"
              id="email"
              name="email"
              placeholder="deine@email.de"
              required
            >

          </div>


          <div class="form-group">

            <label for="message">
              Wobei brauchst du Hilfe?
            </label>

            <textarea
              id="message"
              name="message"
              placeholder="Beschreibe kurz dein Problem..."
              required
            ></textarea>

          </div>


          <button
            type="submit"
            class="button button-primary"
          >
            Anfrage vorbereiten →
          </button>

        </form>

      </div>

    </section>

  </main>


  <!-- =========================
       WHATSAPP
  ========================== -->

  <a
    class="whatsapp"
    href="https://wa.me/4915259463737"
    target="_blank"
    rel="noopener"
    aria-label="TechFix über WhatsApp kontaktieren"
  >
    💬 WhatsApp
  </a>


  <!-- =========================
       FOOTER
  ========================== -->

  <footer>

    <div class="container footer-content">

      <div class="logo">
        Tech<span>Fix</span>
      </div>

      <p>
        © 2026 TechFix · Fleckeby & Umgebung
      </p>

    </div>

  </footer>


  <script>

    /* =========================
       MOBILES MENÜ
    ========================== */

    const menuButton =
      document.getElementById("menuButton");

    const navLinks =
      document.getElementById("navLinks");

    menuButton.addEventListener("click", () => {
      navLinks.classList.toggle("active");
    });


    /* Menü nach Klick schließen */

    document.querySelectorAll(".nav-links a")
      .forEach(link => {

        link.addEventListener("click", () => {
          navLinks.classList.remove("active");
        });

      });


    /* =========================
       KONTAKTFORMULAR
    ========================== */

    const form =
      document.getElementById("contactForm");

    form.addEventListener("submit", function(event) {

      event.preventDefault();

      const name =
        document.getElementById("name").value.trim();

      const email =
        document.getElementById("email").value.trim();

      const message =
        document.getElementById("message").value.trim();


      /*
        Das Formular öffnet das normale
        E-Mail-Programm des Besuchers.

        Für einen echten Online-Versand können wir
        später einen Formular-Dienst oder ein eigenes
        Backend anschließen.
      */

      const subject =
        encodeURIComponent(
          "Neue TechFix Anfrage von " + name
        );

      const body =
        encodeURIComponent(
          "Name: " + name +
          "\nE-Mail: " + email +
          "\n\nNachricht:\n" + message
        );

      window.location.href =
        "mailto:sverre.lausen2011@icloud.com" +
        "?subject=" + subject +
        "&body=" + body;

    });

  </script>

</body>
</html>