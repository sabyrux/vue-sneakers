<script setup lang="ts">
// import AppDrawer from './components/AppDrawer.vue'
import AppHeader from './components/AppHeader.vue'
import CardList from './components/CardList.vue'
</script>

<template>
  <!-- <AppDrawer /> -->
  <main class="bg-white w-270 mx-auto my-14 rounded-xl shadow-xl">
    <h1 class="visually-hidden">Vue Sneakers - Магазин лучших кроссовок</h1>
    <AppHeader />
    <section class="flex flex-col gap-8 p-12">
      <div class="flex justify-between items-center">
        <h2 class="text-[32px] font-bold">Все кроссовки</h2>
        <div class="flex gap-4">
          <select class="py-2 px-3 border border-gray-300 rounded-md outline-none">
            <option value="">По названию</option>
            <option value="">По цене (дешевые)</option>
            <option value="">По цене (дорогие)</option>
          </select>
          <div class="relative">
            <img
              class="absolute left-4 top-3"
              src="/search.svg"
              alt="Search"
              width="14"
              height="14"
              loading="lazy"
            />
            <input
              class="border border-gray-300 rounded-md py-2 pl-11 pr-4 outline-none focus:border-gray-400"
              type="text"
              placeholder="Поиск..."
            />
          </div>
        </div>
      </div>
      <CardList />
    </section>
  </main>
</template>
