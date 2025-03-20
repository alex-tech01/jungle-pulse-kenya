<script>
    let tagline = "Experience the Wild Beauty of Kenya";
</script>

<div class="hero">
    <div class="overlay">
        <h1>Jungle Pulse Kenya</h1>
        <p>{tagline}</p>
        <a href="/destinations" class="cta-button">Explore Destinations</a>
    </div>
</div>

<style>
    .hero {
        width: 100%;
        height: 90vh;
        background: url("/wildlife-hero.jpg") no-repeat center center/cover;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        color: white;
    }

    .overlay {
        background: rgba(0, 0, 0, 0.5);
        padding: 20px;
        border-radius: 10px;
    }

    h1 {
        font-size: 3rem;
        margin: 10px 0;
    }

    .cta-button {
        background-color: #ff9800;
        padding: 12px 24px;
        border-radius: 5px;
        color: white;
        font-size: 1.2rem;
        text-decoration: none;
        transition: 0.3s;
    }

    .cta-button:hover {
        background-color: #e68900;
    }
</style>
