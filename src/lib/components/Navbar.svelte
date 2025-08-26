<script>
    let menuOpen = false;
</script>

<nav class="navbar">
    <div class="logo">
        <img src="logo.svg" alt="logo" />
    </div>

    <button on:click={() => (menuOpen = !menuOpen)} class="hamburger">
        {#if menuOpen}
            ✖
        {:else}
            ☰
        {/if}
    </button>

    <ul class="menu {menuOpen ? 'open' : ''}">
        <li><a href="/">Home</a></li>
        <li><a href="/about">About Us</a></li>
        <li><a href="/contact">Contact</a></li>
    </ul>
</nav>

<style>
    .navbar {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 15px 35px;
        background: transparent;
        color: white;
        position: relative;
        z-index: 100;
        position: fixed;
        width: 100%;
    }

    .logo > img {
        width: 50px;
    }

    .hamburger {
        font-size: 2.5rem;
        background: none;
        border: none;
        color: white;
        cursor: pointer;
        z-index: 101;
    }

    @keyframes slideInBackground {
        0% {
            background-color: rgba(
                139,
                58,
                58,
                0.3
            ); /* #111 with 0.4 opacity */
        }
        100% {
            background-color: rgba(139, 58, 58, 1); /* #111 with full opacity */
        }
    }

    .menu {
        position: fixed;
        top: 0;
        right: 0;
        left: 100%;
        width: 100%;
        height: 100%;
        padding: 4rem 2rem;
        list-style: none;
        display: flex;
        flex-direction: column;
        gap: 2rem;
        margin: 0;
        transform: translateX(0);
        transition: transform 0.6s ease-in-out;
        z-index: 100;
        background-color: rgba(139, 58, 58, 0.8);
    }

    .menu.open {
        right: 0;
        transform: translateX(-100%);
        background-color: rgba(139, 58, 58, 0.3);
        animation: slideInBackground 0.8s ease forwards;
    }

    .menu li a {
        color: white;
        text-decoration: none;
        font-size: 3rem;
        font-family: var(--main, sans-serif);
    }

    @media screen and (max-width: 600px) {
        .logo > img {
            width: 30px;
        }
    }
</style>
