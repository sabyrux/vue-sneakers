<script setup lang="ts">
import DrawerHeader from './DrawerHead.vue'
import CartList from './CartList.vue'
import DrawerFoot from './DrawerFoot.vue'
</script>

<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <aside class="bg-white w-1/4 h-full fixed right-0 top-0 z-20 p-8 flex flex-col gap-8">
    <DrawerHeader />
    <CartList />
    <DrawerFoot />
  </aside>
</template>
