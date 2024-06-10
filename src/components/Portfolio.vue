<script setup lang="ts">
import { ref } from 'vue';
import { Project } from '../models/Project'

const projects = ref<(Project[])>([
    new Project('Webbshop', 'https://cecilial1.github.io/Gottfrids-Munkar/', 'A Fictiv webbshop in the course JavaScript Basics'),
    new Project('Phobia Quiz', 'https://github.com/CeciliaL1/PhobiaQuiz', 'A quiz about phobias from the course JavaScript Bascis'),
    new Project('To the moon', 'https://cecilial1.github.io/Kundprojekt/', 'A one pager from the course HTML/CSS'),
    new Project('Interactive rating', 'https://calm-sea-02ea92d03.5.azurestaticapps.net/', 'Small rating component made with Frontend Mentor'),
])

</script>

<template>
    <div class="grid-container">
        <div class="single-item" v-for="project in projects">
            <a :href="project.link" target="_blank">{{ project.title }}</a>
            <p>{{ project.desc }}</p>
        </div>

    </div>


</template>

<style scoped lang="scss">

.grid-container {
    border: 2px solid red;
    display: grid;
}

</style>