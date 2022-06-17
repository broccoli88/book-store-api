<template>
    <header class="flex">
        <svg
            class="menu-button"
            xmlns="http://www.w3.org/2000/svg"
            aria-hidden="true"
            role="button"
            width="48"
            height="48"
            preserveAspectRatio="xMidYMid meet"
            viewBox="0 0 32 32"
        >
            <path
                fill="var(--color-secondary-dark)"
                d="M16 2a14 14 0 1 0 14 14A14 14 0 0 0 16 2Zm0 26a12 12 0 1 1 12-12a12 12 0 0 1-12 12Z"
            />
            <path
                fill="var(--color-secondary-dark)"
                d="M16 10a6 6 0 1 0 6 6a6 6 0 0 0-6-6Z"
            />
        </svg>
        <div class="branding">Books</div>
        <nav class="flex-col">
            <h3 class="heading">My library</h3>
            <ul class="nav-links flex-col">
                <li class="link"><a href="#">Favourites</a></li>
                <li class="link"><a href="#">Reading now</a></li>
                <li class="link"><a href="#">To Read</a></li>
                <li class="link"><a href="#"> Have Read</a></li>
            </ul>
        </nav>
    </header>
</template>

<script setup>
</script>

<style scoped>
header {
    width: 100vw;
    height: 6rem;

    padding: 1.5rem 3rem 2rem;

    background-color: white;

    justify-content: space-between;

    position: fixed;
}

.menu-button {
    position: absolute;
    top: 0.9rem;
    right: 3rem;

    cursor: pointer;
}

.branding {
    font-size: 2rem;
    font-weight: 900;
    text-transform: uppercase;

    color: var(--color-secondary-dark);
}

nav {
    width: 60%;
    height: calc(100vh - 6rem);

    border-left: 3px solid var(--color-secondary-dark);
    box-shadow: 0 4px 4px hsl(0, 0%, 50%, 0.5);
    background-color: white;

    justify-content: center;
    align-items: flex-start;
    gap: 6rem;

    position: absolute;
    top: 6rem;
    right: 0;
    z-index: 900;
}

.heading {
    padding-left: 1rem;
}

.nav-links {
    list-style-type: none;
    width: 100%;

    z-index: 920;
}

.link {
    padding: 1rem 0 1rem 1rem;
    cursor: pointer;
    position: relative;

    background-color: transparent;

    z-index: 940;
}

.link > a {
    position: relative;
    z-index: 950;

    transition: color 0.6s ease;
}

.link::before {
    content: "";
    display: inline-block;

    position: absolute;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    z-index: 930;

    transform: scaleX(0);
    transform-origin: left;

    background-color: var(--color-secondary-dark);
    transition: all 0.3s linear;
}

.link:hover {
    color: white;
    font-weight: 600;
}

.link:hover.link::before {
    transform: scaleX(1);
    color: white;
}
</style>