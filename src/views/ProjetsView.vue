<script setup>
import Project from '@/components/Project.vue'
</script>

<template>
  <div class="projects" id="projects">
    <project
        title="Zencraft"
        github="Private"
        date="2021 - Aujourd'hui"
        description="Zencraft est un serveur minecraft semi-rp communautaire créer en 2017 et qui aujourd'hui accueil plus de 80 000 joueurs.
            J'ai rejoins l'équipe en temps que développeur Java pour la création de contenenue (plugins) et web pour leur site internet."
        image="./img/Zencraft.jpg"
        :skills="[
                'Java',
                'Maven',
                'Git',
                'Redis',
                'MySQL',
                'PHP',
                'Laravel',
                'JS',
            ]"
        :left="true"
        url="https://zencraft.fr"
        :competences="[
            {competence: 'Réaliser des applications', justification: 'Je suis capable de réaliser des applications car dans le cadre de la réalisation du projet ZenCraftV3, j\'ai su mettre en place un serveur Minecraft basé sur le système multi-server et j\'ai églaement développer tous le système économique et fonctionnel du serveur permettant au joueurs d\'avoir une expériences plaisante et agréable.'},
            {competence: 'Optimiser des applications', justification: 'Je suis capable d\'optimiser des applications car dans le cadre de la réalisation du projet ZenCraftV3, j\'ai su mettre en place un système de cache Redis pour optimiser les performances du serveur Minecraft. J\'ai également mis en place un certain nombre d\'outils de monitoring pour suivre les performances du serveur Minecraft.'},
            {competence: 'Administrer des Systèmes', justification: 'Je suis capable d\'administrer des systèmes informatique car dans le cadre de la réalisation du projet ZenCraftV3, j\'ai su mettre en place un serveur dédié pour héberger le serveur Minecraft. J\'ai également pu mettre en place un système de sauvegarde automatique des données pour éviter toute perte de données.'},
            {competence: 'Gérer des données', justification: 'Je suis capable de gérer des données divers car dans le cadre de la réalisation du projet ZenCraftV3, j\'ai su mettre en place une base de donnée MySQL et Redis pour stocker les données des joueurs et des plugins. J\'ai également pu mettre en place un système de cache Redis pour optimiser les performances du serveur Minecraft. J\'ai également pu mettre en place un système de sauvegarde automatique des données pour éviter toute perte de données.'},
            {competence: 'Conduire une équipe', justification: 'Je suis capable de conduire une équipe informatique car dans le cadre de la réalisation du projet ZenCraftV3, j\'ai su mettre en place une équipe de développeur Java et Web pour la création de contenenue (plugins) et web pour leur site internet. J\'ai également pu mettre en place un système de management en Kanba afin de pouvoir gérer les Deadlines et le projet dans sa globalité. J\'ai également su faire des reunions avec les joueurs et rédiger des comptes rendu afin de pouvoir recueillir les avis des joueurs et les remonter à l\'équipe de développement. J\'ai également pu mettre en place un système de recrutement pour agrandir l\'équipe de développement.'},
            {competence: 'Collaborer en équipe', justification: 'Je suis capable de collaborer en équipe informatique car dans le cadre de la réalisation du projet ZenCraftV3, j\'ai su mettre en place une veille informatique pour être mis au courant des nouvelles mise à jours PaperMC. J\'ai également pu apporter mon expertise dans les divers décisions prises par l\'équipe apportant ainsi des changement au sein de l\'organisation mais accompagnant également le chef de projet au management du projet informatique'},
        ]"
    />

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
        :skills="[
                'Flutter',
                'Dart',
                'Git',
                'OBD2',
                'MySQL',
                'Java',
                'Swift',
            ]"
        :competences="[
            {competence: 'Réaliser des applications', justification: 'Je suis capable de réaliser des applications car dans le cadre de la réalisation du projet FastTrackAuto, j\'ai su mettre en place une application mobile Flutter permettant de communiquer avec un module OBD2 pour récupérer les données de la voiture. J\'ai également pu mettre en place une base de donnée MySQL pour stocker les données des utilisateurs.'},
            {competence: 'Optimiser des applications', justification: 'Je suis capable d\'optimiser des applications car dans le cadre de la réalisation du projet FastTrackAuto, j\'ai su mettre en place un système de cache pour stocker les données des utilisateurs et ainsi éviter de les récupérer à chaque fois. J\'ai également pu mettre en place un système de sauvegarde automatique des données pour éviter toute perte de données.'},
            {competence: 'Administrer des Systèmes', justification: 'Je suis capable d\'administrer des systèmes informatique car dans le cadre de la réalisation du projet FastTrackAuto, j\'ai su mettre en place un serveur dédié pour héberger la base de donnée MySQL. J\'ai également pu mettre en place un système de sauvegarde automatique des données pour éviter toute perte de données.'},
            {competence: 'Gérer des données', justification: 'Je suis capable de gérer des données divers car dans le cadre de la réalisation du projet FastTrackAuto, j\'ai su mettre en place une base de donnée MySQL pour stocker les données des utilisateurs. J\'ai également pu mettre en place un système de cache pour stocker les données des utilisateurs et ainsi éviter de les récupérer à chaque fois. J\'ai également pu mettre en place un système de sauvegarde automatique des données pour éviter toute perte de données.'},
        ]"
        :left="false"
    />

    <project
        title="PortfolioV3"
        github="https://github.com/maximefurious/PorteFolioV3"
        date="2022 - 2023"
        description="Ce projet représente la troisième version de mon portfolio. Il a été réaliser à la suite du projet PortefolioV2
            et il a été réaliser dans le but de découvre l'environnement ReactJS et de pouvoir comparer l'environnemet natif et ReactJS.
            Ce projet est également l'occasion de découvrir les principes fondamentaux du GreenIT et de les appliquer dans le développement."
        image="./img/PortfolioV3.png"
        :skills="['React', 'Git', 'Ajax', 'GreenIT']"
        :left="true"
        :competences="[
            {competence: 'Réaliser des applications', justification: 'Je suis capable de réaliser des applications car dans le cadre de la réalisation du projet PortefolioV3, j\'ai su mettre en place un site internet basé sur le framework ReactJS. J\'ai également pu mettre en place un système de récupération de données en AJAX pour récupérer les données du serveur.'},
            {competence: 'Optimiser des applications', justification: 'Je suis capable d\'optimiser des applications car dans le cadre de la réalisation du projet PortefolioV3, j\'ai su mettre en place des outils d\'analyse afin de pouvoir avoir un site internet respectant le GreenIT. Une grande partie de l\'optimisation a été faite sur le serveur pour réduire la consommation énergétique.'},
        ]"
    />

    <project
        title="PortfolioV4"
        github="https://github.com/maximefurious/PorteFolio"
        date="2023 - Aujourd'hui"
        description="Ce projet représente la quatrième version de mon portfolio. Il a été réaliser dans le contexte de la découverte
            d'un environnement de mise en production en intégration continue. J'ai donc mis en place un environnement de CI/CD avec GitHub et 
            Hostinger qui permet de déployer automatiquement le site et de maintenir une version de production à jour."
        image="./img/PortfolioV4.png"
        :skills="['VueJS', 'ThreeJS', 'Git', 'CI/CD']"
        :left="false"
        :competences="[
            // 'Compétence 1',
            // 'Compétence 2',
            {competence: 'Réaliser des applications', justification: 'Je suis capable de réaliser des applications car dans le cadre de la réalisation du projet PortefolioV4, j\'ai su mettre en place un site internet basé sur le framework VueJS. J\'ai également pu mettre en place un système de récupération de données en AJAX pour récupérer les données du serveur.'},
            {competence: 'Optimiser des applications', justification: 'Je suis capable d\'optimiser des applications car dans le cadre de la réalisation du projet PortefolioV4, j\'ai su mettre en place un système de cache pour stocker les données des utilisateurs et ainsi éviter de les récupérer à chaque fois. J\'ai également pu mettre en place un système de sauvegarde automatique des données pour éviter toute perte de données.'},
            {competence: 'Administrer des Systèmes', justification: 'Je suis capable d\'administrer des systèmes informatique car dans le cadre de la réalisation du projet PortefolioV4, j\'ai su mettre en place un système de déploiement automatique avec GitHub et Hostinger pour déployer automatiquement le site internet'},
        ]"
    />
  </div>
</template>

<style scoped>
.projects {
  margin-top: 50px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

.project-select-tab-button {
  background-color: transparent;
  border: 2px solid #ffffff;
  color: #ffffff;
  padding: 8px 16px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 14px;
  margin: 4px 2px;
  transition: background-color 0.3s ease, color 0.3s ease;
  cursor: pointer;
  border-radius: 4px;
}

.project-select-tab-button:hover {
  background-color: #ffffff;
  color: #000000;
}

.project-select-tab-button:focus {
  outline: none;
  box-shadow: 0 0 0 2px rgba(255, 255, 255, 0.5);
}

.project-select-tab-button.active {
  background-color: #ffffff;
  color: #000000;
}
</style>
