<script setup lang="ts">
import { ref } from 'vue';
import ExperienceCard from './ExperienceCard.vue';
import LandingPage from './LandingPage.vue';
import Home from './Home.vue'



const landingPage = () => {
    click.value = 'Home'
}

const handleMenuClick = (option: string) => {
    click.value = option;
    openMenu = ref(false);
    goHome = ref(false)
}

let goHome = ref(true)
let openMenu = ref(false);
let click = ref<string | null>(null)


let menyOptions = ['Home', 'Portfolio', 'CV', 'Contact']
let openMenuOptions = 'open-menu-options'
</script>

<template>
<header>
    <div class="header-div">
        <div @click="openMenu = !openMenu">
            <span></span>
            <span></span>
            <span></span>
        </div>
        <h1 @click="landingPage">Cecilia Lepik</h1>
    </div>
</header>
<nav>
    <div v-if="openMenu" v-bind:class="openMenuOptions">
        <ul>
            <li v-for="option in menyOptions" @click="handleMenuClick(option)">{{ option }}</li>
        </ul>
    </div>
</nav>

<div class="content">

<LandingPage />
<Home v-if="click === 'Home' || goHome" />
<ExperienceCard v-if="click === 'CV' "/>
</div>
</template>

<style scoped lang="scss">
@import '../assets/_variables.scss';
header{
    font-family: "Raleway", sans-serif;
    position: fixed;
    top: 0;
    z-index: 6;
    
    .header-div {
        display: flex;
        flex-direction: row;
        justify-content: space-around;
        gap: 30px;
        
        div {
            margin-left: 30px;
            margin-top: 32px;
            cursor: pointer;
        }
        span {
            display: block;
            position: relative;
            width: 30px;
            height: 5px;
            background-color: black;
            border-radius: 5px;
            box-shadow: rgba(109, 109, 109, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
        }
        :nth-child(1) {
            top: -3px;
        }

        :nth-child(3) {
            top: 3px;
        }

        h1 {
            text-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;
        }
    }
}

nav {
    .open-menu-options {
        position: fixed;
        top: 0;
        width: 100%;
        min-height: 100vh;
        background-color: rgba(56, 55, 55, 0.7);
        z-index: 5;

        ul{
            display: flex;
            flex-direction: column;
            flex-wrap: wrap;
            margin-top: 150px;
 
        li{
           
            font-family: "Raleway", sans-serif;
            color: rgb(136, 161, 153);
            text-transform: uppercase;
            letter-spacing: 4px;
            list-style: none;
            font-size: 0.9rem;
            font-weight: 800;
            margin: 6px;
            cursor: pointer;
            &:hover {
                color: rgb(105, 103, 103);
            }
        }
        }
    }
}

.content {
    
    display: flex;
    flex-wrap: wrap;
    justify-content: center;

}

</style>