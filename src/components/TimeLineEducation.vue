<script setup>
// <!-- On fait une time line vertical qui si il n'y a que un TimeLineEducationChild on ne fait qu'une ligne avec unpoint au milieu mais si il y en a 2 on met 2 points etc -->
import TimeLineEducationChild from "@/components/TimeLineEducationChild.vue";
</script>

<template>
  <div class="education-timeline">
    <span class="education-title">Education</span>
    <div class="timeline">
      <TimeLineEducationChild
          dateDebut="2021"
          dateFin="Aujourd'hui"
          titre="BUT Informatique"
          description="IUT de Lannion, parcours A, Conception, réalisation et développemet d'application web et mobile"
      />
      <TimeLineEducationChild
          dateDebut="2018"
          dateFin="2021"
          titre="BAC Général"
          description="Lycée Polyvalent Paul Sérusier, Spécialité Mathématiques, Informatique"
      />
    </div>
  </div>

</template>

<style scoped>
.education-timeline {
  width: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  padding: 20px;
}

.education-title {
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