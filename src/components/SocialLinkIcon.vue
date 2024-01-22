<script setup>
import { defineProps } from 'vue'
  defineProps({
    link: String,
    icon: String,
    color: String,
  });
</script>

<template>
  <link rel="stylesheet"
        href="https://use.fontawesome.com/releases/v5.2.0/css/all.css"
        integrity="sha384-hWVjflwFxL6sNzntih27bfxkr27PmbbK/iSvJ+a4+0owXq79v+lsFkW54bOGbiDQ"
        crossorigin="anonymous">
  <div class="social-link-icon" :style="{ color: color }">
    <a :href="link" target="_blank" rel="noopener noreferrer" ref="linkRef">
      <i :class="icon"></i>
    </a>
  </div>
</template>

<style scoped>
.social-link-icon {
  width: 50px;
  height: 50px;
  border-radius: 50%;
  background-color: #fff;
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 10px;
  transition: all 0.3s ease;
}

.social-link-icon:hover {
  transform: scale(1.1);
}

.social-link-icon a {
  text-decoration: none;
  color: inherit;
}

.social-link-icon i {
  font-size: 1.5rem;
}
</style>