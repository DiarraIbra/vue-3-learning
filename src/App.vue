<script setup>
import { ref } from 'vue'
import ProductDisplay from '@/components/ProductDisplay.vue'
const desc=ref("je suis une description")
const cart = ref([])
const premium = ref(true)

const updateCart = (id) => {
  cart.value.push(id)
}
</script>
  
<template>
  <p>Ma description est <strong>{{ desc }}</strong></p>
  <div class="nav-bar"></div>
  <div class="cart">Cart({{ cart.length }})</div>
  <ProductDisplay :premium="premium" @add-to-cart="updateCart"></ProductDisplay>
</template>