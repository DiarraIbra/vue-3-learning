<script setup>
import { ref } from 'vue'
import ProductDisplay from '@/components/ProductDisplay.vue'
const cart = ref([])
const premium = ref(true)
import socksGreen from './assets/images/socks_green.jpeg'
const image =ref(socksGreen)
const updateCart = (id) => {
  cart.value.push(id)
}
</script>
  
<template>
  <div class="product-image">
<img :src="image" alt="">
  </div>
  <div class="nav-bar"></div>
  <div class="cart">Cart({{ cart.length }})</div>
  <ProductDisplay :premium="premium" @add-to-cart="updateCart"></ProductDisplay>
</template>