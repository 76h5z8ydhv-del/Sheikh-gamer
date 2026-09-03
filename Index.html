<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>NexusGames | Digital Game Store</title>
  <style>
    :root {
      --bg-dark: #0b0e14;
      --card-bg: #151a23;
      --accent: #00ff88;
      --accent-hover: #00cc6a;
      --text: #ffffff;
      --text-muted: #94a3b8;
      --danger: #ef4444;
    }

    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif;
    }

    body {
      background-color: var(--bg-dark);
      color: var(--text);
      min-height: 100vh;
      display: flex;
      flex-direction: column;
    }

    header {
      background-color: var(--card-bg);
      padding: 1rem 2rem;
      display: flex;
      justify-content: space-between;
      align-items: center;
      border-bottom: 1px solid #242d3d;
      position: sticky;
      top: 0;
      z-index: 10;
    }

    .logo {
      font-size: 1.5rem;
      font-weight: 800;
      letter-spacing: 1px;
      color: var(--accent);
    }

    .search-box {
      padding: 0.6rem 1rem;
      border-radius: 6px;
      border: 1px solid #334155;
      background: #0b0e14;
      color: #fff;
      width: 260px;
    }

    .cart-btn {
      background: #1e293b;
      border: 1px solid #334155;
      color: #fff;
      padding: 0.6rem 1.2rem;
      border-radius: 6px;
      cursor: pointer;
      font-weight: 600;
    }

    .container {
      max-width: 1200px;
      margin: 2rem auto;
      padding: 0 1rem;
      width: 100%;
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(auto-fill, minmax(260px, 1fr));
      gap: 1.5rem;
    }

    .card {
      background-color: var(--card-bg);
      border-radius: 8px;
      overflow: hidden;
      border: 1px solid #242d3d;
      display: flex;
      flex-direction: column;
    }

    .card-img {
      height: 150px;
      background: #1e293b;
      display: flex;
      align-items: center;
      justify-content: center;
      font-size: 2.5rem;
    }

    .card-body {
      padding: 1.2rem;
      display: flex;
      flex-direction: column;
      flex-grow: 1;
    }

    .card-title {
      font-size: 1.1rem;
      margin-bottom: 0.5rem;
    }

    .platform-badge {
      display: inline-block;
      font-size: 0.75rem;
      text-transform: uppercase;
      color: var(--accent);
      margin-bottom: 0.8rem;
    }

    .card-footer {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: auto;
      padding-top: 1rem;
    }

    .price {
      font-size: 1.25rem;
      font-weight: 700;
    }

    .btn {
      background-color: var(--accent);
      color: #000;
      border: none;
      padding: 0.5rem 1rem;
      border-radius: 4px;
      cursor: pointer;
      font-weight: 600;
      transition: background 0.2s;
    }

    .btn:hover {
      background-color: var(--accent-hover);
    }

    /* Modal / Drawer */
    .modal {
      display: none;
      position: fixed;
      inset: 0;
      background: rgba(0, 0, 0, 0.7);
      backdrop-filter: blur(4px);
      align-items: center;
      justify-content: center;
      z-index: 100;
    }

    .modal-box {
      background: var(--card-bg);
      padding: 2rem;
      border-radius: 8px;
      max-width: 500px;
      width: 90%;
      max-height: 85vh;
      overflow-y: auto;
      border: 1px solid #334155;
    }

    .cart-item {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 0.75rem 0;
      border-bottom: 1px solid #242d3d;
    }

    .key-box {
      background: #0b0e14;
      padding: 0.75rem;
      border: 1px dashed var(--accent);
      color: var(--accent);
      font-family: monospace;
      margin-top: 0.5rem;
      word-break: break-all;
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">NEXUS//STORE</div>
    <input type="text" id="searchInput" class="search-box" placeholder="Search games..." oninput="filterGames()" />
    <button class="cart-btn" onclick="openCart()">Cart (<span id="cartCount">0</span>)</button>
  </header>

  <main class="container">
    <div class="grid" id="gamesGrid"></div>
  </main>

  <!-- Cart & Checkout Modal -->
  <div class="modal" id="cartModal">
    <div class="modal-box">
      <h2>Your Cart</h2>
      <div id="cartItemsList" style="margin: 1.5rem 0;"></div>
      <div style="display: flex; justify-content: space-between; margin-bottom: 1.5rem; font-weight: bold;">
        <span>Total:</span>
        <span id="cartTotal">$0.00</span>
      </div>
      <button class="btn" style="width: 100%; margin-bottom: 0.5rem;" onclick="processCheckout()">Checkout & Get Keys</button>
      <button class="btn" style="width: 100%; background: #334155; color: #fff;" onclick="closeCart()">Close</button>
    </div>
  </div>

  <!-- Key Delivery Modal -->
  <div class="modal" id="keyModal">
    <div class="modal-box">
      <h2 style="color: var(--accent);">Purchase Successful!</h2>
      <p style="color: var(--text-muted); margin: 0.5rem 0 1rem 0;">Redeem these activation codes in your platform launcher:</p>
      <div id="keysContainer"></div>
      <button class="btn" style="width: 100%; margin-top: 1.5rem;" onclick="closeKeys()">Done</button>
    </div>
  </div>

  <script>
    const inventory = [
      { id: 1, title: "Cyber Siege 2088", platform: "Steam", price: 39.99, icon: "👾" },
      { id: 2, title: "Mythic Relic RPG", platform: "Epic Games", price: 29.99, icon: "⚔️" },
      { id: 3, title: "Speed Drift X", platform: "Steam", price: 19.99, icon: "🏎️" },
      { id: 4, title: "Space Marauder", platform: "GOG", price: 14.99, icon: "🚀" },
      { id: 5, title: "Dungeon Survivor", platform: "Steam", price: 9.99, icon: "🛡️" }
    ];

    let cart = [];

    function renderGames(items) {
      const grid = document.getElementById("gamesGrid");
      grid.innerHTML = items.map(game => `
        <div class="card">
          <div class="card-img">${game.icon}</div>
          <div class="card-body">
            <span class="platform-badge">${game.platform} Key</span>
            <h3 class="card-title">${game.title}</h3>
            <div class="card-footer">
              <span class="price">$${game.price.toFixed(2)}</span>
              <button class="btn" onclick="addToCart(${game.id})">Add</button>
            </div>
          </div>
        </div>
      `).join("");
    }

    function filterGames() {
      const q = document.getElementById("searchInput").value.toLowerCase();
      const filtered = inventory.filter(g => g.title.toLowerCase().includes(q) || g.platform.toLowerCase().includes(q));
      renderGames(filtered);
    }

    function addToCart(id) {
      const item = inventory.find(g => g.id === id);
      cart.push(item);
      updateCartUI();
    }

    function updateCartUI() {
      document.getElementById("cartCount").innerText = cart.length;
      const list = document.getElementById("cartItemsList");
      if (cart.length === 0) {
        list.innerHTML = "<p style='color: var(--text-muted);'>Your cart is empty.</p>";
      } else {
        list.innerHTML = cart.map((item, idx) => `
          <div class="cart-item">
            <div>
              <strong>${item.title}</strong><br>
              <small style="color: var(--text-muted);">${item.platform}</small>
            </div>
            <div>
              <span>$${item.price.toFixed(2)}</span>
              <button onclick="removeFromCart(${idx})" style="background: none; border: none; color: var(--danger); margin-left: 10px; cursor: pointer;">✕</button>
            </div>
          </div>
        `).join("");
      }
      const total = cart.reduce((sum, item) => sum + item.price, 0);
      document.getElementById("cartTotal").innerText = `$${total.toFixed(2)}`;
    }

    function removeFromCart(index) {
      cart.splice(index, 1);
      updateCartUI();
    }

    function openCart() { document.getElementById("cartModal").style.display = "flex"; }
    function closeCart() { document.getElementById("cartModal").style.display = "none"; }

    function generateLicenseKey() {
      const seg = () => Math.random().toString(36).substring(2, 7).toUpperCase();
      return `${seg()}-${seg()}-${seg()}`;
    }

    function processCheckout() {
      if (cart.length === 0) return alert("Your cart is empty!");
      const keysContainer = document.getElementById("keysContainer");
      keysContainer.innerHTML = cart.map(item => `
        <div style="margin-bottom: 1rem;">
          <strong style="font-size: 0.9rem;">${item.title} (${item.platform})</strong>
          <div class="key-box">${generateLicenseKey()}</div>
        </div>
      `).join("");

      cart = [];
      updateCartUI();
      closeCart();
      document.getElementById("keyModal").style.display = "flex";
    }

    function closeKeys() { document.getElementById("keyModal").style.display = "none"; }

    renderGames(inventory);
  </script>
</body>
</html>
