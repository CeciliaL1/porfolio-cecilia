<script setup lang="ts"></script>

<template>
     <div class="quote-container">
        <blockquote>"Learning is a journey, not a destination. Every step you take in acquiring knowledge and skills is a step towards your personal growth and development."
        </blockquote>
    </div>
</template>

<style scoped lang="scss">
@import '../assets/_variables';
.quote-container{
    position: absolute;
    top: 95px;
    
    z-index: 4;

    width: 370px;
  
    blockquote{
        text-align: center;
        font-family:monospace;
        font-size: 0.9rem;
        color: $secondary-color;
        opacity: 0.9;
    }
}

@media screen and (min-width: 700px){
    .quote-container{
        left: 450px;
    }
}
@media screen and (min-width: 1100px){
    .quote-container{
        left: 20px;
        top: 150px;
        width: 100%;
    }
    
}
</style>