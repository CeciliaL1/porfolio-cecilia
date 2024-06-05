<script setup lang="ts">
import MenyOptions from './components/MenyOptions.vue'
//import AboutMe from './components/AboutMe.vue'
//import ExperienceCard from './components/ExperienceCard.vue'
import { Competencie } from './models/Competencies'

const educationArray:Competencie[] = [
  new Competencie('Front End Developer', 'Medieinstitutet', 'December 2023 - Graduation july 2025', 'HTML & CSS/SASS, Javascript, TypeScript, Vue & React, node.js, MongoDB & MySQL, Git & Github'),
  new Competencie('Web development 1', 'NTI-gymnasiet', 'January 2022 - may 2022', 'HTML & CSS'),
  new Competencie('Programming 1', 'NTI-gymnasiet', 'Mars 2021 - May 2021', 'C#'),
  new Competencie('Skin therapist', 'Gilda Skolan', 'February 2018 - February 2019', 'Beauty treatments'),
  new Competencie('Assistant nurse', 'Kävlinge kommun', 'August 2014- December 2015', 'Taking vital signs, basic patient hygiene, mobility assistance, and infection control.'),
  new Competencie('Cybergymnasiet', 'Malmö', 'August 2010 - July 2013', 'High school, orientation photography')
]

const workExperienceArray:Competencie[] = [
  new Competencie('Lenhud', 'Lund', 'September 2019 - January 2023', 'Working as a skin therapist'),
  new Competencie('Tite Hudvård', 'Malmö', 'February 2019 - September 2019', 'Working as a skin therapist'),
  new Competencie('Assisytant Nurse', 'Staffanstorp', 'September 2016 - July 2018', 'Elderly care, dementia patiens'),
  new Competencie('Assistant nurse', 'Kävlinge kommun', 'November 2015 - September 2016', 'Elderly care, Domestic service'),
  new Competencie('Assistant nurse', 'Lomma kommun', 'August 2013 - November 2015', 'Elderly care, dementia patiens'),
]
</script>

<template>
  <MenyOptions />

<!-- CV
  <AboutMe />
  <ExperienceCard heading="Education" v-bind:array="educationArray" />
  <ExperienceCard heading="Work Experience" v-bind:array="workExperienceArray" />

-->
</template>

<style scoped>

</style>
