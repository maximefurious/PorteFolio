<script setup>
import ThreeCanvas from "@/components/ThreeCanvas.vue";
</script>

<template>
  <div class="home">
    <div class="home-content">
      <div class="home-text">
        <h1 class="home-title">Hey,</h1>
        <h2 class="home-subtitle">Je m'appelle <span>Maxime Boujeant</span></h2>
        <p class="home-paragrap">
          Je suis un étudiant en informatique en <span class="school">BUT informatique</span> à Lannion. Dans la vie, j'aime l'adrénaline, les voitures et la programmation. Je suis quelqu'un de dynamique et
          je suis toujours à la recherche de nouveaux challenges, ainsi que d'opportunité pour m'améliorer et développer mes compétences.
        </p>
      </div>
      <ThreeCanvas />
    </div>
  </div>
</template>

<style>
.home {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: center;
}

.home-content {
  width: 60%;
}

.home-title {
  font-weight: bold;
  font-size: 3rem;
  margin-bottom: 10px;
  color: var(--primary);
}

.home-subtitle {
  font-weight: bold;
  font-size: 2rem;
  margin-bottom: 10px;
  color: var(--text);
}

.home-subtitle span {
  color: var(--primary);
  font-weight: bolder;
}

.home-paragrap {
  font-size: 1.2rem;
  color: var(--text);
  max-width: 800px;
}

.home-paragrap .school {
  color: var(--primary);
  font-weight: bold;
}
</style>

