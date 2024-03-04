<template>
    <div class="cart">
      <h2>Cart</h2>
      <div v-for="flower in props.cart" :key="flower.name" class="card">
        <h3>{{ flower.name }}</h3>
      </div>
      <div>
        <h3 class="total"> Total = ${{ TotalCost() }}</h3>
      </div>
    </div>
  </template>
  
  <script setup>
  import { defineProps } from 'vue';
  
  const props = defineProps({ cart: Array })
  
  // Calculate total cost method
  const TotalCost = () => {
    return props.cart.reduce((total, flower) => total + flower.price)
  }
  </script>
  
  

<style  scoped>

.total {
  font-weight: bold;
}

.card {
  display: flex;
  border-radius: 5px;
  margin-bottom: 10px;
}


</style>

