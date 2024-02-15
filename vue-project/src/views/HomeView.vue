<template>
  <div>
    <DestCard v-for="destination in destinations" 
    :key="destination.name"
    :Destination="destination"
    @click="addToCart(destination)"
    />
  </div>
  </template>
  
  <script setup>
  import DestCard from '@/components/icons/DestCard.vue';
  const destinations = [
          {
            name: "Baby's Breath",
            International: true,
            price: 1300,
            img: "https://www.weloveflorists.com/wp-content/uploads/2018/09/shutterstock_280568069.jpg;"
          },
          {
            name: "Delphinium",
            International: true,
            price: 800,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/Delphium.png;"
          },
          {
            name: "Forget Me Not",
            International: true,
            price: 1200,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/forget-me-not-.jpg;"
          },
          {
            name: "Gardenia",
            International: false,
            price: 900,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/Gardenia.jpg"
          },
          {
            name: "Hydrangea",
            International: false,
            price: 400,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/Hydrangeas.jpg;"
          },
          {
            name: "Lavender",
            International: true,
            price: 800,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/Lavender.jpg;"
          },
          {
            name: "Peony",
            International: true,
            price: 800,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/Peony1.jpg;"
          },
          {
            name: "Rose",
            International: true,
            price: 800,
            img: "https://www.weloveflorists.com/wp-content/uploads/2019/09/spray-roses.jpg;"
          },
        ]
  
        //design a flower
        //vue store
          
  </script>
  
  <style scoped>
  
  </style>
