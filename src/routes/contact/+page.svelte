<script>
    let name = "";
    let email = "";
    let message = "";

    function handleSubmit() {
        alert("Message sent successfully! 🐾 We'll get back to you soon.");
        name = email = message = "";
    }
</script>

<section class="contact-container">
    <h1>Let's Connect With the Wild!</h1>
    <p class="intro">
        Got questions about safaris, destinations, or wildlife? Send us a
        message — we’d love to hear from you!
    </p>

    <div class="contact-wrapper">
        <form on:submit|preventDefault={handleSubmit} class="contact-form">
            <label for="name">
                Name:
                <input id="name" type="text" bind:value={name} required />
            </label>

            <label for="email">
                Email:
                <input id="email" type="email" bind:value={email} required />
            </label>

            <label for="message">
                Message:
                <textarea id="message" bind:value={message} rows="5" required
                ></textarea>
            </label>

            <button type="submit">Send Message</button>
        </form>

        <div class="contact-info">
            <h2>Jungle Pulse Kenya</h2>
            <p>Email: info@junglepulsekenya.com</p>
            <p>Phone: +254 700 123 456</p>
            <p>Location: Nairobi, Kenya</p>

            <div class="social-links">
                <a href="#">🐦 Twitter</a>
                <a href="#">📸 Instagram</a>
                <a href="#">📘 Facebook</a>
            </div>
        </div>
    </div>
</section>

<style>
    .contact-container {
        padding: 100px 40px 60px;
        max-width: 1200px;
        margin: 0 auto;
        text-align: center;
    }

    h1 {
        font-size: 2.8rem;
        margin-bottom: 10px;
        color: #222;
    }

    .intro {
        color: #555;
        font-size: 1.1rem;
        margin-bottom: 40px;
    }

    .contact-wrapper {
        display: flex;
        flex-wrap: wrap;
        gap: 40px;
        justify-content: center;
        align-items: flex-start;
    }

    .contact-form {
        flex: 1 1 400px;
        background: #f9f9f9;
        padding: 30px;
        border-radius: 12px;
        box-shadow: 0 4px 12px rgba(0, 0, 0, 0.1);
    }

    label {
        display: block;
        margin-bottom: 20px;
        text-align: left;
        font-weight: 500;
        color: #444;
    }

    input,
    textarea {
        width: 100%;
        padding: 10px;
        margin-top: 6px;
        border: 1px solid #ccc;
        border-radius: 8px;
        font-size: 1rem;
    }

    button {
        background-color: #ff7a00;
        color: white;
        padding: 12px 20px;
        font-size: 1rem;
        border: none;
        border-radius: 10px;
        cursor: pointer;
        transition: background 0.3s ease;
    }

    button:hover {
        background-color: #e76a00;
    }

    .contact-info {
        flex: 1 1 300px;
        text-align: left;
    }

    .contact-info h2 {
        color: #222;
        margin-bottom: 10px;
    }

    .contact-info p {
        color: #555;
        margin: 8px 0;
    }

    .social-links a {
        display: inline-block;
        margin-right: 15px;
        text-decoration: none;
        font-size: 1rem;
        color: #ff7a00;
    }

    .social-links a:hover {
        text-decoration: underline;
    }
</style>
