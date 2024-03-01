<template>
    <div>
        <h1>{{ Destination.name }}</h1>
        <img :src="Destination.img" alt="">
        <h2>{{ Destination.price }}</h2>
        <h2>{{ Destination.color }}</h2>
        <button @click="$emit('poop')">Add to Cart</button>
    </div>
    <div>
        <h1></h1>
    </div>
</template>

<script setup>
import {ref} from 'vue';
const props = defineProps({
    Destination: Object,
});
const emit = defineEmits([
"poop"
])
//clicker logic
const clicked = ref(0);


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
