<script setup>
import TimeLineExperienceChild from '@/components/TimeLineExperienceChild.vue'
</script>

<template>
    <div class="experience-timeline">
        <span class="title">Expériences</span>
        <div class="timeline">
            <TimeLineExperienceChild
                dateDebut="2022"
                dateFin="Aujourd'hui"
                titre="Mobil-inn"
                description="Apprenti développeur fullstack et mobile"
            />

            <TimeLineExperienceChild
                dateDebut="2022"
                dateFin="2022"
                titre="Intermarché"
                description="Employé polyvalent, mise en rayon, caisse, accueil"
            />
        </div>
    </div>
</template>

<style scoped>
.experience-timeline {
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 20px;
}

.title {
    font-weight: bold;
    font-size: 2rem;
    margin-bottom: 10px;
}

.timeline {
    position: relative;
    width: 100%;
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 20px;
}
</style>
