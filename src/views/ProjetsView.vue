<script setup>
import Project from "@/components/Project.vue";
</script>

<template>
    <div class="projects">
        <project 
            title="Zencraft" 
            github="Private"
            date="2021 - Aujourd'hui"
            description="Zencraft est un serveur minecraft semi-rp communautaire créer en 2017 et qui aujourd'hui accueil plus de 80 000 joueurs. 
            J'ai rejoins l'équipe en temps que développeur Java pour la création de contenenue (plugins) et web pour leur site internet." 
            image="./img/Zencraft.jpg" 
            :skills="['Java', 'Maven', 'Git', 'Redis', 'MySQL', 'PHP',  'Laravel', 'JS']"
            :left="true"
            url="https://zencraft.fr"/>

        <project 
            title="Fast-Track-Auto" 
            github="https://github.com/maximefurious/Fast-Track-Auto"
            date="2023 - Aujourd'hui"
            description="FastTrackAuto est un projet de développement d'une application Flutter communiquant avec un module OBD2 
            afin de pouvoir faire le suivi kilométrique de sa voiture mais également le suivi d'entretien, ainsi que le suivi en 
            général de toute autre information utile pour les usagers de la route.
        
            Le projet inclut également la conception d'une interface utilisateur conviviale avec des fonctionnalités telles que la 
            visualisation des données, la planification des rappels d'entretien, la gestion des coûts de carburant et de maintenance. 
            La sécurité des données des utilisateurs est une priorité absolue et sera prise en compte tout au long du développement 
            de l'application." 
            image="./img/FastTrackauto.png" 
            :skills="['Flutter', 'Dart', 'Git', 'OBD2', 'MySQL', 'Java', 'Swift']"
            :left="false"/>


        <project 
            title="PortfolioV3" 
            github="https://github.com/maximefurious/PorteFolioV3"
            date="2022 - 2023"
            description="Ce projet représente la troisième version de mon portfolio. Il a été réaliser à la suite du projet PortefolioV2 
            et il a été réaliser dans le but de découvre l'environnement ReactJS et de pouvoir comparer l'environnemet natif et ReactJS.
            Ce projet est également l'occasion de découvrir les principes fondamentaux du GreenIT et de les appliquer dans le développement."             
            image="./img/PortfolioV3.png" 
            :skills="['React', 'Git', 'Ajax', 'GreenIT']"
            :left="true"/>

        <project 
            title="PortfolioV4" 
            github="https://github.com/maximefurious/PorteFolioV4"
            date="2023 - Aujourd'hui"
            description="Ce projet représente la quatrième version de mon portfolio. Il a été réaliser dans le contexte de la découverte 
            d'un environnement de mise en production en intégration continue. J'ai donc mis en place un environnement de CI/CD avec GitHub et 
            Hostinger qui permet de déployer automatiquement le site et de maintenir une version de production à jour."             
            image="./img/PortfolioV4.png" 
            :skills="['VueJS', 'Git', 'CI/CD']"
            :left="false"/>    
    </div>
</template>

<style scoped>
    .projects {
        height: 100%;
        margin-top: 50px;
        display: flex;
        flex-direction: column;
        align-items: center;
    }

</style>
