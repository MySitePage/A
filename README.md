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
      --radius-form: 24px;
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

    /* Tablet & Mobile Navigation */
    @media (max-width: 900px) {
      .nav {
        position: relative;
      }
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
      .nav-toggle {
        display: block;
      }
    }

    @media (max-width: 550px) {
      .container { padding: 0 1rem; }
      .logo-text-main { font-size: 1.1rem; }
      .logo-circle { width: 38px; height: 38px; }
      .logo-text-sub { font-size: 0.55rem; }
    }

    /* ========== HERO SECTION - RESPONSIVE GRID ========== */
    .hero { padding: 2.5rem 0 2rem; }
    .hero-grid {
      display: grid;
      grid-template-columns: 1fr;
      gap: 2rem;
      align-items: start;
    }
    @media (min-width: 768px) and (max-width: 1024px) {
      .hero-grid { gap: 1.8rem; }
    }
    @media (min-width: 1025px) {
      .hero-grid {
        grid-template-columns: 1.4fr 1fr;
        gap: 2.5rem;
      }
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

    /* ========== BOOKING CARD - GRADIENT FORM FIELDS ========== */
    .booking-card {
      background: rgba(255, 255, 255, 0.92);
      backdrop-filter: blur(18px);
      border-radius: 36px;
      padding: 1.6rem;
      box-shadow: 0 25px 45px rgba(255, 179, 230, 0.35);
      border: 2px solid rgba(255, 255, 255, 0.9);
      transition: all 0.3s ease;
    }
    .booking-header { font-size: 1.2rem; font-weight: 700; margin-bottom: 0.3rem; display: flex; align-items: center; gap: 0.5rem; }
    .booking-sub { font-size: 0.74rem; color: var(--text-light); margin-bottom: 1.2rem; padding-bottom: 0.5rem; border-bottom: 1px solid rgba(255, 179, 230, 0.4); }
    
    .form-group { margin-bottom: 1rem; }
    .form-group label {
      display: block;
      font-size: 0.7rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 0.35rem;
      color: var(--text-dark);
    }
    .form-group input, 
    .form-group select, 
    .form-group textarea {
      width: 100%;
      padding: 0.8rem 1rem;
      border-radius: 28px !important;
      border: none;
      background: linear-gradient(135deg, #fff0f8, #fae6ff);
      font-family: "Poppins", sans-serif;
      font-size: 0.85rem;
      color: var(--text-dark);
      transition: all 0.25s ease;
      box-shadow: inset 0 1px 2px rgba(0,0,0,0.02), 0 2px 6px rgba(255, 179, 230, 0.2);
      outline: none;
    }
    .form-group input:focus, 
    .form-group select:focus, 
    .form-group textarea:focus {
      background: linear-gradient(135deg, #ffffff, #ffeef9);
      box-shadow: 0 0 0 3px rgba(217, 179, 255, 0.4);
      transform: scale(1.01);
    }
    .form-row { display: grid; grid-template-columns: 1fr; gap: 0.8rem; }
    @media (min-width: 600px) {
      .form-row { grid-template-columns: 1fr 1fr; gap: 1rem; }
    }
    
    .checkbox-group {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-top: 0.3rem;
    }
    .checkbox-item {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      background: linear-gradient(135deg, #fff5fc, #fdeaff);
      padding: 0.45rem 1rem;
      border-radius: 40px;
      border: 1px solid rgba(255, 179, 230, 0.6);
      font-size: 0.75rem;
      font-weight: 500;
      cursor: pointer;
      transition: all 0.2s;
    }
    .checkbox-item:hover { background: linear-gradient(135deg, #ffeef8, #ffe0ff); transform: translateY(-1px); }
    .checkbox-item input { width: 17px; height: 17px; accent-color: var(--purple-dark); margin: 0; cursor: pointer; }
    
    .file-upload input { padding: 0.7rem 1rem; }
    .booking-note {
      font-size: 0.7rem;
      background: linear-gradient(135deg, rgba(255, 230, 245, 0.8), rgba(230, 210, 255, 0.8));
      padding: 0.8rem;
      border-radius: 28px;
      text-align: center;
      margin: 1rem 0;
      border: 1px solid rgba(255,255,255,0.6);
    }
    .submit-btn {
      width: 100%;
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      padding: 0.9rem;
      border: none;
      border-radius: 60px;
      font-weight: 800;
      font-size: 0.85rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.3s ease;
      color: var(--text-dark);
      box-shadow: 0 8px 20px rgba(255, 179, 230, 0.4);
    }
    .submit-btn:hover { transform: translateY(-3px); box-shadow: 0 14px 28px rgba(255, 179, 230, 0.6); }
    .social-pill {
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      background: rgba(255,255,255,0.85);
      padding: 0.5rem 1.2rem;
      border-radius: 60px;
      font-size: 0.72rem;
      font-weight: 600;
      transition: 0.2s;
    }
    .social-pill:hover { transform: translateY(-2px); background: white; box-shadow: 0 5px 12px rgba(255,179,230,0.4); }
    
    /* ========== SECTIONS - FULLY RESPONSIVE GRIDS ========== */
    section { padding: 2.5rem 0; }
    .section-heading { text-align: center; margin-bottom: 2rem; }
    .section-heading span.kicker { font-size: 0.72rem; letter-spacing: 0.2em; color: var(--text-light); display: block; margin-bottom: 0.3rem; }
    .section-heading h2 { font-size: 1.7rem; margin-bottom: 0.4rem; }
    .section-heading p { font-size: 0.88rem; max-width: 550px; margin: 0 auto; color: var(--text-light); }
    
    .about-grid, .services-grid, .policy-grid {
      display: grid;
      gap: 1.3rem;
    }
    .about-grid { grid-template-columns: 1fr; }
    .services-grid { grid-template-columns: 1fr; }
    .policy-grid { grid-template-columns: 1fr; }
    
    /* Tablet */
    @media (min-width: 768px) {
      .about-grid { grid-template-columns: 1fr 1fr; }
      .services-grid { grid-template-columns: repeat(2, 1fr); }
      .policy-grid { grid-template-columns: repeat(2, 1fr); }
    }
    /* Desktop */
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
      box-shadow: 0 8px 20px rgba(255, 179, 230, 0.2);
      height: 100%;
    }
    .card:hover { transform: translateY(-5px); background: rgba(255, 255, 255, 0.93); }
    .price-item { display: flex; justify-content: space-between; font-size: 0.85rem; margin-bottom: 0.5rem; flex-wrap: wrap; gap: 0.3rem; }
    .price-title { font-weight: 600; }
    .policy-tag {
      display: inline-block;
      font-size: 0.66rem;
      padding: 0.25rem 0.9rem;
      background: linear-gradient(135deg, rgba(255, 204, 255, 0.5), rgba(217, 179, 255, 0.5));
      border-radius: 60px;
      border: 1px solid rgba(255,255,255,0.7);
      margin-right: 0.5rem;
      margin-bottom: 0.5rem;
    }
    
    /* Travel Fees specific card */
    .travel-grid {
      display: grid;
      gap: 1.3rem;
      grid-template-columns: 1fr;
    }
    @media (min-width: 768px) {
      .travel-grid { grid-template-columns: repeat(2, 1fr); }
    }
    @media (min-width: 1024px) {
      .travel-grid { grid-template-columns: repeat(3, 1fr); }
    }
    .travel-location-list {
      margin-top: 0.8rem;
      list-style: none;
      padding-left: 0;
    }
    .travel-location-list li {
      font-size: 0.8rem;
      padding: 0.2rem 0;
      display: flex;
      align-items: center;
      gap: 0.4rem;
      border-bottom: 1px dashed rgba(255,179,230,0.5);
    }
    .travel-location-list li:last-child { border-bottom: none; }
    .travel-note {
      background: linear-gradient(135deg, rgba(255, 220, 245, 0.9), rgba(230, 200, 255, 0.9));
      border-radius: 24px;
      padding: 0.8rem 1rem;
      font-size: 0.75rem;
      text-align: center;
      font-weight: 500;
      margin-top: 0.8rem;
    }
    
    /* GALLERY */
    .gallery-strip {
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(12px);
      border-radius: 28px;
      padding: 1.2rem;
    }
    .gallery-track {
      display: flex;
      gap: 1rem;
      overflow-x: auto;
      scroll-snap-type: x mandatory;
      padding-bottom: 0.8rem;
      -webkit-overflow-scrolling: touch;
      scroll-behavior: smooth;
    }
    .gallery-track::-webkit-scrollbar { height: 6px; }
    .gallery-track::-webkit-scrollbar-track { background: rgba(255, 179, 230, 0.2); border-radius: 10px; }
    .gallery-track::-webkit-scrollbar-thumb { background: linear-gradient(135deg, #ffb3e6, #d9b3ff); border-radius: 10px; }
    .gallery-slide {
      flex: 0 0 auto;
      width: 180px;
      aspect-ratio: 3 / 4;
      border-radius: 24px;
      overflow: hidden;
      scroll-snap-align: center;
      border: 3px solid rgba(255, 255, 255, 0.9);
      box-shadow: 0 12px 25px rgba(255,179,230,0.3);
      transition: transform 0.2s;
    }
    .gallery-slide:hover { transform: scale(1.02); }
    .gallery-slide img { width: 100%; height: 100%; object-fit: cover; }
    @media (min-width: 768px) {
      .gallery-slide { width: 210px; }
    }
    .gallery-btn {
      border-radius: 60px;
      border: 1.5px solid rgba(255, 179, 230, 0.7);
      background: rgba(255, 255, 255, 0.9);
      padding: 0.45rem 1.2rem;
      font-size: 0.75rem;
      font-weight: 600;
      cursor: pointer;
      transition: 0.2s;
    }
    .gallery-btn:hover { background: white; transform: translateY(-2px); }
    
    /* FOOTER */
    footer {
      padding: 1.8rem 0;
      border-top: 2px solid rgba(255, 179, 230, 0.5);
      background: linear-gradient(to right, rgba(255, 179, 230, 0.4), rgba(217, 179, 255, 0.4));
      backdrop-filter: blur(12px);
      margin-top: 1rem;
    }
    .footer-top, .footer-bottom { display: flex; flex-wrap: wrap; justify-content: space-between; align-items: center; gap: 1rem; }
    .footer-socials { display: flex; gap: 0.8rem; flex-wrap: wrap; }
    .footer-pill {
      padding: 0.4rem 1rem;
      border-radius: 60px;
      background: rgba(255, 255, 255, 0.85);
      font-size: 0.72rem;
      transition: 0.2s;
    }
    .footer-pill:hover { transform: translateY(-2px); background: white; }
    @media (max-width: 700px) {
      .footer-top { flex-direction: column; align-items: flex-start; }
      .footer-bottom { flex-direction: column; align-items: flex-start; gap: 0.5rem; }
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
          <a href="#travel-fees">Travel Fees</a>
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
            <div class="badge"><span class="badge-dot"></span> Travel nail tech · SC (fees apply)</div>
          </div>
          <div class="hero-actions">
            <a class="btn-primary" href="https://www.tiktok.com/@ashawniz.nailz" target="_blank"><span>📲</span><span>Book via DM</span></a>
            <a class="btn-secondary" href="#services"><span>👛</span><span>View price list</span></a>
          </div>
          <div class="hero-meta">Send your nail inspo photo when booking so your set can be customized just for you.</div>
        </div>

        <!-- BOOKING FORM -->
        <div class="booking-card" id="booking">
          <div class="booking-header"><span>📅</span><span>Request Appointment</span></div>
          <div class="booking-sub">Fill out the form below. I'll reach out within 24 hours to confirm your date & time.</div>
          <form action="https://forminit.com/f/rw0ekqq2y6e" method="POST" enctype="multipart/form-data">
            <div class="form-row">
              <div class="form-group"><label>Full Name *</label><input type="text" name="fi-sender-fullName" placeholder="First & last name" required></div>
              <div class="form-group"><label>Email *</label><input type="email" name="fi-sender-email" placeholder="your@email.com" required></div>
            </div>
            <div class="form-row">
              <div class="form-group"><label>Instagram (optional)</label><input type="text" name="fi-text-instagram" placeholder="@username - so I can tag you!"></div>
              <div class="form-group"><label>Preferred Date *</label><input type="date" name="fi-date-preferred" required><small style="font-size:0.6rem;">*request - I will confirm</small></div>
            </div>
            <div class="form-row">
              <div class="form-group"><label>Preferred Time</label><input type="text" name="fi-text-time" placeholder="e.g., 2pm, afternoon"></div>
              <div class="form-group"><label>Alternative Time</label><input type="text" name="fi-text-time-alt" placeholder="Alternative time (optional)"></div>
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

            <div class="form-group file-upload"><label>Inspo Photo (optional)</label><input type="file" name="fi-file-inspo" accept="image/*"><small style="font-size:0.6rem;">Upload a photo of your nail inspiration</small></div>
            
            <div class="form-group">
              <label>Anything else? (design ideas, questions, etc.)</label>
              <textarea name="fi-text-notes" placeholder="Add phone number here if you don't wanna communicate through Instagram or email. Also share design ideas, special requests, or any questions!" rows="3"></textarea>
            </div>
            
            <div class="booking-note"><strong>📌 Important:</strong> Your preferred date is a request and may not be available. I will reach out to confirm your appointment and handle payment details. A $20 deposit is required to secure your booking.</div>
            <button type="submit" class="submit-btn">Send Booking Request</button>
          </form>
          <div style="margin-top: 1rem; display: flex; justify-content: center; gap: 0.8rem;">
            <a href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" class="social-pill">TikTok</a>
            <a href="https://instagram.com/ashawniz.nailz" target="_blank" class="social-pill">Instagram</a>
          </div>
        </div>
      </div>
    </section>

    <section id="location"><div class="container"><div class="section-heading"><span class="kicker">About &amp; location</span><h2>Where to find Ashawniz Nailz</h2><p>Full glam acrylic sets or relaxing pedicures — everything with pink & purple energy.</p></div><div class="about-grid"><div class="card"><div class="policy-tag">💅🏾 Registered Cosmetologist</div><h3>The experience</h3><p>Personalized appointments. Bring your inspo, ideas, or vibe — together we create your perfect set.</p></div><div class="card"><div class="policy-tag">📍 Florence, SC area</div><h3>Service Area & Travel</h3><p>Based in Florence, SC. Mobile appointments across South Carolina (travel fees apply). Book via DM or form.</p></div></div></div></section>

    <section id="services"><div class="container"><div class="section-heading"><span class="kicker">Services &amp; pricing</span><h2>Price list</h2><p>Deposits go toward total. Final balance: cash or Cash App <b>$AshawnizNailz</b>.</p></div><div class="services-grid"><div class="card"><h3>Acrylic Sets & Manicures</h3><div class="price-item"><span class="price-title">Full Set Acrylic</span><span>$60</span></div><div class="price-item"><span class="price-title">Acrylic Design Set</span><span>$75</span></div><div class="price-item"><span class="price-title">Acrylic Charm Set</span><span>$75</span></div><div class="price-item"><span class="price-title">Acrylic Charm/Design</span><span>$85</span></div><div class="price-item"><span class="price-title">Basic Manicure</span><span>$45</span></div><div class="price-item"><span class="price-title">Design Manicure</span><span>$50</span></div></div><div class="card"><h3>Pedicure Menu</h3><div class="price-item"><span class="price-title">Classic Pedicure</span><span>$45</span></div><div class="price-item"><span class="price-title">Deluxe Pedicure</span><span>$50</span></div><div class="price-item"><span class="price-title">Luxury Pedicure</span><span>$55</span></div><p style="font-size:0.75rem; margin-top:0.5rem;">✨ Dry pedicure also available</p></div><div class="card"><h3>Add-Ons & Refills</h3><div class="price-item"><span>2 Acrylic toes</span><span>$15</span></div><div class="price-item"><span>Design full set</span><span>$35</span></div><div class="price-item"><span>Charm full set</span><span>$35</span></div><div class="price-item"><span>Acrylic nails refill</span><span>$42</span></div><div class="price-item"><span>Soak Off</span><span>$15</span></div><div class="price-item"><span>Deposit</span><span>$20</span></div></div></div></div></section>

    <!-- TRAVEL FEES SECTION - CORRECTED SPELLING: Marion and Effingham -->
    <section id="travel-fees">
      <div class="container">
        <div class="section-heading">
          <span class="kicker">Mobile service</span>
          <h2>Travel Fees</h2>
          <p>Covering my travel & setup — ensures a full luxury experience. Fees are categorized per round-trip mileage.</p>
        </div>
        <div class="travel-grid">
          <!-- 0-21 miles -->
          <div class="card">
            <div style="font-size:1.8rem; margin-bottom:0.3rem;">📍</div>
            <h3>0-21 miles · $25</h3>
            <ul class="travel-location-list">
              <li>✨ Florence, SC</li>
              <li>✨ Darlington, SC</li>
              <li>✨ Timmonsville, SC</li>
              <li>✨ Effingham, SC</li>
            </ul>
          </div>
          <!-- 21-40 miles -->
          <div class="card">
            <div style="font-size:1.8rem; margin-bottom:0.3rem;">🚗</div>
            <h3>21-40 miles · $45 - $50</h3>
            <ul class="travel-location-list">
              <li>📍 Hartsville, SC</li>
              <li>📍 Lake City, SC</li>
              <li>📍 Marion, SC</li>
            </ul>
          </div>
          <!-- 41-60 miles -->
          <div class="card">
            <div style="font-size:1.8rem; margin-bottom:0.3rem;">⛽</div>
            <h3>41-60 miles · $65 - $75</h3>
            <div class="policy-tag" style="background:#fce4ff;">Longer trips - must be worth it</div>
            <ul class="travel-location-list">
              <li>🌟 Sumter, SC</li>
              <li>🌟 Mullins, SC</li>
              <li>🌟 Conway, SC</li>
            </ul>
          </div>
          <!-- 61-80 miles (Far-premium) -->
          <div class="card">
            <div style="font-size:1.8rem; margin-bottom:0.3rem;">💎</div>
            <h3>61-80 miles · $85+</h3>
            <div class="policy-tag" style="background:#f5e6ff;">Far-premium only</div>
            <ul class="travel-location-list">
              <li>🏖️ Myrtle Beach, SC</li>
              <li>🏛️ Columbia, SC</li>
            </ul>
            <div class="travel-note">⭐ Premium extended service — must be pre-approved</div>
          </div>
        </div>
        <div class="card" style="margin-top:1rem; text-align:center;">
          <div style="display:flex; flex-wrap:wrap; justify-content:center; gap:0.8rem;">
            <span class="policy-tag">💅🏾 Same day - $30 add ons</span>
            <span class="policy-tag">👥 For the same house call: $10 off each service!!</span>
          </div>
          <p style="margin-top:0.8rem; font-weight:500; font-size:0.85rem;"><strong>📌 Important:</strong> All house calls have to have a $120 minimum to cover my travel and setup. This ensures you get a full luxury experience!!</p>
          <div style="margin-top:0.7rem; font-size:0.7rem; background:rgba(255,230,250,0.7); border-radius:40px; padding:0.4rem 0.8rem; display:inline-block;">✨ Travel fees are calculated based on round trip distance from Florence, SC ✨</div>
        </div>
      </div>
    </section>

    <section id="policies"><div class="container"><div class="section-heading"><span class="kicker">Policies</span><h2>Before you book</h2><p>Deposits and time rules keep everything professional.</p></div><div class="policy-grid"><div class="card"><div><span class="policy-tag">Deposits</span><span class="policy-tag">$20 non-refundable</span></div><h3>Deposit Policy</h3><p>$20 deposit required within 24h of booking. No refunds after services.</p></div><div class="card"><div><span class="policy-tag">Timing</span><span class="policy-tag">Late & No-Show</span></div><h3>Late Policy</h3><p>10-min grace period, after that $10 late fee. After 15 min appointment may be canceled.</p></div><div class="card"><div><span class="policy-tag">Nail prep</span><span class="policy-tag">Payments</span></div><h3>Prep & Payments</h3><p>Arrive with bare nails unless soak-off added. Cash or Cash App accepted.</p></div></div></div></section>

    <section id="gallery"><div class="container"><div class="section-heading"><span class="kicker">Client work</span><h2>Gallery preview</h2><p>Swipe to see recent sets by Ashawniz Nailz.</p></div><div class="card"><div class="gallery-strip"><div class="gallery-track" id="galleryTrack"><div class="gallery-slide"><img src="https://i.postimg.cc/ZqYtzPjx/IMG-7932.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/ZqYtzPjP/IMG-7936.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/R0C5x1Gw/IMG-7937.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/XvNS6KxF/IMG-7938.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/tgRQGdDx/IMG-7939.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/q7BVHcQh/IMG-7940.jpg" alt="Nail set"></div><div class="gallery-slide"><img src="https://i.postimg.cc/R0C5x1GS/IMG-7941.jpg" alt="Nail set"></div></div><div class="gallery-controls" style="display:flex; justify-content:space-between; margin-top:0.9rem; align-items:center; flex-wrap:wrap; gap:0.5rem;"><span style="font-size:0.7rem;">← → swipe or click arrows</span><div><button class="gallery-btn" id="galleryPrev">← Prev</button><button class="gallery-btn" id="galleryNext" style="margin-left:0.6rem;">Next →</button></div></div></div></div></div></section>
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
    // Smooth scroll for all devices
    document.querySelectorAll('a[href^="#"]').forEach(anchor => {
      anchor.addEventListener("click", function(e) {
        const targetId = this.getAttribute("href");
        if (targetId === "#" || targetId === "") return;
        const targetElem = document.querySelector(targetId);
        if (targetElem) {
          e.preventDefault();
          const offset = 80;
          const elementPosition = targetElem.getBoundingClientRect().top;
          const offsetPosition = elementPosition + window.pageYOffset - offset;
          window.scrollTo({ top: offsetPosition, behavior: "smooth" });
          const navLinks = document.querySelector(".nav-links");
          if (navLinks && navLinks.classList.contains("open")) navLinks.classList.remove("open");
        }
      });
    });
    
    // Gallery arrows with responsive scroll
    const track = document.getElementById("galleryTrack");
    const prev = document.getElementById("galleryPrev");
    const next = document.getElementById("galleryNext");
    if (track && prev && next) {
      const getScrollAmount = () => {
        const slide = track.querySelector(".gallery-slide");
        if (!slide) return 200;
        let slideWidth = slide.offsetWidth;
        if (window.innerWidth < 768) return slideWidth + 12;
        return slideWidth + 16;
      };
      prev.addEventListener("click", () => track.scrollBy({ left: -getScrollAmount(), behavior: "smooth" }));
      next.addEventListener("click", () => track.scrollBy({ left: getScrollAmount(), behavior: "smooth" }));
    }
  })();
</script>
</body>
</html>
