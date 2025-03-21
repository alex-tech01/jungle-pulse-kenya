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
  <div class="menu-toggle" on:click={toggleMenu}>☰</div>
</nav>

<style>
  .navbar {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background: #222;
    padding: 15px 30px;
    color: white;
    position: fixed;
    width: 100vw; /* Ensures full width */
    top: 0;
    left: 0;
    z-index: 1000;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .nav-links {
    list-style: none;
    display: flex;
    gap: 20px;
    margin: 0; /* Fixes spacing issue */
    padding: 0;
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
</style>
