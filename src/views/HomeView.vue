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
        <a href="/contact" target="_blank" class="btn-contact">Me contacter</a>
      </div>
      <ThreeCanvas />
    </div>
  </div>
</template>

<style>
.home {
  width: 60%;
  height: 100%;
  display: flex;
  align-items: center;
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

.btn-contact {
  padding: 10px 20px;
  border-radius: 20px;
  font-weight: bold;
  font-size: 1.2rem;
  text-decoration: none;
  color: var(--text);
  border: 2px solid var(--primary);
  transition: all 0.3s ease;
  margin-top: 20px !important;
}

.btn-contact:hover {
  background-color: var(--primary);
  color: var(--text);
  transition: all 0.3s ease;
}

@media screen and (max-width: 768px){
  .home {
      width: 100% !important;
    }
}
</style>

