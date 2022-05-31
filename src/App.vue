<script>
  data() {
    return {
      search: "";
    }
  }
</script>

<template>
<header>
  <p>loco de doido</p>
  puta merda
  <input v-model="search" type="text">
  <div>
    <button>favoritos</button>
    <button>carrinho</button>
  </div>
</header>
<p>{{search}}</p>
<HelloWorld/>
</template>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
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
</style>
