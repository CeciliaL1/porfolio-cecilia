<script setup lang="ts"></script>

<template>
  
    <div class="container">
        <div class="container-2">
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

        <div class="container-2">
            <h3>Competencies</h3>

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
    gap: 40px;
    font-family:monospace;

    .container-2 {
        text-align: center;
      
    }

    .about-me-div {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-around;
        align-items: center;
    
        margin-top: 10px;
        gap: 30px;

        img{
            margin-top: 5px;
            height: 300px;
            width: auto;
            box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
        
        }

        p {
            margin-top: 20px;
            color: $primary-color;
            text-align: left;
            width: 400px;
            font-size: 1rem;
        }
    }
}




</style>