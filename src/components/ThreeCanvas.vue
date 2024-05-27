<script setup>
import { onMounted, ref } from 'vue'
import {
    AmbientLight,
    Color,
    PerspectiveCamera,
    PointLight,
    Scene,
    WebGLRenderer,
} from 'three'
import { GLTFLoader } from 'three/examples/jsm/loaders/GLTFLoader.js'

let renderer = null
const experience = ref(null)
const scene = new Scene()
scene.background = new Color(
    getComputedStyle(document.body).getPropertyValue('--background')
)

let camera = new PerspectiveCamera(
    75,
    window.innerWidth / window.innerHeight,
    0.1,
    1000
)
camera.position.z = 7
camera.position.y = 5

scene.add(camera)

// Ajouter une lumière ambiante
const light = new PointLight(0xffffff, 1, 100)
light.position.set(5, 5, 5)
scene.add(light)

const ambientLight = new AmbientLight(0xffffff, 3)
scene.add(ambientLight)

// on charge le fichier glb qui est dans les assets
const loader = new GLTFLoader()
let car = null
loader.load('model/datsun_240z.glb', (glb) => {
    car = glb.scene
    car.scale.set(1.2, 1.2, 1.2)
    car.position.x = 3
    car.position.y = 3.5
    scene.add(car)
})

function updateRenderer() {
    renderer = new WebGLRenderer({
        canvas: experience.value,
        antialias: true,
    })
    renderer.setSize(window.innerWidth, window.innerHeight)
    renderer.render(scene, camera)
}

function updateCamera() {
    camera.aspect = window.innerWidth / window.innerHeight
    camera.updateProjectionMatrix()
}

const loop = () => {
    renderer.render(scene, camera)
    requestAnimationFrame(loop)

    if (car) {
        car.rotation.y += 0.001
    }
}

onMounted(() => {
    updateRenderer()
    updateCamera()

    loop()

    window.addEventListener('resize', () => {
        updateCamera()
        updateRenderer()
    })
})
</script>

<template>
    <canvas ref="experience" class="car"></canvas>
</template>

<style>
.car {
    position: absolute;
    top: 0;
    left: 0;
    z-index: -1;
}
</style>
