<script setup lang="ts">
import { ref } from 'vue';
import { Project } from '../models/Project'

const projects = ref<(Project[])>([
    new Project('Advice generator', 'https://proud-island-03a3a0503.5.azurestaticapps.net/', 'Generates random advice from API using vue', true),
    new Project('Webbshop', 'https://cecilial1.github.io/Gottfrids-Munkar/', 'A Fictiv webbshop in the course JavaScript Basics', true),
    new Project('Phobia Quiz', 'https://github.com/CeciliaL1/PhobiaQuiz', 'A quiz about phobias from the course JavaScript Bascis', false),
    new Project('To the moon', 'https://cecilial1.github.io/Kundprojekt/', 'A one pager from the course HTML/CSS, ', true),
    new Project('Interactive rating', 'https://calm-sea-02ea92d03.5.azurestaticapps.net/', 'Small rating component made with Frontend Mentor', true),
    new Project('GridPainter', 'https://github.com/CeciliaL1/gridpainter', 'API and socket, a painting game where you can play in real time and chat', false),
    new Project('Unittesting', 'https://github.com/CeciliaL1/unittesting-assignment', 'Unittesting in provided code', false),
    new Project('Todo app', 'https://icy-wave-0be513203.5.azurestaticapps.net/', 'A todo app with vue.js', true)
])

</script>

<template>
    <div class="grid-container">
        <div class="single-item" v-for="project in projects">
            <a :href="project.link" target="_blank">{{ project.title }}</a>
            <p class="deployed">{{ project.deployed ? 'Deployed site' : 'Github Repo' }}</p>
            <p>{{ project.desc }}</p>
        </div>

    </div>


</template>

<style scoped lang="scss">
@import '../assets/_variables';

.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 10px;
    width: 80%;
    max-width: 900px;
    font-family: monospace;
    margin-top: 60px;
    margin-left: 30px;

    .single-item {
    width: 80%;
    background-color:  $hover-color;
    color: black;
    padding: 20px;
    text-align: center;
    border-radius: 5px;
    font-size: 1rem;

    a{
        text-decoration: underline;
        cursor: pointer;
        color: $secondary-color;
        font-weight: 600;
        &:hover{
            color: $background-color
        }

    }

    .deployed {
        font-size: 0.8rem;
    }
    }
}

</style>