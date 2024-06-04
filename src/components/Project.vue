<script setup>
import {defineProps, ref} from 'vue'
import Modal from "@/components/Modal.vue";

const dialogState = ref(false)

const show = () => {
  dialogState.value = true
}

defineProps({
  title: String,
  github: String, // soit c'est un lien, soit c'est private
  date: String,
  description: String,
  descriptionExtended: String,
  image: String,
  skills: Array,
  left: Boolean,
  url: String,
  competences: Array
})
</script>

<template>
  <div class="project">
    <Modal v-if="dialogState" @close="dialogState = false">
      <template v-slot:header>
        <h2>{{ title }}</h2>
        <span>{{ date }}</span>
      </template>
      <template v-slot:content>
        <div class="project-skills">
          <div v-for="competence in competences"
              :key="competence"
              class="project-competences">
            <span class="project-competence">{{ competence.competence }} </span> :
            <span>{{ competence.justification }}</span>
          </div>
        </div>
      </template>
    </Modal>
    <div class="project-image-left" v-if="left">
      <a :href="url" target="_blank">
        <img :src="image" alt="project image"/>
      </a>
    </div>
    <div :class="left ? 'project-content-left' : 'project-content-right'">
      <div class="project-title-container">
        <span class="project-title">{{ title }} </span>
        <a v-if="github !== 'Private'" :href="github" target="_blank">
          <i class="fab fa-github"></i>
        </a>
        <button class="open-modal-btn" @click="show">+</button>

      </div>

      <span class="project-date">{{ date }}</span>
      <span class="project-description">{{ description }}</span>
      <div class="project-skills">
        <span
            v-for="skill in skills"
            :key="skill"
            class="project-skill"
        >{{ skill }}</span>
      </div>
      <div class="project-skills">
        <span
            v-for="competence in competences"
            :key="competence"
            class="project-competence"
        >{{ competence.competence }}</span>
      </div>
    </div>
    <div class="project-image-right" v-if="!left">
      <a :href="url" target="_blank">
        <img :src="image" alt="project image"/>
      </a>
    </div>
  </div>
</template>

<style scoped>
.project {
  position: relative;
  display: flex;
  align-items: center;
  margin-bottom: 50px;

  padding: 20px;
  width: 80%;
}

.project-image-left {
  max-width: 500px;
  max-height: 500px;
  margin-right: 20px;
}

.project-image-right {
  max-width: 500px;
  max-height: 500px;
  margin-left: 20px;
}

img {
  max-width: 500px;
  max-height: 500px;
  object-fit: cover;
  border-radius: 10px;
  box-shadow: 5px 7px 10px rgba(255, 255, 255, 0.5);
}

.project-content-left {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-end;
}

.project-content-right {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: flex-start;
}

.project-title-container {
  display: flex;
  align-items: center;
}

.project-title {
  font-size: 2rem;
  font-weight: bold;
  color: var(--primary);
  position: relative;
}

.project-date {
  font-size: 1.2rem;
  font-weight: bold;
  margin-bottom: 10px;
  color: var(--text);
}

.project-description {
  font-size: 1rem;
  margin-bottom: 10px;
  color: var(--text);
  background-color: var(--secondary);
  border-radius: 10px;
  padding: 10px;
  width: 110%;
  box-shadow: 5px 7px 10px rgba(255, 255, 255, 0.5);
  z-index: 1;
}

.project-skills {
  display: flex;
  align-items: center;
  flex-wrap: wrap;
  margin-top: 10px;
}

.project-skill {
  font-size: 1rem;
  font-weight: bold;
  margin-left: 10px;
  margin-bottom: 10px;
  padding: 5px 10px;
  border-radius: 5px;
  border: 1px solid var(--primary);
  background-color: var(--primary);
  color: var(--text);
  transition: all 0.3s ease;
}

.project-skill:hover {
  background-color: var(--primary-opacity-30);
  border: 1px solid var(--primary);
  transition: all 0.3s ease;
}

.project-competences {
  font-size: 1rem;
  font-weight: bold;
  margin-left: 10px;
  margin-bottom: 10px;
  padding: 5px 10px;
  border-radius: 5px;
  color: var(--text);
}

.project-competence {
  font-size: 1rem;
  font-weight: bold;
  margin-left: 10px;
  margin-bottom: 10px;
  padding: 5px 10px;
  border-radius: 5px;
  border: 1px solid var(--secondary);
  background-color: var(--secondary);
  color: var(--text);
  transition: all 0.3s ease;
}

.project-competence:hover {
  background-color: var(--secondary-opacity-30);
  border: 1px solid var(--secondary);
  transition: all 0.3s ease;
}

.fa-github {
  font-size: 2rem;
  color: var(--text);
  margin-left: 10px;
  transition: all 0.3s ease;
}

.fa-github:hover {
  color: var(--primary);
  transition: all 0.3s ease;
}

.open-modal-btn {
  background-color: var(--primary);
  color: var(--text);
  padding: 5px 10px;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  font-size: 1rem;
  margin-left: 10px;
  transition: all 0.3s ease;
}

.open-modal-btn:hover {
  background-color: var(--secondary);
  color: var(--text);
  transition: all 0.3s ease;
}
</style>
