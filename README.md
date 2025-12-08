<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Ashawniz Nailz | South Carolina Nail Tech</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Pacifico&display=swap" rel="stylesheet" />
  <style>
    :root {
      --bg-gradient: linear-gradient(135deg, #ff5fd8, #b400ff);
      --bg-gradient-alt: radial-gradient(circle at top left, #ff8adf, #7b00ff);
      --pink: #ff7ad9;
      --purple: #7a00ff;
      --dark: #06030a;
      --card: rgba(0, 0, 0, 0.75);
      --light: #ffffff;
      --accent: #ffb3f1;
      --shadow-soft: 0 18px 40px rgba(0, 0, 0, 0.55);
      --radius-lg: 24px;
      --radius-pill: 999px;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: var(--bg-gradient-alt);
      color: var(--light);
      min-height: 100vh;
      line-height: 1.6;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    /* Layout */
    .page {
      min-height: 100vh;
      background: radial-gradient(circle at top, rgba(255, 255, 255, 0.18), transparent 60%),
                  radial-gradient(circle at bottom, rgba(0, 0, 0, 0.8), #050008);
      color: #fdf4ff;
    }

    .container {
      width: 100%;
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 1.4rem;
    }

    /* Header / Nav */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(22px);
      background: linear-gradient(to right, rgba(0, 0, 0, 0.85), rgba(15, 0, 32, 0.85));
      border-bottom: 1px solid rgba(255, 255, 255, 0.04);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.9rem 0;
      gap: 1rem;
    }

    .logo-group {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .logo-circle {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background: var(--bg-gradient);
      box-shadow: 0 0 18px rgba(255, 122, 217, 0.85);
      border: 2px solid rgba(255, 255, 255, 0.6);
    }

    .logo-text-main {
      font-family: "Pacifico", cursive;
      font-size: 1.25rem;
      letter-spacing: 0.04em;
    }

    .logo-text-sub {
      font-size: 0.65rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      opacity: 0.8;
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1.4rem;
      font-size: 0.9rem;
    }

    .nav-links a {
      position: relative;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      font-weight: 500;
      font-size: 0.72rem;
      opacity: 0.85;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.3rem;
      width: 0;
      height: 2px;
      border-radius: 999px;
      background: linear-gradient(90deg, #ffb3f1, #ff3bd6, #b57bff);
      transition: width 0.23s ease-out;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

    .nav-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.5rem 1rem;
      border-radius: var(--radius-pill);
      background: radial-gradient(circle at top left, #ffb3f1, #b400ff);
      font-size: 0.72rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      border: 1px solid rgba(255, 255, 255, 0.18);
      box-shadow: 0 0 16px rgba(255, 122, 217, 0.8);
      cursor: pointer;
    }

    .nav-btn span.icon {
      font-size: 1rem;
    }

    /* Mobile nav */
    .nav-toggle {
      display: none;
      background: none;
      border: none;
      color: white;
      font-size: 1.5rem;
      cursor: pointer;
    }

    @media (max-width: 768px) {
      .nav-links {
        position: absolute;
        inset: 100% 0 auto 0;
        flex-direction: column;
        align-items: flex-start;
        padding: 1rem 1.4rem 1.4rem;
        background: radial-gradient(circle at top left, #1d002b, #050008);
        border-bottom: 1px solid rgba(255, 255, 255, 0.08);
        transform-origin: top;
        transform: scaleY(0);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.2s ease-out, opacity 0.2s ease-out;
      }

      .nav-links.open {
        transform: scaleY(1);
        opacity: 1;
        pointer-events: auto;
      }

      .nav-btn {
        width: 100%;
        justify-content: center;
      }

      .nav-toggle {
        display: block;
      }
    }

    /* Hero */
    .hero {
      padding: 3.5rem 0 2.5rem;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 2.3rem;
      align-items: center;
    }

    @media (max-width: 900px) {
      .hero-grid {
        grid-template-columns: 1fr;
        padding-top: 1.5rem;
      }
    }

    .eyebrow {
      text-transform: uppercase;
      font-size: 0.75rem;
      letter-spacing: 0.26em;
      color: var(--accent);
      opacity: 0.95;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      margin-bottom: 0.6rem;
    }

    .eyebrow-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: var(--accent);
      box-shadow: 0 0 12px rgba(255, 158, 235, 1);
    }

    .hero h1 {
      font-size: clamp(2.1rem, 4vw, 3rem);
      line-height: 1.1;
      margin-bottom: 0.75rem;
    }

    .hero h1 span.highlight {
      background: var(--bg-gradient);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      text-shadow: 0 0 20px rgba(255, 122, 217, 0.75);
    }

    .hero-subtitle {
      font-size: 0.95rem;
      max-width: 32rem;
      opacity: 0.9;
      margin-bottom: 1.3rem;
    }

    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 1.4rem;
    }

    .badge {
      padding: 0.4rem 0.85rem;
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(255, 255, 255, 0.22);
      background: rgba(0, 0, 0, 0.6);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }

    .badge-dot {
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: #ff7ad9;
    }

    .hero-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
      margin-bottom: 1.8rem;
    }

    .btn-primary,
    .btn-secondary {
      border-radius: var(--radius-pill);
      padding: 0.8rem 1.5rem;
      font-size: 0.85rem;
      font-weight: 600;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      border: 1px solid transparent;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      transition: transform 0.14s ease-out, box-shadow 0.14s ease-out, background 0.14s ease-out;
      white-space: nowrap;
    }

    .btn-primary {
      background: var(--bg-gradient);
      box-shadow: 0 18px 40px rgba(0, 0, 0, 0.7);
    }

    .btn-primary:hover {
      transform: translateY(-1px) scale(1.01);
      box-shadow: 0 24px 55px rgba(0, 0, 0, 0.85);
    }

    .btn-secondary {
      background: rgba(0, 0, 0, 0.6);
      border-color: rgba(255, 255, 255, 0.18);
    }

    .btn-secondary:hover {
      background: rgba(0, 0, 0, 0.8);
      transform: translateY(-1px);
    }

    .btn-icon {
      font-size: 1rem;
    }

    .hero-meta {
      font-size: 0.75rem;
      opacity: 0.85;
    }

    /* Hero card / fake gallery */
    .hero-card {
      background: radial-gradient(circle at top, rgba(255, 133, 219, 0.26), rgba(0, 0, 0, 0.96));
      border-radius: 32px;
      padding: 1.3rem 1.3rem 1.1rem;
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(255, 255, 255, 0.1);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: -60%;
      background: radial-gradient(circle at top left, rgba(255, 255, 255, 0.15), transparent 55%);
      opacity: 0.7;
      mix-blend-mode: screen;
      pointer-events: none;
    }

    .hero-card-header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-bottom: 0.7rem;
      position: relative;
      z-index: 1;
    }

    .hero-card-title {
      font-size: 0.85rem;
      font-weight: 600;
      letter-spacing: 0.12em;
      text-transform: uppercase;
    }

    .hero-card-pill {
      padding: 0.3rem 0.75rem;
      border-radius: var(--radius-pill);
      background: rgba(0, 0, 0, 0.7);
      font-size: 0.68rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
    }

    .hero-gallery {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 0.35rem;
      margin-bottom: 0.8rem;
      position: relative;
      z-index: 1;
    }

    .hero-thumb {
      aspect-ratio: 3 / 4;
      border-radius: 18px;
      overflow: hidden;
      background: linear-gradient(135deg, #ff7ad9, #7b00ff);
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.65rem;
      text-align: center;
      padding: 0.4rem;
      border: 1px solid rgba(255, 255, 255, 0.15);
      box-shadow: 0 8px 22px rgba(0, 0, 0, 0.6);
      transform: translateY(0);
      transition: transform 0.18s ease-out, box-shadow 0.18s ease-out;
    }

    .hero-thumb:nth-child(2) {
      transform: translateY(4px);
    }

    .hero-thumb:nth-child(3) {
      transform: translateY(8px);
    }

    .hero-thumb:hover {
      transform: translateY(-3px);
      box-shadow: 0 14px 32px rgba(0, 0, 0, 0.9);
    }

    .hero-card-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.7rem;
      opacity: 0.9;
      position: relative;
      z-index: 1;
    }

    .social-row {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }

    .social-pill {
      width: 26px;
      height: 26px;
      border-radius: 999px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(0, 0, 0, 0.7);
      border: 1px solid rgba(255, 255, 255, 0.18);
      font-size: 0.75rem;
    }

    /* Sections */
    section {
      padding: 2.6rem 0;
    }

    .section-heading {
      text-align: center;
      margin-bottom: 1.8rem;
    }

    .section-heading span.kicker {
      font-size: 0.75rem;
      letter-spacing: 0.26em;
      text-transform: uppercase;
      color: var(--accent);
      display: block;
      margin-bottom: 0.4rem;
    }

    .section-heading h2 {
      font-size: 1.6rem;
      margin-bottom: 0.3rem;
    }

    .section-heading p {
      font-size: 0.9rem;
      opacity: 0.85;
      max-width: 35rem;
      margin: 0 auto;
    }

    /* About / Location */
    .about-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.3fr) minmax(0, 1fr);
      gap: 1.8rem;
    }

    @media (max-width: 900px) {
      .about-grid {
        grid-template-columns: 1fr;
      }
    }

    .card {
      background: var(--card);
      border-radius: var(--radius-lg);
      padding: 1.4rem 1.4rem 1.35rem;
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .card h3 {
      font-size: 1.05rem;
      margin-bottom: 0.6rem;
    }

    .card p {
      font-size: 0.88rem;
      opacity: 0.9;
    }

    .pill-chip {
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
      padding: 0.25rem 0.65rem;
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.06);
      border: 1px solid rgba(255, 255, 255, 0.12);
      margin-bottom: 0.6rem;
    }

    .pill-chip i {
      font-style: normal;
      font-size: 0.8rem;
    }

    .about-list {
      list-style: none;
      margin-top: 0.6rem;
      font-size: 0.86rem;
    }

    .about-list li {
      margin-bottom: 0.3rem;
      display: flex;
      gap: 0.4rem;
      align-items: flex-start;
    }

    .about-dot {
      margin-top: 0.35rem;
      width: 5px;
      height: 5px;
      border-radius: 50%;
      background: var(--accent);
      flex-shrink: 0;
    }

    .location-block {
      margin-top: 0.6rem;
      font-size: 0.86rem;
    }

    .location-block strong {
      display: block;
      font-size: 0.9rem;
      margin-bottom: 0.2rem;
    }

    /* Services */
    .services-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.2rem;
    }

    @media (max-width: 900px) {
      .services-grid {
        grid-template-columns: 1fr;
      }
    }

    .service-card h3 {
      font-size: 1rem;
      margin-bottom: 0.4rem;
    }

    .service-card small {
      font-size: 0.75rem;
      opacity: 0.8;
      display: block;
      margin-bottom: 0.6rem;
    }

    .price-item {
      display: flex;
      justify-content: space-between;
      gap: 0.6rem;
      font-size: 0.85rem;
      margin-bottom: 0.3rem;
    }

    .price-title {
      font-weight: 500;
    }

    .price-desc {
      font-size: 0.78rem;
      opacity: 0.8;
      margin-bottom: 0.35rem;
    }

    .addon-title {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      opacity: 0.8;
      margin-top: 0.6rem;
      margin-bottom: 0.25rem;
    }

    /* Policies */
    .policy-grid {
      display: grid;
      grid-template-columns: repeat(3, minmax(0, 1fr));
      gap: 1.1rem;
    }

    @media (max-width: 900px) {
      .policy-grid {
        grid-template-columns: 1fr;
      }
    }

    .policy-card h3 {
      font-size: 0.98rem;
      margin-bottom: 0.4rem;
    }

    .policy-card p {
      font-size: 0.83rem;
      opacity: 0.9;
      margin-bottom: 0.35rem;
    }

    .policy-card ul {
      list-style: none;
      font-size: 0.83rem;
    }

    .policy-card ul li {
      margin-bottom: 0.32rem;
      display: flex;
      gap: 0.4rem;
    }

    .policy-tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-bottom: 0.45rem;
    }

    .policy-tag {
      font-size: 0.7rem;
      padding: 0.24rem 0.6rem;
      background: rgba(255, 255, 255, 0.06);
      border-radius: var(--radius-pill);
      border: 1px solid rgba(255, 255, 255, 0.14);
    }

    /* Booking strip */
    .booking-strip {
      margin-top: 2rem;
      background: linear-gradient(120deg, rgba(255, 122, 217, 0.35), rgba(123, 0, 255, 0.96));
      border-radius: var(--radius-lg);
      padding: 1.2rem 1.3rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
      align-items: center;
      justify-content: space-between;
      box-shadow: var(--shadow-soft);
      border: 1px solid rgba(255, 255, 255, 0.18);
    }

    .booking-strip-text {
      font-size: 0.9rem;
      max-width: 26rem;
    }

    .booking-strip-text strong {
      font-size: 1rem;
    }

    .booking-strip-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
    }

    /* GALLERY SWIPE */
    .gallery-strip {
      border-radius: 20px;
      padding: 1rem 0.9rem 1rem;
      background: rgba(0, 0, 0, 0.6);
      border: 1px solid rgba(255, 255, 255, 0.1);
    }

    .gallery-track {
      display: flex;
      gap: 0.75rem;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      -webkit-overflow-scrolling: touch;
      padding-bottom: 0.4rem;
    }

    .gallery-track::-webkit-scrollbar {
      height: 6px;
    }

    .gallery-track::-webkit-scrollbar-track {
      background: rgba(255, 255, 255, 0.06);
      border-radius: 999px;
    }

    .gallery-track::-webkit-scrollbar-thumb {
      background: rgba(255, 255, 255, 0.35);
      border-radius: 999px;
    }

    .gallery-slide {
      flex: 0 0 auto;
      min-width: 180px;
      max-width: 260px;
      aspect-ratio: 3 / 4;
      border-radius: 18px;
      overflow: hidden;
      position: relative;
      scroll-snap-align: center;
      box-shadow: 0 12px 30px rgba(0, 0, 0, 0.85);
      border: 1px solid rgba(255, 255, 255, 0.14);
      background: linear-gradient(135deg, #ff8adf, #7b00ff);
    }

    .gallery-slide img {
      width: 100%;
      height: 100%;
      object-fit: cover;
      display: block;
    }

    .gallery-controls {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 0.6rem;
      font-size: 0.78rem;
      opacity: 0.9;
      gap: 0.75rem;
      flex-wrap: wrap;
    }

    .gallery-buttons {
      display: flex;
      gap: 0.4rem;
    }

    .gallery-btn {
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.4);
      background: rgba(0, 0, 0, 0.7);
      padding: 0.25rem 0.7rem;
      font-size: 0.8rem;
      color: #fff;
      cursor: pointer;
    }

    .gallery-btn:hover {
      background: rgba(0, 0, 0, 0.9);
    }

    /* Footer */
    footer {
      padding: 1.8rem 0 2.4rem;
      border-top: 1px solid rgba(255, 255, 255, 0.08);
      margin-top: 1rem;
    }

    .footer-top {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
      justify-content: space-between;
      font-size: 0.8rem;
    }

    .footer-socials {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .footer-pill {
      padding: 0.3rem 0.65rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(255, 255, 255, 0.16);
      font-size: 0.76rem;
      background: rgba(0, 0, 0, 0.6);
    }

    .footer-bottom {
      margin-top: 1rem;
      font-size: 0.7rem;
      opacity: 0.7;
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      justify-content: space-between;
    }

    @media (max-width: 640px) {
      .hero {
        padding-bottom: 2rem;
      }
      section {
        padding: 2.1rem 0;
      }
      .card {
        padding: 1.15rem 1.1rem 1.1rem;
      }
      .booking-strip {
        padding: 1.1rem 1rem;
      }
    }
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

          <button class="nav-toggle" aria-label="Toggle navigation" onclick="document.querySelector('.nav-links').classList.toggle('open')">
            ☰
          </button>

          <div class="nav-links">
            <a href="#services">Services</a>
            <a href="#policies">Policies</a>
            <a href="#location">Location</a>
            <a href="#gallery">Gallery</a>
            <a href="#contact" class="nav-btn">
              <span class="icon">💅🏾</span>
              <span>Book Now</span>
            </a>
          </div>
        </nav>
      </div>
    </header>

    <main>
      <!-- HERO -->
      <section class="hero" id="top">
        <div class="container hero-grid">
          <div>
            <div class="eyebrow">
              <span class="eyebrow-dot"></span>
              SOUTH CAROLINA NAIL TECH
            </div>
            <h1>
              Nails done right.
              <span class="highlight">Every style. Every color. Every time.</span>
            </h1>
            <p class="hero-subtitle">
              Registered cosmetologist creating acrylic sets, pedicures, and custom designs for
              clients who want their nails to match their energy. DM bookings accepted.
            </p>

            <div class="hero-badges">
              <div class="badge"><span class="badge-dot"></span> Registered Cosmetologist</div>
              <div class="badge"><span class="badge-dot"></span> Florence, SC Area</div>
              <div class="badge"><span class="badge-dot"></span> Travel nail tech · SC (fees apply)</div>
            </div>

            <div class="hero-actions">
              <a class="btn-primary" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" rel="noopener">
                <span class="btn-icon">📲</span>
                <span>Book via DM</span>
              </a>
              <a class="btn-secondary" href="#services">
                <span class="btn-icon">👛</span>
                <span>View price list</span>
              </a>
            </div>

            <div class="hero-meta">
              Send your nail inspo photo when booking so your set can be customized just for you.
            </div>
          </div>

          <aside class="hero-card">
            <div class="hero-card-header">
              <div>
                <div class="hero-card-title">Recent Sets</div>
                <div style="font-size:0.75rem;opacity:0.85;">Soft glam · Bright colors · Bling</div>
              </div>
              <div class="hero-card-pill">SC Nail Tech ⭐</div>
            </div>

            <div class="hero-gallery">
              <div class="hero-thumb">
                <span>Upload a photo of<br />your acrylic sets here.</span>
              </div>
              <div class="hero-thumb">
                <span>Perfect spot for<br />pedicure pics.</span>
              </div>
              <div class="hero-thumb">
                <span>Feature your<br />favorite nail art.</span>
              </div>
            </div>

            <div class="hero-card-footer">
              <div>
                <div style="font-size:0.74rem;opacity:0.9;">Now accepting DM bookings</div>
                <div style="font-size:0.7rem;opacity:0.75;">Based in Florence, SC area</div>
              </div>
              <div class="social-row">
                <a href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" rel="noopener" class="social-pill">TikTok</a>
                <a href="https://instagram.com/ashawniz.nailz" target="_blank" rel="noopener" class="social-pill">IG</a>
              </div>
            </div>
          </aside>
        </div>
      </section>

      <!-- ABOUT / LOCATION -->
      <section id="location">
        <div class="container">
          <div class="section-heading">
            <span class="kicker">About &amp; location</span>
            <h2>Where to find Ashawniz Nailz</h2>
            <p>
              Whether you're booking a full glam acrylic set or a relaxing pedicure, everything is done with care,
              creativity, and a whole lot of pink &amp; purple energy.
            </p>
          </div>

          <div class="about-grid">
            <div class="card">
              <div class="pill-chip"><i>💅🏾</i> Registered Cosmetologist</div>
              <h3>The experience</h3>
              <p>
                Every appointment is personal. Bring your inspo, your ideas, or just your vibe—together, we'll create
                a set that fits your lifestyle, budget, and style.
              </p>
              <ul class="about-list">
                <li>
                  <span class="about-dot"></span>
                  <span>Soft, classy, colorful, or extra — all styles welcome.</span>
                </li>
                <li>
                  <span class="about-dot"></span>
                  <span>Clean tools, detailed prep, and quality products every time.</span>
                </li>
                <li>
                  <span class="about-dot"></span>
                  <span>Respectful, professional environment where your time matters.</span>
                </li>
              </ul>
            </div>

            <div class="card">
              <div class="pill-chip"><i>📍</i> Florence, SC area</div>
              <h3>Service Area &amp; Travel</h3>
              <div class="location-block">
                <strong>Service Area</strong>
                Based in Florence, SC area
              </div>
              <div class="location-block" style="margin-top:0.7rem;">
                <strong>Travel Nail Services</strong>
                Mobile appointments are available across South Carolina. Travel fees apply based on distance —
                message to get a quote for your area.
              </div>
              <div class="location-block" style="margin-top:0.7rem;">
                <strong>Booking</strong>
                Bookings accepted via DM on TikTok or Instagram.
              </div>
            </div>
          </div>
        </div>
      </section>

      <!-- SERVICES -->
      <section id="services">
        <div class="container">
          <div class="section-heading">
            <span class="kicker">Services &amp; pricing</span>
            <h2>Price list</h2>
            <p>Deposits go toward your total. Final balance can be paid in cash or via Cash App at <b>$AshawnizNailz</b>.</p>
          </div>

          <div class="services-grid">
            <!-- Acrylic sets -->
            <div class="card service-card">
              <h3>Acrylic Sets</h3>
              <small>Custom designs, charms, &amp; glam details.</small>

              <div class="price-item">
                <span class="price-title">Full Set</span>
                <span>$50</span>
              </div>

              <div class="price-item">
                <span class="price-title">Design Set</span>
                <span>$65</span>
              </div>

              <div class="price-item">
                <span class="price-title">Charm Set</span>
                <span>$75</span>
              </div>

              <div class="price-item">
                <span class="price-title">Charm / Design Set</span>
                <span>$80</span>
              </div>

              <div class="addon-title">Length add-ons</div>
              <div class="price-item">
                <span class="price-title">Medium</span>
                <span>+ $10</span>
              </div>
              <div class="price-item">
                <span class="price-title">Long</span>
                <span>+ $15</span>
              </div>
              <div class="price-item">
                <span class="price-title">XXL</span>
                <span>+ $20</span>
              </div>
            </div>

            <!-- Pedicures -->
            <div class="card service-card">
              <h3>Pedicure Menu</h3>
              <small>Relaxing, hydrating, and perfect for sandal season.</small>

              <div class="price-item">
                <span class="price-title">Basic Pedicure</span>
                <span>$40</span>
              </div>
              <p class="price-desc">
                Relaxing foot soak, nail shaping, cuticle care &amp; polish.
              </p>

              <div class="price-item">
                <span class="price-title">Spa Pedicure</span>
                <span>$50</span>
              </div>
              <p class="price-desc">
                Includes exfoliating scrub, foot massage &amp; moisturizing mask.
              </p>

              <div class="price-item">
                <span class="price-title">Deluxe Pedicure</span>
                <span>$65</span>
              </div>
              <p class="price-desc">
                Deep exfoliating scrub, callus treatment, hot towel wrap, and soothing massage to leave your feet silky
                and refreshed.
              </p>

              <div class="price-item">
                <span class="price-title">Luxurious Pedicure</span>
                <span>$75</span>
              </div>
              <p class="price-desc">
                Full pampering with exfoliation, hot stones, jelly pedicure, and an extended massage for total
                relaxation.
              </p>
            </div>

            <!-- Other services -->
            <div class="card service-card">
              <h3>Other Services</h3>
              <small>For when you just need a quick fix or removal.</small>

              <div class="price-item">
                <span class="price-title">Nail Repair</span>
                <span>$10 each</span>
              </div>

              <div class="price-item">
                <span class="price-title">Soak Off</span>
                <span>$15</span>
              </div>

              <div class="price-item">
                <span class="price-title">Deposit</span>
                <span>$20</span>
              </div>
              <p class="price-desc">
                Non-refundable deposit required to secure your appointment. Goes toward your total.
              </p>

              <p class="price-desc">
                Book via DM on TikTok or Instagram.
              </p>
            </div>
          </div>

          <!-- Booking CTA -->
          <div class="booking-strip" id="contact">
            <div class="booking-strip-text">
              <strong>Ready to book?</strong><br />
              Send a DM with your name, service, preferred date/time, and your inspo photo so your nails can be planned
              before you arrive.
            </div>
            <div class="booking-strip-actions">
              <a class="btn-primary" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" rel="noopener">
                📲 DM on TikTok
              </a>
              <a class="btn-secondary" href="https://instagram.com/ashawniz.nailz" target="_blank" rel="noopener">
                💖 DM on Instagram
              </a>
            </div>
          </div>
        </div>
      </section>

      <!-- POLICIES -->
      <section id="policies">
        <div class="container">
          <div class="section-heading">
            <span class="kicker">Policies</span>
            <h2>Before you book</h2>
            <p>
              Please read through all policies before booking. Deposits and time rules help keep everything fair and
              professional for every client.
            </p>
          </div>

          <div class="policy-grid">
            <!-- Deposits -->
            <div class="card policy-card">
              <div class="policy-tag-row">
                <span class="policy-tag">Deposits</span>
                <span class="policy-tag">$20 · Non-refundable</span>
              </div>
              <h3>Deposit Policy</h3>
              <p>
                A <b>$20 non-refundable deposit</b> is required to secure every appointment. Your deposit goes toward your total
                balance.
              </p>
              <ul>
                <li><span class="about-dot"></span><span>Deposits must be sent within 24 hours of booking.</span></li>
                <li><span class="about-dot"></span><span>If your deposit is not received on time, your appointment will be canceled.</span></li>
                <li><span class="about-dot"></span><span>Once services are complete, there are <b>no refunds</b>.</span></li>
              </ul>
            </div>

            <!-- Late / No show -->
            <div class="card policy-card">
              <div class="policy-tag-row">
                <span class="policy-tag">Timing</span>
                <span class="policy-tag">Late &amp; No-Show</span>
              </div>
              <h3>Late &amp; No-Show Policy</h3>
              <p><b>Grace Period:</b> There is a 10-minute grace period.</p>
              <ul>
                <li><span class="about-dot"></span><span>After 10 minutes, a <b>$10 late fee</b> is added.</span></li>
                <li><span class="about-dot"></span><span>After 15 minutes, your appointment may be canceled.</span></li>
              </ul>
              <p style="margin-top:0.4rem;">
                <b>No Call / No Show:</b> If you do not show up or contact in advance, you can be blocked from booking
                future appointments.
              </p>
            </div>

            <!-- Prep / Payments / Respect -->
            <div class="card policy-card">
              <div class="policy-tag-row">
                <span class="policy-tag">Nail prep</span>
                <span class="policy-tag">Payments</span>
              </div>
              <h3>Nail Prep &amp; Payments</h3>
              <p>
                Please arrive with <b>bare nails</b> unless you booked a soak-off. Acrylic removal or soak-off is not
                included unless it is added to your appointment.
              </p>
              <p>
                Remaining balances can be paid in <b>cash</b> or via <b>Cash App: $AshawnizNailz</b>.
              </p>
              <p>
                <b>Respect My Time:</b> Come ready, be respectful, and communicate any changes ahead of time. Any
                disrespect before, during, or after your appointment can result in you being blocked as a client.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- GALLERY / SWIPE -->
      <section id="gallery">
        <div class="container">
          <div class="section-heading">
            <span class="kicker">Client work</span>
            <h2>Gallery preview</h2>
            <p>
              Swipe through some of the nail sets and pedicures created by Ashawniz Nailz. Replace or add more photos
              anytime as your work grows.
            </p>
          </div>

          <div class="card">
            <div class="gallery-strip">
              <div class="gallery-track" id="galleryTrack">
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6802.jpeg?raw=1" alt="Client nail set 1 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6803.jpeg?raw=1" alt="Client nail set 2 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6805.jpeg?raw=1" alt="Client nail set 3 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6808.jpeg?raw=1" alt="Client nail set 4 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6809.jpeg?raw=1" alt="Client nail set 5 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6810.jpeg?raw=1" alt="Client nail set 6 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://github.com/Bakerreniya/AshawnizNailz/blob/8c168792d0ef172cfc4bbcf319068f2f89370ffb/IMG_6811.jpeg?raw=1" alt="Client nail set 7 by Ashawniz Nailz" />
                </div>
              </div>

              <div class="gallery-controls">
                <div>Swipe left/right on your phone, or use the arrows to see more sets.</div>
                <div class="gallery-buttons">
                  <button class="gallery-btn" id="galleryPrev">←</button>
                  <button class="gallery-btn" id="galleryNext">→</button>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <!-- FOOTER -->
    <footer>
      <div class="container">
        <div class="footer-top">
          <div>
            <div class="logo-text-main" style="font-size:1.1rem;">Ashawniz Nailz</div>
            <div class="logo-text-sub" style="margin-top:0.14rem;">South Carolina Nail Tech · Pink &amp; Purple Vibes Only</div>
          </div>
          <div class="footer-socials">
            <a class="footer-pill" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" rel="noopener">TikTok · @ashawniz.nailz</a>
            <a class="footer-pill" href="https://instagram.com/ashawniz.nailz" target="_blank" rel="noopener">Instagram · @ashawniz.nailz</a>
            <a class="footer-pill" href="https://facebook.com/ashawniz.nailz" target="_blank" rel="noopener">Facebook · @ashawniz.nailz</a>
          </div>
        </div>

        <div class="footer-bottom">
          <span>Bookings available via DM. Based in Florence, SC area.</span>
          <span>Website design by your web designer 👑</span>
        </div>
      </div>
    </footer>
  </div>

  <!-- Smooth scroll + gallery controls -->
  <script>
    // Smooth scroll
    document.querySelectorAll('a[href^="#"]').forEach(link => {
      link.addEventListener("click", function (e) {
        const target = document.querySelector(this.getAttribute("href"));
        if (!target) return;
        e.preventDefault();
        window.scrollTo({
          top: target.offsetTop - 80,
          behavior: "smooth"
        });
        const navLinks = document.querySelector(".nav-links");
        if (navLinks && navLinks.classList.contains("open")) {
          navLinks.classList.remove("open");
        }
      });
    });

    // Gallery arrows
    const track = document.getElementById("galleryTrack");
    const prevBtn = document.getElementById("galleryPrev");
    const nextBtn = document.getElementById("galleryNext");

    if (track && prevBtn && nextBtn) {
      const scrollAmount = () => {
        const slide = track.querySelector(".gallery-slide");
        return slide ? slide.getBoundingClientRect().width + 12 : 250;
      };

      prevBtn.addEventListener("click", () => {
        track.scrollBy({ left: -scrollAmount(), behavior: "smooth" });
      });

      nextBtn.addEventListener("click", () => {
        track.scrollBy({ left: scrollAmount(), behavior: "smooth" });
      });
    }
  </script>
</body>
</html>
