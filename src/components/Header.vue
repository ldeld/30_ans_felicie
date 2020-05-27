<template>
<div class="header" @mouseover="animate()" @mouseout="stopAnimate()">
  <div class="header-images">
    <img src="../assets/party-cone.png" alt="party cone" class="header-icon">
    <img src="../assets/fefe-1.png" alt="main felicie image" class="header-center-image">
    <img src="../assets/party-cone.png" alt="party cone" class="header-icon flipped">
  </div>
  <h1 class="title">
    Les <span class="age-span">30</span> glorieuses de Félicie
  </h1>
</div>
</template>

<script>
export default {
  name: 'header',
  methods: {
    animate() {
      console.log("animating...")
    },
    stopAnimate() {
      console.log("stop Animation")
    }
  }
}

</script>

<style scoped lang="scss">
  .header-images {
    width: 100%;
    display: flex;
    justify-content: space-around;
    align-items: center;
  }

  .header-center-image {
    height: 160px;
  }

  .header-icon-image {
    height: 140px;
  }

  .flipped {
    transform: scaleX(-1)
  }

  .title {
    color: white;
  }

  .age-span {
    color: #ffc107;
    font-size: 42px;
  }

</style>
