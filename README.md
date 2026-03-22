<html lang="en">
<head>
  <meta charset="UTF-8" />
  <title>Ashawniz Nailz | South Carolina Nail Tech</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;500;600;700&family=Pacifico&display=swap" rel="stylesheet" />
  <style>
    :root {
      --primary-gradient: linear-gradient(135deg, #ffb3e6, #ff99cc);
      --secondary-gradient: linear-gradient(135deg, #d9b3ff, #b366ff);
      --bg-gradient: linear-gradient(135deg, #ffccff 0%, #ffb3e6 45%, #d9b3ff 55%, #b366ff 100%);
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

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
    }

    body {
      font-family: "Poppins", system-ui, -apple-system, BlinkMacSystemFont, sans-serif;
      background: var(--page-bg-gradient);
      background-attachment: fixed;
      background-size: 100% 100%;
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
      background: 
        radial-gradient(circle at 20% 80%, rgba(255, 204, 255, 0.4) 0%, transparent 30%),
        radial-gradient(circle at 80% 20%, rgba(217, 179, 255, 0.4) 0%, transparent 30%),
        radial-gradient(circle at 40% 40%, rgba(255, 179, 230, 0.3) 0%, transparent 40%),
        radial-gradient(circle at 60% 60%, rgba(217, 179, 255, 0.3) 0%, transparent 40%);
      z-index: -1;
      pointer-events: none;
    }

    a {
      color: inherit;
      text-decoration: none;
    }

    img {
      max-width: 100%;
      display: block;
    }

    .page {
      min-height: 100vh;
      position: relative;
      z-index: 1;
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
      background: linear-gradient(to right, rgba(255, 179, 230, 0.9), rgba(217, 179, 255, 0.9));
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
      opacity: 0.95;
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
      opacity: 0.9;
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
      transition: width 0.23s ease-out;
    }

    .nav-links a:hover::after {
      width: 100%;
    }

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
      cursor: pointer;
      transition: all 0.3s ease;
    }

    .nav-btn:hover {
      transform: translateY(-3px);
      box-shadow: 0 6px 25px rgba(255, 179, 230, 0.7);
      background: var(--light);
    }

    .nav-btn span.icon {
      font-size: 1rem;
    }

    .nav-toggle {
      display: none;
      background: none;
      border: none;
      color: var(--text-dark);
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
        background: linear-gradient(to right, rgba(255, 179, 230, 0.98), rgba(217, 179, 255, 0.98));
        border-bottom: 2px solid rgba(255, 255, 255, 0.8);
        transform-origin: top;
        transform: scaleY(0);
        opacity: 0;
        pointer-events: none;
        transition: transform 0.2s ease-out, opacity 0.2s ease-out;
        box-shadow: 0 10px 30px rgba(255, 179, 230, 0.4);
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

    /* Hero with booking form */
    .hero {
      padding: 3.5rem 0 2.5rem;
      position: relative;
      overflow: hidden;
    }

    .hero::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at 90% 10%, rgba(255, 204, 255, 0.4) 0%, transparent 40%);
      z-index: -1;
    }

    .hero-grid {
      display: grid;
      grid-template-columns: minmax(0, 1.4fr) minmax(0, 1fr);
      gap: 2.3rem;
      align-items: start;
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
      color: var(--text-light);
      opacity: 0.95;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      margin-bottom: 0.6rem;
    }

    .eyebrow-dot {
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background: var(--pink-medium);
      box-shadow: 0 0 15px rgba(255, 179, 230, 0.8);
    }

    .hero h1 {
      font-size: clamp(2.1rem, 4vw, 3rem);
      line-height: 1.1;
      margin-bottom: 0.75rem;
      color: var(--text-dark);
    }

    .hero h1 span.highlight {
      background: linear-gradient(135deg, #ff99cc, #b366ff);
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
    }

    .hero-subtitle {
      font-size: 0.95rem;
      max-width: 32rem;
      opacity: 0.9;
      margin-bottom: 1.3rem;
      color: var(--text-light);
    }

    .hero-badges {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      margin-bottom: 1.4rem;
    }

    .badge {
      padding: 0.5rem 0.9rem;
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      border: 2px solid rgba(255, 255, 255, 0.8);
      background: rgba(255, 255, 255, 0.7);
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
      color: var(--text-light);
      backdrop-filter: blur(10px);
      box-shadow: 0 4px 15px rgba(255, 179, 230, 0.25);
    }

    .badge-dot {
      width: 7px;
      height: 7px;
      border-radius: 50%;
      background: var(--pink-medium);
      box-shadow: 0 0 10px rgba(255, 179, 230, 0.8);
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
      padding: 0.9rem 1.8rem;
      font-size: 0.85rem;
      font-weight: 700;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      border: 2px solid transparent;
      cursor: pointer;
      display: inline-flex;
      align-items: center;
      gap: 0.4rem;
      transition: all 0.3s ease;
      white-space: nowrap;
    }

    .btn-primary {
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      color: var(--text-dark);
      box-shadow: 0 18px 40px rgba(255, 179, 230, 0.4);
    }

    .btn-primary:hover {
      transform: translateY(-4px) scale(1.03);
      box-shadow: 0 25px 60px rgba(255, 179, 230, 0.6);
      background: linear-gradient(135deg, #ffc2eb, #e0c2ff);
    }

    .btn-secondary {
      background: rgba(255, 255, 255, 0.8);
      color: var(--text-dark);
      border-color: rgba(255, 179, 230, 0.5);
      box-shadow: 0 8px 25px rgba(255, 179, 230, 0.3);
      backdrop-filter: blur(10px);
    }

    .btn-secondary:hover {
      background: rgba(255, 255, 255, 0.95);
      transform: translateY(-4px);
      box-shadow: 0 18px 40px rgba(255, 179, 230, 0.4);
    }

    .btn-icon {
      font-size: 1rem;
    }

    .hero-meta {
      font-size: 0.75rem;
      opacity: 0.85;
      color: var(--text-light);
    }

    /* Booking Form Card - Transparent */
    .booking-card {
      background: rgba(255, 255, 255, 0.85);
      backdrop-filter: blur(16px);
      border-radius: 32px;
      padding: 1.5rem;
      box-shadow: var(--shadow-soft);
      border: 3px solid rgba(255, 255, 255, 0.9);
      transition: all 0.3s ease;
    }

    .booking-card:hover {
      transform: translateY(-4px);
      background: rgba(255, 255, 255, 0.92);
      box-shadow: 0 25px 45px rgba(255, 179, 230, 0.4);
    }

    .booking-header {
      display: flex;
      align-items: center;
      gap: 0.5rem;
      margin-bottom: 0.5rem;
      font-size: 1.2rem;
      font-weight: 700;
      color: var(--text-dark);
    }

    .booking-sub {
      font-size: 0.75rem;
      color: var(--text-light);
      margin-bottom: 1.2rem;
      padding-bottom: 0.5rem;
      border-bottom: 1px solid rgba(255, 179, 230, 0.3);
    }

    .form-group {
      margin-bottom: 1rem;
    }

    .form-group label {
      display: block;
      font-size: 0.7rem;
      font-weight: 600;
      text-transform: uppercase;
      letter-spacing: 0.08em;
      margin-bottom: 0.3rem;
      color: var(--text-dark);
    }

    .form-group input,
    .form-group select,
    .form-group textarea {
      width: 100%;
      padding: 0.7rem 0.9rem;
      border-radius: var(--radius-pill);
      border: 2px solid rgba(255, 179, 230, 0.5);
      background: rgba(255, 255, 255, 0.7);
      font-family: "Poppins", sans-serif;
      font-size: 0.8rem;
      color: var(--text-dark);
      transition: all 0.2s ease;
    }

    .form-group input:focus,
    .form-group select:focus,
    .form-group textarea:focus {
      outline: none;
      border-color: var(--purple-medium);
      background: rgba(255, 255, 255, 0.9);
      box-shadow: 0 0 0 3px rgba(217, 179, 255, 0.2);
    }

    .form-group textarea {
      border-radius: 20px;
      resize: vertical;
      min-height: 60px;
    }

    .form-row {
      display: grid;
      grid-template-columns: 1fr 1fr;
      gap: 0.8rem;
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
      gap: 0.4rem;
      background: rgba(255, 255, 255, 0.6);
      padding: 0.4rem 0.8rem;
      border-radius: var(--radius-pill);
      border: 1px solid rgba(255, 179, 230, 0.5);
      font-size: 0.75rem;
    }

    .checkbox-item input {
      width: 16px;
      height: 16px;
      margin: 0;
      accent-color: var(--purple-medium);
    }

    .file-upload {
      position: relative;
    }

    .file-upload input {
      padding: 0.5rem;
      font-size: 0.7rem;
    }

    .booking-note {
      font-size: 0.7rem;
      background: rgba(255, 230, 245, 0.6);
      padding: 0.7rem;
      border-radius: 20px;
      text-align: center;
      margin: 1rem 0;
      color: var(--text-light);
    }

    .booking-note strong {
      color: var(--text-dark);
    }

    .submit-btn {
      width: 100%;
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      color: var(--text-dark);
      padding: 0.8rem;
      border: none;
      border-radius: var(--radius-pill);
      font-weight: 700;
      font-size: 0.85rem;
      letter-spacing: 0.1em;
      text-transform: uppercase;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 8px 20px rgba(255, 179, 230, 0.4);
    }

    .submit-btn:hover {
      transform: translateY(-2px);
      box-shadow: 0 12px 28px rgba(255, 179, 230, 0.6);
    }

    .success-message {
      text-align: center;
      padding: 1rem;
      background: rgba(255, 255, 255, 0.9);
      border-radius: 24px;
      color: var(--text-dark);
    }

    .social-row {
      display: flex;
      gap: 0.5rem;
      align-items: center;
    }

    .social-pill {
      width: 28px;
      height: 28px;
      border-radius: 999px;
      display: flex;
      align-items: center;
      justify-content: center;
      background: rgba(255, 255, 255, 0.7);
      border: 2px solid rgba(255, 255, 255, 0.9);
      font-size: 0.75rem;
      color: var(--text-dark);
      transition: all 0.2s ease;
      box-shadow: 0 4px 10px rgba(255, 179, 230, 0.3);
    }

    .social-pill:hover {
      background: rgba(255, 255, 255, 0.9);
      transform: translateY(-3px);
      box-shadow: 0 6px 15px rgba(255, 179, 230, 0.4);
    }

    /* Sections */
    section {
      padding: 2.6rem 0;
      position: relative;
    }

    .section-heading {
      text-align: center;
      margin-bottom: 1.8rem;
    }

    .section-heading span.kicker {
      font-size: 0.75rem;
      letter-spacing: 0.26em;
      text-transform: uppercase;
      color: var(--text-light);
      display: block;
      margin-bottom: 0.4rem;
    }

    .section-heading h2 {
      font-size: 1.6rem;
      margin-bottom: 0.3rem;
      color: var(--text-dark);
    }

    .section-heading p {
      font-size: 0.9rem;
      opacity: 0.9;
      max-width: 35rem;
      margin: 0 auto;
      color: var(--text-light);
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
      background: rgba(255, 255, 255, 0.85);
      border-radius: var(--radius-lg);
      padding: 1.4rem 1.4rem 1.35rem;
      box-shadow: var(--shadow-soft);
      border: 2px solid rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(15px);
      transition: all 0.3s ease;
    }

    .card:hover {
      transform: translateY(-6px);
      box-shadow: 0 25px 50px rgba(255, 179, 230, 0.4);
      background: rgba(255, 255, 255, 0.95);
      border-color: rgba(255, 255, 255, 1);
    }

    .card h3 {
      font-size: 1.05rem;
      margin-bottom: 0.6rem;
      color: var(--text-dark);
    }

    .card p {
      font-size: 0.88rem;
      opacity: 0.9;
      color: var(--text-light);
    }

    .pill-chip {
      display: inline-flex;
      align-items: center;
      gap: 0.3rem;
      padding: 0.3rem 0.7rem;
      font-size: 0.7rem;
      border-radius: var(--radius-pill);
      background: linear-gradient(135deg, rgba(255, 204, 255, 0.4), rgba(217, 179, 255, 0.4));
      border: 2px solid rgba(255, 255, 255, 0.9);
      margin-bottom: 0.6rem;
      color: var(--text-dark);
      backdrop-filter: blur(10px);
      box-shadow: 0 4px 15px rgba(255, 179, 230, 0.25);
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
      color: var(--text-light);
    }

    .about-dot {
      margin-top: 0.35rem;
      width: 6px;
      height: 6px;
      border-radius: 50%;
      background: var(--pink-medium);
      flex-shrink: 0;
      box-shadow: 0 0 8px rgba(255, 179, 230, 0.8);
    }

    .location-block {
      margin-top: 0.6rem;
      font-size: 0.86rem;
      color: var(--text-light);
    }

    .location-block strong {
      display: block;
      font-size: 0.9rem;
      margin-bottom: 0.2rem;
      color: var(--text-dark);
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
      color: var(--text-dark);
    }

    .service-card small {
      font-size: 0.75rem;
      opacity: 0.8;
      display: block;
      margin-bottom: 0.6rem;
      color: var(--text-light);
    }

    .price-item {
      display: flex;
      justify-content: space-between;
      gap: 0.6rem;
      font-size: 0.85rem;
      margin-bottom: 0.3rem;
      color: var(--text-light);
    }

    .price-title {
      font-weight: 600;
      color: var(--text-dark);
    }

    .price-desc {
      font-size: 0.78rem;
      opacity: 0.8;
      margin-bottom: 0.35rem;
      color: var(--text-light);
    }

    .addon-title {
      font-size: 0.8rem;
      text-transform: uppercase;
      letter-spacing: 0.16em;
      opacity: 0.8;
      margin-top: 0.6rem;
      margin-bottom: 0.25rem;
      color: var(--text-light);
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
      color: var(--text-dark);
    }

    .policy-card p {
      font-size: 0.83rem;
      opacity: 0.9;
      margin-bottom: 0.35rem;
      color: var(--text-light);
    }

    .policy-card ul {
      list-style: none;
      font-size: 0.83rem;
    }

    .policy-card ul li {
      margin-bottom: 0.32rem;
      display: flex;
      gap: 0.4rem;
      color: var(--text-light);
    }

    .policy-tag-row {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
      margin-bottom: 0.45rem;
    }

    .policy-tag {
      font-size: 0.7rem;
      padding: 0.25rem 0.65rem;
      background: linear-gradient(135deg, rgba(255, 204, 255, 0.4), rgba(217, 179, 255, 0.4));
      border-radius: var(--radius-pill);
      border: 2px solid rgba(255, 255, 255, 0.9);
      color: var(--text-dark);
      backdrop-filter: blur(10px);
      box-shadow: 0 4px 10px rgba(255, 179, 230, 0.25);
    }

    /* Booking strip */
    .booking-strip {
      margin-top: 2rem;
      background: linear-gradient(120deg, rgba(255, 179, 230, 0.95), rgba(217, 179, 255, 0.95));
      border-radius: var(--radius-lg);
      padding: 1.3rem 1.5rem;
      display: flex;
      flex-wrap: wrap;
      gap: 0.7rem;
      align-items: center;
      justify-content: space-between;
      box-shadow: var(--shadow-soft);
      border: 3px solid rgba(255, 255, 255, 0.9);
      position: relative;
      overflow: hidden;
    }

    .booking-strip::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, transparent 40%, rgba(255, 255, 255, 0.3) 50%, transparent 60%);
      animation: shimmer 3s infinite linear;
    }

    .booking-strip-text {
      font-size: 0.9rem;
      max-width: 26rem;
      color: var(--text-dark);
      position: relative;
      z-index: 1;
    }

    .booking-strip-text strong {
      font-size: 1rem;
    }

    .booking-strip-actions {
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      position: relative;
      z-index: 1;
    }

    /* GALLERY SWIPE */
    .gallery-strip {
      border-radius: 20px;
      padding: 1.1rem 1rem 1.1rem;
      background: rgba(255, 255, 255, 0.85);
      border: 2px solid rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(15px);
      box-shadow: 0 15px 35px rgba(255, 179, 230, 0.35);
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
      height: 8px;
    }

    .gallery-track::-webkit-scrollbar-track {
      background: rgba(255, 179, 230, 0.25);
      border-radius: 999px;
    }

    .gallery-track::-webkit-scrollbar-thumb {
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      border-radius: 999px;
      border: 1px solid rgba(255, 255, 255, 0.9);
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
      box-shadow: 0 12px 30px rgba(255, 179, 230, 0.45);
      border: 3px solid rgba(255, 255, 255, 0.9);
      background: linear-gradient(135deg, #ffb3e6, #d9b3ff);
      transition: all 0.3s ease;
    }

    .gallery-slide:hover {
      transform: translateY(-6px) scale(1.03);
      box-shadow: 0 20px 40px rgba(255, 179, 230, 0.6);
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
      margin-top: 0.8rem;
      font-size: 0.78rem;
      opacity: 0.9;
      gap: 0.75rem;
      flex-wrap: wrap;
      color: var(--text-light);
    }

    .gallery-buttons {
      display: flex;
      gap: 0.4rem;
    }

    .gallery-btn {
      border-radius: 999px;
      border: 2px solid rgba(255, 179, 230, 0.7);
      background: rgba(255, 255, 255, 0.8);
      color: var(--text-dark);
      padding: 0.3rem 0.8rem;
      font-size: 0.8rem;
      cursor: pointer;
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(255, 179, 230, 0.25);
      backdrop-filter: blur(10px);
    }

    .gallery-btn:hover {
      background: rgba(255, 255, 255, 0.95);
      transform: translateY(-3px);
      box-shadow: 0 6px 20px rgba(255, 179, 230, 0.35);
    }

    /* Footer */
    footer {
      padding: 2rem 0 2.5rem;
      border-top: 2px solid rgba(255, 179, 230, 0.6);
      margin-top: 1rem;
      background: linear-gradient(to right, rgba(255, 179, 230, 0.4), rgba(217, 179, 255, 0.4));
      backdrop-filter: blur(15px);
      position: relative;
    }

    footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: linear-gradient(45deg, transparent 40%, rgba(255, 255, 255, 0.25) 50%, transparent 60%);
      animation: shimmer 6s infinite linear;
      pointer-events: none;
    }

    .footer-top {
      display: flex;
      flex-wrap: wrap;
      gap: 1rem;
      align-items: center;
      justify-content: space-between;
      font-size: 0.8rem;
      position: relative;
      z-index: 1;
    }

    .footer-socials {
      display: flex;
      flex-wrap: wrap;
      gap: 0.4rem;
    }

    .footer-pill {
      padding: 0.35rem 0.7rem;
      border-radius: var(--radius-pill);
      border: 2px solid rgba(255, 255, 255, 0.9);
      font-size: 0.76rem;
      background: rgba(255, 255, 255, 0.8);
      color: var(--text-dark);
      transition: all 0.3s ease;
      box-shadow: 0 4px 15px rgba(255, 179, 230, 0.25);
      backdrop-filter: blur(10px);
    }

    .footer-pill:hover {
      background: rgba(255, 255, 255, 0.95);
      transform: translateY(-3px);
      box-shadow: 0 8px 25px rgba(255, 179, 230, 0.35);
    }

    .footer-bottom {
      margin-top: 1rem;
      font-size: 0.7rem;
      opacity: 0.7;
      display: flex;
      flex-wrap: wrap;
      gap: 0.6rem;
      justify-content: space-between;
      color: var(--text-light);
      position: relative;
      z-index: 1;
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
      .form-row {
        grid-template-columns: 1fr;
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
            <a href="#booking" class="nav-btn">
              <span class="icon">💅🏾</span>
              <span>Book Now</span>
            </a>
          </div>
        </nav>
      </div>
    </header>

    <main>
      <!-- HERO with Booking Form -->
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
              clients who want their nails to match their energy.
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

          <!-- BOOKING FORM - Connected to Forminit.io -->
          <div class="booking-card" id="booking">
            <div class="booking-header">
              <span>📅</span>
              <span>Request Appointment</span>
            </div>
            <div class="booking-sub">
              Fill out the form below. I'll reach out within 24 hours to confirm your date & time.
            </div>

            <form action="https://forminit.com/f/ubtd9cmvaiy" method="POST" enctype="multipart/form-data" id="bookingForm">
              <!-- Contact Information -->
              <div class="form-row">
                <div class="form-group">
                  <label>Full Name *</label>
                  <input type="text" name="fi-sender-fullName" placeholder="First & last name" required>
                </div>
                <div class="form-group">
                  <label>Email *</label>
                  <input type="email" name="fi-sender-email" placeholder="your@email.com" required>
                </div>
              </div>

              <div class="form-row">
                <div class="form-group">
                  <label>Phone *</label>
                  <input type="tel" name="fi-sender-phone" placeholder="(123) 456-7890" required>
                </div>
                <div class="form-group">
                  <label>Instagram (optional)</label>
                  <input type="text" name="fi-text-instagram" placeholder="@username - so I can tag you!">
                </div>
              </div>

              <!-- Preferred Date & Time -->
              <div class="form-row">
                <div class="form-group">
                  <label>Preferred Date *</label>
                  <input type="date" name="fi-date-preferred" required>
                  <small style="font-size:0.6rem; color:#7a5a7c;">*This is a request - I will confirm availability</small>
                </div>
                <div class="form-group">
                  <label>Preferred Time</label>
                  <input type="text" name="fi-text-time" placeholder="e.g., 2pm, afternoon, after 5pm">
                </div>
              </div>

              <!-- Services (Cart style - multiple selection) -->
              <div class="form-group">
                <label>Select Services (can choose multiple) *</label>
                <div class="checkbox-group">
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Full Set Acrylic - $60"> Full Set Acrylic ($60)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Acrylic Design Set - $75"> Acrylic Design ($75)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Acrylic Charm Set - $75"> Acrylic Charm ($75)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Acrylic Charm/Design Set - $85"> Charm/Design Set ($85)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Basic Manicure - $45"> Basic Manicure ($45)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Classic Pedicure - $45"> Classic Pedicure ($45)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Deluxe Pedicure - $50"> Deluxe Pedicure ($50)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-service" value="Luxury Pedicure - $55"> Luxury Pedicure ($55)
                  </label>
                </div>
              </div>

              <!-- Add-Ons (gems, charms, etc.) -->
              <div class="form-group">
                <label>Add-Ons (select any extras)</label>
                <div class="checkbox-group">
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="2 Acrylic toes - $15"> 2 Acrylic toes (+$15)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Acrylic nails set - $25"> Acrylic nails set (+$25)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Design full set - $35"> Design full set (+$35)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Charm full set - $35"> Charm full set (+$35)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Design/charm full set - $49"> Design/charm full set (+$49)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Polish change - $18"> Polish change (+$18)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Acrylic toes refill - $12"> Acrylic toes refill (+$12)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-addons" value="Acrylic nails refill - $42"> Acrylic nails refill (+$42)
                  </label>
                </div>
              </div>

              <!-- Length Add-Ons -->
              <div class="form-group">
                <label>Length (for acrylics)</label>
                <div class="checkbox-group">
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-length" value="Medium +$10"> Medium (+$10)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-length" value="Long +$15"> Long (+$15)
                  </label>
                  <label class="checkbox-item">
                    <input type="checkbox" name="fi-checkbox-length" value="XXL +$20"> XXL (+$20)
                  </label>
                </div>
              </div>

              <!-- Inspo Photo Upload -->
              <div class="form-group file-upload">
                <label>Inspo Photo (optional)</label>
                <input type="file" name="fi-file-inspo" accept="image/*">
                <small style="font-size:0.6rem; color:#7a5a7c;">Upload a photo of your nail inspiration</small>
              </div>

              <!-- Notes / Additional Info -->
              <div class="form-group">
                <label>Anything else? (design ideas, questions, etc.)</label>
                <textarea name="fi-text-notes" placeholder="Tell me about your vision or any special requests..."></textarea>
              </div>

              <div class="booking-note">
                <strong>📌 Important:</strong> Your preferred date is a request and may not be available. I will reach out to confirm your appointment and handle payment details. A $20 deposit is required to secure your booking.
              </div>

              <button type="submit" class="submit-btn">Send Booking Request</button>
            </form>

            <div class="social-row" style="margin-top: 1rem; justify-content: center;">
              <a href="https://www.tiktok.com/@ashawniz.nailz" target="_blank" rel="noopener" class="social-pill">TikTok</a>
              <a href="https://instagram.com/ashawniz.nailz" target="_blank" rel="noopener" class="social-pill">IG</a>
            </div>
          </div>
        </div>
      </section>

      <!-- ABOUT / LOCATION (unchanged) -->
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

      <!-- SERVICES (updated with correct pricing from your image) -->
      <section id="services">
        <div class="container">
          <div class="section-heading">
            <span class="kicker">Services &amp; pricing</span>
            <h2>Price list</h2>
            <p>Deposits go toward your total. Final balance can be paid in cash or via Cash App at <b>$AshawnizNailz</b>.</p>
          </div>

          <div class="services-grid">
            <!-- Acrylic Sets & Manicures -->
            <div class="card service-card">
              <h3>Acrylic Sets & Manicures</h3>
              <small>Custom designs, charms, &amp; glam details.</small>

              <div class="price-item">
                <span class="price-title">Full Set Acrylic Nails</span>
                <span>$60</span>
              </div>
              
              <div class="price-item">
                <span class="price-title">Acrylic Design Set</span>
                <span>$75</span>
              </div>

              <div class="price-item">
                <span class="price-title">Acrylic Charm Set</span>
                <span>$75</span>
              </div>

              <div class="price-item">
                <span class="price-title">Acrylic Charm/Design Set</span>
                <span>$85</span>
              </div>

              <div class="price-item">
                <span class="price-title">Freestyle</span>
                <span>$65</span>
              </div>
              <p class="price-desc">(Nail tech choice only)</p>

              <div class="price-item" style="margin-top: 0.8rem;">
                <span class="price-title">Basic Manicure</span>
                <span>$45</span>
              </div>

              <div class="price-item">
                <span class="price-title">Design Manicure</span>
                <span>$50</span>
              </div>

              <div class="price-item">
                <span class="price-title">Charm/Design Manicure</span>
                <span>$55</span>
              </div>
            </div>

            <!-- Pedicures - Updated with your exact pricing -->
            <div class="card service-card">
              <h3>Pedicure Menu</h3>
              <small>Polish included with all pedicures</small>

              <div class="price-item">
                <span class="price-title">Classic Pedicure</span>
                <span>$45</span>
              </div>
              <p class="price-desc">
                Nail shaping, cuticle care, polish & relaxing soak.
              </p>

              <div class="price-item">
                <span class="price-title">Deluxe Pedicure</span>
                <span>$50</span>
              </div>
              <p class="price-desc">
                Exfoliating scrub, massage & polish.
              </p>

              <div class="price-item">
                <span class="price-title">Luxury Pedicure</span>
                <span>$55</span>
              </div>
              <p class="price-desc">
                Hot stones, hydrating mask, extended massage & polish.
              </p>
              <p class="price-desc" style="margin-top:0.5rem;">
                ✨ Dry pedicure also available — just ask!
              </p>
            </div>

            <!-- Add-Ons & Other Services - Updated from your image -->
            <div class="card service-card">
              <h3>Add-Ons & Refills</h3>
              <small>Extras to complete your look</small>

              <div class="price-item">
                <span class="price-title">2 Acrylic toes</span>
                <span>$15</span>
              </div>
              <div class="price-item">
                <span class="price-title">Acrylic nails set</span>
                <span>$25</span>
              </div>
              <div class="price-item">
                <span class="price-title">Design full set</span>
                <span>$35</span>
              </div>
              <div class="price-item">
                <span class="price-title">Charm full set</span>
                <span>$35</span>
              </div>
              <div class="price-item">
                <span class="price-title">Design/charm full set</span>
                <span>$49</span>
              </div>
              <div class="price-item">
                <span class="price-title">Freestyle</span>
                <span>$50</span>
              </div>
              
              <div class="price-item" style="margin-top: 0.8rem;">
                <span class="price-title">Polish change</span>
                <span>$18</span>
              </div>
              <div class="price-item">
                <span class="price-title">Acrylic toes refill</span>
                <span>$12</span>
              </div>
              <p class="price-desc">*must have at least all 5 toes still on</p>
              <div class="price-item">
                <span class="price-title">Acrylic nails refill</span>
                <span>$42</span>
              </div>
              <p class="price-desc">*must have at least 4 nails on</p>
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
                Non-refundable deposit required to secure your appointment.
              </p>
            </div>
          </div>
        </div>
      </section>

      <!-- POLICIES (unchanged) -->
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
                  <img src="https://i.postimg.cc/ZqYtzPjx/IMG-7932.jpg" alt="Client nail set 1 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://i.postimg.cc/ZqYtzPjP/IMG-7936.jpg" alt="Client nail set 2 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://i.postimg.cc/R0C5x1Gw/IMG-7937.jpg" alt="Client nail set 3 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://i.postimg.cc/XvNS6KxF/IMG-7938.jpg" alt="Client nail set 4 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://i.postimg.cc/tgRQGdDx/IMG-7939.jpg" alt="Client nail set 5 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://i.postimg.cc/q7BVHcQh/IMG-7940.jpg" alt="Client nail set 6 by Ashawniz Nailz" />
                </div>
                <div class="gallery-slide">
                  <img src="https://i.postimg.cc/R0C5x1GS/IMG-7941.jpg" alt="Client nail set 7 by Ashawniz Nailz" />
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
          <span>Bookings available via DM or booking form. Based in Florence, SC area.</span>
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

    // Form submission success handling
    const form = document.getElementById('bookingForm');
    if (form) {
      form.addEventListener('submit', function(e) {
        // Form will submit normally to Forminit.io
        // You'll receive email notifications automatically
        console.log('Booking form submitted');
      });
    }
  </script>
</body>
</html>
