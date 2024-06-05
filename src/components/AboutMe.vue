<script setup lang="ts">

const fullName = 'Cecilia Lepik';
const city = 'Hofterup'
const region = 'Skåne';
const email = 'cecilialepik@gmail.com';
const phoneNumber = '0729681659';

//css - class
const contactDiv ='contact-div'
const hissPitch = 'hiss-pitch'
</script>

<template>
<div v-bind:class="contactDiv">

    <img src="../../public/images/cecilia.jpg" alt="profile picture on a woman">
    <div>
        <h3> {{ fullName }}</h3>
        <span>{{ city }}</span><span>, </span><span>{{ region }}</span> <br>
        <a v-bind:href="email">{{ email }}</a> <br>
        <a v-bind-href="phoneNumber">0729681659</a>
    </div>

   
</div>

<div v-bind:class="hissPitch">

</div>

</template>



<style scoped lang="scss">

.contact-div {
    h3{
        font-family: "Rubik", sans-serif;
        margin-bottom: 7px;
        font-size: 1.5rem;
    }
    font-family: "Raleway", sans-serif;
    margin-top: 10px;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    gap: 30px;
    margin-left: 80px;

    div{
        margin-top: 25px;
    }
    
    img{
        margin-top: 25px;
        height: 300px;
        width: auto;
        box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
  
    }
}

</style>