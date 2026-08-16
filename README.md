
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, user-scalable=yes" />
  <title>Ashawniz Nailz | South Carolina Nail Tech</title>
  <meta name="description" content="Ashawniz Nailz — registered cosmetologist in South Carolina. Acrylic sets, pedicures, custom designs, and mobile services in Florence, SC area. Book directly via Google Calendar." />
  <meta property="og:title" content="Ashawniz Nailz | Book Your Appointment" />
  <meta property="og:description" content="Professional nail tech in South Carolina. Acrylic sets, pedicures, custom designs. Book online!" />
  <meta property="og:type" content="website" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Pacifico&display=swap" rel="stylesheet" />
  <link href="https://calendar.google.com/calendar/scheduling-button-script.css" rel="stylesheet">
  <script src="https://calendar.google.com/calendar/scheduling-button-script.js" async></script>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
      -webkit-tap-highlight-color: transparent;
    }

    :root {
      --primary-gradient: linear-gradient(135deg, #ffb3e6, #ff99cc);
      --secondary-gradient: linear-gradient(135deg, #d9b3ff, #b366ff);
      --page-bg-gradient: linear-gradient(135deg, #ffccff 0%, #ffb3e6 45%, #d9b3ff 55%, #b366ff 100%);
      --pink-medium: #ffb3e6;
      --purple-medium: #d9b3ff;
      --purple-dark: #b366ff;
      --light: #ffffff;
      --text-dark: #5a3d5c;
      --text-light: #7a5a7c;
      --shadow-soft: 0 18px 40px rgba(255, 179, 230, 0.3);
      --radius-lg: 28px;
      --radius-pill: 999px;
      --highlight-purple-bg: #f3e8ff;
      --highlight-purple-border: #c084fc;
      --highlight-pink-bg: #ffe4f3;
      --highlight-pink-border: #f9a8d4;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: var(--page-bg-gradient);
      background-attachment: fixed;
      color: var(--text-dark);
      min-height: 100vh;
      line-height: 1.5;
      position: relative;
    }

    body::before {
      content: '';
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at 20% 80%, rgba(255, 204, 255, 0.4) 0%, transparent 30%),
                  radial-gradient(circle at 80% 20%, rgba(217, 179, 255, 0.4) 0%, transparent 30%),
                  radial-gradient(circle at 40% 40%, rgba(255, 179, 230, 0.3) 0%, transparent 40%);
      pointer-events: none;
      z-index: -1;
    }

    a { text-decoration: none; color: inherit; transition: all 0.2s ease; }
    img { max-width: 100%; display: block; }

    .container {
      width: 100%;
      max-width: 1280px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* Highlight styles */
    .highlight-purple {
      background: linear-gradient(135deg, var(--highlight-purple-bg), var(--highlight-pink-bg));
      border-left: 4px solid var(--highlight-purple-border);
      padding: 0.3rem 0.6rem;
      border-radius: 16px;
      font-weight: 600;
      margin: 0.2rem 0;
    }
    .price-highlight {
      background: linear-gradient(135deg, #f3e8ff, #ffe4f3);
      border-radius: 24px;
      padding: 0.2rem 0.8rem;
      display: inline-block;
      color: #7c3aed;
      font-weight: 600;
    }
    .price-item.highlight-item {
      background: linear-gradient(135deg, #faf0ff, #fff0f8);
      border-radius: 20px;
      padding: 0.3rem 0.6rem;
      margin: 0.2rem 0;
    }
    .policy-highlight {
      background: #fdf2f8;
      border-left: 4px solid #f9a8d4;
      padding: 0.8rem;
      border-radius: 20px;
      margin-bottom: 1rem;
    }
    .big-bold {
      font-size: 1.2rem;
      font-weight: 800;
      text-transform: uppercase;
      color: #dc3545;
    }
    .warning-box {
      background: linear-gradient(135deg, rgba(255, 220, 220, 0.9), rgba(255, 200, 200, 0.9));
      border: 2px solid #dc3545;
      padding: 0.8rem;
      border-radius: 20px;
      margin: 1rem 0;
      text-align: center;
    }
    /* FAQ Section */
    .faq-section {
      margin-top: 1rem;
      background: rgba(255, 255, 255, 0.9);
      border-radius: 24px;
      padding: 1.2rem;
      border: 2px solid rgba(217, 179, 255, 0.5);
    }
    .faq-section h3 {
      font-size: 1.1rem;
      margin-bottom: 0.8rem;
      color: var(--purple-dark);
      display: flex;
      align-items: center;
      gap: 0.5rem;
    }
    .faq-list {
      display: flex;
      flex-direction: column;
      gap: 0.6rem;
    }
    .faq-item {
      display: flex;
      align-items: flex-start;
      gap: 0.6rem;
      font-size: 0.8rem;
      padding: 0.3rem 0;
      border-bottom: 1px solid rgba(255, 179, 230, 0.3);
    }
    .faq-question {
      font-weight: 700;
      color: var(--purple-dark);
      min-width: 140px;
    }
    .faq-answer {
      color: var(--text-dark);
    }
    .refill-note {
      background: linear-gradient(135deg, #f3e8ff, #ffe4f3);
      border-radius: 16px;
      padding: 0.4rem 0.8rem;
      font-size: 0.7rem;
      margin-top: 0.3rem;
      text-align: center;
      font-weight: 500;
    }
    /* SUPER BOLD KIDS MANICURE NOTE */
    .kids-highlight {
      background: linear-gradient(135deg, #f0d4ff, #ffcce5);
      border: 2px solid #c084fc;
      border-radius: 20px;
      padding: 0.5rem 0.8rem;
      margin: 0.5rem 0;
      text-align: center;
      box-shadow: 0 2px 8px rgba(192, 132, 252, 0.3);
    }
    .kids-highlight .price-title {
      font-weight: 800;
      font-size: 0.9rem;
    }
    .kids-highlight span {
      font-weight: 800;
    }
    .kids-badge {
      background: #c084fc;
      color: white;
      border-radius: 40px;
      padding: 0.2rem 0.7rem;
      font-size: 0.65rem;
      margin-left: 0.5rem;
      display: inline-block;
    }

    /* ========== RESPONSIVE HEADER ========== */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(20px);
      background: linear-gradient(to right, rgba(255, 179, 230, 0.96), rgba(217, 179, 255, 0.96));
      border-bottom: 2px solid rgba(255, 255, 255, 0.8);
      box-shadow: 0 4px 20px rgba(255, 179, 230, 0.25);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.8rem 0;
      gap: 1rem;
    }

    .logo-group {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      flex-shrink: 0;
    }

    .logo-circle {
      width: 44px;
      height: 44px;
      border-radius: 50%;
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      box-shadow: 0 0 18px rgba(255, 179, 230, 0.6);
      border: 2px solid rgba(255, 255, 255, 0.9);
    }

    .logo-text-main {
      font-family: "Pacifico", cursive;
      font-size: 1.3rem;
      letter-spacing: 0.02em;
      color: var(--text-dark);
      line-height: 1.2;
    }

    .logo-text-sub {
      font-size: 0.65rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-light);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.5rem;
    }

    .nav-links a {
      position: relative;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      font-weight: 600;
      font-size: 0.75rem;
      color: var(--text-dark);
      white-space: nowrap;
      padding: 0.4rem 0;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.2rem;
      width: 0;
      height: 2.5px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--pink-medium), var(--purple-medium));
      transition: width 0.25s ease;
    }

    .nav-links a:hover::after { width: 100%; }

    .nav-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.55rem 1.3rem;
      border-radius: var(--radius-pill);
      background: var(--light);
      color: var(--text-dark);
      font-size: 0.72rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.1em;
      border: 2px solid rgba(255, 255, 255, 0.9);
      box-shadow: 0 4px 12px rgba(255, 179, 230, 0.4);
      transition: all 0.25s ease;
    }

    .nav-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 8px 20px rgba(255, 179, 230, 0.5);
    }

    .nav-toggle {
      display: none;
      background: none;
      border: none;
      font-size: 1.8rem;
      cursor: pointer;
      color: var(--text-dark);
      padding: 0.2rem;
      line-height: 1;
    }

    @media (max-width: 900px) {
      .nav { position: relative; }
      .nav-links {
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        flex-direction: column;
        align-items: flex-start;
        padding: 1.2rem 1.5rem 1.5rem;
        background: linear-gradient(135deg, rgba(255, 179, 230, 0.98), rgba(217, 179, 255, 0.98));
        border-bottom: 2px solid rgba(255, 255, 255, 0.9);
        transform: scaleY(0);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.25s ease, opacity 0.2s ease;
        transform-origin: top;
        gap: 1rem;
        backdrop-filter: blur(24px);
        z-index: 100;
        border-radius: 0 0 28px 28px;
        box-shadow: 0 20px 35px rgba(0,0,0,0.1);
      }
      .nav-links.open {
        transform: scaleY(1);
        opacity: 1;
        pointer-events: auto;
      }
      .nav-links a {
        width: 100%;
        font-size: 0.9rem;
        padding: 0.6rem 0;
      }
      .nav-btn {
        width: auto;
        justify-content: center;
        margin-top: 0.3rem;
      }
      .nav-toggle { display: block; }
    }

    @media (max-width: 550px) {
      .container { padding: 0 1rem; }
      .logo-text-main { font-size: 1.1rem; }
      .logo-circle { width: 38px; height: 38px; }
      .logo-text-sub { font-size: 0.55rem; }
    }

    /* Hero */
    .hero { padding: 2.5rem 0 2rem; }
    .hero-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
      align-items: start;
    }
    @media (min-width: 1025px) {
      .hero-grid { grid-template-columns: 1.4fr 1fr; gap: 2.5rem; }
    }
    .eyebrow {
      text-transform: uppercase;
      font-size: 0.7rem;
      letter-spacing: 0.2em;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      margin-bottom: 0.7rem;
      color: var(--text-light);
    }
    .eyebrow-dot { width: 7px; height: 7px; border-radius: 50%; background: var(--pink-medium); }
    .hero h1 {
      font-size: clamp(1.8rem, 6vw, 3rem);
      line-height: 1.2;
      margin-bottom: 0.8rem;
    }
    .hero h1 span.highlight {
      background: linear-gradient(135deg, #ff99cc, #b366ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-subtitle { font-size: 0.95rem; opacity: 0.9; margin-bottom: 1.3rem; color: var(--text-light); }
    .hero-badges { display: flex; flex-wrap: wrap; gap: 0.6rem; margin-bottom: 1.3rem; }
    .badge {
      padding: 0.45rem 1rem;
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.8);
      backdrop-filter: blur(8px);
      border: 1.5px solid rgba(255, 255, 255, 0.85);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }
    .hero-actions { display: flex; flex-wrap: wrap; gap: 0.8rem; margin-bottom: 1.2rem; }
    .btn-primary, .btn-secondary {
      border-radius: var(--radius-pill);
      padding: 0.8rem 1.6rem;
      font-size: 0.8rem;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      transition: all 0.25s ease;
      cursor: pointer;
    }
    @media (max-width: 550px) {
      .btn-primary, .btn-secondary { padding: 0.65rem 1.2rem; font-size: 0.7rem; }
    }
    .btn-primary {
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      color: var(--text-dark);
      box-shadow: 0 12px 25px rgba(255, 179, 230, 0.4);
    }
    .btn-primary:hover { transform: translateY(-3px); }
    .btn-secondary {
      background: rgba(255, 255, 255, 0.88);
      border: 1.5px solid rgba(255, 179, 230, 0.7);
    }
    .hero-meta { font-size: 0.72rem; opacity: 0.85; }

    /* Booking Card */
    .booking-card {
      background: rgba(255, 255, 255, 0.92);
      backdrop-filter: blur(18px);
      border-radius: 36px;
      padding: 1.8rem;
      box-shadow: 0 25px 45px rgba(255, 179, 230, 0.35);
      border: 2px solid rgba(255, 255, 255, 0.9);
      transition: all 0.3s ease;
      text-align: center;
    }
    .booking-header { font-size: 1.3rem; font-weight: 700; margin-bottom: 0.5rem; display: flex; align-items: center; justify-content: center; gap: 0.6rem; }
    .booking-sub { font-size: 0.8rem; color: var(--text-light); margin-bottom: 1.5rem; }
    .calendar-button-container { margin: 1rem 0; display: flex; flex-direction: column; align-items: center; gap: 0.8rem; }
    .calendar-link, .direct-booking-link {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      gap: 0.6rem;
      background: linear-gradient(135deg, #039BE5, #0288d1);
      color: white;
      padding: 0.9rem 2rem;
      border-radius: 60px;
      font-weight: 700;
      font-size: 1rem;
      text-transform: uppercase;
      letter-spacing: 0.05em;
      transition: all 0.25s ease;
      width: 100%;
      max-width: 320px;
      text-align: center;
    }
    .direct-booking-link { background: linear-gradient(135deg, #8e44ad, #9b59b6); }
    .alt-booking { margin-top: 1.8rem; padding-top: 1.2rem; border-top: 1px solid rgba(255, 179, 230, 0.4); }
    .alt-title { font-size: 0.75rem; text-transform: uppercase; letter-spacing: 0.1em; color: var(--text-light); margin-bottom: 0.8rem; }
    .social-buttons { display: flex; justify-content: center; gap: 1rem; flex-wrap: wrap; }
    .social-book-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.5rem;
      background: rgba(255,255,255,0.85);
      padding: 0.6rem 1.3rem;
      border-radius: 60px;
      font-size: 0.75rem;
      font-weight: 600;
      border: 1px solid rgba(255, 179, 230, 0.6);
    }
    .deposit-note {
      background: linear-gradient(135deg, rgba(255, 230, 245, 0.7), rgba(230, 210, 255, 0.7));
      padding: 0.6rem;
      border-radius: 28px;
      font-size: 0.7rem;
      margin-top: 1rem;
      text-align: center;
    }

    /* Sections */
    section { padding: 2.5rem 0; }
    .section-heading { text-align: center; margin-bottom: 2rem; }
    .section-heading span.kicker { font-size: 0.72rem; letter-spacing: 0.2em; color: var(--text-light); display: block; margin-bottom: 0.3rem; }
    .section-heading h2 { font-size: 1.7rem; margin-bottom: 0.4rem; }

    .about-grid, .services-grid, .policy-grid { display: grid; gap: 1.3rem; }
    .about-grid { grid-template-columns: 1fr; }
    .services-grid { grid-template-columns: 1fr; }
    .policy-grid { grid-template-columns: 1fr; }
    @media (min-width: 768px) {
      .about-grid { grid-template-columns: 1fr 1fr; }
      .services-grid { grid-template-columns: repeat(2, 1fr); }
      .policy-grid { grid-template-columns: repeat(2, 1fr); }
    }
    @media (min-width: 1024px) {
      .services-grid { grid-template-columns: repeat(3, 1fr); }
      .policy-grid { grid-template-columns: repeat(3, 1fr); }
    }
    .card {
      background: rgba(255, 255, 255, 0.85);
      border-radius: 28px;
      padding: 1.4rem;
      backdrop-filter: blur(12px);
      border: 1.5px solid rgba(255, 255, 255, 0.9);
      transition: all 0.25s ease;
      height: 100%;
    }
    .price-item {
      display: flex;
      justify-content: space-between;
      font-size: 0.85rem;
      margin-bottom: 0.5rem;
      flex-wrap: wrap;
      gap: 0.3rem;
      align-items: center;
    }
    .price-title { font-weight: 600; }
    .price-note { font-size: 0.7rem; color: var(--purple-dark); margin-top: 0.25rem; font-style: italic; }
    .policy-tag {
      display: inline-block;
      font-size: 0.66rem;
      padding: 0.25rem 0.9rem;
      background: linear-gradient(135deg, rgba(255, 204, 255, 0.5), rgba(217, 179, 255, 0.5));
      border-radius: 60px;
      margin-right: 0.5rem;
      margin-bottom: 0.5rem;
    }
    .service-notes { margin-top: 0.8rem; padding: 0.6rem; background: rgba(255, 240, 250, 0.6); border-radius: 20px; font-size: 0.7rem; border-left: 3px solid var(--purple-medium); }

    /* Gallery */
    .gallery-strip { background: rgba(255, 255, 255, 0.85); border-radius: 28px; padding: 1.2rem; }
    .gallery-track { display: flex; gap: 1rem; overflow-x: auto; scroll-snap-type: x mandatory; padding-bottom: 0.8rem; }
    .gallery-slide {
      flex: 0 0 auto;
      width: 180px;
      aspect-ratio: 3 / 4;
      border-radius: 24px;
      overflow: hidden;
      border: 3px solid rgba(255, 255, 255, 0.9);
    }
    .gallery-slide img { width: 100%; height: 100%; object-fit: cover; }
    .gallery-btn {
      border-radius: 60px;
      border: 1.5px solid rgba(255, 179, 230, 0.7);
      background: rgba(255, 255, 255, 0.9);
      padding: 0.45rem 1.2rem;
      font-size: 0.75rem;
      font-weight: 600;
      cursor: pointer;
    }

    footer {
      padding: 1.8rem 0;
      border-top: 2px solid rgba(255, 179, 230, 0.5);
      background: linear-gradient(to right, rgba(255, 179, 230, 0.4), rgba(217, 179, 255, 0.4));
    }
    .footer-top, .footer-bottom { display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 1rem; }
    .footer-socials { display: flex; gap: 0.8rem; flex-wrap: wrap; }
    .footer-pill { padding: 0.4rem 1rem; border-radius: 60px; background: rgba(255, 255, 255, 0.85); font-size: 0.72rem; }
  </style>
</head>
<body>
<div class="page">
  <header>
    <div class="container">
      <nav class="nav">
        <div class="logo-group">
          <div class="logo-circle"></div>
          <div>
            <div class="logo-text-main">Ashawniz Nailz</div>
            <div class="logo-text-sub">South Carolina Nail Tech</div>
          </div>
        </div>
        <button class="nav-toggle" onclick="document.querySelector('.nav-links').classList.toggle('open')">☰</button>
        <div class="nav-links">
          <a href="#services">Services</a>
          <a href="#policies">Policies</a>
          <a href="#location">Location</a>
          <a href="#gallery">Gallery</a>
          <a href="#booking" class="nav-btn"><span>💅🏾</span><span>Book Now</span></a>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <section class="hero" id="top">
      <div class="container hero-grid">
        <div>
          <div class="eyebrow"><span class="eyebrow-dot"></span> SOUTH CAROLINA NAIL TECH</div>
          <h1>Nails done right. <span class="highlight">Every style. Every color. Every time.</span></h1>
          <p class="hero-subtitle">Registered cosmetologist creating acrylic sets, pedicures, and custom designs for clients who want their nails to match their energy.</p>
          <div class="hero-badges">
            <div class="badge"><span class="badge-dot"></span> Registered Cosmetologist</div>
            <div class="badge"><span class="badge-dot"></span> Florence, SC Area</div>
          </div>
          <div class="hero-actions">
            <a class="btn-primary" href="#booking"><span>📅</span><span>Book via Calendar</span></a>
            <a class="btn-secondary" href="#services"><span>👛</span><span>View price list</span></a>
          </div>
        </div>
        <div class="booking-card" id="booking">
          <div class="booking-header"><span>📅</span><span>Book Direct Appointment</span></div>
          <div class="booking-sub">Schedule your nail appointment instantly using my calendar.</div>
          <div class="calendar-button-container">
            <div id="google-calendar-btn"></div>
            <!-- REPLACED BOOKING LINK -->
            <a href="https://calendar.app.google/meNdHchW6ueV8aKn9" target="_blank" class="direct-booking-link" rel="noopener noreferrer">📆 Open Booking Link</a>
          </div>
          <script>
            (function() {
              var target = document.getElementById('google-calendar-btn');
              if (target) {
                var checkCalendar = function() {
                  if (window.calendar && window.calendar.schedulingButton) {
                    target.innerHTML = '';
                    window.calendar.schedulingButton.load({ url: 'https://calendar.app.google/meNdHchW6ueV8aKn9', color: '#039BE5', label: '📅 Book with Google Calendar', target: target });
                  } else { target.innerHTML = '<a href="https://calendar.app.google/meNdHchW6ueV8aKn9" target="_blank" class="calendar-link">📅 Book with Google Calendar</a>'; }
                };
                window.addEventListener('load', checkCalendar);
              }
            })();
          </script>
          <div class="deposit-note"><strong>💎 $20 Deposit Required</strong> — Non-refundable & non-transferable. Deposits go towards final total!</div>
          <div class="alt-booking"><div class="alt-title">✨ Or book via social media ✨</div><div class="social-buttons"><a href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" class="social-book-btn">📲 TikTok DM</a><a href="https://instagram.com/ashawniz.nailz" target="_blank" class="social-book-btn">📸 Instagram DM</a></div></div>
        </div>
      </div>
    </section>

    <section id="location"><div class="container"><div class="section-heading"><span class="kicker">About &amp; location</span><h2>Where to find Ashawniz Nailz</h2></div><div class="about-grid"><div class="card"><div class="policy-tag">💅🏾 Registered Cosmetologist</div><h3>The experience</h3><p>Personalized appointments. Bring your inspo, ideas, or vibe — together we create your perfect set.</p><div class="service-notes"><p><strong>📝 For Acrylic Nails:</strong> Charm sets = unlimited charms | Design sets = unlimited designs | Combo = unlimited both</p></div></div><div class="card"><div class="policy-tag">📍 Florence, SC area</div><h3>Service Area</h3><p>Based in Florence, SC.</p></div></div></div></section>

    <section id="services"><div class="container">
      <div class="section-heading"><span class="kicker">Services &amp; pricing</span><h2>Price list</h2><p>Deposits go toward total. Final balance accepted in cash.</p></div>
      <div class="services-grid">
        <div class="card">
          <h3>💅 Acrylic Sets & Manicures</h3>
          <!-- Sorted least to greatest -->
          <div class="price-item"><span class="price-title">Basic Manicure</span><span>$50</span></div>
          <div class="price-item"><span class="price-title">Design Manicure</span><span>$60</span></div>
          <div class="price-item"><span class="price-title">Fullset Acrylic</span><span>$70</span></div>
          <div class="price-item"><span class="price-title">Charm/Design Manicure</span><span>$75</span></div>
          <div class="price-item"><span class="price-title">Acrylic Charm sets</span><span>$90</span></div>
          <div class="price-item"><span class="price-title">Acrylic Design sets</span><span>$90</span></div>
          <div class="price-item highlight-item"><span class="price-title">✨ Acrylic Charm/Design sets</span><span>$95</span></div>
          <!-- SUPER BOLD KIDS MANICURE - HIGHLIGHTED IN PINK/PURPLE -->
          <div class="kids-highlight">
            <span class="price-title">👧 Kids Manicure (Ages 5-12 ONLY)</span>
            <span style="font-weight:800; font-size:1rem;">$20</span>
            <span class="kids-badge">⚠️ Ages 5-12 ONLY ⚠️</span>
          </div>
          <div class="price-note">✨ Charm/Design sets include unlimited charms & designs | No extra charge for length!</div>
        </div>
        <div class="card">
          <h3>🦶 Pedicure Menu <span class="price-highlight">(UPDATED PRICES)</span></h3>
          <!-- Sorted least to greatest -->
          <div class="price-item highlight-item"><span class="price-title">Classic Pedicure</span><span>$50</span></div>
          <div class="price-item highlight-item"><span class="price-title">Deluxe Pedicure</span><span>$65</span></div>
          <div class="price-item highlight-item"><span class="price-title">Luxury Pedicure</span><span>$75</span></div>
          <p class="price-note">✨ Dry pedicure also available | Polish included</p>
          <div class="service-notes"><p><strong>📝 French Tip Special (June 1 – July 10):</strong> Classic Pedicure + Fullset French Tips + Toes French tips = $90 (was $180)</p></div>
        </div>
        <div class="card">
          <h3>✍️ Add-Ons, Refills & Toes</h3>
          <!-- Sorted least to greatest -->
          <div class="price-item"><span class="price-title">Polish change</span><span>$18</span></div>
          <div class="price-item"><span class="price-title">Deposit</span><span>$20</span></div>
          <div class="price-item"><span class="price-title">Acrylic (Toes) Refill</span><span>$30</span></div>
          <div class="refill-note">⚠️ Must have at least 5 toes still on for toe refill</div>
          <div class="price-item highlight-item"><span class="price-title">Acrylic Refill (nails)</span><span>$35</span></div>
          <div class="price-item highlight-item"><span class="price-title">Gel toes (no acrylic)</span><span>$35</span></div>
          <div class="refill-note">⚠️ Must have at least 4 nails on for nail refill</div>
          <div class="price-item"><span>2 Acrylic Toes</span><span>$55</span></div>
          <div class="price-item"><span>Fullsets (Toes)</span><span>$65</span></div>
          <div class="price-item"><span>Design Fullsets (Toes)</span><span>$70</span></div>
          <div class="price-item"><span>Charm Fullsets (Toes)</span><span>$75</span></div>
          <div class="price-item"><span>Charm/Design Fullset (Toes)</span><span>$80</span></div>
          <div class="price-item"><span>Nail Repair</span><span>$10 each</span></div>
          <div class="price-item"><span>Soak Off</span><span>$15</span></div>
          <div class="price-item"><span>Freestyle (Tech choice only)</span><span>$70</span></div>
        </div>
      </div>
      
      <!-- FAQ SECTION - Most clients ask these questions -->
      <div class="faq-section">
        <h3>💬 Frequently Asked Questions 💬</h3>
        <div class="faq-list">
          <div class="faq-item"><span class="faq-question">❓ Do you charge for length?</span><span class="faq-answer">No, we don't charge for length!</span></div>
          <div class="faq-item"><span class="faq-question">❓ Does deposit go towards total?</span><span class="faq-answer">Yes! Deposits go towards your final total.</span></div>
          <div class="faq-item"><span class="faq-question">❓ What does Charm set include?</span><span class="faq-answer">Unlimited charms ONLY</span></div>
          <div class="faq-item"><span class="faq-question">❓ What does Design set include?</span><span class="faq-answer">Unlimited designs ONLY</span></div>
          <div class="faq-item"><span class="faq-question">❓ What does Charm/Design set include?</span><span class="faq-answer">Unlimited charms AND unlimited designs</span></div>
          <div class="faq-item"><span class="faq-question">❓ Refill requirements?</span><span class="faq-answer">Nail refill: at least 4 nails on | Toe refill: at least 5 toes on</span></div>
        </div>
      </div>
    </div></section>

    <section id="policies"><div class="container">
      <div class="section-heading"><span class="kicker">Policies</span><h2>Before you book</h2></div>
      <div class="policy-grid">
        <div class="card">
          <div><span class="policy-tag">Deposits</span><span class="policy-tag">Non-refundable</span></div>
          <h3>Deposit Policy</h3>
          <div class="policy-highlight">
            <p><strong>⚠️ ALL DEPOSITS ARE NON-REFUNDABLE AND NON-TRANSFERABLE.</strong> If you cancel your appointment for ANY reason, a <strong>NEW deposit is required</strong> to book another appointment.</p>
          </div>
          <div class="warning-box">
            <span class="big-bold">🚨 NO REFUNDS 🚨</span>
            <p style="margin-top:0.3rem;">After a service is completed, you have <strong>48 HOURS</strong> to request changes for <strong>FREE</strong>. After 48 hours, you will have to pay full price for any fixes.</p>
          </div>
        </div>
        <div class="card">
          <div><span class="policy-tag">Timing</span><span class="policy-tag">Late & No-Show</span></div>
          <h3>Late Policy</h3>
          <p>10-min grace period, after that <strong>$10 late fee</strong>. After 15 minutes, your appointment may be canceled and deposit forfeited.</p>
          <div class="warning-box" style="margin-top:0.8rem;">
            <strong>⚠️ I DO NOT ALLOW you to come with nails on already from a previous tech you've been to. YOU WILL BE DECLINED at your appointment.</strong>
          </div>
        </div>
        <div class="card">
          <div><span class="policy-tag">Nail prep</span><span class="policy-tag">Payments</span></div>
          <h3>Prep & Payments</h3>
          <p>Arrive with <strong>bare nails</strong> unless soak-off was booked. Remaining balance accepted in cash.</p>
          <div class="service-notes" style="margin-top:0.8rem;"><p><strong>👧 Kids Manicure:</strong> Ages 5-12 years old only. Parent/guardian must be present.</p></div>
        </div>
      </div>
    </div></section>

    <section id="gallery"><div class="container">
      <div class="section-heading"><span class="kicker">Client work</span><h2>Gallery preview</h2><p>Swipe to see recent sets by Ashawniz Nailz.</p></div>
      <div class="card"><div class="gallery-strip"><div class="gallery-track" id="galleryTrack"><div class="gallery-slide"><img src="https://i.postimg.cc/ZqYtzPjx/IMG-7932.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/ZqYtzPjP/IMG-7936.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/R0C5x1Gw/IMG-7937.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/XvNS6KxF/IMG-7938.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/tgRQGdDx/IMG-7939.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/q7BVHcQh/IMG-7940.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/R0C5x1GS/IMG-7941.jpg" alt="Nail set"></div></div><div class="gallery-controls" style="display:flex; justify-content:space-between; margin-top:0.9rem;"><span style="font-size:0.7rem;">← → swipe or click arrows</span><div><button class="gallery-btn" id="galleryPrev">← Prev</button><button class="gallery-btn" id="galleryNext" style="margin-left:0.6rem;">Next →</button></div></div></div></div>
    </div></section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-top">
        <div><div class="logo-text-main" style="font-size:1.1rem;">Ashawniz Nailz</div><div class="logo-text-sub">South Carolina Nail Tech · Pink & Purple Vibes</div></div>
        <div class="footer-socials"><a class="footer-pill" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank">TikTok · @ashawniz.nailz</a><a class="footer-pill" href="https://instagram.com/ashawniz.nailz" target="_blank">Instagram · @ashawniz.nailz</a></div>
      </div>
      <div class="footer-bottom"><span>Book directly via Google Calendar or DM. Based in Florence, SC. © Ashawniz Nailz</span></div>
    </div>
  </footer>
</div>
<script>
  (function() {
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener("click", function(e) {
        const targetId = this.getAttribute("href");
        if (targetId === "#" || targetId === "") return;
        const targetElem = document.querySelector(targetId);
        if (targetElem) {
          e.preventDefault();
          window.scrollTo({ top: targetElem.offsetTop - 80, behavior: "smooth" });
          const navLinks = document.querySelector(".nav-links");
          if (navLinks && navLinks.classList.contains("open")) navLinks.classList.remove("open");
        }
      });
    });
    const track = document.getElementById("galleryTrack");
    const prev = document.getElementById("galleryPrev");
    const next = document.getElementById("galleryNext");
    if (track && prev && next) {
      const getScrollAmount = () => { const slide = track.querySelector(".gallery-slide"); return slide ? slide.offsetWidth + 12 : 200; };
      prev.addEventListener("click", () => track.scrollBy({ left: -getScrollAmount(), behavior: "smooth" }));
      next.addEventListener("click", () => track.scrollBy({ left: getScrollAmount(), behavior: "smooth" }));
    }
  })();
</script>
</body>
</html>
