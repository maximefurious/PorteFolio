
<script setup>
import Header from '@/components/Header.vue'
</script>

<template>
  <Header />
  <router-view />
</template>

<style>
body{
  color: var(--text);
  background: var(--background);
}
</style>
