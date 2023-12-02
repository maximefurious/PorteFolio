<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
    <nav class="navbar">
        <div class="left">
            <router-link to="/" class="nav-item">Portefolio.</router-link>
        </div>
        <div class="right">
            <router-link to="/about" class="nav-item">À propos</router-link>
            <router-link to="/projects" class="nav-item">Projets</router-link>
            <router-link to="/skills" class="nav-item">Compétences</router-link>
            <router-link to="/experiences" class="nav-item">Expériences</router-link>
            <router-link to="/contact" class="nav-item">Contact</router-link>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Navbar',
};
</script>

<style>
.navbar {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 60px;
    display: flex;
    justify-content: space-around;
    align-items: center;
}
.nav-item {
    text-decoration: none;
    color: var(--text);
    font-weight: bold;
    font-size: 1.2rem;
}

.nav-item:hover {
    color: var(--primary);
    transition: color 0.3s ease;
}
.navbar .left {
    position: absolute;
    left: 0;
    margin-left: 20px;
}

.navbar .right {
    position: absolute;
    right: 0;
    margin-right: 20px;
}

.navbar .right .nav-item {
    margin-left: 40px;
}
</style>

