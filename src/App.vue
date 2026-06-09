<script setup lang="ts">
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
</script>

<template>
  <div class="bg-white w-270 mx-auto my-14 rounded-xl shadow-xl">
    <AppHeader />
    <section class="flex flex-col gap-8 p-12">
      <h1 class="text-[32px] font-bold">Все кроссовки</h1>
      <CardList />
    </section>
  </div>
</template>
