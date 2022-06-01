<script>
  export default {
    data() {
      posterImg: undefined,
      releaseDate: undefined,
      title: undefined,
      rating: undefined,
      genre: undefined,
      price: undefined,
      isFavorite: false,
      onCart: false
    },
    props: {
      posterImg: String,
      releaseDate: String,
      title: String,
      rating: Number,
      genre: String,
      price: Number,
      isFavorite: Boolean,
      onCart: Boolean
    }
  }
</script>

<template class="card">
  <div>
    <img :src="posterImg" alt="Eitcha">
    <button :class="{ favorited: isFavorite, notFavorited: !isFavorite }">favoritar</button>
    <span>{{releaseDate}}</span>
  </div>
  <div>
    <span>{{title}}</span>
    <span>{{rating}}</span>
    <span>{{genre}}</span>
    <span>R${{price}}</span>
  </div>
  <button :class="{ added: onCart}">Adicionar</button>
</template>

<style>
.card {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>