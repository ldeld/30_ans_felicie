<template>
  <div class="caroussel">
    <agile>
      <div class="slide">
        <iframe width="806" height="453" src="https://www.youtube.com/embed/4vajlWofWS8" frameborder="0" allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
      <div class="slide">
        <img src="https://source.unsplash.com/random" alt="">
      </div>
      <div class="slide">
        <img src="https://source.unsplash.com/random" alt="">
      </div>
    </agile>
  </div>
</template>

<script>
  // https://github.com/lukaszflorczak/vue-agile
  import { VueAgile } from 'vue-agile'

  export default {
    name: 'Caroussel',
    components: {
      agile: VueAgile
    }
  }
</script>

<style scoped lang="scss">
  .slide {
    img, iframe {
      height: 60vh;
    }
  }
</style>
