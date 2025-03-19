<script>
    let images = [
        { src: "/lion.jpg", alt: "Lion in Maasai Mara" },
        { src: "/elephant.jpg", alt: "Elephant in Amboseli" },
        { src: "/zebra.jpg", alt: "Zebras in the savanna" },
        { src: "/giraffe.jpg", alt: "Giraffe in Samburu National Reserve" },
        { src: "/rhino.jpg", alt: "Rhino in Tsavo National Park" },
    ];
</script>

<main>
    <h1>Wildlife Photo Gallery 📸</h1>
    <p>Explore the stunning wildlife found in Kenya’s national parks.</p>

    <div class="gallery">
        {#each images as img}
            <img src={img.src} alt={img.alt} />
        {/each}
    </div>
</main>

<style>
    main {
        text-align: center;
        padding: 20px;
    }
    .gallery {
        display: flex;
        gap: 10px;
        flex-wrap: wrap;
        justify-content: center;
    }
    .gallery img {
        width: 300px;
        height: auto;
        border-radius: 10px;
        transition: transform 0.3s ease-in-out;
    }
    .gallery img:hover {
        transform: scale(1.1);
    }
</style>
