
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

    /* Layout */
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

    /* Mobile nav */
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

    /* Hero */
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

    /* Hero card / fake gallery */
    .hero-card {
      background: linear-gradient(135deg, rgba(255, 179, 230, 0.9), rgba(217, 179, 255, 0.9));
      border-radius: 32px;
      padding: 1.3rem 1.3rem 1.1rem;
      box-shadow: var(--shadow-soft);
      border: 3px solid rgba(255, 255, 255, 0.9);
      position: relative;
      overflow: hidden;
    }

    .hero-card::before {
      content: "";
      position: absolute;
      inset: 0;
      background: linear-gradient(45deg, transparent 40%, rgba(255, 255, 255, 0.3) 50%, transparent 60%);
      animation: shimmer 3s infinite linear;
    }

    @keyframes shimmer {
      0% { transform: translateX(-100%); }
      100% { transform: translateX(100%); }
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
      font-weight: 700;
      letter-spacing: 0.12em;
      text-transform: uppercase;
      color: var(--text-dark);
    }

    .hero-card-pill {
      padding: 0.4rem 0.9rem;
      border-radius: var(--radius-pill);
      background: rgba(255, 255, 255, 0.7);
      color: var(--text-dark);
      font-size: 0.68rem;
      text-transform: uppercase;
      letter-spacing: 0.18em;
      border: 2px solid rgba(255, 255, 255, 0.9);
      backdrop-filter: blur(10px);
      box-shadow: 0 4px 15px rgba(255, 179, 230, 0.3);
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
      background: linear-gradient(135deg, rgba(255, 204, 255, 0.9), rgba(217, 179, 255, 0.9));
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 0.65rem;
      text-align: center;
      padding: 0.4rem;
      border: 2px solid rgba(255, 255, 255, 0.9);
      box-shadow: 0 8px 22px rgba(255, 179, 230, 0.4);
      transform: translateY(0);
      transition: all 0.3s ease;
      color: var(--text-dark);
    }

    .hero-thumb:nth-child(2) {
      transform: translateY(4px);
    }

    .hero-thumb:nth-child(3) {
      transform: translateY(8px);
    }

    .hero-thumb:hover {
      transform: translateY(-6px) scale(1.03);
      box-shadow: 0 14px 32px rgba(255, 179, 230, 0.6);
    }

    .hero-card-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      font-size: 0.7rem;
      opacity: 0.9;
      position: relative;
      z-index: 1;
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
            <!-- Acrylic Sets & Manicures -->
            <div class="card service-card">
              <h3>Acrylic Sets & Manicures</h3>
              <small>Custom designs, charms, &amp; glam details.</small>

              <div class="price-item">
                <span class="price-title">Acrylic Full Set</span>
                <span>$50</span>
              </div>
              
              <div class="price-item">
                <span class="price-title">Acrylic Design Set</span>
                <span>$65</span>
              </div>

              <div class="price-item">
                <span class="price-title">Acrylic Charm Set</span>
                <span>$75</span>
              </div>

              <div class="price-item">
                <span class="price-title">Acrylic Charm/Design Set</span>
                <span>$80</span>
              </div>

              <div class="price-item" style="margin-top: 0.8rem;">
                <span class="price-title">Basic Manicure</span>
                <span>$40</span>
              </div>

              <div class="price-item">
                <span class="price-title">Design Manicure</span>
                <span>$45</span>
              </div>

              <div class="price-item">
                <span class="price-title">Charm/Design Manicure</span>
                <span>$55</span>
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
