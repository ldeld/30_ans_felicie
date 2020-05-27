<template>
  <div id="app">
    <HeaderSection />
    <Caroussel />
    <canvas id="confetti-canvas"></canvas>
  </div>
</template>

<script>
import HeaderSection from './components/HeaderSection.vue'
import Caroussel from './components/Caroussel.vue'
// Todo: move this to it's own component?
import ConfettiGenerator from "confetti-js";

export default {
  name: 'App',
  components: {
    HeaderSection,
    Caroussel
  },
  mounted() {
    window.addEventListener("load", () => {
      const confettiSettings = {"target":"confetti-canvas","max":"220","size":"1","animate":true,"props":["circle","square","triangle","line"],"colors":[[165,104,246],[230,61,135],[0,199,228],[253,214,126]],"clock":"50","rotate":true,"width":"1280","height":"1000","start_from_edge":true,"respawn":false};
      const confetti = new ConfettiGenerator(confettiSettings);
      setTimeout(() => confetti.render(), 1000)
    })
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

#confetti-canvas {
  position: absolute;
  top: 0;
  left: 0;
  height: 100vh;
  width: 100vw;
  z-index: -1;
}
</style>
