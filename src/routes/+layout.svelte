<nav>
    <a href="/">Home</a>
    <a href="/safari-guide">Safari Guide</a>
    <a href="/gallery">Gallery</a>
</nav>

<slot />

<style>
    nav {
        background: #2c3e50;
        padding: 10px;
        text-align: center;
    }
    nav a {
        color: white;
        text-decoration: none;
        margin: 0 15px;
        font-weight: bold;
    }
    nav a:hover {
        text-decoration: underline;
    }
</style>
