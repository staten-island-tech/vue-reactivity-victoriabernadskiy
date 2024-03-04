<template>
  <h1 class="title">Vik's Flower Shop</h1>
  <div class="cards">
    <FlowerCard v-for="item in items" 
    :key="item.name"
    :Item="item"
    @poop="addToCart(item)"
    class="item"
    />
  </div>
 <div>
  <MyCart class="cart" 
    :cart="cart"/>
  </div>
  </template>
 


  <script setup>
  import FlowerCard from '@/components/icons/FlowerCard.vue';
  import MyCart from '@/components/MyCart.vue';
  import { ref } from 'vue'
  
  const items = [
  {
    "name": "Baby's Breath",
    "price": 7.25,
    "color": "White",
    "significance": "Innocence",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2018/09/shutterstock_280568069.jpg"
  },
  {
    "name": "Delphinium",
    "price": 8.99,
    "color": "Blue",
    "significance": "Open Heart",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Delphium.png"
  },
  {
    "name": "Forget Me Not",
    "price": 3.99,
    "color": "Blue",
    "significance": "True Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/forget-me-not-.jpg"
  },
  {
    "name": "Gardenia",
    "price": 7.99,
    "color": "White",
    "significance": "Purity and Sweetness",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Gardenia.jpg"
  },
  {
    "name": "Hydrangea",
    "price": 9.99,
    "color": "Blue, Pink, Purple, White",
    "significance": "Heartfelt Emotions",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Hydrangeas.jpg"
  },
  {
    "name": "Lavender",
    "price": 5.99,
    "color": "Purple",
    "significance": "Devotion",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Lavender.jpg"
  },
  {
    "name": "Peony",
    "price": 4.99,
    "color": "Pink, White, Red, Coral",
    "significance": "Romance and Prosperity",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Peony1.jpg"
  },
  {
    "name": "Rose",
    "price": 11.99,
    "color": "Various",
    "significance": "Love, Beauty, Courage",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/spray-roses.jpg"
  },
  {
    "name": "Tulip",
    "price": 6.99,
    "color": "Red, Yellow, Pink, White, Purple",
    "significance": "Perfect Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Tulips12.jpg"
  },
  {
    "name": "Daisy",
    "price": 5.99,
    "color": "White, Yellow",
    "significance": "Loyal Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/daisies.jpg"
  },
  {
    "name": "Sunflower",
    "price": 7.99,
    "color": "Yellow",
    "significance": "Adoration, Loyalty",
    "img": "https://www.almanac.com/sites/default/files/styles/or/public/image_nodes/sunflower-1627193_1920.jpg?itok=td7mL8qA"
  },
  {
    "name": "Orchid",
    "price": 10.99,
    "color": "Various",
    "significance": "Love, Beauty, Strength",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Orchid.jpg"
  },
  {
    "name": "Carnation",
    "price": 4.99,
    "color": "Various",
    "significance": "Love, Fascination",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/04/Blushcarnation.png"
  },
]

let cart = ref([])

function addToCart(flower){
  cart.value.push(flower)
  console.log(cart.value)
}


  
   
  </script>
  
  <style scoped>
  
  .cart {
  gap: 20px;
  padding: 20px;
  background-color: #f9f9f9;
  border: 3px solid #000000;
  border-radius: 5px;
  position: fixed;
  right: 110px;
  top: 30px;
  width: 300px;
  color: black;
  font-family: 'Josefin Sans', sans-serif;
}

.cards{
  display: flex;
  flex-wrap: wrap;
  flex-direction: row;
  
}

.title {
  position: relative;
  top: 330px;
  left: 1050px;
  color: rgb(0, 0, 0);
  font-family: 'Josefin Sans', sans-serif;
  font-size: 50px;
  text-shadow: 2px 2px 4px rgb(17, 78, 8), 0 0 2em rgb(105, 61, 10), 0 0 0.4em rgb(88, 229, 41);
}


  </style>
