<template>
  <footer class="flex flex-col gap-6">
    <div class="flex flex-col gap-4">
      <div class="flex justify-between items-end gap-1.5">
        <div class="text-base">Итого:</div>
        <div class="flex-1 border-b border-dotted border-gray-400 bottom-1"></div>
        <div class="text-base font-semibold">21 498 тг.</div>
      </div>
      <div class="flex justify-between items-end gap-1.5">
        <div class="text-base">Налог 5%:</div>
        <div class="flex-1 border-b border-dotted border-gray-400 bottom-1"></div>
        <div class="text-base font-semibold">1 074 тг.</div>
      </div>
    </div>
    <button
      class="flex items-center justify-center gap-3 py-4.5 bg-[#9DD458] text-white text-base font-semibold rounded-[18px] cursor-pointer hover:bg-[#7FB140] active:bg-[#91D43D] transition-colors"
      type="button"
    >
      <span>Оформить заказ</span>
      <svg
        width="16"
        height="14"
        viewBox="0 0 16 14"
        fill="none"
        xmlns="http://www.w3.org/2000/svg"
      >
        <path
          d="M1 7H14.7143"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
        <path
          d="M8.71436 1L14.7144 7L8.71436 13"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
        />
      </svg>
    </button>
  </footer>
</template>
