<script setup lang="ts">
import { onMounted } from 'vue';

 defineProps<{value: number}>();

onMounted(() => {

})
</script>

<template>

   <span class="container"> <span class="bar" :style="{ width: value*10 + '%' }"></span></span>

</template>

<style scoped lang="scss">
@import '../assets/_variables';
.container {
    display: block;
    width: 100px;
    height: 20px;
    background-color: $hover-color;
    border-radius: 20px;

}

.bar {
    display: block;
    width: 100px;
    height: 20px;
    background-color: $secondary-color;
    border-radius: 20px;
    box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;
}
</style>