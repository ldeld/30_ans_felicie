<template>
<div class="header">
  <div class="header-images">
    <img src="../assets/party-cone.png" alt="party cone" class="header-icon-image">
    <div class="center-image-wrapper">
      <img src="../assets/fefe-1.png" alt="main felicie image" class="header-center-image original">
      <img src="../assets/fefe-1.png" class="header-center-image blue">
      <img src="../assets/fefe-1.png" class="header-center-image orange">

    </div>
    <img src="../assets/party-cone-flipped.png" alt="party cone" class="header-icon-image flipped">
  </div>
  <h1 class="title">
    Les <span class="age-span">30</span> glorieuses de Félicie
  </h1>
</div>
</template>

<script>
export default {
  name: 'header-section',
}

</script>

<style lang="scss">
$icon-rotate-degree: 5deg;
$center-image-rotate-degree: 15deg;

.title {
  color: white;
  margin: 0;
  margin-bottom: 10px;
}

.age-span {
  color: #ffc107;
  font-size: 45px;
  font-family: 'Yellowtail'
}

.header-images {
  width: 100%;
  display: flex;
  justify-content: space-around;
  align-items: center;
}

.center-image-wrapper {
  position: relative;
  height: 120px;
  width: 100px;
}

.header-icon-image {
  height: 90px;
  transition: 0.2s ease height;
}

.header-center-image {
  height: 120px;
  position: absolute;
  left: 0;
  top: 0;
  transition: 0.2s ease all;

  &.original {
    z-index: 3;
  }
  &.orange {
    filter: brightness(0) saturate(100%) invert(75%) sepia(26%) saturate(6771%) hue-rotate(342deg) brightness(101%) contrast(99%);
    transform-origin: bottom left;
  }

  &.blue {
    filter: brightness(0) saturate(100%) invert(42%) sepia(67%) saturate(780%) hue-rotate(171deg) brightness(99%) contrast(92%);
    transform-origin: bottom right;

  }
}

.header:hover {
  .header-icon-image {
    height: 100px;
    animation: vibrate linear 0.2s infinite;
  }

  .header-center-image.blue {
    transform: rotate($center-image-rotate-degree);
  }

  .header-center-image.orange {
    transform: rotate(-$center-image-rotate-degree);
  }
}

@keyframes vibrate {
  0%, 50%, 100% {
    transform: rotate(0deg)
  }

  25% {
    transform: rotate($icon-rotate-degree)
  }

  75% {
    transform: rotate(-$icon-rotate-degree)
  }
}

</style>
