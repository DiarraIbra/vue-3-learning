<script setup>
import { ref } from 'vue'
import ProductDisplay from '@/components/ProductDisplay.vue'
const cart = ref([])
const premium = ref(true)
import socksGreen from './assets/images/socks_green.jpeg'
const image =ref(socksGreen)
const url_link = 'https://vuejs.org/'
const inStock = ref(true)
const onSale = ref(false)
const updateCart = (id) => {
  cart.value.push(id)
}
</script>
  
<template>
  <div class="product-image">
    <img :src="image" alt="">
    <a :href="url_link" target="_blank">Lien vers le site de Vue</a>
    <p v-if="inStock">En stock</p>
    <p v-else>En rupture de stock</p>
    <p v-if="onSale">Actuellement en solde.</p>
    <p v-else>Pas de solde disponible actuellement.</p>
  </div>
  <div class="nav-bar"></div>
  <div class="cart">Cart({{ cart.length }})</div>
  <ProductDisplay :premium="premium" @add-to-cart="updateCart"></ProductDisplay>
</template>