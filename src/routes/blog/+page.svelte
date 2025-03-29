<script>
    const blogPosts = [
        {
            title: "The Magic of the Maasai Mara",
            image: "/maasai-mara.jpg",
            description:
                "Explore the breathtaking beauty and wildlife encounters in Kenya’s most iconic park.",
            link: "#",
        },
        {
            title: "Photographing Wildlife Like a Pro",
            image: "/lion.jpg",
            description:
                "Tips and tricks for capturing stunning wildlife moments on your safari adventure.",
            link: "#",
        },
        {
            title: "Why Kenya Should Be Your Next Safari Destination",
            image: "/why-kenya-safari.jpg",
            description:
                "From the Big Five to the Great Migration—discover what makes Kenya the ultimate safari hub.",
            link: "#",
        },
    ];
</script>

<a href="/blog/photographing-wildlife">Read Full Post</a>

<a href="/blog/photographing-wildlife">Read Full Post</a>

<section class="blog">
    <h1 class="title">Latest Stories from the Wild</h1>
    <p class="subtitle">
        Dive into exciting travel stories, wildlife tales, and safari tips
        written by nature lovers like you.
    </p>

    <div class="blog-grid">
        {#each blogPosts as post}
            <div class="blog-card">
                <img src={post.image} alt={post.title} />
                <h2>{post.title}</h2>
                <p>{post.description}</p>
                <a href={post.link} class="read-more">Read More</a>
            </div>
        {/each}
    </div>
</section>

<style>
    .blog {
        padding: 100px 40px;
        max-width: 1200px;
        margin: 0 auto;
    }

    .title {
        text-align: center;
        font-size: 2.8rem;
        margin-bottom: 10px;
        color: #111;
    }

    .subtitle {
        text-align: center;
        font-size: 1.2rem;
        color: #555;
        margin-bottom: 60px;
    }

    .blog-grid {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
        gap: 30px;
    }

    .blog-card {
        background: #fff;
        border-radius: 12px;
        box-shadow: 0 4px 10px rgba(0, 0, 0, 0.1);
        overflow: hidden;
        text-align: center;
        padding-bottom: 20px;
    }

    .blog-card img {
        width: 100%;
        height: 200px;
        object-fit: cover;
    }

    .blog-card h2 {
        font-size: 1.5rem;
        margin: 15px 0 10px;
        color: #000;
    }

    .blog-card p {
        color: #444;
        padding: 0 15px;
        font-size: 1rem;
    }

    .read-more {
        display: inline-block;
        margin-top: 10px;
        color: #e65c00;
        font-weight: bold;
        text-decoration: none;
    }

    .read-more:hover {
        text-decoration: underline;
    }
</style>
