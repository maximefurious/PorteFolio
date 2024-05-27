<script setup>
import Header from '@/components/Header.vue'

function handleScroll() {
    const header = document.querySelector('.navbar')
    if (window.scrollY > 0) {
        header.classList.add('scroll')
    } else {
        header.classList.remove('scroll')
    }
}

onscroll = handleScroll
</script>

<template>
    <Header />
    <router-view />
</template>
<style>
body {
    color: var(--text);
    background: var(--background);

    font-family: 'Poppins', sans-serif;
}

.scroll {
    background-color: var(--secondary);
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.5);
    transition: all 0.3s ease;
}
</style>
