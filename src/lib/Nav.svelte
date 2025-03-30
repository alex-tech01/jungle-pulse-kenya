<script>
  let menuOpen = false;

  function toggleMenu() {
    menuOpen = !menuOpen;
  }
</script>

<nav class="nav">
  <a href="/" class="logo">Jungle Pulse Kenya</a>

  <button
    on:click={toggleMenu}
    aria-label="Toggle menu"
    aria-expanded={menuOpen}
    class="menu-toggle"
  >
    ☰
  </button>

  <div class={`nav-links ${menuOpen ? "open" : ""}`}>
    <a href="/destinations">Destinations</a>
    <a href="/wildlife">Wildlife</a>
    <a href="/blog">Blog</a>
    <a href="/contact">Contact</a>
  </div>
</nav>

<style>
  .nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: #0f4d1a;
    padding: 1rem 2rem;
    color: white;
  }

  .logo {
    font-size: 1.5rem;
    font-weight: bold;
    text-decoration: none;
    color: white;
    transition: color 0.3s ease;
  }

  .logo:hover {
    color: #ffd700; /* gold-ish on hover */
  }

  .menu-toggle {
    display: none;
    background: none;
    font-size: 2rem;
    color: white;
    border: none;
    cursor: pointer;
    transition: transform 0.3s ease;
  }

  .menu-toggle:hover {
    transform: rotate(90deg);
  }

  .nav-links {
    display: flex;
    gap: 1rem;
    transition: all 0.4s ease;
  }

  .nav-links a {
    color: white;
    text-decoration: none;
    position: relative;
    padding: 0.3rem 0.5rem;
    transition: color 0.3s ease;
  }

  .nav-links a::after {
    content: "";
    position: absolute;
    left: 0;
    bottom: -2px;
    width: 0;
    height: 2px;
    background-color: #ffd700;
    transition: width 0.3s ease;
  }

  .nav-links a:hover::after {
    width: 100%;
  }

  .nav-links a:hover {
    color: #ffd700;
  }

  @media (max-width: 768px) {
    .menu-toggle {
      display: block;
    }

    .nav-links {
      flex-direction: column;
      margin-top: 1rem;
      overflow: hidden;
      max-height: 0;
      opacity: 0;
      pointer-events: none;
    }

    .nav-links.open {
      max-height: 500px;
      opacity: 1;
      pointer-events: auto;
    }
    nav {
      width: 100%;
      max-width: 100vw;
      overflow-x: hidden;
      box-sizing: border-box;
    }
  }
</style>
