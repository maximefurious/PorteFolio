<!-- On créer un composant qui prend en paramètre le nom de la compétence la class pour l'icon devicon  -->
<script setup>
import { defineProps } from 'vue'
const props = defineProps({
    name: String,
    icon: String,
})
</script>

<template>
    <div class="skill">
        <i :class="icon"></i>
        <span>{{ name }}</span>
    </div>
</template>

<style scoped>
.skill {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.skill i {
    font-size: 4rem;
}

.skill i:hover {
    transform: scale(1.1);
    transition: all 0.3s ease;
}

.skill span {
    font-size: 1.2rem;
    font-weight: bold;
    color: var(--primary);
}
</style>
