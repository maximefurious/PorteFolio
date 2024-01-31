<script setup>
import TimeLineEducation from "@/components/TimeLineEducation.vue";
import TimeLineExperience from "@/components/TimeLineExperience.vue";
</script>

<template>
  <div class="experiences" id="experiences">
    <TimeLineEducation />
    <TimeLineExperience />
  </div>
</template>

<style>
.experiences {
  width: 100%;
  display: flex;
  justify-content: center;
  padding: 20px;
}

@media screen and (max-width: 768px) {
  .experiences {
    flex-direction: column;
  }
}
</style>