<script>
    import "../app.css"; // 👈 This connects your global CSS
    import Nav from "$lib/Nav.svelte";
</script>

<Nav />

<slot />

<style>
    nav {
        background-color: #1f2937;
        padding: 10px;
    }
    a {
        color: white;
        text-decoration: none;
        margin-right: 15px;
    }
    a:hover {
        text-decoration: underline;
    }
</style>
