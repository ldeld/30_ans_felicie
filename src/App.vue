<template>
  <div id="app">
    <Header />
    <Caroussel />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Caroussel from './components/Caroussel.vue'

export default {
  name: 'App',
  components: {
    Header,
    Caroussel
  }
}
</script>

<style>
body {
  background-color: #23336B;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 20px;
}
</style>
