<script setup>
import {defineProps} from "vue";

defineProps({
  dateDebut: {
    type: String,
    required: true,
  },
  dateFin: {
    type: String,
    required: true,
  },
  titre: {
    type: String,
    required: true,
  },
  description: {
    type: String,
    required: true,
  },
});
</script>

<template>
  <div class="timeline-container left">
    <div class="timeline-content">
      <span class="date">{{ dateDebut }} - {{ dateFin }}</span>
      <span class="title">{{ titre }}</span>
      <span class="description">{{ description }}</span>
    </div>
  </div>
</template>

<style scoped>
.timeline-container {
  padding: 10px 40px;
  position: relative;
  background-color: inherit;
  width: 50%;
}

.timeline-container::before {
  content: '';
  position: absolute;
  width: 25px;
  height: 25px;
  right: -17px;
  background-color: var(--primary);
  border: 4px solid var(--primary);
  top: 15px;
  border-radius: 50%;
  z-index: 1;
}

.timeline-container:last-of-type::before {
  border-color: var(--primary);
  background-color: var(--background);
}

.timeline-container::after {
  content: '';
  position: absolute;
  width: 10px;
  height: 100%;
  right: -9px;
  top: 0;
  background-color: var(--secondary);
}

.timeline-container:first-of-type::after {
  border-top-right-radius: 6px;
  border-top-left-radius: 6px;
}

.timeline-container:last-of-type::after {
  height: 25%;
  border-bottom-right-radius: 6px;
  border-bottom-left-radius: 6px;
}

.timeline-content {
  position: relative;
  width: 90%;
  background-color: var(--secondary);
  border: 1px solid var(--primary);
  box-shadow: 3px 3px 7px rgba(255, 255, 255, 0.5);
  padding: 20px;
  border-radius: 6px;
  transition: all 0.3s ease;
}

.timeline-content:hover {
  background-color: var(--primary);
  opacity: 0.7;
  border: 1px solid var(--primary);
  box-shadow: 3px 3px 7px rgba(255, 255, 255, 0.5);
  transition: all 0.3s ease;
}

.date {
  display: block;
  margin-top: 10px;
  color: var(--text);
  font-weight: bold;
}

.title {
  display: block;
  font-size: 1.2rem;
  font-weight: bold;
  color: var(--text);
}

.description {
  font-size: 1rem;
  color: var(--text);
  opacity: 0.7;
}

@media screen and (max-width: 600px) {
  .timeline-container {
    width: 100%;
    padding-right: 25px;
  }
}

</style>