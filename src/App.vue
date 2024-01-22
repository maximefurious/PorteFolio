
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
body{
  color: var(--text);
  background: var(--background);
  
  font-family: 'Poppins', sans-serif;
}
</style>
