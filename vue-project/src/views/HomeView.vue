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
  import MyCart from '@/views/MyCart.vue'
  <MyCart v-if= "length > 0" />
  const destinations = [
  {
    "name": "Baby's Breath",
    "price": "$7.25",
    "color": "White",
    "significance": "Innocence",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2018/09/shutterstock_280568069.jpg"
  },
  {
    "name": "Delphinium",
    "price": "$8.00",
    "color": "Blue",
    "significance": "Open Heart",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Delphium.png"
  },
  {
    "name": "Forget Me Not",
    "price": "$3.50",
    "color": "Blue",
    "significance": "True Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/forget-me-not-.jpg"
  },
  {
    "name": "Gardenia",
    "price": "$7.99",
    "color": "White",
    "significance": "Purity and Sweetness",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Gardenia.jpg"
  },
  {
    "name": "Hydrangea",
    "price": "$9.00",
    "color": "Blue, Pink, Purple, White",
    "significance": "Heartfelt Emotions",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Hydrangeas.jpg"
  },
  {
    "name": "Lavender",
    "price": "$5.99",
    "color": "Purple",
    "significance": "Devotion",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Lavender.jpg"
  },
  {
    "name": "Peony",
    "price": "$4.50",
    "color": "Pink, White, Red, Coral",
    "significance": "Romance and Prosperity",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Peony1.jpg"
  },
  {
    "name": "Rose",
    "price": "$11.99",
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


  
   
  </script>
  
  <style scoped>
  
  </style>
