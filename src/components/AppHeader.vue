<template>
  <header class="border-b border-gray-200 p-12">
    <div class="flex items-center justify-between">
      <a href="/" class="flex items-center gap-4">
        <img src="/logo.png" alt="Logo" width="40" height="40" />
        <div class="flex flex-col">
          <span class="font-bold text-xl/5">VUE SNEAKERS</span>
          <span>Магазин лучших кроссовок</span>
        </div>
      </a>
      <nav>
        <ul class="flex items-center gap-8">
          <li>
            <a
              href="/"
              class="flex items-center gap-2 font-semibold text-gray-500 hover:text-black transition-colors"
            >
              <img src="/nav-menu/cart.svg" alt="Корзина" width="18" height="18" />
              <span>1205 руб.</span>
            </a>
          </li>
          <li>
            <a
              href="/"
              class="flex items-center gap-2 font-semibold text-gray-500 hover:text-black transition-colors"
            >
              <img src="/nav-menu/heart.svg" alt="Закладки" width="18" height="18" />
              <span>Закладки</span>
            </a>
          </li>
          <li>
            <a
              href="/"
              class="flex items-center gap-2 font-semibold text-gray-500 hover:text-black transition-colors"
            >
              <img src="/nav-menu/profile.svg" alt="Профиль" width="18" height="18" />
              <span>Профиль</span>
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>
