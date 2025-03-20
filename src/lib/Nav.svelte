<script>
    import { onMount } from "svelte";
    let isMenuOpen = false;
  
    // Close menu when clicking outside (on mobile)
    function toggleMenu() {
      isMenuOpen = !isMenuOpen;
    }
  
    onMount(() => {
      // Close menu when clicking outside (on mobile)
      document.addEventListener("click", (event) => {
        if (isMenuOpen && !event.target.closest(".navbar")) {
          isMenuOpen = false;
        }
      });
    });
  </script>
  
  <nav class="navbar">
    <div class="logo">
      <a href="/">Jungle Pulse Kenya</a>
    </div>
  
    <ul class="nav-links {isMenuOpen ? 'open' : ''}">
      <li><a href="/" class="nav-link">Home</a></li>
      <li><a href="/destinations" class="nav-link">Destinations</a></li>
      <li><a href="/wildlife" class="nav-link">Wildlife</a></li>
      <li><a href="/blog" class="nav-link">Blog</a></li>
      <li><a href="/contact" class="nav-link">Contact</a></li>
    </ul>
  
    <!-- Mobile Menu Toggle -->
    <div class="menu-toggle" on:click={toggleMenu}>
      ☰
    </div>
  </nav>
  
  <style>
    /* General Navigation Styling */
    .navbar {
      display: flex;
      justify-content: space-between;
      align-items: center;
      background: #222;
      padding: 15px 30px;
      color: white;
      position: fixed;
      width: 100%;
      top: 0;
      left: 0;
      z-index: 1000;
      box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    }
  
    .logo a {
      color: white;
      font-size: 1.5rem;
      font-weight: bold;
      text-decoration: none;
    }
  
    .nav-links {
      list-style: none;
      display: flex;
      gap: 20px;
    }
  
    .nav-links li {
      display: inline;
    }
  
    .nav-link {
      color: white;
      text-decoration: none;
      padding: 8px 12px;
      border-radius: 5px;
      transition: 0.3s;
    }
  
    .nav-link:hover {
      background: #ff9800;
      color: black;
    }
  
    /* Mobile Menu */
    .menu-toggle {
      display: none;
      font-size: 1.8rem;
      cursor: pointer;
    }
  
    /* Responsive Navigation */
    @media (max-width: 768px) {
      .menu-toggle {
        display: block;
      }
  
      .nav-links {
        display: none;
        position: absolute;
        top: 60px;
        right: 0;
        background: rgba(34, 34, 34, 0.95);
        flex-direction: column;
        width: 200px;
        padding: 15px;
        border-radius: 5px;
      }
  
      .nav-links.open {
        display: flex;
      }
  
      .nav-links li {
        margin: 10px 0;
        text-align: center;
      }
    }
  </style>
  