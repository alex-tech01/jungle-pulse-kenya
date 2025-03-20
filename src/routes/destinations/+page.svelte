<script>
    let destinations = [
        {
            name: "Maasai Mara",
            image: "/maasai-mara.jpg",
            description:
                "The ultimate safari experience with the Great Migration.",
        },
        {
            name: "Amboseli",
            image: "/amboseli.jpg",
            description:
                "Famous for its large elephant herds and Kilimanjaro views.",
        },
        {
            name: "Tsavo",
            image: "/tsavo.jpg",
            description:
                "One of the largest national parks with diverse wildlife.",
        },
    ];
</script>

<div class="destinations">
    <h1>Safari Destinations</h1>
    <p>Discover the best wildlife destinations in Kenya.</p>

    <div class="grid">
        {#each destinations as destination}
            <div class="card">
                <img src={destination.image} alt={destination.name} />
                <h2>{destination.name}</h2>
                <p>{destination.description}</p>
            </div>
        {/each}
    </div>
</div>

<style>
    .destinations {
        text-align: center;
        padding: 20px;
    }

    .grid {
        display: flex;
        justify-content: center;
        gap: 20px;
    }

    .card {
        background: white;
        border-radius: 8px;
        overflow: hidden;
        box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
        width: 300px;
    }

    .card img {
        width: 100%;
        height: 200px;
        object-fit: cover;
    }

    .card h2 {
        margin: 10px 0;
    }
</style>
