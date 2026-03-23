<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover" />
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
      line-height: 1.6;
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
      max-width: 1100px;
      margin: 0 auto;
      padding: 0 1.4rem;
    }

    /* HEADER */
    header {
      position: sticky;
      top: 0;
      z-index: 50;
      backdrop-filter: blur(22px);
      background: linear-gradient(to right, rgba(255, 179, 230, 0.92), rgba(217, 179, 255, 0.92));
      border-bottom: 2px solid rgba(255, 255, 255, 0.8);
      box-shadow: 0 4px 30px rgba(255, 179, 230, 0.4);
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
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      box-shadow: 0 0 20px rgba(255, 179, 230, 0.6);
      border: 2px solid rgba(255, 255, 255, 0.9);
    }

    .logo-text-main {
      font-family: "Pacifico", cursive;
      font-size: 1.25rem;
      letter-spacing: 0.04em;
      color: var(--text-dark);
    }

    .logo-text-sub {
      font-size: 0.65rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      color: var(--text-light);
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
      font-weight: 600;
      font-size: 0.72rem;
      color: var(--text-dark);
    }

    .nav-links a::after {
      content: "";
      position: absolute;
      left: 0;
      bottom: -0.3rem;
      width: 0;
      height: 3px;
      border-radius: 999px;
      background: linear-gradient(135deg, var(--pink-medium), var(--purple-medium));
      transition: width 0.23s ease;
    }

    .nav-links a:hover::after { width: 100%; }

    .nav-btn {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      padding: 0.6rem 1.2rem;
      border-radius: var(--radius-pill);
      background: var(--light);
      color: var(--text-dark);
      font-size: 0.72rem;
      font-weight: 700;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      border: 2px solid rgba(255, 255, 255, 0.9);
      box-shadow: 0 0 20px rgba(255, 179, 230, 0.5);
      transition: all 0.3s ease;
    }

    .nav-btn:hover {
      transform: translateY(-3px);
      background: var(--light);
      box-shadow: 0 6px 25px rgba(255, 179, 230, 0.7);
    }

    .nav-toggle {
      display: none;
      background: none;
      border: none;
      font-size: 1.5rem;
      cursor: pointer;
      color: var(--text-dark);
    }

    @media (max-width: 768px) {
      .nav-links {
        position: absolute;
        inset: 100% 0 auto 0;
        flex-direction: column;
        align-items: flex-start;
        padding: 1rem 1.4rem 1.4rem;
        background: linear-gradient(to right, rgba(255, 179, 230, 0.98), rgba(217, 179, 255, 0.98));
        border-bottom: 2px solid rgba(255, 255, 255, 0.8);
        transform: scaleY(0);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.2s ease, opacity 0.2s ease;
        transform-origin: top;
      }
      .nav-links.open {
        transform: scaleY(1);
        opacity: 1;
        pointer-events: auto;
      }
      .nav-toggle { display: block; }
      .nav-btn { width: 100%; justify-content: center; }
    }

    /* Hero & Booking Card */
    .hero { padding: 3.5rem 0 2.5rem; position: relative; }
    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 2.3rem;
      align-items: start;
    }
    @media (max-width: 900px) { .hero-grid { grid-template-columns: 1fr; } }

    .eyebrow {
      text-transform: uppercase;
      font-size: 0.75rem;
      letter-spacing: 0.26em;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      margin-bottom: 0.6rem;
      color: var(--text-light);
    }
    .eyebrow-dot { width: 8px; height: 8px; border-radius: 50%; background: var(--pink-medium); }
    .hero h1 {
      font-size: clamp(2.1rem, 4vw, 3rem);
      line-height: 1.1;
      margin-bottom: 0.75rem;
    }
    .hero h1 span.highlight {
      background: linear-gradient(135deg, #ff99cc, #b366ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }
    .hero-subtitle { font-size: 0.95rem; opacity: 0.9; margin-bottom: 1.3rem; color: var(--text-light); }
    .hero-badges { display: flex; flex-wrap: wrap; gap: 0.6rem; margin-bottom: 1.4rem; }
    .badge {
      padding: 0.5rem 0.9rem;
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.7);
      backdrop-filter: blur(10px);
      border: 2px solid rgba(255, 255, 255, 0.8);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
    }
    .badge-dot { width: 7px; height: 7px; border-radius: 50%; background: var(--pink-medium); }
    .hero-actions { display: flex; flex-wrap: wrap; gap: 0.7rem; margin-bottom: 1.8rem; }
    .btn-primary, .btn-secondary {
      border-radius: var(--radius-pill);
      padding: 0.9rem 1.8rem;
      font-size: 0.85rem;
      font-weight: 700;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      transition: all 0.3s ease;
      cursor: pointer;
    }
    .btn-primary {
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      color: var(--text-dark);
      box-shadow: 0 18px 40px rgba(255, 179, 230, 0.4);
    }
    .btn-primary:hover { transform: translateY(-4px) scale(1.02); }
    .btn-secondary {
      background: rgba(255, 255, 255, 0.8);
      border: 2px solid rgba(255, 179, 230, 0.5);
      backdrop-filter: blur(10px);
    }
    .btn-secondary:hover { transform: translateY(-4px); background: rgba(255, 255, 255, 0.95); }

    /* Booking Form */
    .booking-card {
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(16px);
      border-radius: 32px;
      padding: 1.5rem;
      box-shadow: var(--shadow-soft);
      border: 3px solid rgba(255, 255, 255, 0.9);
      transition: all 0.3s ease;
    }
    .booking-card:hover { transform: translateY(-4px); background: rgba(255, 255, 255, 0.92); }
    .booking-header {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      font-size: 1.2rem;
      font-weight: 700;
    }
    .booking-sub {
      font-size: 0.75rem;
      color: var(--text-light);
      margin-bottom: 1.2rem;
      padding-bottom: 0.5rem;
      border-bottom: 1px solid rgba(255, 179, 230, 0.3);
    }
    .form-group { margin-bottom: 1rem; }
    .form-group label {
      display: block;
      font-size: 0.7rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 0.3rem;
    }
    .form-group input, .form-group select, .form-group textarea {
      width: 100%;
      padding: 0.7rem 0.9rem;
      border-radius: var(--radius-pill);
      border: 2px solid rgba(255, 179, 230, 0.5);
      background: rgba(255, 255, 255, 0.7);
      font-family: "Poppins", sans-serif;
      font-size: 0.8rem;
      transition: all 0.2s ease;
    }
    .form-group input:focus, .form-group select:focus, .form-group textarea:focus {
      outline: none;
      border-color: var(--purple-medium);
      background: rgba(255, 255, 255, 0.9);
    }
    .form-row { display: grid; grid-template-columns: 1fr 1fr; gap: 0.8rem; }
    @media (max-width: 640px) { .form-row { grid-template-columns: 1fr; } }
    .checkbox-group {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-top: 0.3rem;
    }
    .checkbox-item {
      display: flex;
      align-items: center;
      gap: 0.4rem;
      background: rgba(255, 255, 255, 0.6);
      padding: 0.4rem 0.8rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(255, 179, 230, 0.5);
      font-size: 0.75rem;
    }
    .checkbox-item input { width: 16px; height: 16px; accent-color: var(--purple-medium); margin: 0; }
    .file-upload input { padding: 0.5rem; }
    .booking-note {
      font-size: 0.7rem;
      background: rgba(255, 230, 245, 0.6);
      padding: 0.7rem;
      border-radius: 20px;
      text-align: center;
      margin: 1rem 0;
    }
    .submit-btn {
      width: 100%;
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      padding: 0.8rem;
      border: none;
      border-radius: var(--radius-pill);
      font-weight: 700;
      font-size: 0.85rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.3s ease;
    }
    .submit-btn:hover { transform: translateY(-2px); box-shadow: 0 12px 28px rgba(255, 179, 230, 0.5); }
    .social-pill {
      width: 32px;
      height: 32px;
      border-radius: 999px;
      display: inline-flex;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.7);
      border: 2px solid rgba(255, 255, 255, 0.9);
      font-size: 0.7rem;
      transition: 0.2s ease;
    }
    .social-pill:hover { transform: translateY(-3px); background: white; }

    /* cards & sections */
    section { padding: 2.6rem 0; }
    .section-heading { text-align: center; margin-bottom: 1.8rem; }
    .section-heading span.kicker {
      font-size: 0.75rem;
      letter-spacing: 0.26em;
      text-transform: uppercase;
      color: var(--text-light);
    }
    .section-heading h2 { font-size: 1.6rem; margin-bottom: 0.3rem; }
    .card {
      background: rgba(255, 255, 255, 0.85);
      border-radius: var(--radius-lg);
      padding: 1.4rem;
      backdrop-filter: blur(15px);
      border: 2px solid rgba(255, 255, 255, 0.9);
      transition: all 0.3s ease;
      box-shadow: var(--shadow-soft);
    }
    .card:hover { transform: translateY(-6px); background: rgba(255, 255, 255, 0.95); }
    .about-grid, .services-grid, .policy-grid { display: grid; gap: 1.2rem; }
    .about-grid { grid-template-columns: 1fr 1fr; }
    .services-grid { grid-template-columns: repeat(3, 1fr); }
    .policy-grid { grid-template-columns: repeat(3, 1fr); }
    @media (max-width: 900px) {
      .about-grid, .services-grid, .policy-grid { grid-template-columns: 1fr; }
    }
    .price-item { display: flex; justify-content: space-between; font-size: 0.85rem; margin-bottom: 0.3rem; }
    .price-title { font-weight: 600; }
    .policy-tag-row { display: flex; flex-wrap: wrap; gap: 0.4rem; margin-bottom: 0.6rem; }
    .policy-tag {
      font-size: 0.7rem;
      padding: 0.25rem 0.65rem;
      background: linear-gradient(135deg, rgba(255, 204, 255, 0.4), rgba(217, 179, 255, 0.4));
      border-radius: var(--radius-pill);
      border: 2px solid rgba(255, 255, 255, 0.9);
    }
    .gallery-strip {
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(15px);
      border-radius: 20px;
      padding: 1rem;
    }
    .gallery-track {
      display: flex;
      gap: 0.75rem;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      padding-bottom: 0.4rem;
    }
    .gallery-track::-webkit-scrollbar { height: 8px; }
    .gallery-track::-webkit-scrollbar-thumb { background: linear-gradient(135deg, #ffb3e6, #d9b3ff); border-radius: 999px; }
    .gallery-slide {
      flex: 0 0 auto;
      min-width: 180px;
      max-width: 260px;
      aspect-ratio: 3 / 4;
      border-radius: 18px;
      overflow: hidden;
      scroll-snap-align: center;
      border: 3px solid rgba(255, 255, 255, 0.9);
    }
    .gallery-slide img { width: 100%; height: 100%; object-fit: cover; }
    .gallery-btn {
      border-radius: 999px;
      border: 2px solid rgba(255, 179, 230, 0.7);
      background: rgba(255, 255, 255, 0.8);
      padding: 0.3rem 0.8rem;
      cursor: pointer;
    }
    footer {
      padding: 2rem 0;
      border-top: 2px solid rgba(255, 179, 230, 0.6);
      background: linear-gradient(to right, rgba(255, 179, 230, 0.4), rgba(217, 179, 255, 0.4));
      backdrop-filter: blur(15px);
    }
    .footer-pill {
      padding: 0.35rem 0.7rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.8);
      font-size: 0.76rem;
      transition: 0.2s;
    }
    .footer-pill:hover { transform: translateY(-2px); background: rgba(255, 255, 255, 0.95); }
    .footer-top, .footer-bottom { display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 1rem; }
    .footer-socials { display: flex; gap: 0.5rem; flex-wrap: wrap; }
    @media (max-width: 600px) { .footer-top { flex-direction: column; align-items: flex-start; } }
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
    <!-- HERO SECTION with REPLACED FORM ID and OPTIONAL PHONE FIELD -->
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

        <!-- BOOKING FORM - REPLACED FORM ID: rw0ekqq2y6e & PHONE FIELD IS NOW OPTIONAL -->
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
                <small style="font-size:0.6rem; display:block; margin-top:0.2rem;">Include country code (e.g., +1 for US). Not required, but helpful for confirming your appointment.</small>
              </div>
              <div class="form-group"><label>Instagram (optional)</label><input type="text" name="fi-text-instagram" placeholder="@username - so I can tag you!"></div>
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

            <div class="form-group"><label>Length (for acrylics)</label>
              <div class="checkbox-group">
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-length" value="Medium +$10"> Medium (+$10)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-length" value="Long +$15"> Long (+$15)</label>
                <label class="checkbox-item"><input type="checkbox" name="fi-checkbox-length" value="XXL +$20"> XXL (+$20)</label>
              </div>
            </div>

            <div class="form-group file-upload"><label>Inspo Photo (optional)</label><input type="file" name="fi-file-inspo" accept="image/*"><small style="font-size:0.6rem;">Upload a photo of your nail inspiration</small></div>
            <div class="form-group"><label>Anything else? (design ideas, questions, etc.)</label><textarea name="fi-text-notes" placeholder="Tell me about your vision or any special requests..."></textarea></div>
            <div class="booking-note"><strong>📌 Important:</strong> Your preferred date is a request and may not be available. I will reach out to confirm your appointment and handle payment details. A $20 deposit is required to secure your booking.</div>
            <button type="submit" class="submit-btn">Send Booking Request</button>
          </form>
          <div class="social-row" style="margin-top: 1rem; display: flex; justify-content: center; gap: 0.5rem;">
            <a href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" class="social-pill">TikTok</a>
            <a href="https://instagram.com/ashawniz.nailz" target="_blank" class="social-pill">IG</a>
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
          <div class="card"><h3>Pedicure Menu</h3><div class="price-item"><span class="price-title">Classic Pedicure</span><span>$45</span></div><div class="price-item"><span class="price-title">Deluxe Pedicure</span><span>$50</span></div><div class="price-item"><span class="price-title">Luxury Pedicure</span><span>$55</span></div><p class="price-desc" style="font-size:0.75rem;">✨ Dry pedicure also available</p></div>
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
            <div class="gallery-controls" style="display:flex; justify-content:space-between; margin-top:0.8rem; align-items:center;">
              <span style="font-size:0.7rem;">← → swipe or click arrows</span>
              <div><button class="gallery-btn" id="galleryPrev">←</button><button class="gallery-btn" id="galleryNext">→</button></div>
            </div>
          </div>
        </div>
      </div>
    </section>
  </main>

  <footer>
    <div class="container">
      <div class="footer-top">
        <div><div class="logo-text-main" style="font-size:1.1rem;">Ashawniz Nailz</div><div class="logo-text-sub">South Carolina Nail Tech · Pink & Purple Vibes</div></div>
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
          window.scrollTo({ top: targetElem.offsetTop - 80, behavior: "smooth" });
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
      const scrollStep = () => { const slide = track.querySelector(".gallery-slide"); return slide ? slide.offsetWidth + 12 : 220; };
      prev.addEventListener("click", () => track.scrollBy({ left: -scrollStep(), behavior: "smooth" }));
      next.addEventListener("click", () => track.scrollBy({ left: scrollStep(), behavior: "smooth" }));
    }
  })();
</script>
</body>
</html>
