<script setup lang="ts">
import { ref } from 'vue'
import CardItem from './CardItem.vue'

const cards = ref([
  {
    id: 1,
    imgSrc: '/sneakers/sneakers-1.jpg',
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 12999,
    isLiked: true,
    isAdded: false,
  },
  {
    id: 2,
    imgSrc: '/sneakers/sneakers-2.jpg',
    title: 'Мужские Кроссовки Nike Air Max 270',
    price: 12999,
    isLiked: false,
    isAdded: true,
  },
  {
    id: 3,
    imgSrc: '/sneakers/sneakers-3.jpg',
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 8499,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 4,
    imgSrc: '/sneakers/sneakers-4.jpg',
    title: 'Кроссовки Puma X Aka Boku Future Rider',
    price: 8999,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 5,
    imgSrc: '/sneakers/sneakers-5.jpg',
    title: 'Мужские Кроссовки Under Armour Curry 8',
    price: 15199,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 6,
    imgSrc: '/sneakers/sneakers-6.jpg',
    title: 'Мужские Кроссовки Nike Kyrie 7',
    price: 11299,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 7,
    imgSrc: '/sneakers/sneakers-7.jpg',
    title: 'Мужские Кроссовки Jordan Air Jordan 11',
    price: 10799,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 8,
    imgSrc: '/sneakers/sneakers-8.jpg',
    title: 'Мужские Кроссовки Nike LeBron XVIII',
    price: 16499,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 9,
    imgSrc: '/sneakers/sneakers-9.jpg',
    title: 'Мужские Кроссовки Nike Lebron XVIII Low',
    price: 13999,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 10,
    imgSrc: '/sneakers/sneakers-10.jpg',
    title: 'Мужские Кроссовки Nike Blazer Mid Suede',
    price: 8499,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 11,
    imgSrc: '/sneakers/sneakers-11.jpg',
    title: 'Кроссовки Puma X Aka Boku Future Rider',
    price: 8999,
    isLiked: false,
    isAdded: false,
  },
  {
    id: 12,
    imgSrc: '/sneakers/sneakers-12.jpg',
    title: 'Мужские Кроссовки Nike Kyrie Flytrap IV',
    price: 11299,
    isLiked: false,
    isAdded: false,
  },
])

const handleToggleLike = (id: number) => {
  const card = cards.value.find((c) => c.id === id)

  if (card) {
    card.isLiked = !card.isLiked
  }
}

const handleToggleAdd = (id: number) => {
  const card = cards.value.find((c) => c.id === id)

  if (card) {
    card.isAdded = !card.isAdded
  }
}
</script>

<template>
  <ul class="grid grid-cols-4 gap-4">
    <li class="flex" v-for="card in cards" :key="card.id">
      <CardItem v-bind="card" @toggle-like="handleToggleLike" @toggle-add="handleToggleAdd" />
    </li>
  </ul>
</template>
