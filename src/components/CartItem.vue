<script setup lang="ts">
interface Props {
  imgSrc: string
  title: string
  price: number
}

const { imgSrc, title, price } = defineProps<Props>()
</script>

<template>
  <article
    class="flex items-center gap-4 rounded-[20px] p-5 border border-gray-200 transition hover:-translate-y-2 hover:shadow-xl"
  >
    <img :src="imgSrc" :alt="title" width="70" height="70" loading="lazy" />
    <div>
      <h3 class="text-sm">{{ title }}</h3>
      <span class="text-sm font-bold">{{ price.toLocaleString('ru-RU') }} тг.</span>
    </div>
    <img
      class="self-end transition hover:shadow-xl hover:scale-115 active:scale-90"
      src="/close.svg"
      alt="Delete"
      width="32"
      height="32"
      loading="lazy"
    />
  </article>
</template>
