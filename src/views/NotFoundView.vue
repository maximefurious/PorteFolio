<template>
    <div class="notfoundpage">
        <span class="main">404</span>
        <h2>Page not found</h2>
        <p>Sorry, the page you're looking for doesn't exist.</p>
        <router-link to="/">Go back to the homepage</router-link>
    </div>
</template>

<script>
export default {
    name: 'NotFoundView',
}
</script>

<style>
.notfoundpage {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100%;
}

.notfoundpage .main {
    font-size: 10rem;
    color: var(--primary);
    transition: all 0.3s ease;
}

.notfoundpage h2 {
    font-size: 3rem;
    color: var(--text);
    transition: all 0.3s ease;
}

.notfoundpage p {
    font-size: 1.5rem;
    color: var(--text);
    transition: all 0.3s ease;
}

.notfoundpage a {
    font-size: 1.5rem;
    color: var(--primary);
    text-decoration: none;
    transition: all 0.3s ease;
}

.notfoundpage a:hover {
    color: var(--secondary);
}

@media (max-width: 768px) {
    .notfoundpage .main {
        font-size: 5rem;
    }

    .notfoundpage h2 {
        font-size: 2rem;
    }

    .notfoundpage p {
        font-size: 1rem;
    }

    .notfoundpage a {
        font-size: 1rem;
    }
}
</style>
