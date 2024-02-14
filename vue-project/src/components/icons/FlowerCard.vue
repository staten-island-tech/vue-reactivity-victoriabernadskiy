<template>
    <div>
        <h1>{{ Flowers.name }}</h1>
        <img :src="Flowers.img" alt="">
        <h2>{{ Flowers.price }}</h2>
        <h2>{{ clicked }}</h2>
        <button @click="increment">Click me</button>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props = defineProps({
    Flowers: Object,
});
//clicker logic
const clicked = ref(0);
function increment(){
clicked.value++
} 

</script>

<style  scoped>
img {
    width: 150px;
    display: flex;
    flex-direction: row;
    margin: auto 0;
}
</style>
