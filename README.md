<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <title>KELVINE_SESSION PAIR SITE</title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
  <link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@400;700&amp;family=Roboto:wght@300;400;500;700&amp;display=swap" rel="stylesheet">

  <!-- Standard Favicon -->
  <link rel="icon" type="image/png" sizes="512x512" href="img/logo-green.png">
  <link rel="icon" type="image/png" sizes="192x192" href="img/logo-green.png">
  <link rel="icon" type="image/png" sizes="32x32" href="img/logo-green.png">

  <!-- Apple Touch Icon (For iOS) -->
  <link rel="apple-touch-icon" href="img/logo-green.png">

  <!-- Web Manifest (Optional, for PWA Support) -->
  <link rel="manifest" href="img/site.webmanifest">


  <!-- Open Graph (Facebook, WhatsApp, etc.) -->
  <meta property="og:title" content="CREEPY SESSION">
  <meta property="og:description" content="CREATE YOUR SESSION WITH CREEPY SESSION GENERATOR BY DANNY">
  <meta property="og:image" content="img/logo.png">
  <meta property="og:url" content="https://creepytech.org">
  <meta property="og:type" content="website">

  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="CREEPY SESSION">
  <meta name="twitter:description" content="SESSION GENERATOR BY DANNY">
  <meta name="twitter:image" content="img/logo.png">

  <style>
    /* ========== BASE STYLES ========== */
    :root {
      --primary: #00ff9d;
      --primary-dark: #00c97a;
      --secondary: #7700ff;
      --dark: #0a0a0a;
      --dark-light: #1a1a1a;
      --gray: #888;
      --light: #f5f5f5;
      --danger: #ff3d3d;
      --warning: #ffc107;
      
      --font-main: 'Roboto', sans-serif;
      --font-heading: 'Orbitron', sans-serif;
      
      --transition: all 0.3s ease;
      --shadow: 0 4px 20px rgba(0, 0, 0, 0.25);
      --shadow-lg: 0 10px 40px rgba(0, 0, 0, 0.3);
      --shadow-primary: 0 0 15px rgba(0, 255, 157, 0.5);
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
      font-family: var(--font-main);
      color: var(--light);
      background-color: var(--dark);
      overflow-x: hidden;
      position: relative;
      min-height: 100vh;
      line-height: 1.6;
    }

    h1, h2, h3, h4, h5, h6 {
      font-family: var(--font-heading);
      font-weight: 700;
      line-height: 1.2;
      margin-bottom: 1rem;
    }

    a {
      text-decoration: none;
      color: inherit;
      transition: var(--transition);
    }

    img {
      max-width: 100%;
      height: auto;
    }

    ul {
      list-style: none;
    }

    .container {
      width: 100%;
      max-width: 1200px;
      margin: 0 auto;
      padding: 0 1.5rem;
    }

    /* ========== BACKGROUND ANIMATION ========== */
    .bg-animation {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -2;
      background: radial-gradient(ellipse at bottom, #0a0a0a 0%, #000000 100%);
      overflow: hidden;
    }

    .particles {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      z-index: -1;
    }

    .particles::before {
      content: "";
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background: url('data:image/svg+xml;utf8,<svg xmlns="http://www.w3.org/2000/svg" width="100" height="100" viewBox="0 0 100 100"><circle cx="50" cy="50" r="1" fill="rgba(0, 255, 157, 0.1)"/></svg>');
      background-size: 2px 2px;
      opacity: 0.5;
      animation: particleMove 100s linear infinite;
    }

    .glow {
      position: absolute;
      width: 100%;
      height: 100%;
      background: radial-gradient(circle at center, rgba(0, 255, 157, 0.1) 0%, transparent 70%);
      animation: pulseGlow 8s ease infinite alternate;
    }

    @keyframes particleMove {
      0% {
        transform: translateY(0) translateX(0);
      }
      100% {
        transform: translateY(-1000px) translateX(-500px);
      }
    }

    @keyframes pulseGlow {
      0% {
        opacity: 0.2;
        transform: scale(0.8);
      }
      100% {
        opacity: 0.5;
        transform: scale(1.2);
      }
    }

    /* ========== HEADER ========== */
    .header {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      z-index: 1000;
      padding: 1rem 0;
      background-color: rgba(10, 10, 10, 0.8);
      backdrop-filter: blur(10px);
      border-bottom: 1px solid rgba(0, 255, 157, 0.1);
      transition: var(--transition);
    }

    .header.scrolled {
      padding: 0.5rem 0;
      background-color: rgba(10, 10, 10, 0.95);
      box-shadow: var(--shadow);
    }

    .header .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

    .logo-link {
      display: flex;
      align-items: center;
      gap: 0.75rem;
    }

    .logo-text {
      font-family: var(--font-heading);
      font-size: 1.5rem;
      font-weight: 700;
      color: var(--light);
    }

    .logo-text span {
      color: var(--primary);
    }

    .nav-list {
      display: flex;
      align-items: center;
      gap: 2rem;
    }

    .nav-list li a {
      position: relative;
      padding: 0.5rem 0;
      font-weight: 500;
      color: var(--gray);
    }

    .nav-list li a:hover,
    .nav-list li a.active {
      color: var(--light);
    }

    .nav-list li a::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 0;
      height: 2px;
      background-color: var(--primary);
      transition: var(--transition);
    }

    .nav-list li a:hover::after,
    .nav-list li a.active::after {
      width: 100%;
    }

    .nav-cta {
      padding: 0.5rem 1.5rem;
      background-color: var(--primary);
      color: var(--dark);
      border-radius: 50px;
      font-weight: 600;
      transition: var(--transition);
    }

    .nav-cta:hover {
      background-color: var(--primary-dark);
      color: var(--dark);
      box-shadow: var(--shadow-primary);
    }

    /* ========== HERO SECTION ========== */
    .hero {
      padding: 10rem 0 5rem;
      min-height: 100vh;
      display: flex;
      align-items: center;
      position: relative;
      overflow: hidden;
    }

    .hero .container {
      display: flex;
      align-items: center;
      justify-content: space-between;
      gap: 3rem;
    }

    .hero-content {
      flex: 1;
      max-width: 600px;
      position: relative;
      z-index: 1;
    }

    .hero-image {
      flex: 1;
      display: flex;
      justify-content: center;
      align-items: center;
      position: relative;
      z-index: 1;
    }

    .hero-title {
      font-size: 3.5rem;
      margin-bottom: 1.5rem;
      line-height: 1.1;
    }

    .title-gradient {
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      -webkit-background-clip: text;
      background-clip: text;
      color: transparent;
      animation: gradientShift 8s ease infinite;
      background-size: 200% 200%;
    }

    .hero-subtitle {
      font-size: 1.25rem;
      color: var(--gray);
      margin-bottom: 2rem;
      max-width: 500px;
    }

    .hero-buttons {
      display: flex;
      gap: 1rem;
      margin-top: 2rem;
    }

    .ai-orb {
      position: relative;
      width: 400px;
      height: 400px;
      border-radius: 50%;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    .orb-core {
      width: 200px;
      height: 200px;
      border-radius: 50%;
      background: radial-gradient(circle at center, var(--primary), transparent 70%);
      box-shadow: 0 0 50px var(--primary);
      animation: pulseOrb 3s ease infinite alternate;
    }

    .orb-ring {
      position: absolute;
      width: 100%;
      height: 100%;
      border: 2px solid rgba(0, 255, 157, 0.3);
      border-radius: 50%;
      animation: rotateRing 20s linear infinite;
    }

    .orb-ring::before {
      content: '';
      position: absolute;
      top: -10px;
      left: 50%;
      transform: translateX(-50%);
      width: 20px;
      height: 20px;
      border-radius: 50%;
      background-color: var(--primary);
      box-shadow: 0 0 20px var(--primary);
    }

    .orb-particles {
      position: absolute;
      width: 100%;
      height: 100%;
    }

    .orb-particles span {
      position: absolute;
      width: 8px;
      height: 8px;
      border-radius: 50%;
      background-color: var(--primary);
      opacity: 0.6;
    }

    @keyframes pulseOrb {
      0% {
        transform: scale(0.95);
        box-shadow: 0 0 30px var(--primary);
      }
      100% {
        transform: scale(1.05);
        box-shadow: 0 0 70px var(--primary);
      }
    }

    @keyframes rotateRing {
      0% {
        transform: rotate(0deg);
      }
      100% {
        transform: rotate(360deg);
      }
    }

    @keyframes gradientShift {
      0% {
        background-position: 0% 50%;
      }
      50% {
        background-position: 100% 50%;
      }
      100% {
        background-position: 0% 50%;
      }
    }

    /* ========== BUTTONS ========== */
    .cta-button {
      display: inline-flex;
      align-items: center;
      justify-content: center;
      padding: 0.75rem 2rem;
      border-radius: 50px;
      font-weight: 600;
      transition: var(--transition);
      gap: 0.5rem;
    }

    .cta-button.primary {
      background-color: var(--primary);
      color: var(--dark);
      box-shadow: var(--shadow-primary);
    }

    .cta-button.primary:hover {
      background-color: var(--primary-dark);
      transform: translateY(-3px);
      box-shadow: 0 10px 25px rgba(0, 255, 157, 0.4);
    }

    .cta-button.secondary {
      background-color: transparent;
      color: var(--light);
      border: 2px solid var(--primary);
    }

    .cta-button.secondary:hover {
      background-color: rgba(0, 255, 157, 0.1);
      transform: translateY(-3px);
      box-shadow: var(--shadow-primary);
    }

    /* ========== FEATURES SECTION ========== */
    .features {
      padding: 5rem 0;
      position: relative;
    }

    .section-header {
      text-align: center;
      margin-bottom: 4rem;
    }

    .section-header h2 {
      font-size: 2.5rem;
      margin-bottom: 1rem;
    }

    .section-header p {
      color: var(--gray);
      max-width: 600px;
      margin: 0 auto;
    }

    .features-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
      gap: 2rem;
    }

    .feature-card {
      background-color: var(--dark-light);
      border-radius: 1rem;
      padding: 2rem;
      position: relative;
      overflow: hidden;
      transition: var(--transition);
      border: 1px solid rgba(255, 255, 255, 0.05);
    }

    .feature-card:hover {
      transform: translateY(-10px);
      box-shadow: var(--shadow-lg);
      border-color: rgba(0, 255, 157, 0.3);
    }

    .feature-icon {
      width: 60px;
      height: 60px;
      background: rgba(0, 255, 157, 0.1);
      border-radius: 50%;
      display: flex;
      align-items: center;
      justify-content: center;
      margin-bottom: 1.5rem;
      color: var(--primary);
      font-size: 1.5rem;
    }

    .feature-card h3 {
      font-size: 1.5rem;
      margin-bottom: 1rem;
    }

    .feature-card p {
      color: var(--gray);
      margin-bottom: 1.5rem;
    }

    .feature-wave {
      position: absolute;
      bottom: 0;
      left: 0;
      width: 100%;
      height: 5px;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      transform: scaleX(0);
      transform-origin: left;
      transition: transform 0.5s ease;
    }

    .feature-card:hover .feature-wave {
      transform: scaleX(1);
    }

    /* ========== FOOTER ========== */
    .footer {
      background-color: var(--dark-light);
      padding: 5rem 0 2rem;
      position: relative;
    }

    .footer::before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 1px;
      background: linear-gradient(90deg, transparent, var(--primary), transparent);
    }

    .footer-grid {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
      gap: 3rem;
      margin-bottom: 3rem;
    }

    .footer-about {
      max-width: 300px;
    }

    .footer-logo {
      display: flex;
      align-items: center;
      gap: 0.75rem;
      margin-bottom: 1.5rem;
    }

    .footer-logo span {
      font-family: var(--font-heading);
      font-size: 1.25rem;
      font-weight: 700;
    }

    .footer p {
      color: var(--gray);
      margin-bottom: 1.5rem;
    }

    .social-links {
      display: flex;
      gap: 1rem;
    }

    .social-links a {
      width: 40px;
      height: 40px;
      border-radius: 50%;
      background-color: rgba(255, 255, 255, 0.05);
      display: flex;
      align-items: center;
      justify-content: center;
      color: var(--gray);
      transition: var(--transition);
    }

    .social-links a:hover {
      background-color: var(--primary);
      color: var(--dark);
      transform: translateY(-3px);
    }

    .footer-links h3 {
      font-size: 1.25rem;
      margin-bottom: 1.5rem;
      color: var(--light);
      position: relative;
      padding-bottom: 0.5rem;
    }

    .footer-links h3::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0;
      width: 40px;
      height: 2px;
      background-color: var(--primary);
    }

    .footer-links ul li {
      margin-bottom: 0.75rem;
    }

    .footer-links ul li a {
      color: var(--gray);
      transition: var(--transition);
    }

    .footer-links ul li a:hover {
      color: var(--primary);
      padding-left: 5px;
    }

    .footer-bottom {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding-top: 2rem;
      border-top: 1px solid rgba(255, 255, 255, 0.05);
    }

    .footer-bottom p {
      color: var(--gray);
      font-size: 0.9rem;
    }

    .legal-links {
      display: flex;
      gap: 1.5rem;
    }

    .legal-links a {
      color: var(--gray);
      font-size: 0.9rem;
      transition: var(--transition);
    }

    .legal-links a:hover {
      color: var(--primary);
    }

    /* Loading Animation */
    .loading-screen {
      position: fixed;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      background-color: var(--dark);
      display: flex;
      justify-content: center;
      align-items: center;
      z-index: 9999;
      opacity: 1;
      visibility: visible;
      transition: opacity 0.5s ease, visibility 0.5s ease;
    }

    .loading-screen.loaded {
      opacity: 0;
      visibility: hidden;
    }

    .loading-content {
      text-align: center;
      max-width: 300px;
      width: 100%;
    }

    .loading-logo {
      position: relative;
      width: 150px;
      height: 150px;
      margin: 0 auto 2rem;
      animation: pulse 2s infinite ease-in-out;
    }

    .loading-logo i {
      font-size: 5rem;
      color: var(--primary);
      position: relative;
      z-index: 2;
      filter: drop-shadow(0 0 10px rgba(0, 255, 157, 0.5));
    }

    .loading-glow {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border-radius: 50%;
      background: radial-gradient(circle, rgba(0, 255, 157, 0.3) 0%, transparent 70%);
      z-index: 1;
      animation: glowPulse 3s infinite alternate;
    }

    .loading-progress {
      height: 4px;
      width: 100%;
      background-color: rgba(255, 255, 255, 0.1);
      border-radius: 2px;
      overflow: hidden;
      position: relative;
    }

    .loading-progress::after {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      width: 0;
      background: linear-gradient(90deg, var(--primary), var(--secondary));
      animation: progressLoad 2s infinite ease-in-out;
    }

    @keyframes pulse {
      0% { transform: scale(0.95); }
      50% { transform: scale(1.05); }
      100% { transform: scale(0.95); }
    }

    @keyframes glowPulse {
      0% { opacity: 0.3; transform: scale(0.8); }
      100% { opacity: 0.7; transform: scale(1.2); }
    }

    @keyframes progressLoad {
      0% { width: 0; left: 0; }
      50% { width: 100%; left: 0; }
      100% { width: 0; left: 100%; }
    }

    /* Back to Top Button */
    .back-to-top {
      position: fixed;
      bottom: 30px;
      right: 30px;
      width: 60px;
      height: 60px;
      border-radius: 50%;
      background: var(--primary);
      border: none;
      cursor: pointer;
      display: flex;
      align-items: center;
      justify-content: center;
      box-shadow: 0 4px 20px rgba(0, 255, 157, 0.3);
      z-index: 999;
      opacity: 0;
      visibility: hidden;
      transform: translateY(20px);
      transition: all 0.3s ease;
      padding: 0;
      overflow: hidden;
    }

    .back-to-top.visible {
      opacity: 1;
      visibility: visible;
      transform: translateY(0);
    }

    .back-to-top:hover {
      background: var(--primary-dark);
      box-shadow: 0 6px 25px rgba(0, 255, 157, 0.5);
    }

    /* Responsive Styles */
    @media (max-width: 992px) {
      .hero .container {
        flex-direction: column;
        text-align: center;
      }
      
      .hero-content {
        max-width: 100%;
        margin-bottom: 3rem;
      }
      
      .hero-title {
        font-size: 3rem;
      }
      
      .hero-buttons {
        justify-content: center;
      }
      
      .ai-orb {
        width: 300px;
        height: 300px;
      }
      
      .orb-core {
        width: 150px;
        height: 150px;
      }
    }

    @media (max-width: 768px) {
      .nav-list {
        position: fixed;
        top: 0;
        right: -100%;
        width: 80%;
        max-width: 300px;
        height: 100vh;
        background-color: var(--dark-light);
        flex-direction: column;
        align-items: flex-start;
        padding: 6rem 2rem 2rem;
        transition: var(--transition);
        box-shadow: -5px 0 15px rgba(0, 0, 0, 0.2);
      }
      
      .nav-list.active {
        right: 0;
      }
      
      .nav-list li a {
        font-size: 1.1rem;
        padding: 0.75rem 0;
      }
      
      .hero {
        padding-top: 8rem;
      }
      
      .hero-title {
        font-size: 2.5rem;
      }
      
      .section-header h2 {
        font-size: 2rem;
      }
    }

    @media (max-width: 576px) {
      .hero-title {
        font-size: 2rem;
      }
      
      .hero-subtitle {
        font-size: 1.1rem;
      }
      
      .hero-buttons {
        flex-direction: column;
      }
      
      .feature-card {
        padding: 1.5rem;
      }
      
      .footer-grid {
        grid-template-columns: 1fr;
      }
      
      .footer-bottom {
        flex-direction: column;
        gap: 1rem;
        text-align: center;
      }
      
      .legal-links {
        flex-wrap: wrap;
        justify-content: center;
      }
    }
  </style>
</head>

<body>


  <!-- Loading Animation -->


  <!-- Background Animation -->
  <div class="bg-animation">
    <div class="particles"></div>
    <div class="glow"></div>
  </div>

  <!-- Header -->
  <header class="header">
    <div class="container">
      <a href="https://creepytech.org" class="logo-link">
        <span class="logo-text">KELVIN<span>_SESSION</span></span>
      </a>

      <ul class="nav-list">
        <li><a href="#" class="active">Home</a></li>
        <li><a href="/qr">QR Pair</a></li>
        <li><a href="/pair">Code Pair</a></li>
        <li><a href="https://github.com/JAMPAN47" class="nav-cta">Deploy Now</a></li>
      </ul>
    </div>
  </header>

  <!-- Hero Section -->
  <section class="hero">
    <div class="container">
      <div class="hero-content">
        <h1 class="hero-title">
          <span class="title-gradient">KELVINE_SESSION</span>
        </h1>
        <p class="hero-subtitle">The most terrifying WhatsApp bot experience. Pair your session with our haunted QR code or cursed pairing number.</p>

        <div class="hero-buttons">
          <a href="/qr" class="cta-button primary">
            <i class="fas fa-qrcode"></i> QR Pair
          </a>
          <a href="/pair" class="cta-button secondary">
            <i class="fas fa-key"></i> Code Pair
          </a>
        </div>
      </div>

      <div class="hero-image">
        <div class="ai-orb">
          <div class="orb-core">
            <i class="fas fa-skull orb-logo"></i>
          </div>
          <div class="orb-ring"></div>
          <div class="orb-particles"><span style="left: 11.0962%; top: 17.8855%; width: 4.11728px; height: 4.11728px; animation-delay: 2.52117s; animation-duration: 14.6662s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 46.0795%; top: 38.08%; width: 4.85888px; height: 4.85888px; animation-delay: 2.05851s; animation-duration: 11.1594s; animation-name: float; animation-iteration-count: infinite;"></span>
            <span
              style="left: 59.7717%; top: 81.3056%; width: 4.40952px; height: 4.40952px; animation-delay: 1.32455s; animation-duration: 5.16401s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 56.8331%; top: 73.1215%; width: 9.70133px; height: 9.70133px; animation-delay: 2.53063s; animation-duration: 10.7349s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 71.3165%; top: 44.3935%; width: 5.21544px; height: 5.21544px; animation-delay: 0.69741s; animation-duration: 12.5344s; animation-name: float; animation-iteration-count: infinite;"></span>
              <span
                style="left: 26.9971%; top: 46.3521%; width: 7.42423px; height: 7.42423px; animation-delay: 4.4124s; animation-duration: 14.107s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 59.0886%; top: 1.59927%; width: 8.72916px; height: 8.72916px; animation-delay: 4.5074s; animation-duration: 11.2407s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 16.6955%; top: 1.31914%; width: 11.1716px; height: 11.1716px; animation-delay: 1.9067s; animation-duration: 8.73036s; animation-name: float; animation-iteration-count: infinite;"></span>
                <span
                  style="left: 46.3322%; top: 98.2998%; width: 8.1017px; height: 8.1017px; animation-delay: 0.122638s; animation-duration: 10.6323s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 69.87%; top: 20.4218%; width: 4.12336px; height: 4.12336px; animation-delay: 4.26448s; animation-duration: 13.1486s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 65.6819%; top: 79.1457%; width: 4.00545px; height: 4.00545px; animation-delay: 3.47154s; animation-duration: 9.48813s; animation-name: float; animation-iteration-count: infinite;"></span>
                  <span
                    style="left: 68.5196%; top: 52.7438%; width: 4.64074px; height: 4.64074px; animation-delay: 0.761617s; animation-duration: 5.64742s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 72.3371%; top: 85.0681%; width: 9.78765px; height: 9.78765px; animation-delay: 2.45816s; animation-duration: 5.70726s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 95.929%; top: 98.8867%; width: 4.423px; height: 4.423px; animation-delay: 0.990947s; animation-duration: 6.36906s; animation-name: float; animation-iteration-count: infinite;"></span>
                    <span
                      style="left: 86.4695%; top: 90.483%; width: 7.49211px; height: 7.49211px; animation-delay: 3.42692s; animation-duration: 13.955s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 19.0752%; top: 43.5184%; width: 5.29739px; height: 5.29739px; animation-delay: 3.57398s; animation-duration: 8.11563s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 81.0235%; top: 53.4611%; width: 4.7735px; height: 4.7735px; animation-delay: 2.67889s; animation-duration: 12.4358s; animation-name: float; animation-iteration-count: infinite;"></span>
                      <span
                        style="left: 66.24%; top: 79.3402%; width: 11.2631px; height: 11.2631px; animation-delay: 0.0999964s; animation-duration: 8.03827s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 43.3223%; top: 74.8648%; width: 8.21204px; height: 8.21204px; animation-delay: 1.0257s; animation-duration: 9.47108s; animation-name: float; animation-iteration-count: infinite;"></span><span style="left: 86.0699%; top: 28.2852%; width: 10.2277px; height: 10.2277px; animation-delay: 0.813529s; animation-duration: 13.0302s; animation-name: float; animation-iteration-count: infinite;"></span></div>
        </div>
      </div>
    </div>
  </section>

  <!-- Features Section -->
  <section class="features">
    <div class="container">
      <div class="section-header">
        <h2>Dark Features</h2>
        <p>Unleash the supernatural capabilities of KELVINE_SESSION</p>
      </div>

      <div class="features-grid">
        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-qrcode"></i>
          </div>
          <h3>Haunted QR</h3>
          <p>Summon a spectral QR code to connect your WhatsApp with the other side. Scan if you dare...</p>
          <div class="feature-wave"></div>
        </div>

        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-key"></i>
          </div>
          <h3>Cursed Pair Code</h3>
          <p>Enter your number to receive a cursed pairing code. The spirits will handle the rest.</p>
          <div class="feature-wave"></div>
        </div>

        <div class="feature-card">
          <div class="feature-icon">
            <i class="fas fa-code-branch"></i>
          </div>
          <h3>Deploy Your Own</h3>
          <p>Summon your own KELVINE_SESSION bot from the depths of GitHub.</p>
          <div class="feature-wave"></div>
        </div>
      </div>
    </div>
  </section>

  <!-- Footer -->
  <footer class="footer">
    <div class="container">
      <div class="footer-grid">
        <div class="footer-about">
          <div class="footer-logo">
            <span>KELVINE<span>_SESSION</span></span>
          </div>
          <p>The most terrifying WhatsApp bot experience</p>
          <p>Developed with dark magic by Danny</p>

          <div class="social-links">
            <a href="https://whatsapp.com/channel/0029VacQFw65Ui2gGv0Kwk1r" target="_blank"><i class="fab fa-whatsapp"></i></a>
            <a href="https://t.me/creepytech" target="_blank"><i class="fab fa-telegram"></i></a>
            <a href="https://github.com/JAMPAN47" target="_blank"><i class="fab fa-github"></i></a>
            <a href="https://youtube.com/@creepy_technology" target="_blank"><i class="fab fa-youtube"></i></a>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <p>© 2025 KELVIN_SESSION. All rights reserved.</p>
        <div class="legal-links">
          <a href="#">Privacy Policy</a>
          <a href="#">Terms of Service</a>
        </div>
      </div>
    </div>
  </footer>

  <!-- Back to Top Button -->
  <button class="back-to-top" title="Back to Top">
    <i class="fas fa-arrow-up"></i>
  </button>

  <script>
    // Loading animation script
    document.addEventListener('DOMContentLoaded', function() {
      const loadingScreen = document.querySelector('.loading-screen');
      
      window.addEventListener('load', function() {
        setTimeout(function() {
          loadingScreen.classList.add('loaded');
          setTimeout(function() {
            loadingScreen.remove();
          }, 500);
        }, 1000);
      });
      
      setTimeout(function() {
        loadingScreen.classList.add('loaded');
        setTimeout(function() {
          loadingScreen.remove();
        }, 500);
      }, 5000);

      // Create particles for AI orb
      const orbParticles = document.querySelector('.orb-particles');
      if (orbParticles) {
        for (let i = 0; i < 20; i++) {
          const particle = document.createElement('span');
          particle.style.left = `${Math.random() * 100}%`;
          particle.style.top = `${Math.random() * 100}%`;
          particle.style.width = `${Math.random() * 8 + 4}px`;
          particle.style.height = particle.style.width;
          particle.style.animationDelay = `${Math.random() * 5}s`;
          particle.style.animationDuration = `${Math.random() * 10 + 5}s`;
          particle.style.animationName = 'float';
          particle.style.animationIterationCount = 'infinite';
          orbParticles.appendChild(particle);
        }
      }

      // Back to Top Button
      const backToTopButton = document.querySelector('.back-to-top');
      window.addEventListener('scroll', function() {
        if (window.pageYOffset > 300) {
          backToTopButton.classList.add('visible');
        } else {
          backToTopButton.classList.remove('visible');
        }
      });
      
      backToTopButton.addEventListener('click', function(e) {
        e.preventDefault();
        window.scrollTo({
          top: 0,
          behavior: 'smooth'
        });
      });

      // Header scroll effect
      const header = document.querySelector('.header');
      window.addEventListener('scroll', function() {
        if (window.scrollY > 50) {
          header.classList.add('scrolled');
        } else {
          header.classList.remove('scrolled');
        }
      });
    });
  </script>


</body>