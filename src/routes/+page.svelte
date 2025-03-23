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
        position: relative;
        width: 100vw;
        height: calc(100vh - 60px); /* Adjust height to account for navbar */
        background: url("/wildlife-hero.jpg") no-repeat center center/cover;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        color: white;
        margin: 0;
        padding: 0;
        overflow: hidden;
    }

    html,
    body {
        margin: 0;
        padding: 0;
        overflow-x: hidden;
    }
</style>
