<script>
    // No logic yet
</script>

<!-- HERO SECTION -->
<section class="hero">
    <div
        class="bg-black bg-opacity-[0.7] p-8 rounded-lg text-center max-w-2xl w-full mx-4 shadow-xl"
    >
        <h1
            class="text-white text-5xl md:text-6xl font-extrabold drop-shadow-md mb-4"
        >
            Jungle Pulse Kenya
        </h1>
        <p class="text-gray-100 text-lg md:text-2xl italic mb-6">
            Experience the Wild Beauty of Kenya
        </p>
        <a
            href="/destinations"
            class="inline-block bg-yellow-400 hover:bg-yellow-500 text-black font-bold py-3 px-8 rounded-full transition duration-300 shadow-md"
        >
            Explore Destinations
        </a>
    </div>
</section>

<!-- FOOTER -->
<footer class="bg-white text-gray-800 py-6 px-4 border-t border-gray-200">
    <div class="max-w-4xl mx-auto text-center">
        <p class="text-sm italic font-bold text-gray-700 mb-2">
            "Jungle Pulse Kenya is your gateway to the heart of Africa. Discover
            wild beauty, untamed landscapes, and unforgettable journeys."
        </p>
        <p class="text-xs italic font-bold text-gray-600">
            © 2025 Jungle Pulse Kenya. All Rights Reserved.
        </p>
    </div>
</footer>

<style>
    .hero {
        height: 90vh;
        background-image: url("/majestic-lion.jpg");
        background-size: cover;
        background-position: center;
        background-repeat: no-repeat;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    @media (max-width: 768px) {
        .hero {
            height: 60vh;
        }

        .hero h1 {
            font-size: 2rem;
        }

        .hero p {
            font-size: 1rem;
        }

        .hero a {
            font-size: 0.9rem;
            padding: 0.5rem 1rem;
        }
    }
</style>
