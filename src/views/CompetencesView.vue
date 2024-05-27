<script setup>
import Skill from '@/components/Skill.vue'
</script>

<template>
  <div class="wave">
    <div class="wave-limiter">
      <div class="left"></div>
    </div>
    <div class="wave-limiter">
      <div class="right"></div>
    </div>
  </div>
  <div id="skills">
    <div class="categories">
      <div
          v-for="category in categories"
          :key="category.id"
          @click="selectCategory(category)"
          :class="{
                    'active-category': selectedCategory === category.name,
                }"
          class="category"
      >
        {{ category.name }}
      </div>
    </div>

    <div class="language-list">
      <div
          v-for="language in filteredLanguages"
          :key="language.id"
          class="language-item"
      >
        <div class="language-item-inner">
          <Skill :name="language.name" :icon="language.class"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      categories: [
        {id: 1, name: 'Front-end'},
        {id: 2, name: 'Back-end'},
        {id: 3, name: 'Software'},
        // Ajoutez d'autres catégories au besoin
      ],
      languages: [
        {
          id: 0,
          name: 'HTML',
          class: 'devicon-html5-plain colored',
          category: 'Front-end',
        },
        {
          id: 1,
          name: 'CSS',
          class: 'devicon-css3-plain colored',
          category: 'Front-end',
        },
        {
          id: 2,
          name: 'JavaScript',
          class: 'devicon-javascript-plain colored',
          category: 'Front-end',
        },
        {
          id: 3,
          name: 'jQuery',
          class: 'devicon-jquery-plain colored',
          category: 'Front-end',
        },
        {
          id: 4,
          name: 'Bootstrap',
          class: 'devicon-bootstrap-plain colored',
          category: 'Front-end',
        },
        {
          id: 5,
          name: 'Sass',
          class: 'devicon-sass-original colored',
          category: 'Front-end',
        },
        {
          id: 6,
          name: 'React',
          class: 'devicon-react-original colored',
          category: 'Front-end',
        },
        {
          id: 7,
          name: 'MySQL',
          class: 'devicon-mysql-plain colored',
          category: 'Back-end',
        },
        {
          id: 8,
          name: 'PostgreSQL',
          class: 'devicon-postgresql-plain colored',
          category: 'Back-end',
        },
        {
          id: 9,
          name: 'PHP',
          class: 'devicon-php-plain colored',
          category: 'Back-end',
        },
        {
          id: 10,
          name: 'THREE.js',
          class: 'devicon-threejs-original',
          category: 'Front-end',
        },
        {
          id: 11,
          name: 'GitLab',
          class: 'devicon-gitlab-plain colored',
          category: 'Software',
        },
        {
          id: 12,
          name: 'GitHub',
          class: 'devicon-github-plain',
          category: 'Software',
        },
        {
          id: 13,
          name: 'Apache',
          class: 'devicon-apache-plain colored',
          category: 'Software',
        },
        {
          id: 14,
          name: 'Vue.js',
          class: 'devicon-vuejs-plain colored',
          category: 'Front-end',
        },
        {
          id: 15,
          name: 'Java',
          class: 'devicon-java-plain colored',
          category: 'Software',
        },
        {
          id: 16,
          name: 'C',
          class: 'devicon-c-plain colored',
          category: 'Software',
        },
        {
          id: 17,
          name: 'CodeIgniter',
          class: 'devicon-codeigniter-plain colored',
          category: 'Back-end',
        },
        {
          id: 18,
          name: 'Android',
          class: 'devicon-android-plain colored',
          category: 'Software',
        },
        {
          id: 19,
          name: 'Flutter',
          class: 'devicon-flutter-plain colored',
          category: 'Software',
        },
        {
          id: 20,
          name: 'Dart',
          class: 'devicon-dart-plain colored',
          category: 'Software',
        },
        {
          id: 21,
          name: 'Python',
          class: 'devicon-python-plain colored',
          category: 'Software',
        },
        {
          id: 22,
          name: 'Docker',
          class: 'devicon-docker-plain colored',
          category: 'Software',
        },
        {
          id: 23,
          name: 'Bash',
          class: 'devicon-bash-plain',
          category: 'Software',
        },
        {
          id: 24,
          name: 'Laravel',
          class: 'devicon-laravel-plain colored',
          category: 'Back-end',
        },
        {
          id: 25,
          name: 'Redis',
          class: 'devicon-redis-plain colored',
          category: 'Back-end',
        },
        {
          id: 26,
          name: 'Swift',
          class: 'devicon-swift-plain colored',
          category: 'Software',
        },
        {
          id: 27,
          name: 'Gradle',
          class: 'devicon-gradle-plain',
          category: 'Software',
        },
        {
          id: 28,
          name: 'Flask Server',
          class: 'devicon-flask-original',
          category: 'Back-end',
        },
        {
          id: 29,
          name: 'NodeJS',
          class: 'devicon-nodejs-plain colored',
          category: 'Back-end',
        },
        {
          id: 30,
          name: 'MongoDB',
          class: 'devicon-mongodb-plain colored',
          category: 'Back-end',
        },
        {
          id: 31,
          name: 'Django',
          class: 'devicon-django-plain colored',
          category: 'Back-end',
        },
        {
          id: 32,
          name: 'Subversion',
          class: 'devicon-subversion-plain colored',
          category: 'Software',
        },
        {
          id: 33,
          name: 'Maven',
          class: 'devicon-maven-plain colored',
          category: 'Software',
        },
        {
          id: 34,
          name: 'elasticsearch',
          class: 'devicon-elasticsearch-plain colored',
          category: 'Back-end',
        }
      ],
      selectedCategory: 'Front-end', // La catégorie sélectionnée par défaut
    }
  },
  computed: {
    filteredLanguages() {
      return this.languages.filter(
          (language) => language.category === this.selectedCategory
      )
    },
  },
  methods: {
    selectCategory(category) {
      this.selectedCategory = category.name
    },
  },
}
</script>

<style scoped>
#skills {
  margin-bottom: 50px;
  min-height: 500px;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  background-color: var(--primary);
  position: relative;
}

.wave {
  height: 5em;
  display: flex;
}

.wave-limiter {
  width: 50%;
  background: var(--background);
}

.wave .left {
  width: 100%;
  height: 5em;
  background: var(--primary);
  border-top-left-radius: 200%;
}

.wave .right {
  width: 100%;
  height: 5em;
  background: var(--primary);
  border-top-right-radius: 200%;
}

/* Styles pour la liste des catégories */
.categories {
  display: flex;
  justify-content: center;
  width: fit-content;
  margin-bottom: 20px;
  background-color: var(--secondary);
  border-radius: 10px;
  padding: 20px;
  box-shadow: 5px 7px 10px rgba(255, 255, 255, 0.5);
}

.category {
  cursor: pointer;
  padding: 10px 15px;
  margin-right: 10px;
  border-radius: 10px;
  font-size: 1.2rem;
  font-weight: bold;
}

.category:hover {
  background-color: var(--primary);
  color: var(--background);
}

.active-category {
  background-color: var(--primary);
  color: var(--background);
}

/* Styles pour la liste des langages */
.language-list {
  width: 60%;

  display: flex;
  justify-content: space-around;
  align-items: center;
  flex-wrap: wrap;

  margin: 20px;

  background-color: var(--secondary);
  border-radius: 10px;
  padding: 20px;
  box-shadow: 5px 7px 10px rgba(255, 255, 255, 0.5);
}

.language-item-inner {
  margin-left: 20px;
}

.language-item {
  text-align: center;
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  margin: 10px;
}
</style>
