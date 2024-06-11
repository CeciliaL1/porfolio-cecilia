<script setup lang="ts">
import { ref } from 'vue';
import { Competence } from '../models/Competence';
import ProgressBar from './ProgressBar.vue';

const competencies = ref<Competence[]>([
    new Competence('JavaScript', 6),
    new Competence('TypeScript', 5),
    new Competence('HTML/CSS', 8),
    new Competence('Vue', 4),
    new Competence('node.js', 6),
    new Competence('MongoDB', 3),
    new Competence('MySQL', 3 )
]);


</script>

<template>
    <div class="container">
        <div class="about-me-container">
            <h3>Who am I?</h3>
            <div class="about-me-div">
            <img src="/images/cecilia.jpg" alt="profile picture on a woman">
                    <div>
                        <p>I am a person who likes challenges and loves to be creative. My family is a central part of my life, and we often spend time together through various activities, often in nature, discovering new or old nature reserves.</p>
                        <p>I also enjoy cooking and use cooking and baking as a way to express my creativity and share joy with those I love. I always strive for personal development and to learn new things. Every day is an opportunity to grow and improve myself.</p>
                        <p>By challenging myself in different aspects of life, I continue to develop and reach new heights.</p>        
                    </div>   
            </div>
        </div>

        <div class="competencies-container">
            <h3>Competencies</h3>

                <div class="competence" v-for="comp in competencies" >
                    <div>{{ comp.type }}</div>
                    <div><ProgressBar :value="comp.rate" /></div>
                </div>
        </div>
    </div>

   
</template>

<style scoped lang="scss">
@import '../assets/_variables';

.container {
    position: relative;
    z-index: 4;
    display: flex;
    flex-wrap: wrap;
    gap: 50px;
    font-family:monospace;
   

    .about-me-container{
        text-align: center;

        h3{
            color: $primary-color;
            font-family: 'raleway';
            font-size: 1.2rem;
        }

        .about-me-div {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: center;
        margin-top: 10px;
        gap: 50px;

        img{
            margin-top: 5px;
            height: 200px;
            width: auto;
            box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
        }

     
        p {
            margin-top: 20px;
            color: $primary-color;
            text-align: left;
            width: 350px;
            font-size: 1rem;
        }
    }
    }

    .competencies-container {
        margin-left: 50px;
           width: 300px;
           
            
           .competence {
            margin-top: 30px;
            display: flex;
            flex-direction: row;
            gap: 40px;
            justify-content: space-between;
            margin-bottom: 20px;
            font-size: 1.1rem;
            font-weight: 600;
            color: $hover-color;
           }
          
        h3{
            color: $primary-color;
            font-family: 'raleway';
            font-size: 1.2rem;
        }
    }

    
}
</style>