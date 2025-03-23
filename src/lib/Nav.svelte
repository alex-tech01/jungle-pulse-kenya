<script>
  import { onMount } from "svelte";

  let isMenuOpen = false;

  const toggleMenu = () => {
    isMenuOpen = !isMenuOpen;
  };

  const closeMenu = () => {
    isMenuOpen = false;
  };

  onMount(() => {
    document.addEventListener("click", (e) => {
      if (isMenuOpen && !e.target.closest(".navbar")) {
        closeMenu();
      }
    });
  });
</script>

<nav class="navbar">
  <div class="logo">
    <a href="/">Jungle Pulse Kenya</a>
  </div>

  <!-- Hamburger Icon -->
  <div class="menu-toggle" on:click={toggleMenu}>&#9776;</div>

  <!-- Nav Links -->
  <ul class:open={isMenuOpen} class="nav-links">
    <li><a href="/">Home</a></li>
    <li><a href="/destinations">Destinations</a></li>
    <li><a href="/wildlife">Wildlife</a></li>
    <li><a href="/blog">Blog</a></li>
    <li><a href="/contact">Contact</a></li>
  </ul>
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
    width: 100%;
    top: 0;
    left: 0;
    z-index: 1000;
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
    gap: 25px;
  }

  .nav-links li a {
    color: white;
    text-decoration: none;
    font-weight: 500;
    padding: 8px 12px;
    border-radius: 5px;
    transition: 0.3s;
  }

  .nav-links li a:hover {
    background: #ff9800;
    color: black;
  }

  .menu-toggle {
    display: none;
    font-size: 2rem;
    cursor: pointer;
    color: white;
  }

  /* Mobile/Tablet view */
  @media (max-width: 768px) {
    .menu-toggle {
      display: block;
    }

    .nav-links {
      display: none;
      position: absolute;
      top: 60px;
      right: 30px;
      background: rgba(0, 0, 0, 0.95);
      flex-direction: column;
      padding: 20px;
      border-radius: 8px;
      width: 200px;
    }

    .nav-links.open {
      display: flex;
    }

    .nav-links li {
      margin: 10px 0;
      text-align: right;
    }
  }
</style>
