<script>
    let parks = [
        {
            name: "Maasai Mara",
            animals: "Lions, Cheetahs, Elephants",
            location: "Southwestern Kenya",
            image: "/maasai-mara.jpg",
        },
        {
            name: "Amboseli National Park",
            animals: "Elephants, Giraffes, Zebras",
            location: "Near Mt. Kilimanjaro",
            image: "/amboseli.jpg",
        },
        {
            name: "Tsavo National Park",
            animals: "Buffalo, Rhinos, Crocodiles",
            location: "Eastern Kenya",
            image: "/tsavo.jpg",
        },
    ];
</script>

<main>
    <h1>Kenya Safari Guide</h1>
    <p>
        Explore Kenya's top wildlife destinations and the magnificent animals
        you can find there.
    </p>

    <section class="safari-list">
        {#each parks as park}
            <article class="safari-card">
                <img src={park.image} alt={park.name} />
                <h2>{park.name}</h2>
                <p><strong>Wildlife:</strong> {park.animals}</p>
                <p><strong>Location:</strong> {park.location}</p>
            </article>
        {/each}
    </section>
</main>

<style>
    main {
        text-align: center;
        padding: 20px;
    }
    .safari-list {
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 20px;
    }
    .safari-card {
        background: #f4f4f4;
        padding: 15px;
        border-radius: 10px;
        max-width: 300px;
        text-align: center;
    }
    .safari-card img {
        width: 100%;
        border-radius: 10px;
    }
</style>
