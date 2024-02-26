<template>
  <div>
    <DestCard v-for="destination in destinations" 
    :key="destination.name"
    :Destination="destination"
    @poop="addToCart(destination)"
    />
  </div>
  </template>
  
  <script setup>
  import DestCard from '@/components/icons/DestCard.vue';
  const destinations = [
  {
    "name": "Baby's Breath",
    "price": 1300,
    "color": "White",
    "significance": "Innocence",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2018/09/shutterstock_280568069.jpg"
  },
  {
    "name": "Delphinium",
    "price": 800,
    "color": "Blue",
    "significance": "Open Heart",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Delphium.png"
  },
  {
    "name": "Forget Me Not",
    "price": 1200,
    "color": "Blue",
    "significance": "True Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/forget-me-not-.jpg"
  },
  {
    "name": "Gardenia",
    "price": 900,
    "color": "White",
    "significance": "Purity and Sweetness",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Gardenia.jpg"
  },
  {
    "name": "Hydrangea",
    "price": 400,
    "color": "Blue, Pink, Purple, White",
    "significance": "Heartfelt Emotions",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Hydrangeas.jpg"
  },
  {
    "name": "Lavender",
    "price": 800,
    "color": "Purple",
    "significance": "Devotion",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Lavender.jpg"
  },
  {
    "name": "Peony",
    "price": 800,
    "color": "Pink, White, Red, Coral",
    "significance": "Romance and Prosperity",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Peony1.jpg"
  },
  {
    "name": "Rose",
    "price": 800,
    "color": "Various",
    "significance": "Love, Beauty, Courage",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/spray-roses.jpg"
  }
]

var cart = []

function addToCart(flower){
  cart.push(flower)
  console.log(cart)
}


  
        //design a flower
        //vue store
          
  </script>
  
  <style scoped>
  
  </style>
