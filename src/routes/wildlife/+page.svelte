<script>
    const animals = [
        {
            name: "African Elephant",
            image: "/elephant.jpg",
            description:
                "The largest land animal, found in Amboseli and Tsavo parks.",
        },
        {
            name: "Lion",
            image: "/lion.jpg", // ✅ Make sure lion.jpg is in the static folder
            description:
                "The king of the jungle, often spotted in Maasai Mara and Nairobi National Park.",
        },
        {
            name: "Giraffe",
            image: "/giraffe.jpg",
            description:
                "The world's tallest animal, gracefully roaming across Kenya’s savannahs.",
        },
    ];
</script>

<section class="wildlife-section">
    <h1 class="title">Explore Kenya’s Iconic Wildlife</h1>

    <div class="cards-container">
        {#each animals as animal}
            <div class="card">
                <img src={animal.image} alt={animal.name} />
                <h2>{animal.name}</h2>
                <p>{animal.description}</p>
            </div>
        {/each}
    </div>
</section>

<style>
    .wildlife-section {
        padding: 100px 40px 60px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .title {
        text-align: center;
        font-size: 2.8rem;
        font-weight: bold;
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
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        text-align: center;
        transition: transform 0.2s;
    }

    .card:hover {
        transform: scale(1.02);
    }

    .card img {
        width: 100%;
        height: 220px;
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
