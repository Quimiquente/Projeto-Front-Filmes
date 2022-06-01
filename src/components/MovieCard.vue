<script>
  export default {
    data() {
      return {
        isFavorite: false,
        onCart: false,
      }
    },
    props: {
      movieInfo:  {
        posterImg: String,
        releaseDate: String,
        title: String,
        rating: Number,
        genre: String,
        price: Number,
      }
    },
    mounted() {
      console.log(this.movieInfo)
    },
    methods: {
      toggleFavorite() {
        this.isFavorite = !this.isFavorite
      },
      toggleCart() {
        this.onCart = !this.onCart
      }
    }
  }
</script>

<template>
  <div class="card">
    <div>
      <img :src="posterImg" alt="Eitcha">
      <button :class="{ favorited: this.isFavorite, notFavorited: !this.isFavorite }" @click="toggleFavorite">favoritar</button>
      <span>{{this.movieInfo.releaseDate}}</span>
    </div>
    <div>
      <span>{{this.movieInfo.title}}</span>
      <span>{{this.movieInfo.rating}}</span>
      <span>{{this.movieInfo.genre}}</span>
      <span>R${{this.movieInfo.price}}</span>
    </div>
    <button :class="{ added: onCart}">Adicionar</button>
  </div>
</template>

<style>
.card {
  border: 2px black solid;
  width: 200px
}
.card div {
  border: 2px black solid;
}
</style>