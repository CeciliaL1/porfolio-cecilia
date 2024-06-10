<script setup lang="ts">
import {ref } from 'vue'
import { PersonalInfo } from '../models/PersonalInfo';

const personalInfo = ref<PersonalInfo[]>([new PersonalInfo()]);
</script>

<template>
<div class="container">
    <div class="contact-info" v-for="info in personalInfo">
        <h2>{{ info.Firstname  }} {{ info.LastName }}</h2>
        <p>{{ info.City  }} {{ info.Region }}</p>
        <a :href="info.Phonenumber">0729681659</a> <br>
        <a :href="info.Email">cecilialepik@gmail.com</a>
    </div>

    <div class="icons">
        <a href="https://github.com/CeciliaL1" target="_blank"><i class="fa-brands fa-github"></i></a>
        <a href="www.linkedin.com/in/cecilia-lepik-70360b213"><i class="fa-brands fa-linkedin"></i></a>

    </div>

</div>
</template>

<style scoped lang="scss">
@import '../assets/_variables.scss';

.container {
    position: relative;
    top: 50px;
    display: flex;
    flex-direction: row;
    gap: 100px;

    .contact-info {
        font-family: raleway;
        color: $primary-color;

        h2 {
            margin: 0;
        }
        p {
            margin: 2px;
        }
        a {
            text-decoration: none;
            color: $secondary-color;
            cursor: pointer;
            &:hover {
                text-decoration: underline;
            }
        }
    }
    
    .icons{
        display: flex;
        flex-direction: column;
        justify-content: center;
        gap: 10px;
        
        a{
            font-size: 2.5rem;
            color: $secondary-color;
            text-decoration: none;
            &:hover {
                color: $primary-color;
            }
        }
    }
}

</style>