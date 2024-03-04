<template>
    <div class="item">
        <h1>{{ Item.name }}</h1>
        <img :src="Item.img" alt="">
        <h2>${{ Item.price }}</h2>
        <h2>Color: {{ Item.color }}</h2>
        <h2>Meaning: {{ Item.significance }}</h2>
        <button id="btn" @click="$emit('poop')">Add to Cart</button>
    </div>
  
</template>

<script setup>
import {ref} from 'vue';
const props = defineProps({
    Item: Object,
});
const emit = defineEmits([
"poop"
])
//clicker logic
const clicked = ref(0);


</script>

<style  scoped>
img {
    display: flex;
    flex-direction: row;
    margin: auto 0;
    max-width: 100px;
    margin-right: 5px;
    border: 1px solid #134b0a;
}
.item {
  display: flex;
  flex-wrap: wrap;
  flex-direction: column;
  align-items: baseline;
  justify-content: space-between;
  padding: 50px;
  border-bottom: 5px solid #ddd;
  border: 5px solid #5c3018;
  margin: 30px;
  background-color: rgb(245, 229, 210);
  color: black;
  flex: 0 0 calc(33.33% - 20px);
  font-family: 'Josefin Sans', sans-serif;
}

#btn {
  background-color: white;
  border: 2px solid black;
  box-shadow: 0 5px 15px rgba(0, 0, 0, 0.3);
  transition: transform 0.2s, box-shadow 0.2s;
}

#btn:hover {
  transform: translateY(-2px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.4);
}


</style>
