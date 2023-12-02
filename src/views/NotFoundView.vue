<template>
    <div class="notfoundpage">
        <h1>404</h1>
        <h2>Page not found</h2>
        <p>Sorry, the page you're looking for doesn't exist.</p>
        <router-link to="/">Go back to the homepage</router-link>
    </div>
</template>

<script>
export default {
    name: 'NotFoundView',
};
</script>

<style>
.notfoundpage {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    height: 100vh;
}
</style>