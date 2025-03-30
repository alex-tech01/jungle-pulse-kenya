<script>
    // We're not letting this lion win
</script>

<main>
    <img src="/images/home-hero.jpg" alt="Jungle Pulse Kenya" class="hero-bg" />

    <div class="hero-content">
        <h1 style="font-size: 2.5rem; font-weight: bold;">
            Jungle Pulse Kenya
        </h1>
        <p style="font-size: 1.25rem; margin-top: 0.5rem;">
            Experience the Wild Beauty of Kenya
        </p>
        <a href="/destinations" class="hero-button">Explore Destinations</a>
    </div>
</main>

<style>

    main {
        min-height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        position: relative;
        overflow: hidden;
    }

    .hero-bg {
        position: absolute;
        inset: 0;
        width: 100%;
        height: 100%;
        object-fit: cover;
        z-index: 1;
    }

    .hero-content {
        position: relative;
        z-index: 2;
        color: white;
        text-align: center;
        padding: 2rem;
        background: rgba(0, 0, 0, 0.5);
        border-radius: 1rem;
        max-width: 90%;
    }

    .hero-button {
        margin-top: 1.5rem;
        background-color: #facc15;
        color: black;
        padding: 0.75rem 1.5rem;
        border-radius: 0.5rem;
        text-decoration: none;
        font-weight: bold;
        display: inline-block;
    }

    .hero-button:hover {
        background-color: #fbbf24;
    }
</style>
