<script setup lang="ts">
import CartItem from './CartItem.vue'

const carts = [
  {
    id: 1,
    imgSrc: '/sneakers/sneakers-2.jpg',
    title: 'Мужские Кроссовки Nike Air Max 270',
    price: 12999,
  },
  {
    id: 1,
    imgSrc: '/sneakers/sneakers-4.jpg',
    title: 'Мужские Кроссовки Nike Air Max 270',
    price: 8499,
  },
]
</script>

<template>
  <ul class="flex flex-col gap-5 grow overflow-y-auto">
    <li v-for="cart in carts" :key="cart.id">
      <CartItem v-bind="cart" />
    </li>
  </ul>
</template>
