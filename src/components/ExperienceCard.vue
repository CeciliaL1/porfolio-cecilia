<script setup lang="ts">
import { Education } from '@/models/Education';

defineProps<{ heading: string, array:Education[] }>()

const singleDiv = 'single-div'

</script>

<template>
<section>

    <h1>{{ heading }}</h1>

    <div v-for="a in array">
    <div v-bind:class="singleDiv">
        <h4>{{ a.education }}</h4>
        <h4>{{ a.school }}</h4>
    </div>
    <h5>{{ a.duration }}</h5>
    <p>{{ a.competencies }}</p>
    </div>
    
</section>

</template>

<style scoped lang="scss">

section {
    box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
    padding: 10px;
margin: 50px;
    h1{
        text-align: center;
    }
    
    div{
        h5{
            margin-top: 5px;
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
    gap: 10px;
}
}

</style>