<template>
    <div>
        <h1>{{ Destination.name }}</h1>
        <img :src="Destination.img" alt="">
        <h2>{{ Destination.price }}</h2>
        <button @click="increment">Add to Cart</button>
    </div>
</template>

<script setup>
import {ref} from "vue";
const props = defineProps({
    Destination: Object,
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
    justify-content: center;
}
</style>
