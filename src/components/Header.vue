<script setup>
defineProps({
  totalPrice: Number,
})

const emit = defineEmits(['openDrawer'])
</script>

<template>
  <header class="flex justify-between border-b border-slate-200 px-10 py-8 flex-wrap">
    <router-link to="/">
      <div class="flex items-center gap-4">
        <img src="/logo2.png" alt="logo" class="w-10" />
        <div>
          <h2 class="text-xl font-bold uppercase">Best Shop</h2>
          <p class="text-slate-400">Магазин лучших кроссовок</p>
        </div>
      </div>
    </router-link>

    <ul class="flex items-center gap-10 flex-wrap md:my-5 sm:my-5 my-5">
      <li
        @click="() => emit('openDrawer')"
        class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black"
      >
        <img src="/cart.svg" alt="Cart" />
        <b>{{ totalPrice }} руб.</b>
      </li>

      <router-link to="/favorites">
        <li
          class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black relative count"
        >
          <img src="/heart.svg" alt="Cart" />
          <span>Избранное</span>
        </li>
      </router-link>

      <router-link to="/profile">
        <li class="flex items-center cursor-pointer gap-3 text-gray-500 hover:text-black">
          <img src="/profile.svg" alt="Cart" />
          <b>Войти</b>
        </li>
      </router-link>
    </ul>
  </header>
</template>
