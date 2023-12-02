<script setup>
import {onMounted, ref} from 'vue';
import {
  AmbientLight, Color,
  PerspectiveCamera,
  PointLight,
  Scene,
  WebGLRenderer
} from "three";
import {GLTFLoader} from 'three/examples/jsm/loaders/GLTFLoader.js';


let renderer = null;
const experience = ref(null);
const scene = new Scene();
scene.background = new Color(getComputedStyle(document.body).getPropertyValue('--background'));

let camera = new PerspectiveCamera(75,
    window.innerWidth / window.innerHeight,
    0.1,
    1000);
camera.position.z = 6;
camera.position.y = 4;

scene.add(camera);

// Ajouter une lumière ambiante
const light = new PointLight(0xffffff, 1, 100);
light.position.set(5, 5, 5);
scene.add(light);

const ambientLight = new AmbientLight(0xffffff, 3);
scene.add(ambientLight);

// on charge le model GLTF qui est dans les assets
const loader = new GLTFLoader();
let planet = null;
loader.load(
    'https://raw.githubusercontent.com/Tresjs/assets/main/models/gltf/low-poly/planet.gltf',
    (gltf) => {
      planet = gltf.scene;
      planet.scale.set(1.5, 1.5, 1.5);
      planet.position.x = 3;
      planet.position.y = 4;
      scene.add(planet);
    }
);

function updateRenderer() {
  renderer = new WebGLRenderer({
    canvas: experience.value,
    antialias: true,
  });
  renderer.setSize(window.innerWidth, window.innerHeight);
  renderer.render(scene, camera);
}

function updateCamera() {
  camera.aspect = window.innerWidth / window.innerHeight;
  camera.updateProjectionMatrix();
}

const loop = () => {
  renderer.render(scene, camera);
  requestAnimationFrame(loop);

  if (planet) {
    planet.rotation.y += 0.01;
    planet.rotation.x += 0.01;
  }
};

onMounted(() => {
  updateRenderer();
  updateCamera();

  loop();

  window.addEventListener('resize', () => {
    updateCamera();
    updateRenderer();
  });
});
</script>

<template>
  <canvas ref="experience" class="experiences"></canvas>
</template>

<style>
.experiences {
  position: absolute;
  top: 0;
  left: 0;
  z-index: -1;
}
</style>
