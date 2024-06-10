<script setup lang="ts">


</script>


<template>
    <div class="background-div"></div>
   
    <div class="background-image"></div>
</template>

<style scoped lang="scss">
@import '../assets/_variables';
.background-image{
    background-image: linear-gradient(rgba(24, 24, 24, 0.4), rgba(0, 0, 0, 0.6)), url("/images/IMG_1982-modified.JPEG");
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 70% 13%;
    width: 100%;
    min-height: 45vh;
}
.background-div{
    position: absolute;
    top: 200px;
    width: 100%;
   
    background-color: $background-color;
    box-shadow: rgba(0, 0, 0, 0.25) 0px 54px 55px, rgba(0, 0, 0, 0.12) 0px -12px 30px, rgba(0, 0, 0, 0.12) 0px 4px 6px, rgba(0, 0, 0, 0.17) 0px 12px 13px, rgba(0, 0, 0, 0.09) 0px -3px 5px;  
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    p{
        color: white;
    }
}

@media screen and (min-width: 800px){
    .background-image {
        min-height: 20vh;
    }
}
@media screen and (min-width: 1100px){
    .background-image {
        min-height: 30vh;
    }
}
</style>