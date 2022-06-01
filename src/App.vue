<script>
import MovieCard from "./components/MovieCard.vue"
import movieInfo from "./assets/cardData.js"

export default {
  components: {
    MovieCard
  },

  data() {
    return {
      search: '',
      cardData: movieInfo
    }
  },
  mounted() {
    console.log(this.cardData.releaseDate)
  }
}
</script>

<template>
<header>
  <p>loco de doido</p>
  <input v-model="search" type="text">
  <div>
    <button>favoritos</button>
    <button>carrinho</button>
  </div>
</header>
<p>{{search}}</p>
<div class="card-section">
  <MovieCard :movieInfo="cardData"/>
</div>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  display: flex;
  flex-flow: column nowrap;
  
}
header {
  display: flex;
  flex-flow: row nowrap;
  justify-content: space-evenly;
  height: 30px;
}
header p {
  padding: 0;
  margin: auto 0;
}
header div {
  height: 100%;
}
button {
  height: inherit;
}
.card-section {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
