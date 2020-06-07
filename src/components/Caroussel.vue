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
      <template slot="prevButton"><i class="fas fa-chevron-left"></i></template>
      <template slot="nextButton"><i class="fas fa-chevron-right"></i></template>
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

<style lang="scss">
  .slide {
    img, iframe {
      height: 60vh;
    }
  }

  .agile__nav-button {
    z-index: 5;
    margin: -60vh 60px 0 60px;
    padding: 0 30px;
    border-radius: 6px;
    border: none;
    background-color: transparent;
    color: #ddd;
    font-size: 40px;

    transition: 0.2s ease;

    &:hover {
      background-color: rgba(255, 255, 255, 0.05);
    }
  }

  .agile__dot {
    button {
      border: none;
      background-color: #888;
      width: 40px;
      height: 3px;
      margin: 0 10px;
      border-radius: 2px;
    }

    &--current button {
      background-color: #fff;
    }
  }
</style>
