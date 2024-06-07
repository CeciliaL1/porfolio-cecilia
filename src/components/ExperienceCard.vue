<script setup lang="ts">
import { ref } from 'vue';
import { Competencie } from '@/models/Competencies';

const educationArray = ref<Competencie[]>([
  new Competencie('Front End Developer', 'Medieinstitutet', 'December 2023 - Graduation july 2025', 'HTML & CSS/SASS, Javascript, TypeScript, Vue & React, node.js, MongoDB & MySQL, Git & Github'),
  new Competencie('Web development 1', 'NTI-gymnasiet', 'January 2022 - may 2022', 'HTML & CSS'),
  new Competencie('Programming 1', 'NTI-gymnasiet', 'Mars 2021 - May 2021', 'C#'),
  new Competencie('Skin therapist', 'Gilda Skolan', 'February 2018 - February 2019', 'Beauty treatments'),
  new Competencie('Assistant nurse', 'Kävlinge kommun', 'August 2014- December 2015', 'Taking vital signs, basic patient hygiene, mobility assistance, and infection control.'),
  new Competencie('Cybergymnasiet', 'Malmö', 'August 2010 - July 2013', 'High school, orientation photography')
]
)
const workExperienceArray = ref<Competencie[]>([
  new Competencie('Lenhud', 'Lund', 'September 2019 - January 2023', 'Working as a skin therapist'),
  new Competencie('Tite Hudvård', 'Malmö', 'February 2019 - September 2019', 'Working as a skin therapist'),
  new Competencie('Assisytant Nurse', 'Staffanstorp', 'September 2016 - July 2018', 'Elderly care, dementia patiens'),
  new Competencie('Assistant nurse', 'Kävlinge kommun', 'November 2015 - September 2016', 'Elderly care, Domestic service'),
  new Competencie('Assistant nurse', 'Lomma kommun', 'August 2013 - November 2015', 'Elderly care, dementia patiens'),
])

const singleDiv = 'single-div'

</script>

<template>
    <section>
        <div class="experience">

            <h1>Education</h1>

            <div v-for="a in educationArray">
                <div :class="singleDiv">
                    <h4>{{ a.title }}</h4>
                    <h4>{{ a.environment }}</h4>
            </div>
            <h5>{{ a.duration }}</h5>
            <p>{{ a.competencies }}</p>
            </div>

        </div>
        <div class="experience">

            <h1>Work experience</h1>

            <div v-for="a in workExperienceArray">
                <div :class="singleDiv">
                <h4>{{ a.title }}</h4>
                <h4>{{ a.environment }}</h4>
            </div>
            <h5>{{ a.duration }}</h5>
            <p>{{ a.competencies }}</p>
            </div>

        </div>
    </section>
</template>

<style scoped lang="scss">
@import '../assets/_variables';

section{
    font-family: monospace;
    display: flex;
    flex-direction: row;
    flex-wrap: wrap;
    justify-content: center;
    position: absolute;
    top: 300px;
    z-index: 4;
    
}

.experience {
    width: 400px;
    background-color: rgb(157, 156, 156);
    box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
    padding: 10px;
    margin: 20px;
    border-radius: 10px;
    h1{
        text-align: center;
        margin-bottom: 6px;
    }
    
    div{
        h5{
            margin: 0;
        }
        p{
            margin-top: 2px;
            margin-bottom: 6px;
        }
        div{
            h4{
                margin-bottom: 5px;
            }
        }
    }


    .single-div {
    display: flex;
    flex-direction: row;
    gap: 5px;
}
}

</style>