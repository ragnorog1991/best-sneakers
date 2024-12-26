<script setup>
import { inject } from 'vue'
import Cartitem from './Cartitem.vue'

const { cart, removeFromCart } = inject('cart')
</script>




<template>
  <div class="flex flex-col flex-1 gap-4 justify-between" v-auto-animate>
    <Cartitem
      v-for="item in cart"
      :key="item.id"
      :title="item.title"
      :price="item.price"
      :image-url="item.imageUrl"
      @on-click-remove="() => removeFromCart(item)"
    />
  </div>
</template>
