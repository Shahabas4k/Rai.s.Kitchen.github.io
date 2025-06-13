<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Rai's Kitchen – Thalassery Dum Biryani & Snacks</title>
  <link rel="icon" href="https://cdn-icons-png.flaticon.com/512/1046/1046784.png" />
  <!-- Google Font -->
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap" rel="stylesheet">
  <!-- AOS Animate on Scroll -->
  <link href="https://unpkg.com/aos@2.3.1/dist/aos.css" rel="stylesheet">

  <!-- SEO + Social -->
  <meta name="description" content="Rai's Kitchen – Homemade Thalassery Dum Biryani & Malabar Snacks delivered fresh in Kannur." />
  <meta property="og:title" content="Rai's Kitchen – Home‑Made Biryani Delivered!" />
  <meta property="og:description" content="Authentic flavours of Thalassery, right at your home. Order now!" />
  <meta property="og:image" content="https://your-domain.com/preview-image.jpg" />
  <meta name="keywords" content="Thalassery Biryani, Homemade Food, Kannur, Dum Biryani" />

  <style>
    :root {
      --primary: #e63946;
      --accent: #ffb703;
      --bg: #fffaf5;
      --text: #333;
    }
    *, *::before, *::after { box-sizing: border-box; }

    body {
      font-family: 'Poppins', sans-serif;
      margin: 0; padding: 0;
      background: var(--bg);
      color: var(--text);
      scroll-behavior: smooth;
    }
    header {
      background: var(--primary);
      color: white;
      padding: 1.5rem;
      text-align: center;
    }
    nav {
      position: sticky;
      top: 0;
      background: var(--accent);
      z-index: 1000;
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.75rem 1.5rem;
    }
    nav .logo { font-weight: 600; font-size: 1.2rem; }
    nav ul {
      list-style: none;
      display: flex;
      gap: 1rem;
      margin: 0;
      padding: 0;
    }
    nav ul li a {
      text-decoration: none;
      color: var(--text);
      font-weight: 600;
    }
    /* hamburger */
    .menu-toggle {
      display: none;
      flex-direction: column;
      cursor: pointer;
    }
    .menu-toggle div {
      width: 25px;
      height: 3px;
      background: var(--text);
      margin: 4px 0;
    }
    /* Hero */
    .hero {
      background: url('https://plus.unsplash.com/premium_photo-1680291971402-ccb1640bcd23?q=80&w=2070') center/cover no-repeat;
      height: 90vh;
      color: white;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      text-align: center;
      padding: 0 1rem;
    }
    .hero h1 {
      font-size: 3rem;
      margin: 0;
      text-shadow: 2px 2px 8px rgba(0,0,0,0.5);
    }
    .hero p {
      margin: 1rem 0;
      font-size: 1.25rem;
      text-shadow: 1px 1px 4px rgba(0,0,0,0.5);
    }
    .hero a {
      padding: 1rem 2rem;
      background: var(--primary);
      color: white;
      border-radius: 30px;
      text-decoration: none;
      font-weight: 600;
    }
    /* Sections */
    .section {
      padding: 4rem 1.5rem;
      max-width: 900px;
      margin: auto;
    }
    h2 { text-align: center; margin-bottom: 2rem; }

    /* Food Grid */
    .grid-menu {
      display: grid;
      grid-template-columns: repeat(auto-fit, minmax(200px,1fr));
      gap: 1.5rem;
    }
    .food-card {
      background: white;
      border-radius: 12px;
      box-shadow: 0 2px 8px rgba(0,0,0,0.1);
      overflow: hidden;
      position: relative;
      transition: transform 0.2s;
    }
    .food-card:hover { transform: translateY(-5px); }
    .food-card img {
      width: 100%;
      height: 140px;
      object-fit: cover;
    }
    .info {
      padding: 1rem;
      text-align: center;
    }
    .info h3 {
      margin: 0.5rem 0;
      font-size: 1.1rem;
    }
    .info p { margin: 0.3rem 0; color: #555; }
    .info button {
      margin-top: 0.5rem;
      background: var(--accent);
      color: var(--text);
      border: none;
      padding: 0.6rem 1.2rem;
      border-radius: 20px;
      cursor: pointer;
      font-weight: 600;
    }
    .food-card .tag {
      position: absolute;
      top: 10px; right: 10px;
      background: var(--accent);
      padding: 5px 10px;
      border-radius: 20px;
      font-size: 0.8rem;
    }
    /* Cart Bar */
    #cart-bar {
      position: fixed;
      bottom: 0; left: 0;
      width: 100%;
      background: var(--primary);
      color: white;
      padding: 1rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      box-shadow: 0 -2px 6px rgba(0,0,0,0.2);
      transform: translateY(100%);
      transition: transform 0.3s;
    }
    #cart-bar.show { transform: translateY(0); }
    #cart-bar span { font-weight: 600; }
    #checkout-btn {
      background: white;
      color: var(--primary);
      border: none;
      padding: 0.6rem 1.2rem;
      border-radius: 20px;
      font-weight: 600;
      cursor: pointer;
    }
    /* Footer */
    footer {
      background: #333;
      color: white;
      text-align: center;
      padding: 1.5rem;
      margin-top: 2rem;
    }
    /* Responsive */
    @media(max-width:768px){
      .menu-toggle { display: flex; }
      nav ul { display: none; flex-direction: column; background: var(--accent); position: absolute; top: 60px; right: 0; width: 200px; }
      nav ul.show { display: flex; }
    }
  </style>
</head>
<body>

  <header>
    <h1>Rai's Kitchen</h1>
    <p>Thalassery Dum Biryani & Snacks – Delivered Fresh</p>
  </header>

  <nav>
    <div class="logo">Rai's Kitchen</div>
    <div class="menu-toggle" onclick="toggleMenu()">
      <div></div><div></div><div></div>
    </div>
    <ul id="nav-menu">
      <li><a href="#menu">Menu</a></li>
      <li><a href="#about">About</a></li>
      <li><a href="#offer">Offer</a></li>
      <li><a href="#contact">Contact</a></li>
    </ul>
  </nav>

  <section class="hero" data-aos="fade-in">
    <h1>Authentic Thalassery Dum Biryani</h1>
    <p>Home‑cooked. Soul‑warming. Delivered fresh.</p>
    <a href="#menu">View Menu</a>
  </section>

  <section id="menu" class="section" data-aos="fade-up">
    <h2>Our Menu</h2>
    <div class="grid-menu">
      <!-- Example card -->
      <div class="food-card" data-name="Chicken Biryani">
        <img src="https://images.pexels.com/photos/16020573/pexels-photo-16020573.jpeg" alt="Chicken Biryani">
        <div class="tag">🔥 Popular</div>
        <div class="info">
          <h3>Chicken Biryani</h3>
          <p><strong>₹120</strong> Full | <strong>₹100</strong> Half</p>
          <button onclick="addToCart('Chicken Biryani')">Add</button>
        </div>
      </div>
      <!-- Repeat similar cards for others -->
      <div class="food-card" data-name="Beef Biryani">
        <img src="https://media.istockphoto.com/id/1410130688/photo/mutton-biryani.jpg" alt="Beef Biryani">
        <div class="tag">🔥 Best Seller</div>
        <div class="info">
          <h3>Beef Biryani</h3>
          <p><strong>₹140</strong> Full | <strong>₹110</strong> Half</p>
          <button onclick="addToCart('Beef Biryani')">Add</button>
        </div>
      </div>
      <!-- Add more as needed -->
    </div>
  </section>

  <section id="about" class="section" data-aos="fade-up">
    <h2>About Us</h2>
    <p>We’re a home-based food service in Kannur delivering authentic flavors of Thalassery. Every dish is made with care, love, and traditional recipes passed down through generations.</p>
  </section>

  <section id="offer" class="section" data-aos="fade-up">
    <h2>Special Offer</h2>
    <p><strong>Buy 2 Full Chicken Dum Biriyanis, Get 1 Half Free!</strong></p>
  </section>

  <section id="contact" class="section" data-aos="fade-up">
    <h2>Contact & Orders</h2>
    <p>📍 Thalassery, Kannur</p>
    <p>📞 <a href="tel:+919188335430">+91 91883 35430</a></p>
    <p>💬 <a href="https://wa.me/919188335430">Order via WhatsApp</a></p>
    <iframe
      src="https://www.google.com/maps/embed?pb=!1m18..."
      width="100%" height="250" style="border:0; border-radius:8px;"
      allowfullscreen="" loading="lazy"></iframe>
  </section>

  <footer data-aos="fade-up">
    <p>© 2025 Rai's Food | Homemade Taste, Delivered Fresh</p>
  </footer>

  <!-- Cart Bar (hidden initially) -->
  <div id="cart-bar">
    <span id="cart-count">0 items</span>
    <button id="checkout-btn" onclick="checkout()">Order via WhatsApp</button>
  </div>

  <script src="https://unpkg.com/aos@2.3.1/dist/aos.js"></script>
  <script>
    AOS.init();

    // Mobile Menu
    function toggleMenu() {
      document.getElementById('nav-menu').classList.toggle('show');
    }

    // Simple JS Cart
    const cart = [];
    const cartBar = document.getElementById('cart-bar');
    const cartCount = document.getElementById('cart-count');

    function addToCart(item) {
      cart.push(item);
      cartCount.textContent = cart.length + (cart.length === 1 ? ' item' : ' items');
      cartBar.classList.add('show');
    }

    function checkout() {
      if (cart.length === 0) return;
      const message = encodeURIComponent(`Hello, I’d like to order:\n- ${cart.join('\n- ')}\n\nThank you!`);
      window.open(`https://wa.me/919188335430?text=${message}`, '_blank');
    }
  </script>
</body>
</html>
