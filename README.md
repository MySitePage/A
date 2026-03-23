<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover, user-scalable=yes" />
  <title>Ashawniz Nailz | South Carolina Nail Tech</title>
  <meta name="description" content="Ashawniz Nailz — registered cosmetologist in South Carolina. Acrylic sets, pedicures, custom designs, and mobile services in Florence, SC area." />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Pacifico&display=swap" rel="stylesheet" />
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --primary-gradient: linear-gradient(135deg, #ffb3e6, #ff99cc);
      --secondary-gradient: linear-gradient(135deg, #d9b3ff, #b366ff);
      --page-bg-gradient: linear-gradient(135deg, #ffccff 0%, #ffb3e6 45%, #d9b3ff 55%, #b366ff 100%);
      --pink-light: #ffe6f2;
      --pink-medium: #ffb3e6;
      --pink-dark: #ff99cc;
      --purple-light: #e6d9ff;
      --purple-medium: #d9b3ff;
      --purple-dark: #b366ff;
      --light: #ffffff;
      --text-dark: #5a3d5c;
      --text-light: #7a5a7c;
      --shadow-soft: 0 18px 40px rgba(255, 179, 230, 0.3);
      --radius-lg: 24px;
      --radius-pill: 999px;
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

    a { text-decoration: none; color: inherit; }
    img { max-width: 100%; display: block; }

    .container {
      width: 100%;
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 1rem;
    }

    /* HEADER - FIXED LAYOUT, BETTER MOBILE */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(22px);
      background: linear-gradient(to right, rgba(255, 179, 230, 0.96), rgba(217, 179, 255, 0.96));
      border-bottom: 2px solid rgba(255, 255, 255, 0.8);
      box-shadow: 0 4px 20px rgba(255, 179, 230, 0.3);
    }

    .nav {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 0.7rem 0;
      gap: 0.8rem;
      flex-wrap: wrap;
    }

    .logo-group {
      display: flex;
      align-items: center;
      gap: 0.6rem;
      flex-shrink: 0;
    }

    .logo-circle {
      width: 38px;
      height: 38px;
      border-radius: 50%;
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      box-shadow: 0 0 15px rgba(255, 179, 230, 0.6);
      border: 2px solid rgba(255, 255, 255, 0.9);
    }

    .logo-text-main {
      font-family: "Pacifico", cursive;
      font-size: 1.15rem;
      letter-spacing: 0.03em;
      color: var(--text-dark);
      line-height: 1.2;
    }

    .logo-text-sub {
      font-size: 0.6rem;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      color: var(--text-light);
    }

    .nav-links {
      display: flex;
      align-items: center;
      gap: 1rem;
      flex-wrap: wrap;
    }

    .nav-links a {
      position: relative;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      font-weight: 600;
      font-size: 0.7rem;
      color: var(--text-dark);
      white-space: nowrap;
      padding: 0.3rem 0;
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.2rem;
      width: 0;
      height: 2px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--pink-medium), var(--purple-medium));
      transition: width 0.2s ease;
    }

    .nav-links a:hover::after { width: 100%; }

    .nav-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
      padding: 0.45rem 1rem;
      border-radius: var(--radius-pill);
      background: var(--light);
      color: var(--text-dark);
      font-size: 0.68rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.12em;
      border: 2px solid rgba(255, 255, 255, 0.9);
      box-shadow: 0 0 12px rgba(255, 179, 230, 0.4);
      transition: all 0.2s ease;
      white-space: nowrap;
    }

    .nav-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 4px 15px rgba(255, 179, 230, 0.6);
    }

    .nav-toggle {
      display: none;
      background: none;
      border: none;
      font-size: 1.6rem;
      cursor: pointer;
      color: var(--text-dark);
      padding: 0.2rem;
      line-height: 1;
    }

    /* MOBILE HEADER COLLAPSE */
    @media (max-width: 780px) {
      .nav {
        flex-wrap: nowrap;
        position: relative;
      }
      .nav-links {
        position: absolute;
        top: 100%;
        left: 0;
        right: 0;
        flex-direction: column;
        align-items: flex-start;
        padding: 1rem 1.2rem 1.2rem;
        background: linear-gradient(to right, rgba(255, 179, 230, 0.98), rgba(217, 179, 255, 0.98));
        border-bottom: 2px solid rgba(255, 255, 255, 0.8);
        transform: scaleY(0);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.2s ease, opacity 0.2s ease;
        transform-origin: top;
        gap: 0.9rem;
        backdrop-filter: blur(20px);
        z-index: 100;
        border-radius: 0 0 24px 24px;
        box-shadow: 0 15px 30px rgba(0,0,0,0.1);
      }
      .nav-links.open {
        transform: scaleY(1);
        opacity: 1;
        pointer-events: auto;
      }
      .nav-links a {
        width: 100%;
        font-size: 0.85rem;
        padding: 0.5rem 0;
      }
      .nav-btn {
        width: auto;
        justify-content: center;
        margin-top: 0.2rem;
      }
      .nav-toggle {
        display: block;
      }
    }

    @media (max-width: 480px) {
      .logo-text-main { font-size: 1rem; }
      .logo-circle { width: 32px; height: 32px; }
      .logo-text-sub { font-size: 0.55rem; }
    }

    /* Hero Grid - better mobile stacking */
    .hero { padding: 2rem 0 2rem; }
    .hero-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 1.8rem;
      align-items: start;
    }
    @media (min-width: 900px) {
      .hero-grid {
        grid-template-columns: 1.4fr 1fr;
        gap: 2rem;
      }
    }

    .eyebrow {
      text-transform: uppercase;
      font-size: 0.7rem;
      letter-spacing: 0.2em;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      margin-bottom: 0.6rem;
      color: var(--text-light);
    }
    .eyebrow-dot { width: 7px; height: 7px; border-radius: 50%; background: var(--pink-medium); }
    .hero h1 {
      font-size: clamp(1.8rem, 5vw, 2.8rem);
      line-height: 1.2;
      margin-bottom: 0.7rem;
    }
    .hero h1 span.highlight {
      background: linear-gradient(135deg, #ff99cc, #b366ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-subtitle { font-size: 0.9rem; opacity: 0.9; margin-bottom: 1.2rem; color: var(--text-light); }
    .hero-badges { display: flex; flex-wrap: wrap; gap: 0.5rem; margin-bottom: 1.2rem; }
    .badge {
      padding: 0.4rem 0.8rem;
      font-size: 0.65rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.75);
      backdrop-filter: blur(8px);
      border: 1.5px solid rgba(255, 255, 255, 0.8);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }
    .badge-dot { width: 6px; height: 6px; border-radius: 50%; background: var(--pink-medium); }
    .hero-actions { display: flex; flex-wrap: wrap; gap: 0.7rem; margin-bottom: 1.2rem; }
    .btn-primary, .btn-secondary {
      border-radius: var(--radius-pill);
      padding: 0.7rem 1.3rem;
      font-size: 0.75rem;
      font-weight: 700;
      letter-spacing: 0.08em;
      text-transform: uppercase;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      transition: all 0.2s ease;
      cursor: pointer;
      white-space: nowrap;
    }
    @media (max-width: 480px) {
      .btn-primary, .btn-secondary { white-space: normal; text-align: center; padding: 0.6rem 1rem; font-size: 0.7rem; }
    }
    .btn-primary {
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      color: var(--text-dark);
      box-shadow: 0 12px 25px rgba(255, 179, 230, 0.4);
    }
    .btn-primary:hover { transform: translateY(-2px); }
    .btn-secondary {
      background: rgba(255, 255, 255, 0.85);
      border: 1.5px solid rgba(255, 179, 230, 0.6);
      backdrop-filter: blur(8px);
    }
    .hero-meta { font-size: 0.7rem; opacity: 0.85; }

    /* Booking Card - fully responsive */
    .booking-card {
      background: rgba(255, 255, 255, 0.88);
      backdrop-filter: blur(16px);
      border-radius: 28px;
      padding: 1.2rem;
      box-shadow: var(--shadow-soft);
      border: 2px solid rgba(255, 255, 255, 0.9);
    }
    .booking-header { font-size: 1.1rem; margin-bottom: 0.2rem; }
    .booking-sub { font-size: 0.7rem; margin-bottom: 1rem; }
    .form-group { margin-bottom: 0.9rem; }
    .form-group label { font-size: 0.68rem; margin-bottom: 0.25rem; }
    .form-group input, .form-group select, .form-group textarea {
      padding: 0.6rem 0.85rem;
      font-size: 0.8rem;
    }
    .form-row { display: grid; grid-template-columns: 1fr; gap: 0.7rem; }
    @media (min-width: 550px) {
      .form-row { grid-template-columns: 1fr 1fr; gap: 0.8rem; }
    }
    .checkbox-group { gap: 0.5rem; }
    .checkbox-item {
      padding: 0.3rem 0.7rem;
      font-size: 0.7rem;
    }
    .booking-note { font-size: 0.68rem; padding: 0.6rem; margin: 0.8rem 0; }
    .submit-btn { padding: 0.7rem; font-size: 0.8rem; }

    /* Sections spacing */
    section { padding: 2rem 0; }
    .section-heading { margin-bottom: 1.5rem; }
    .section-heading span.kicker { font-size: 0.7rem; letter-spacing: 0.2em; }
    .section-heading h2 { font-size: 1.4rem; }
    .section-heading p { font-size: 0.85rem; padding: 0 0.5rem; }

    /* Cards grid responsive */
    .about-grid, .services-grid, .policy-grid {
      display: grid;
      gap: 1rem;
    }
    .about-grid { grid-template-columns: 1fr; }
    .services-grid { grid-template-columns: 1fr; }
    .policy-grid { grid-template-columns: 1fr; }
    @media (min-width: 700px) {
      .about-grid { grid-template-columns: 1fr 1fr; }
      .services-grid { grid-template-columns: repeat(2, 1fr); }
      .policy-grid { grid-template-columns: repeat(2, 1fr); }
    }
    @media (min-width: 980px) {
      .services-grid { grid-template-columns: repeat(3, 1fr); }
      .policy-grid { grid-template-columns: repeat(3, 1fr); }
    }
    .card {
      background: rgba(255, 255, 255, 0.85);
      border-radius: 24px;
      padding: 1.2rem;
      backdrop-filter: blur(12px);
      border: 1.5px solid rgba(255, 255, 255, 0.9);
      transition: all 0.2s ease;
    }
    .card:hover { transform: translateY(-3px); }
    .price-item { font-size: 0.82rem; margin-bottom: 0.3rem; }
    .policy-tag { font-size: 0.65rem; padding: 0.2rem 0.6rem; }

    /* Gallery */
    .gallery-strip { padding: 0.8rem; }
    .gallery-slide { min-width: 150px; max-width: 200px; }
    .gallery-controls { flex-wrap: wrap; gap: 0.5rem; margin-top: 0.6rem; }
    .gallery-btn { padding: 0.2rem 0.7rem; font-size: 0.75rem; }

    /* Footer */
    footer { padding: 1.5rem 0; margin-top: 0.5rem; }
    .footer-top { flex-direction: column; align-items: flex-start; gap: 0.8rem; }
    .footer-socials { flex-wrap: wrap; gap: 0.5rem; }
    .footer-pill { font-size: 0.7rem; padding: 0.3rem 0.7rem; }
    .footer-bottom { font-size: 0.65rem; margin-top: 0.8rem; flex-direction: column; align-items: flex-start; gap: 0.3rem; }
    @media (min-width: 600px) {
      .footer-top { flex-direction: row; justify-content: space-between; align-items: center; }
      .footer-bottom { flex-direction: row; justify-content: space-between; }
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
        <button class="nav-toggle" aria-label="Toggle navigation" onclick="document.querySelector('.nav-links').classList.toggle('open')">☰</button>
        <div class="nav-links">
          <a href="#services">Services</a>
          <a href="#policies">Policies</a>
          <a href="#location">Location</a>
          <a href="#gallery">Gallery</a>
          <a href="#booking" class="nav-btn"><span class="icon">💅🏾</span><span>Book Now</span></a>
        </div>
      </nav>
    </div>
  </header>

  <main>
    <!-- HERO SECTION with FORM ID and OPTIONAL PHONE -->
    <section class="hero" id="top">
      <div class="container hero-grid">
        <div>
          <div class="eyebrow"><span class="eyebrow-dot"></span> SOUTH CAROLINA NAIL TECH</div>
          <h1>Nails done right. <span class="highlight">Every style. Every color. Every time.</span></h1>
          <p class="hero-subtitle">Registered cosmetologist creating acrylic sets, pedicures, and custom designs for clients who want their nails to match their energy.</p>
          <div class="hero-badges">
            <div class="badge"><span class="badge-dot"></span> Registered Cosmetologist</div>
            <div class="badge"><span class="badge-dot"></span> Florence, SC Area</div>
            <div class="badge"><span class="badge-dot"></span> Travel nail tech · SC (fees apply)</div>
          </div>
          <div class="hero-actions">
            <a class="btn-primary" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" rel="noopener"><span class="btn-icon">📲</span><span>Book via DM</span></a>
            <a class="btn-secondary" href="#services"><span class="btn-icon">👛</span><span>View price list</span></a>
          </div>
          <div class="hero-meta">Send your nail inspo photo when booking so your set can be customized just for you.</div>
        </div>

        <!-- BOOKING FORM - Forminit ID rw0ekqq2y6e, phone optional, LENGTH SECTION REMOVED -->
        <div class="booking-card" id="booking">
          <div class="booking-header"><span>📅</span><span>Request Appointment</span></div>
          <div class="booking-sub">Fill out the form below. I'll reach out within 24 hours to confirm your date & time.</div>

          <form action="https://forminit.com/f/rw0ekqq2y6e" method="POST" enctype="multipart/form-data" id="bookingForm">
            <div class="form-row">
              <div class="form-group"><label>Full Name *</label><input type="text" name="fi-sender-fullName" placeholder="First & last name" required></div>
              <div class="form-group"><label>Email *</label><input type="email" name="fi-sender-email" placeholder="your@email.com" required></div>
            </div>
            <div class="form-row">
              <div class="form-group">
                <label>Phone <span style="font-weight:400; text-transform:none;">(optional)</span></label>
                <input type="tel" name="fi-sender-phone" placeholder="+1 123 456 7890">
                <small style="font-size:0.6rem; display:block; margin-top:0.2rem;">Include country code (e.g., +1 for US). Not required.</small>
              </div>
              <div class="form-group"><label>Instagram (optional)</label><input type="text" name="fi-text-instagram" placeholder="@username"></div>
            </div>
            <div class="form-row">
              <div class="form-group"><label>Preferred Date *</label><input type="date" name="fi-date-preferred" required><small style="font-size:0.6rem;">*request - I will confirm</small></div>
              <div class="form-group"><label>Preferred Time</label><input type="text" name="fi-text-time" placeholder="e.g., 2pm, afternoon"></div>
            </div>

            <div class="form-group"><label>Select Services (can choose multiple) *</label>
              <div class="checkbox-group">
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Full Set Acrylic - $60"> Full Set Acrylic ($60)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Acrylic Design Set - $75"> Acrylic Design ($75)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Acrylic Charm Set - $75"> Acrylic Charm ($75)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Acrylic Charm/Design Set - $85"> Charm/Design Set ($85)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Basic Manicure - $45"> Basic Manicure ($45)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Classic Pedicure - $45"> Classic Pedicure ($45)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Deluxe Pedicure - $50"> Deluxe Pedicure ($50)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-service" value="Luxury Pedicure - $55"> Luxury Pedicure ($55)</label>
              </div>
            </div>

            <div class="form-group"><label>Add-Ons (select any extras)</label>
              <div class="checkbox-group">
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="2 Acrylic toes - $15"> 2 Acrylic toes (+$15)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Design full set - $35"> Design full set (+$35)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Charm full set - $35"> Charm full set (+$35)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Design/charm full set - $49"> Design/charm full set (+$49)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Polish change - $18"> Polish change (+$18)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Acrylic toes refill - $12"> Acrylic toes refill (+$12)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Acrylic nails refill - $42"> Acrylic nails refill (+$42)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-addons" value="Freestyle - $50"> Freestyle (+$50)</label>
              </div>
            </div>

            <!-- LENGTH SECTION REMOVED - NO LONGER DISPLAYED -->

            <div class="form-group file-upload"><label>Inspo Photo (optional)</label><input type="file" name="fi-file-inspo" accept="image/*"><small style="font-size:0.6rem;">Upload a photo of your nail inspiration</small></div>
            <div class="form-group"><label>Anything else? (design ideas, questions, etc.)</label><textarea name="fi-text-notes" placeholder="Tell me about your vision or any special requests..." rows="2"></textarea></div>
            <div class="booking-note"><strong>📌 Important:</strong> Your preferred date is a request and may not be available. I will reach out to confirm your appointment and handle payment details. A $20 deposit is required to secure your booking.</div>
            <button type="submit" class="submit-btn">Send Booking Request</button>
          </form>
          <div class="social-row" style="margin-top: 1rem; display: flex; justify-content: center; gap: 0.6rem;">
            <a href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" class="social-pill" style="width: auto; padding: 0.4rem 0.9rem; border-radius: 999px; background: rgba(255,255,255,0.8); font-size:0.7rem;">TikTok</a>
            <a href="https://instagram.com/ashawniz.nailz" target="_blank" class="social-pill" style="width: auto; padding: 0.4rem 0.9rem; border-radius: 999px; background: rgba(255,255,255,0.8); font-size:0.7rem;">Instagram</a>
          </div>
        </div>
      </div>
    </section>

    <!-- LOCATION / ABOUT -->
    <section id="location">
      <div class="container">
        <div class="section-heading"><span class="kicker">About &amp; location</span><h2>Where to find Ashawniz Nailz</h2><p>Full glam acrylic sets or relaxing pedicures — everything with pink & purple energy.</p></div>
        <div class="about-grid">
          <div class="card"><div class="policy-tag"><i>💅🏾</i> Registered Cosmetologist</div><h3>The experience</h3><p>Personalized appointments. Bring your inspo, ideas, or vibe — together we create your perfect set.</p></div>
          <div class="card"><div class="policy-tag"><i>📍</i> Florence, SC area</div><h3>Service Area & Travel</h3><p>Based in Florence, SC. Mobile appointments across South Carolina (travel fees apply). Book via DM or form.</p></div>
        </div>
      </div>
    </section>

    <!-- SERVICES -->
    <section id="services">
      <div class="container">
        <div class="section-heading"><span class="kicker">Services &amp; pricing</span><h2>Price list</h2><p>Deposits go toward total. Final balance: cash or Cash App <b>$AshawnizNailz</b>.</p></div>
        <div class="services-grid">
          <div class="card"><h3>Acrylic Sets & Manicures</h3><div class="price-item"><span class="price-title">Full Set Acrylic</span><span>$60</span></div><div class="price-item"><span class="price-title">Acrylic Design Set</span><span>$75</span></div><div class="price-item"><span class="price-title">Acrylic Charm Set</span><span>$75</span></div><div class="price-item"><span class="price-title">Acrylic Charm/Design</span><span>$85</span></div><div class="price-item"><span class="price-title">Basic Manicure</span><span>$45</span></div><div class="price-item"><span class="price-title">Design Manicure</span><span>$50</span></div></div>
          <div class="card"><h3>Pedicure Menu</h3><div class="price-item"><span class="price-title">Classic Pedicure</span><span>$45</span></div><div class="price-item"><span class="price-title">Deluxe Pedicure</span><span>$50</span></div><div class="price-item"><span class="price-title">Luxury Pedicure</span><span>$55</span></div><p style="font-size:0.75rem; margin-top:0.5rem;">✨ Dry pedicure also available</p></div>
          <div class="card"><h3>Add-Ons & Refills</h3><div class="price-item"><span>2 Acrylic toes</span><span>$15</span></div><div class="price-item"><span>Design full set</span><span>$35</span></div><div class="price-item"><span>Charm full set</span><span>$35</span></div><div class="price-item"><span>Acrylic nails refill</span><span>$42</span></div><div class="price-item"><span>Soak Off</span><span>$15</span></div><div class="price-item"><span>Deposit</span><span>$20</span></div></div>
        </div>
      </div>
    </section>

    <!-- POLICIES -->
    <section id="policies">
      <div class="container">
        <div class="section-heading"><span class="kicker">Policies</span><h2>Before you book</h2><p>Deposits and time rules keep everything professional.</p></div>
        <div class="policy-grid">
          <div class="card"><div class="policy-tag-row"><span class="policy-tag">Deposits</span><span class="policy-tag">$20 non-refundable</span></div><h3>Deposit Policy</h3><p>$20 deposit required within 24h of booking. No refunds after services.</p></div>
          <div class="card"><div class="policy-tag-row"><span class="policy-tag">Timing</span><span class="policy-tag">Late & No-Show</span></div><h3>Late Policy</h3><p>10-min grace period, after that $10 late fee. After 15 min appointment may be canceled.</p></div>
          <div class="card"><div class="policy-tag-row"><span class="policy-tag">Nail prep</span><span class="policy-tag">Payments</span></div><h3>Prep & Payments</h3><p>Arrive with bare nails unless soak-off added. Cash or Cash App accepted.</p></div>
        </div>
      </div>
    </section>

    <!-- GALLERY -->
    <section id="gallery">
      <div class="container">
        <div class="section-heading"><span class="kicker">Client work</span><h2>Gallery preview</h2><p>Swipe to see recent sets by Ashawniz Nailz.</p></div>
        <div class="card">
          <div class="gallery-strip">
            <div class="gallery-track" id="galleryTrack">
              <div class="gallery-slide"><img src="https://i.postimg.cc/ZqYtzPjx/IMG-7932.jpg" alt="Nail set 1"></div>
              <div class="gallery-slide"><img src="https://i.postimg.cc/ZqYtzPjP/IMG-7936.jpg" alt="Nail set 2"></div>
              <div class="gallery-slide"><img src="https://i.postimg.cc/R0C5x1Gw/IMG-7937.jpg" alt="Nail set 3"></div>
              <div class="gallery-slide"><img src="https://i.postimg.cc/XvNS6KxF/IMG-7938.jpg" alt="Nail set 4"></div>
              <div class="gallery-slide"><img src="https://i.postimg.cc/tgRQGdDx/IMG-7939.jpg" alt="Nail set 5"></div>
              <div class="gallery-slide"><img src="https://i.postimg.cc/q7BVHcQh/IMG-7940.jpg" alt="Nail set 6"></div>
              <div class="gallery-slide"><img src="https://i.postimg.cc/R0C5x1GS/IMG-7941.jpg" alt="Nail set 7"></div>
            </div>
            <div class="gallery-controls" style="display:flex; justify-content:space-between; margin-top:0.8rem; align-items:center; flex-wrap:wrap;">
              <span style="font-size:0.65rem;">← → swipe or click arrows</span>
              <div><button class="gallery-btn" id="galleryPrev">← Prev</button><button class="gallery-btn" id="galleryNext" style="margin-left:0.4rem;">Next →</button></div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-top">
        <div><div class="logo-text-main" style="font-size:1rem;">Ashawniz Nailz</div><div class="logo-text-sub">South Carolina Nail Tech · Pink & Purple Vibes</div></div>
        <div class="footer-socials">
          <a class="footer-pill" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank">TikTok · @ashawniz.nailz</a>
          <a class="footer-pill" href="https://instagram.com/ashawniz.nailz" target="_blank">Instagram · @ashawniz.nailz</a>
        </div>
      </div>
      <div class="footer-bottom"><span>Bookings via DM or booking form. Based in Florence, SC area. © Ashawniz Nailz</span></div>
    </div>
  </footer>
</div>

<script>
  (function() {
    // smooth scroll + close mobile menu
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener("click", function(e) {
        const targetId = this.getAttribute("href");
        if (targetId === "#" || targetId === "") return;
        const targetElem = document.querySelector(targetId);
        if (targetElem) {
          e.preventDefault();
          window.scrollTo({ top: targetElem.offsetTop - 70, behavior: "smooth" });
          const navLinks = document.querySelector(".nav-links");
          if (navLinks && navLinks.classList.contains("open")) navLinks.classList.remove("open");
        }
      });
    });
    // gallery arrows
    const track = document.getElementById("galleryTrack");
    const prev = document.getElementById("galleryPrev");
    const next = document.getElementById("galleryNext");
    if (track && prev && next) {
      const scrollStep = () => { const slide = track.querySelector(".gallery-slide"); return slide ? slide.offsetWidth + 12 : 170; };
      prev.addEventListener("click", () => track.scrollBy({ left: -scrollStep(), behavior: "smooth" }));
      next.addEventListener("click", () => track.scrollBy({ left: scrollStep(), behavior: "smooth" }));
    }
  })();
</script>
</body>
</html>
