<div class="contact">
    <h1>Contact Us</h1>
    <p>Have questions? Get in touch with us.</p>

    <form>
        <label>Name:</label>
        <input type="text" placeholder="Your Name" />

        <label>Email:</label>
        <input type="email" placeholder="Your Email" />

        <label>Message:</label>
        <textarea placeholder="Your Message"></textarea>

        <button type="submit">Send Message</button>
    </form>
</div>

<style>
    .contact {
        text-align: center;
        padding: 50px;
    }

    form {
        display: flex;
        flex-direction: column;
        width: 300px;
        margin: auto;
    }

    input,
    textarea {
        padding: 10px;
        margin: 5px 0;
        width: 100%;
    }

    button {
        background: #ff9800;
        color: white;
        padding: 10px;
        border: none;
        cursor: pointer;
    }
</style>
