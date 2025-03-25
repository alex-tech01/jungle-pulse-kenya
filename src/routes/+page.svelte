<script>
    // No need for any script for now
</script>

<!-- Hero Section -->
<section class="hero">
    <div class="overlay">
        <h1>Jungle Pulse Kenya</h1>
        <p>Experience the Wild Beauty of Kenya</p>
        <a href="/destinations" class="cta-button">Explore Destinations</a>
    </div>
</section>

<!-- Styles -->
<style>
    .hero {
        position: relative;
        width: 100vw;
        height: calc(100vh - 60px); /* adjusts for navbar height */
        background: url("/wildlife-hero.jpg") no-repeat center center/cover;
        display: flex;
        align-items: center;
        justify-content: center;
        padding: 0;
        margin: 0;
        overflow: hidden;
    }

    .overlay {
        background-color: rgba(0, 0, 0, 0.6); /* dark overlay for contrast */
        padding: 30px 40px;
        border-radius: 10px;
        text-align: center;
        color: #fff;
    }

    h1 {
        font-size: 3rem;
        margin-bottom: 10px;
        color: #ffd700; /* Gold for standout title */
    }

    p {
        font-size: 1.3rem;
        margin-bottom: 20px;
        color: #ffffff;
    }

    .cta-button {
        background-color: #ffa500; /* Bright safari orange */
        color: white;
        padding: 12px 24px;
        border-radius: 8px;
        font-size: 1.1rem;
        font-weight: bold;
        text-decoration: none;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
        transition:
            background 0.3s ease,
            transform 0.2s ease;
        display: inline-block;
    }

    .cta-button:hover {
        background-color: #e67600;
        transform: scale(1.05);
        color: white;
    }

    html,
    body {
        margin: 0;
        padding: 0;
        overflow-x: hidden;
    }
</style>
