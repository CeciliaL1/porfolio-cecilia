<script setup lang="ts">
let menyOptions = ['About me', 'Education', 'Work experience', 'Other']

</script>

<template>
<header>
<nav>
    <ul>
        <li v-for="option in menyOptions">{{ option }}</li>
    </ul>
</nav>

</header>

</template>

<style scoped lang="scss">
@import '../assets/_variables.scss';
nav {
    display: flex;
    align-items: center;
}
ul{
    display: flex;
    flex-direction: row;
    gap: 11px;
    padding: 15px;
    margin: 10px;
    margin-top: 20px;
  
   &:hover {
    background-color: $hover-background-color;
    border-radius: 10px;
    box-shadow: rgba(100, 100, 111, 0.2) 0px 7px 29px 0px;

   }
   
    li{
        font-family: "Raleway", sans-serif;
        list-style: none;
        font-size: 0.9rem;
        cursor: pointer;
        &:hover {
            background-color: #eae5df;      
        }
    }
}


</style>