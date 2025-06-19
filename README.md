<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>S.L.E.E.K</title>
  <meta name="description" content="Shop fashion and accessories at S.L.E.E.K. Discover clothes, bags, and jewelry for all styles with fast WhatsApp delivery.">
  <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
  <link href="https://unpkg.com/aos@2.3.4/dist/aos.css" rel="stylesheet">
  <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Lato:wght@400;700&display=swap" rel="stylesheet">
  <style>
    html {
      scroll-behavior: smooth;
    }
    .sticky-nav {
      position: sticky;
      top: 0;
      z-index: 50;
      background: #16a34a; /* Tailwind bg-green-600 */
    }
    .product-card:hover img {
      transform: scale(1.05);
      transition: transform 0.3s ease;
      animation: sparkle-hover 1.5s infinite;
    }
    .pagination-btn:hover {
      background-color: #e5e7eb;
      transition: background-color 0.3s ease;
    }
    h2, h3, h4 {
      font-family: 'Playfair Display', serif;
      font-weight: 700;
    }
    p, .product-card p, input, select, textarea, a, button {
      font-family: 'Lato', sans-serif;
      font-weight: 400;
    }
    h2 {
      font-size: 2.5rem;
    }
    h3 {
      font-size: 1.75rem;
    }
    h4 {
      font-size: 1.25rem;
    }
    .hero-title {
      position: relative;
      display: inline-block;
    }
    .hero-title::after {
      content: '✨';
      position: absolute;
      top: -10px;
      right: -20px;
      font-size: 1.5rem;
      animation: sparkle 2s infinite;
    }
    .shop-now-btn:hover {
      animation: bounce 0.5s ease;
    }
    .glow-text {
      text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc;
      animation: glow 1.5s ease-in-out infinite;
    }
    #home {
      background: linear-gradient(135deg, #0d1b2a 0%, #1b263b 100%); /* Dark space gradient */
    }
    #starfield {
      background: transparent;
    }
    @keyframes sparkle {
      0% { opacity: 0; transform: scale(0); }
      50% { opacity: 1; transform: scale(1); }
      100% { opacity: 0; transform: scale(0); }
    }
    @keyframes sparkle-hover {
      0% { box-shadow: 0 0 5px rgba(0, 255, 204, 0.5); }
      50% { box-shadow: 0 0 15px rgba(0, 255, 204, 0.8); }
      100% { box-shadow: 0 0 5px rgba(0, 255, 204, 0.5); }
    }
    @keyframes bounce {
      0%, 100% { transform: translateY(0); }
      50% { transform: translateY(-5px); }
    }
    @keyframes glow {
      0% { text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc; }
      50% { text-shadow: 0 0 15px #00ffcc, 0 0 30px #00ffcc, 0 0 50px #00ffcc; }
      100% { text-shadow: 0 0 10px #00ffcc, 0 0 20px #00ffcc, 0 0 30px #00ffcc; }
    }
    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 1rem;
      border-bottom: 1px solid #e5e7eb;
    }
    .cart-total {
      font-weight: 700;
      font-size: 1.2rem;
    }
    .pagination-container {
      display: flex;
      justify-content: center;
      align-items: center;
      space-x-1;
    }
    .pagination-btn:disabled {
      opacity: 0.5;
      cursor: not-allowed;
    }
  </style>
</head>
<body class="bg-white text-gray-800">

  <!-- Sticky Navbar -->
  <nav class="sticky-nav shadow-md py-4 px-6 flex justify-between items-center">
    <img src="sleek-logo.png" alt="SLEEK Logo" class="h-10">
    <div class="space-x-4 text-sm">
      <a href="#home" class="text-white hover:text-gray-200">Home</a>
      <a href="#about" class="text-white hover:text-gray-200">About</a>
      <a href="#services" class="text-white hover:text-gray-200">Services</a>
      <a href="#shop" class="text-white hover:text-gray-200">Shop</a>
      <a href="#cart" class="text-white hover:text-gray-200">Cart</a>
      <a href="#contact" class="text-white hover:text-gray-200">Contact</a>
    </div>
  </nav>

  <!-- Hero Section -->
  <section id="home" class="h-screen flex items-center justify-center relative overflow-hidden" data-aos="fade-up">
    <canvas id="starfield" class="absolute inset-0 z-0"></canvas>
    <div class="text-center px-4 z-10">
      <h2 class="text-4xl font-bold mb-4 text-white hero-title">
        <span class="text-2xl">WELCOME</span>
        <span class="text-5xl glow-text"> S.L.E.E.K</span>
      </h2>
      <p class="text-lg mb-6 text-gray-200">Style for Every Story: From Luxury to Everyday</p>
      <a href="#shop" class="bg-green-600 text-white px-6 py-3 rounded-full shop-now-btn hover:bg-green-500 transition">Shop Now</a>
    </div>
  </section>

  <!-- About Section -->
  <section id="about" class="py-16 px-6 bg-white" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-4">About Us</h3>
    <p>S.L.E.E.K offers stylish fashion and accessories for everyone, from luxury collections to everyday essentials. Shop trendy clothes, bags, jewelry, and more with seamless WhatsApp ordering.</p>
  </section>

  <!-- Services Section -->
  <section id="services" class="py-16 px-6 bg-green-50" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Our Services</h3>
    <ul class="list-disc list-inside space-y-2">
      <li>Personalized styling advice</li>
      <li>Wide range of sizes and styles</li>
      <li>Fast delivery via WhatsApp</li>
    </ul>
  </section>

  <!-- Shop Section -->
  <section id="shop" class="py-16 px-6 bg-white" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Shop Fashion</h3>
    <div class="mb-4">
      <select id="category-filter" class="p-2 border rounded">
        <option value="all">All Categories</option>
        <option value="Men’s">Men’s</option>
        <option value="Women’s">Women’s</option>
        <option value="Luxury">Luxury</option>
        <option value="Casual">Casual</option>
      </select>
    </div>
    <div id="product-grid" class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-4"></div>
    <div id="pagination" class="mt-6 text-center pagination-container" data-aos="fade-up"></div>
  </section>

  <!-- Cart Section -->
  <section id="cart" class="py-16 px-6 bg-green-50" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Your Cart</h3>
    <div id="cart-items" class="space-y-4"></div>
    <div class="mt-6 flex justify-between items-center">
      <p id="cart-total" class="cart-total">Total: ₦0.00</p>
      <div>
        <button id="clear-cart" class="bg-red-600 text-white px-4 py-2 rounded mr-4">Clear Cart</button>
        <a id="checkout-btn" href="#" class="bg-green-600 text-white px-4 py-2 rounded">Checkout via WhatsApp</a>
      </div>
    </div>
  </section>

  <!-- Contact Section -->
  <section id="contact" class="py-16 px-6 bg-white" data-aos="fade-up">
    <h3 class="text-2xl font-semibold mb-6">Contact Us</h3>
    <form action="https://formspree.io/f/xayraoqz" method="POST" class="space-y-4">
      <input type="text" name="name" placeholder="Your Name" class="w-full p-2 border rounded" required>
      <input type="email" name="email" placeholder="Your Email" class="w-full p-2 border rounded" required>
      <textarea name="message" placeholder="Your Message" class="w-full p-2 border rounded" required></textarea>
      <button type="submit" class="bg-green-600 text-white px-4 py-2 rounded">Send Message</button>
    </form>
    <div class="mt-4">
      <a href="https://wa.me/2348100123242" class="text-green-600 underline">Order via WhatsApp</a>
    </div>
  </section>

  <!-- Footer -->
  <footer id="footer" class="py-6 text-center bg-green-100">
    <p>© 2025 S.L.E.E.K. All rights reserved.</p>
  </footer>

  <!-- WhatsApp Floating Button -->
  <a href="https://wa.me/2348100123242" class="fixed bottom-4 right-4 bg-green-500 text-white p-3 rounded-full shadow-lg hover:bg-green-600 transition">
    💬
  </a>

  <!-- Search Bar -->
  <div class="fixed bottom-4 left-4 bg-white border rounded-full shadow-md flex items-center px-3 py-1 w-60">
    <input type="text" id="search-input" placeholder="Search products..." class="outline-none flex-1 p-1 text-sm">
  </div>

  <!-- Scripts -->
  <script src="https://unpkg.com/aos@2.3.4/dist/aos.js"></script>
  <script>
    AOS.init({
      duration: 800,
      delay: 100,
      once: true
    });

    // Starfield animation
    function initStarfield() {
      const canvas = document.getElementById('starfield');
      const ctx = canvas.getContext('2d');
      
      // Set canvas size
      canvas.width = window.innerWidth;
      canvas.height = window.innerHeight;

      // Handle window resize
      window.addEventListener('resize', () => {
        canvas.width = window.innerWidth;
        canvas.height = window.innerHeight;
      });

      // Star properties
      const stars = [];
      const numStars = 200;

      // Create stars
      for (let i = 0; i < numStars; i++) {
        stars.push({
          x: Math.random() * canvas.width,
          y: Math.random() * canvas.height,
          radius: Math.random() * 1.5,
          alpha: Math.random() * 0.5 + 0.5,
          speed: Math.random() * 0.5 + 0.2
        });
      }

      // Animation loop
      function animate() {
        ctx.clearRect(0, 0, canvas.width, canvas.height);
        stars.forEach(star => {
          ctx.beginPath();
          ctx.arc(star.x, star.y, star.radius, 0, Math.PI * 2);
          ctx.fillStyle = `rgba(255, 255, 255, ${star.alpha})`;
          ctx.fill();
          star.y += star.speed;
          if (star.y > canvas.height) {
            star.y = 0;
            star.x = Math.random() * canvas.width;
          }
        });
        requestAnimationFrame(animate);
      }
      animate();
    }

    // Initialize starfield when the page loads
    document.addEventListener('DOMContentLoaded', initStarfield);

    // Products array
    const products = [
      { name: "Elegant Dress Black", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Elegant%20Dress%20Black", img: "https://images.unsplash.com/photo-1566174053879-3151930a7d1a", price: "₦25000.00", category: "Women’s Luxury", description: "A stunning evening dress in soft silk." },
      { name: "Casual Sneakers White", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Casual%20Sneakers%20White", img: "https://images.unsplash.com/photo-1600185365483-26d7a4cc7519", price: "₦10000.00", category: "Casual", description: "Comfortable sneakers for daily wear." },
      { name: "Leather Jacket Black", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Leather%20Jacket%20Black", img: "https://images.unsplash.com/photo-1521223890158-f9f7c3d5d504", price: "₦35000.00", category: "Men’s", description: "Classic black leather jacket." },
      { name: "Gold Necklace Classic", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Gold%20Necklace%20Classic", img: "https://images.unsplash.com/photo-1608043152269-423dbba4e7e1", price: "₦45000.00", category: "Luxury", description: "Elegant 18k gold necklace." },
      { name: "Summer Skirt Floral", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Summer%20Skirt%20Floral", img: "https://images.unsplash.com/photo-1590102426319-8a1b79966b07", price: "₦8000.00", category: "Women’s", description: "Light and breezy floral skirt." },
      { name: "Denim Jeans Blue", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Denim%20Jeans%20Blue", img: "https://images.unsplash.com/photo-1542272604-787c3835535d", price: "₦12000.00", category: "Casual", description: "Slim-fit blue denim jeans." },
      { name: "Designer Sunglasses Black", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Designer%20Sunglasses%20Black", img: "https://images.unsplash.com/photo-1577803645773-f96470509666", price: "₦20000.00", category: "Luxury", description: "Trendy polarized sunglasses." },
      { name: "Formal Shirt White", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Formal%20Shirt%20White", img: "https://images.unsplash.com/photo-1603252109303-1751441dd551", price: "₦15000.00", category: "Men’s", description: "Crisp white dress shirt." },
      { name: "Tote Bag Leather", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Tote%20Bag%20Leather", img: "https://images.unsplash.com/photo-1584917869284-3c4f71a6c7c4", price: "₦18000.00", category: "Women’s", description: "Spacious leather tote bag." },
      { name: "Sports Cap Black", link: "https://wa.me/2348100123242?text=Hi%2C%20I'm%20interested%20in%20Sports%20Cap%20Black", img: "https://images.unsplash.com/photo-1573649471415-1df0b9b4d9c3", price: "₦3500.00", category: "Casual", description: "Breathable cotton sports cap." }
    ].flatMap((product, i) => Array(16).fill().map((_, j) => ({
      ...product,
      name: `${product.name} ${['Black', 'White', 'Blue', 'Red', 'Green', 'Grey', 'Pink', 'Navy', 'Beige', 'Brown', 'Silver', 'Gold', 'Purple', 'Orange', 'Yellow', 'Teal'][j]}`,
      price: `₦${(parseFloat(product.price.replace('₦', '')) + j * 1000).toFixed(2)}`,
      link: product.link.replace(product.name, `${product.name} ${['Black', 'White', 'Blue', 'Red', 'Green', 'Grey', 'Pink', 'Navy', 'Beige', 'Brown', 'Silver', 'Gold', 'Purple', 'Orange', 'Yellow', 'Teal'][j]}`)
    })));

    const productsPerPage = 8;
    let currentPage = 1;

    document.getElementById('search-input').addEventListener('input', function(e) {
      const searchValue = e.target.value.toLowerCase();
      const items = document.querySelectorAll('#product-grid > div');
      items.forEach(item => {
        const text = item.textContent.toLowerCase();
        item.style.display = text.includes(searchValue) ? 'block' : 'none';
      });
    });

    function displayProducts(page, category = 'all') {
      const grid = document.getElementById('product-grid');
      grid.innerHTML = "";
      const filteredProducts = category === 'all' ? products : products.filter(p => p.category === category);
      const start = (page - 1) * productsPerPage;
      const end = start + productsPerPage;
      const paginatedItems = filteredProducts.slice(start, end);

      paginatedItems.forEach(p => {
        const div = document.createElement('div');
        div.className = 'p-4 border rounded shadow hover:shadow-lg product-card';
        div.setAttribute('data-aos', 'slide-up');
        const formattedPrice = parseFloat(p.price.replace('₦', '')).toLocaleString('en-NG', { style: 'currency', currency: 'NGN' });
        div.innerHTML = `<img src="${p.img}" alt="${p.name}" class="h-48 w-full object-cover mb-2 rounded">
                         <h4 class="font-semibold mb-1 text-center">${p.name}</h4>
                         <p class="text-sm text-gray-600 text-center">${formattedPrice}</p>
                         <p class="text-xs text-gray-500 text-center">${p.description}</p>
                         <div class="flex justify-center space-x-2 mt-2">
                           <a href="${p.link}" target="_blank" class="text-green-600 underline">Order via WhatsApp</a>
                           <button class="add-to-cart bg-green-600 text-white px-2 py-1 rounded text-sm" data-name="${p.name}" data-price="${p.price}">Add to Cart</button>
                         </div>`;
        grid.appendChild(div);
      });

      document.querySelectorAll('.add-to-cart').forEach(button => {
        button.addEventListener('click', function() {
          const name = this.getAttribute('data-name');
          const price = parseFloat(this.getAttribute('data-price').replace('₦', ''));
          addToCart({ name, price });
        });
      });

      renderPagination(filteredProducts.length);
    }

    function renderPagination(totalItems) {
      const pagination = document.getElementById('pagination');
      pagination.innerHTML = "";
      const pageCount = Math.ceil(totalItems / productsPerPage);
      const maxPagesToShow = 3;

      const prevBtn = document.createElement('button');
      prevBtn.textContent = 'Prev';
      prevBtn.className = 'mx-1 px-3 py-1 rounded-full border pagination-btn ' + (currentPage === 1 ? 'bg-gray-200' : 'bg-white');
      prevBtn.disabled = currentPage === 1;
      prevBtn.setAttribute('aria-label', 'Previous page');
      prevBtn.onclick = () => {
        if (currentPage > 1) {
          currentPage--;
          displayProducts(currentPage, document.getElementById('category-filter').value);
        }
      };
      pagination.appendChild(prevBtn);

      if (currentPage > 2) {
        const firstBtn = document.createElement('button');
        firstBtn.textContent = '1';
        firstBtn.className = 'mx-1 px-3 py-1 rounded-full border pagination-btn bg-white';
        firstBtn.setAttribute('aria-label', 'Go to page 1');
        firstBtn.onclick = () => {
          currentPage = 1;
          displayProducts(currentPage, document.getElementById('category-filter').value);
        };
        pagination.appendChild(firstBtn);
      }

      if (currentPage > 3) {
        const ellipsis = document.createElement('span');
        ellipsis.textContent = '...';
        ellipsis.className = 'mx-1 px-3 py-1';
        pagination.appendChild(ellipsis);
      }

      const startPage = Math.max(1, currentPage - 1);
      const endPage = Math.min(pageCount, startPage + maxPagesToShow - 1);
      for (let i = startPage; i <= endPage; i++) {
        const btn = document.createElement('button');
        btn.textContent = i;
        btn.className = 'mx-1 px-3 py-1 rounded-full border pagination-btn ' + (i === currentPage ? 'bg-green-600 text-white' : 'bg-white');
        btn.setAttribute('aria-label', `Go to page ${i}`);
        btn.onclick = () => {
          currentPage = i;
          displayProducts(currentPage, document.getElementById('category-filter').value);
        };
        pagination.appendChild(btn);
      }

      if (currentPage < pageCount - 2) {
        const ellipsis = document.createElement('span');
        ellipsis.textContent = '...';
        ellipsis.className = 'mx-1 px-3 py-1';
        pagination.appendChild(ellipsis);
      }

      if (currentPage < pageCount - 1) {
        const lastBtn = document.createElement('button');
        lastBtn.textContent = pageCount;
        lastBtn.className = 'mx-1 px-3 py-1 rounded-full border pagination-btn bg-white';
        lastBtn.setAttribute('aria-label', `Go to page ${pageCount}`);
        lastBtn.onclick = () => {
          currentPage = pageCount;
          displayProducts(currentPage, document.getElementById('category-filter').value);
        };
        pagination.appendChild(lastBtn);
      }

      const nextBtn = document.createElement('button');
      nextBtn.textContent = 'Next';
      nextBtn.className = 'mx-1 px-3 py-1 rounded-full border pagination-btn ' + (currentPage === pageCount ? 'bg-gray-200' : 'bg-white');
      nextBtn.disabled = currentPage === pageCount;
      nextBtn.setAttribute('aria-label', 'Next page');
      nextBtn.onclick = () => {
        if (currentPage < pageCount) {
          currentPage++;
          displayProducts(currentPage, document.getElementById('category-filter').value);
        }
      };
      pagination.appendChild(nextBtn);
    }

    document.getElementById('category-filter').addEventListener('change', function() {
      currentPage = 1;
      displayProducts(currentPage, this.value);
    });

    function addToCart(product) {
      const cart = JSON.parse(localStorage.getItem('cart') || '[]');
      cart.push(product);
      localStorage.setItem('cart', JSON.stringify(cart));
      loadCart();
    }

    function removeFromCart(index) {
      const cart = JSON.parse(localStorage.getItem('cart') || '[]');
      cart.splice(index, 1);
      localStorage.setItem('cart', JSON.stringify(cart));
      loadCart();
    }

    function loadCart() {
      const container = document.getElementById('cart-items');
      const totalElement = document.getElementById('cart-total');
      container.innerHTML = "";
      const cart = JSON.parse(localStorage.getItem('cart') || '[]');
      
      if (cart.length === 0) {
        container.innerHTML = '<p class="text-center text-gray-600">Your cart is empty.</p>';
        totalElement.textContent = 'Total: ₦0.00';
        document.getElementById('checkout-btn').setAttribute('href', '#');
        return;
      }

      let total = 0;
      cart.forEach((item, index) => {
        total += item.price;
        const div = document.createElement('div');
        div.className = 'cart-item';
        div.setAttribute('data-aos', 'slide-up');
        const formattedPrice = item.price.toLocaleString('en-NG', { style: 'currency', currency: 'NGN' });
        div.innerHTML = `<span>${item.name} - ${formattedPrice}</span>
                         <button class="remove-from-cart bg-red-600 text-white px-2 py-1 rounded text-sm" data-index="${index}">Remove</button>`;
        container.appendChild(div);
      });

      totalElement.textContent = `Total: ${total.toLocaleString('en-NG', { style: 'currency', currency: 'NGN' })}`;
      
      const checkoutMessage = encodeURIComponent(`Hi, I'd like to order:\n${cart.map(item => `- ${item.name} (${item.price.toLocaleString('en-NG', { style: 'currency', currency: 'NGN' })})`).join('\n')}\nTotal: ${total.toLocaleString('en-NG', { style: 'currency', currency: 'NGN' })}`);
      document.getElementById('checkout-btn').setAttribute('href', `https://wa.me/2348100123242?text=${checkoutMessage}`);

      document.querySelectorAll('.remove-from-cart').forEach(button => {
        button.addEventListener('click', function() {
          const index = parseInt(this.getAttribute('data-index'));
          removeFromCart(index);
        });
      });
    }

    // Initialize products and cart on page load
    document.addEventListener('DOMContentLoaded', () => {
      displayProducts(currentPage);
      loadCart();
      document.getElementById('clear-cart').addEventListener('click', () => {
        localStorage.setItem('cart', '[]');
        loadCart();
      });
    });
  </script>
</body>
</html>
