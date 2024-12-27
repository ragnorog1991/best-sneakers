
<style>
.favorite-counter {
  display: flex;
  align-items: center;
}

.heart-button {
  background: none;
  border: none;
  cursor: pointer;
  font-size: 24px; /* Размер иконки */
}

.count {
  margin-left: 8px; /* Отступ между иконкой и счетчиком */
  font-size: 18px; /* Размер текста счетчика */
}
</style>

<script>
export default {
  data() {
    return {
      isFavorite: false, // Состояние, добавлен ли товар в избранное
      favoriteCount: 0, // Счетчик избранных товаров
    }
  },
  methods: {
    toggleFavorite() {
      this.isFavorite = !this.isFavorite // Переключаем состояние
      this.favoriteCount += this.isFavorite ? 1 : -1 // Увеличиваем или уменьшаем счетчик
    },
  },
}
</script>
