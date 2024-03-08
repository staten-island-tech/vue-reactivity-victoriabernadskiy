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
    "price": Number(4.55),
    "color": "White",
    "significance": "Innocence",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2018/09/shutterstock_280568069.jpg"
  },
  {
    "name": "Delphinium",
    "price": Number(8.99),
    "color": "Blue",
    "significance": "Open Heart",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Delphium.png"
  },
  {
    "name": "Forget Me Not",
    "price": Number(6.99),
    "color": "Blue",
    "significance": "True Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/forget-me-not-.jpg"
  },
  {
    "name": "Gardenia",
    "price": Number(7.99),
    "color": "White",
    "significance": "Purity and Sweetness",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Gardenia.jpg"
  },
  {
    "name": "Hydrangea",
    "price": Number(9.99),
    "color": "Blue, Pink, Purple, White",
    "significance": "Heartfelt Emotions",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Hydrangeas.jpg"
  },
  {
    "name": "Lavender",
    "price": Number(5.99),
    "color": "Purple",
    "significance": "Devotion",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Lavender.jpg"
  },
  {
    "name": "Peony",
    "price": Number(4.99),
    "color": "Pink, White, Red, Coral",
    "significance": "Romance and Prosperity",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Peony1.jpg"
  },
  {
    "name": "Rose",
    "price": Number(11.99),
    "color": "Various",
    "significance": "Love, Beauty, Courage",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/spray-roses.jpg"
  },
  {
    "name": "Tulip",
    "price": Number(6.99),
    "color": "Red, Yellow, Pink, White, Purple",
    "significance": "Perfect Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Tulips12.jpg"
  },
  {
    "name": "Daisy",
    "price": Number(5.99),
    "color": "White, Yellow",
    "significance": "Loyal Love",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/daisies.jpg"
  },
  {
    "name": "Sunflower",
    "price": Number(7.99),
    "color": "Yellow",
    "significance": "Adoration, Loyalty",
    "img": "https://www.almanac.com/sites/default/files/styles/or/public/image_nodes/sunflower-1627193_1920.jpg?itok=td7mL8qA"
  },
  {
    "name": "Orchid",
    "price": Number(10.99),
    "color": "Various",
    "significance": "Love, Beauty, Strength",
    "img": "https://www.weloveflorists.com/wp-content/uploads/2019/09/Orchid.jpg"
  },
  {
    "name": "Carnation",
    "price": Number(4.99),
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
  border: 1px solid #ddd;
  border-radius: 5px;
  position: fixed;
  right: 110px;
  top: 30px;
  width: 300px;
  color: black;
  font-family: 'Josefin Sans', sans-serif;
  border: 3px solid black;
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
