<script setup>
import { ref } from 'vue'
import ProductDisplay from '@/components/ProductDisplay.vue'
const cart = ref([])
const premium = ref(true)
// import socksGreen from './assets/images/socks_green.jpeg'
// const image =ref(socksGreen)
//const url_link = ref('https://vuejs.org/')
// const inStock = ref(true)
// const onSale = ref(false)
// const details = ref(['50% cotton', '30% wool', '20% polyester'])
// const variants=ref([
//   {
//     id: 2234,
//     color: 'green',
//     dispo:false
//   },
//   {
//     id: 2235,
//     color: 'blue',
//     dispo:true
//   }
// ])
// const tableau=ref(["vert","jaune","rouge"])
const updateCart = (id) => {
  cart.value.push(id)
}
// const cart_test=ref(0)
// const addToCartTest=()=> {
//   cart_test.value+=1
//   console.log(cart_test.value)
// }
// const decremeter=()=>{
//   if(cart_test.value <= 0) {
//     return alert('Le panier est vide')
//   }
//   cart_test.value-=1
// }
</script>
  
<template>
  <!-- <a :href="url_link" target="_blank">Lien vers le site de Vue</a> -->
  <!-- <div class="product-image">
    <img :src="image" alt="">
    <a :href="url_link" target="_blank">Lien vers le site de Vue</a>
    <p v-if="inStock">En stock</p>
    <p v-else>En rupture de stock</p>
    <p v-if="onSale">Actuellement en solde.</p>
    <p v-else>Pas de solde disponible actuellement.</p>
    <ul>
      <li v-for="detail in details">{{ detail }}</li>
    </ul>
    Voici la liste des couleurs disponibles sont :
    <ul>
      <li  v-for="variant in variants" :key="variant.id">
        <p v-if="variant.dispo">
         variant dispo  {{ variant.color }}
        </p></li>
    </ul>
    La couleur du drapeau du mali est : <div v-for="tab in tableau">{{ tab }}</div>
    <button @click="addToCartTest">Ajouter au panier</button>
    <button @click="decremeter">Enlever du panier</button>
    <span class="span-button">{{cart_test}}</span>
  </div> -->
  <div class="nav-bar"></div>
  <div class="cart">Cart({{ cart.length }})</div>
  <ProductDisplay :premium="premium" @add-to-cart="updateCart"></ProductDisplay>
</template>
<!-- <style>
.span-button{
  background-color: red;
  color: white;
  padding: 5px;
  margin-left: 20px;
  border-radius: 2px;
  cursor: pointer;
  width: 20%;
  display: block;
  margin: 20px auto;
  text-align: center;
}
</style> -->