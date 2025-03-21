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
        height: 100vh;
        background: url("/wildlife-hero.jpg") no-repeat center center/cover;
        display: flex;
        align-items: center;
        justify-content: center;
        text-align: center;
        color: white;
        margin: 0;
        padding: 0;
    }

    .overlay {
        background: rgba(
            0,
            0,
            0,
            0.6
        ); /* Darker overlay for better text contrast */
        padding: 20px 30px;
        border-radius: 10px;
        max-width: 80%;
        text-align: center;
    }

    h1 {
        font-size: 3.5rem;
        font-weight: bold;
        color: #ffd700; /* Bright gold color for impact */
        text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.7); /* Adds depth */
    }

    p {
        font-size: 1.5rem;
        color: #fff; /* White for clarity */
        text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
    }

    .cta-button {
        background-color: #ffa500; /* Brighter Orange */
        padding: 15px 25px;
        border-radius: 8px;
        color: #222; /* Darker text for better contrast */
        font-size: 1.3rem;
        font-weight: bold;
        text-decoration: none;
        transition: 0.3s;
        box-shadow: 0 5px 10px rgba(255, 165, 0, 0.5); /* Adds a glow effect */
    }

    .cta-button:hover {
        background-color: #ffcc00;
        box-shadow: 0 5px 15px rgba(255, 204, 0, 0.8); /* More glow on hover */
    }
</style>
