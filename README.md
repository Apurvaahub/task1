# task1
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Landing Page</title>
  <style>
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    html {
      scroll-behavior: smooth;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
      background-color: #f9f9f9;
      color: #333;
      line-height: 1.6;
    }

    /* Navbar */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1.2rem 2rem;
      background: white;
      box-shadow: 0 2px 10px rgba(0,0,0,0.05);
      position: sticky;
      top: 0;
      z-index: 999;
    }

    .logo {
      font-size: 1.6rem;
      font-weight: bold;
      color: #2C3E50;
    }

    .nav-links {
      list-style: none;
      display: flex;
      gap: 1.5rem;
    }

    .nav-links a {
      text-decoration: none;
      color: #333;
      font-weight: 500;
      transition: color 0.3s ease;
    }

    .nav-links a:hover {
      color: #007BFF;
    }

    /* Hero Section */
    .hero {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 6rem 2rem;
      background: linear-gradient(to right, #007BFF, #00C6FF);
      color: white;
    }

    .hero h1 {
      font-size: 2.8rem;
      margin-bottom: 1rem;
    }

    .hero p {
      font-size: 1.2rem;
      max-width: 600px;
      margin-bottom: 2rem;
    }

    .btn {
      padding: 0.75rem 1.5rem;
      border: none;
      border-radius: 30px;
      font-size: 1rem;
      cursor: pointer;
      transition: background 0.3s ease;
    }

    .primary-btn {
      background: white;
      color: #007BFF;
      font-weight: bold;
    }

    .primary-btn:hover {
      background: #f0f0f0;
    }

    .section {
      padding: 4rem 2rem;
      text-align: center;
    }

    .features {
      background-color: #fff;
    }

    .feature-items {
      display: flex;
      flex-direction: column;
      gap: 2rem;
      max-width: 1000px;
      margin: 2rem auto 0;
    }

    .feature-card {
      background: #f2f2f2;
      padding: 2rem;
      border-radius: 8px;
      transition: transform 0.3s ease;
    }

    .feature-card:hover {
      transform: translateY(-5px);
    }

    .about {
      background-color: #eef6fb;
    }

    .cta {
      background: #007BFF;
      color: white;
    }

    .secondary-btn {
      background: white;
      color: #007BFF;
      font-weight: bold;
    }

    .secondary-btn:hover {
      background: #f0f0f0;
    }

    .footer {
      text-align: center;
      padding: 2rem;
      background: #222;
      color: #ccc;
    }

    /* Fade-in Animation */
    .fade-in {
      opacity: 0;
      transform: translateY(20px);
      transition: opacity 0.8s ease-out, transform 0.8s ease-out;
    }

    .fade-in.visible {
      opacity: 1;
      transform: translateY(0);
    }

    /* Responsive */
    @media (min-width: 768px) {
      .feature-items {
        flex-direction: row;
        justify-content: space-between;
      }
    }
  </style>
</head>
<body>

  <header class="hero">
    <nav class="navbar">
      <div class="logo">BrandName</div>
      <ul class="nav-links">
        <li><a href="#features">Features</a></li>
        <li><a href="#about">About</a></li>
        <li><a href="#cta">Get Started</a></li>
      </ul>
    </nav>
    <div class="hero-content">
      <h1>Your Solution Starts Here</h1>
      <p>Boost your business with our innovative tools designed for success.</p>
      <a href="#cta" class="btn primary-btn">Start Free Trial</a>
    </div>
  </header>

  <section id="features" class="features section">
    <h2>Features</h2>
    <div class="feature-items">
      <div class="feature-card fade-in">
        <h3>Fast & Scalable</h3>
        <p>Our platform grows with you and ensures performance at scale.</p>
      </div>
      <div class="feature-card fade-in">
        <h3>Secure</h3>
        <p>Top-tier encryption and compliance for your peace of mind.</p>
      </div>
      <div class="feature-card fade-in">
        <h3>24/7 Support</h3>
        <p>We’re here to help, anytime you need us.</p>
      </div>
    </div>
  </section>

  <section id="about" class="section about">
    <div class="about-content fade-in">
      <h2>About Us</h2>
      <p>We're passionate innovators helping businesses like yours achieve more. Trusted by thousands worldwide.</p>
    </div>
  </section>

  <section id="cta" class="section cta">
    <h2>Get Started Today</h2>
    <p>Join 10,000+ users growing with our tools. No credit card required.</p>
    <a href="#" class="btn secondary-btn">Create Your Account</a>
  </section>

  <footer class="footer">
    <p>© 2025 BrandName. All rights reserved.</p>
  </footer>

  <script>
    // Fade-in on scroll
    const fadeElements = document.querySelectorAll('.fade-in');
    const observer = new IntersectionObserver(entries => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          entry.target.classList.add('visible');
          observer.unobserve(entry.target);
        }
      });
    }, { threshold: 0.1 });

    fadeElements.forEach(el => observer.observe(el));
  </script>

</body>
</html>
