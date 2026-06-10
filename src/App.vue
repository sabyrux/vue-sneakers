<script setup lang="ts">
import AppDrawer from './components/AppDrawer.vue'
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
</script>

<template>
  <AppDrawer />
  <main class="bg-white w-270 mx-auto my-14 rounded-xl shadow-xl">
    <h1 class="visually-hidden">Vue Sneakers - Магазин лучших кроссовок</h1>
    <AppHeader />
    <section class="flex flex-col gap-8 p-12">
      <h2 class="text-[32px] font-bold">Все кроссовки</h2>
      <CardList />
    </section>
  </main>
</template>
