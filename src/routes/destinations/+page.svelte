<script>
    const destinations = [
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
        {
            name: "Lake Nakuru",
            image: "/lake-nakuru.jpg",
            description: "Home to flamingos, rhinos, and beautiful lake views.",
        },
        {
            name: "Samburu",
            image: "/samburu.jpg",
            description:
                "Untamed beauty with rare wildlife like Grevy’s zebra and reticulated giraffes.",
        },
        {
            name: "Nairobi National Park",
            image: "/nairobi-park.jpg",
            description:
                "A safari within the city with lions, rhinos, and skyscrapers in the background.",
        },
        {
            name: "Mount Kenya",
            image: "/mount-kenya.jpg",
            description:
                "Explore Africa's second-highest peak, glaciers, and alpine wilderness.",
        },
    ];
</script>

<section class="destination-page">
    <h1 class="title">Discover the Best Wildlife Destinations in Kenya</h1>

    <div class="cards-container">
        {#each destinations as dest}
            <div class="card">
                <img src={dest.image} alt={dest.name} />
                <h2>{dest.name}</h2>
                <p>{dest.description}</p>
            </div>
        {/each}
    </div>
</section>

<style>
    .destination-page {
        padding: 100px 40px 60px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .title {
        text-align: center;
        font-size: 2.5rem;
        margin-bottom: 40px;
        color: #222;
    }

    .cards-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
    }

    .card {
        background: white;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        transition: transform 0.2s;
        text-align: center;
    }

    .card:hover {
        transform: scale(1.03);
    }

    .card img {
        width: 100%;
        height: 200px;
        object-fit: cover;
    }

    .card h2 {
        font-size: 1.5rem;
        margin: 15px 0 10px;
        color: #000;
    }

    .card p {
        padding: 0 15px 20px;
        color: #444;
    }

    @media (max-width: 768px) {
        .title {
            font-size: 2rem;
        }

        .card img {
            height: 160px;
        }
    }
</style>
