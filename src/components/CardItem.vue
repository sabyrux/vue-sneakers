<script setup lang="ts">
interface Props {
  id: number
  imgSrc: string
  title: string
  price: number
  isLiked: boolean
  isAdded: boolean
}

const { id, imgSrc, title, price, isLiked, isAdded } = defineProps<Props>()

const emit = defineEmits<{
  (e: 'toggleLike', id: number): void
  (e: 'toggleAdd', id: number): void
}>()

const onLikeClick = () => {
  emit('toggleLike', id)
}

const onAddClick = () => {
  emit('toggleAdd', id)
}
</script>

<template>
  <article
    class="relative flex flex-col gap-3.5 py-6 px-7 w-56 rounded-[40px] border border-gray-200 transition hover:-translate-y-2 hover:shadow-xl cursor-pointer"
  >
    <img
      class="absolute cursor-pointer transition hover:shadow-xl hover:scale-115 active:scale-90"
      @click="onLikeClick"
      :src="isLiked ? '/heart/heart-fill.svg' : '/heart/heart-outline.svg'"
      alt="Unlike"
      width="32"
      height="32"
      loading="lazy"
    />
    <img :src="imgSrc" :alt="title" width="133" height="112" loading="lazy" />
    <h3 class="text-sm">{{ title }}</h3>
    <div class="flex justify-between items-center">
      <div class="flex flex-col">
        <span class="text-xs text-gray-400">Цена:</span>
        <span class="text-sm font-bold">{{ price.toLocaleString('ru-RU') }} тг.</span>
      </div>
      <img
        class="cursor-pointer transition hover:shadow-xl hover:scale-115 active:scale-90"
        @click="onAddClick"
        :src="isAdded ? '/cart/checked.svg' : '/cart/plus.svg'"
        alt="Add"
        width="32"
        height="32"
        loading="lazy"
      />
    </div>
  </article>
</template>
