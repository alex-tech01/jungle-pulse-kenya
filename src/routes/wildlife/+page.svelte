<script>
    import { fade } from "svelte/transition";

    const wildlife = [
        {
            name: "African Elephant",
            image: "/elephant.jpg",
            description:
                "The largest land animal, found in Amboseli and Tsavo parks.",
        },
        {
            name: "Lion",
            image: "/lion.jpg",
            description:
                "The king of the jungle, often spotted in Maasai Mara and Nairobi National Park.",
        },
        {
            name: "Giraffe",
            image: "/giraffe.jpg",
            description:
                "The world’s tallest animal, gracefully roaming across Kenya’s savannahs.",
        },
    ];
</script>

<section class="wildlife-section">
    <h1>Explore Kenya’s Iconic Wildlife</h1>
    <div class="cards-container">
        {#each wildlife as animal, i (animal.name)}
            <div class="card" in:fade={{ duration: 400, delay: i * 150 }}>
                <img src={animal.image} alt={animal.name} />
                <h2>{animal.name}</h2>
                <p>{animal.description}</p>
            </div>
        {/each}
    </div>
</section>

<style>
    .wildlife-section {
        padding: 80px 30px;
        text-align: center;
    }

    .wildlife-section h1 {
        font-size: 2.8rem;
        margin-bottom: 50px;
        color: #1c1c1c;
    }

    .cards-container {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
        justify-items: center;
    }

    .card {
        background: white;
        border-radius: 16px;
        box-shadow: 0 6px 20px rgba(0, 0, 0, 0.08);
        overflow: hidden;
        transition:
            transform 0.3s ease,
            box-shadow 0.3s ease;
        cursor: pointer;
        max-width: 100%;
        width: 100%;
    }

    .card:hover {
        transform: scale(1.04) translateY(-5px);
        box-shadow: 0 12px 30px rgba(0, 0, 0, 0.15);
    }

    .card img {
        width: 100%;
        height: 220px;
        object-fit: cover;
    }

    .card h2 {
        font-size: 1.5rem;
        margin: 20px 0 10px;
        color: #222;
    }

    .card p {
        padding: 0 20px 20px;
        font-size: 1rem;
        color: #555;
    }
</style>
