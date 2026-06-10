<script setup lang="ts">
import DrawerHeader from './DrawerHeader.vue'
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
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <aside class="bg-white w-sm h-full fixed right-0 top-0 z-20 p-8 flex flex-col gap-8">
    <DrawerHeader />
    <ul class="flex flex-col gap-5">
      <li v-for="cart in carts" :key="cart.id">
        <CartItem v-bind="cart" />
      </li>
    </ul>
  </aside>
</template>
