<script setup>
</script>


<template>
  <h1 class="text-3xl font-bold mb-8">Войти или создать профиль</h1>
  <div class="justify-items-center">
    <div
      class="flex-auto justify-items-center bg-white shadow-xl border border-slate-100 rounded-lg"
    >
      <div class="flex relative justify-center m-40">
        <p class="absolute bottom-10 left-0 text-slate-400">Контактный телефон</p>
        <select class="py-2 px-3 border rounded-md outline-none mr-5" name="code">
          <option value="code">+7</option>
          <option value="code">+374</option>
          <option value="code">+375</option>
          <option value="code">+996</option>
          <option value="code">+998</option>
        </select>
        <input
          class="border w-60 justify-center rounded-lg px-3"
          value="(XXX)-XXX-XX-XX"
          type="text"
        />
      </div>
      <button
        class="flex justify-center p-2 border-slate-400 rounded-xl m-10 border w-2/4 hover:text-slate-300 hover:border-slate-300"
      >
        Получить код
      </button>
      <div class="flex w-96 mb-10 relative">
        <input class="mx-3 flex align-baseline absolute top-1.5 left-82" type="checkbox" />
        <p class="text-slate-400 px-8">
          Соглашаюсь с
          <a href="#" class="font-bold text-slate-800">правилами пользования торговой площадкой</a>
          и <a href="#" class="font-bold text-slate-800">возврата</a>
        </p>
      </div>
    </div>
  </div>
</template>
