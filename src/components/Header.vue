<script setup>
import { RouterLink } from 'vue-router'
import {onMounted, onUnmounted} from 'vue'


function toggleMenu() {
  document.querySelector('.menu-btn').classList.toggle('open')
  document.querySelector('.menu').classList.toggle('open')
}

function closeMenu() {
  document.querySelector('.menu-btn').classList.remove('open')
  document.querySelector('.menu').classList.remove('open')
}

function handleMenuClick(e) {
  console.log('handleMenuClick')
  if (e.target.classList.contains('menu__nav-link')) {
    closeMenu()
  } else {
    toggleMenu()
  }
}

function handleEscKey(e) {
  if (e.key === 'Escape') {
    closeMenu()
  }
}

function handleResize() {
  if (window.innerWidth > 768) {
    closeMenu()
  }
}

onMounted(() => {
  let menuBtn = document.querySelector('.menu-btn')
  menuBtn.addEventListener('click', handleMenuClick)
  window.addEventListener('keydown', handleEscKey)
  window.addEventListener('resize', handleResize)
})

onUnmounted(() => {
  let menuBtn = document.querySelector('.menu-btn')
  menuBtn.removeEventListener('click', handleMenuClick)
  window.removeEventListener('keydown', handleEscKey)
  window.removeEventListener('resize', handleResize)
})


</script>

<template>
    <nav class="navbar" ref="navbar">
        <div class="left">
            <router-link to="/" class="nav-item">Portefolio.</router-link>
        </div>
        <div class="right">
            <router-link to="/" class="nav-item">Accueil</router-link>
            <router-link to="/about" class="nav-item">À propos</router-link>
            <router-link to="/projects" class="nav-item">Projets</router-link>
            <router-link to="/skills" class="nav-item">Compétences</router-link>
            <router-link to="/experiences" class="nav-item">Expériences</router-link>
            <router-link to="/contact" class="nav-item">Contact</router-link>
        </div>
    </nav>

<!--  munu burger-->

<div class="menu-btn" ref="menuBtn">
    <div class="menu-btn__burger"></div>
  </div>

  <div class="menu">
    <ul class="menu__nav">
      <li class="menu__nav-item">
        <router-link href="/" class="menu__nav-link">Accueil</router-link>
      </li>
      <li class="menu__nav-item">
        <router-link href="/about" class="menu__nav-link">À propos</router-link>
      </li>
      <li class="menu__nav-item">
        <router-link href="/projects" class="menu__nav-link">Projets</router-link>
      </li>
      <li class="menu__nav-item">
        <router-link href="/skills" class="menu__nav-link">Compétences</router-link>
      </li>
      <li class="menu__nav-item">
        <router-link href="/experiences" class="menu__nav-link">Expériences</router-link>
      </li>
      <li class="menu__nav-item">
        <router-link href="/contact" class="menu__nav-link">Contact</router-link>
      </li>
    </ul>
  </div>

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

.menu-btn {
    display: none;
    position: absolute;
    top: 20px;
    right: 20px;
    width: 50px;
    height: 50px;
    cursor: pointer;
    z-index: 1000;
  }

  .menu-btn__burger {
    width: 50px;
    height: 6px;
    background-color: var(--text);
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(255, 101, 47, 0.2);
    transition: all 0.3s ease;
  }

  .menu-btn__burger::before,
  .menu-btn__burger::after {
    content: "";
    position: absolute;
    width: 50px;
    height: 6px;
    background-color: var(--text);
    border-radius: 5px;
    box-shadow: 0 2px 5px rgba(255, 101, 47, 0.2);
    transition: all 0.3s ease;
  }

  .menu-btn__burger::before {
    transform: translateY(16px);
  }

  .menu-btn__burger::after {
    transform: translateY(32px);
  }

  .menu-btn.open .menu-btn__burger {
    transform: translate(-50px, 20px);
    background-color: transparent;
    box-shadow: none;
  }

  .menu-btn.open .menu-btn__burger::before {
    transform: rotate(45deg) translate(35px, -35px);
  }

  .menu-btn.open .menu-btn__burger::after {
    transform: rotate(-45deg) translate(35px, 35px);
  }

  .menu {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    clip-path: circle(0px at 100% -10%);
    background-color: var(--primary);
    transition: all 0.3s ease;
    z-index: 999;
  }

  .menu.open {
    clip-path: circle(1400px at 100% -10%);
  }

  .menu__nav {
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    text-align: center;
    width: 100%;
  }

  .menu__nav-item {
    list-style: none;
    margin-bottom: 20px;
  }

  .menu__nav-link {
    text-decoration: none;
    color: var(--text);
    font-weight: bold;
    font-size: 1.2rem;
    transition: color 0.3s ease;
  }

  .menu__nav-link:hover {
    color: var(--secondary);
  }

  @media screen and (max-width: 768px) {
    .menu-btn {
      display: flex;
    }

    .navbar .right {
      display: none;
    }
  }

</style>

