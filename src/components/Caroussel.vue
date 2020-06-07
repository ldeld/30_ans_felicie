<template>
  <div class="caroussel">
    <agile>
      <div class="slide">
        <div class="wistia-video">
        <!-- Script tag is in index -->
          <div class="wistia_responsive_padding" style="padding:56.25% 0 0 0;position:relative;">
            <div class="wistia_responsive_wrapper" style="height:100%;left:0;position:absolute;top:0;width:100%;">
              <div class="wistia_embed wistia_async_77dep11u9c seo=false videoFoam=true" style="height:100%;position:relative;width:100%">
                <div class="wistia_swatch" style="height:100%;left:0;opacity:0;overflow:hidden;position:absolute;top:0;transition:opacity 200ms;width:100%;">
                  <img src="https://fast.wistia.com/embed/medias/77dep11u9c/swatch" style="filter:blur(5px);height:100%;object-fit:contain;width:100%;" alt="" aria-hidden="true" onload="this.parentNode.style.opacity=1;" />
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="slide">
        <div class="wistia-video">
          <div class="wistia_responsive_padding" style="padding:56.25% 0 0 0;position:relative;"><div class="wistia_responsive_wrapper" style="height:100%;left:0;position:absolute;top:0;width:100%;"><div class="wistia_embed wistia_async_jpqafa9mg4 seo=false videoFoam=true" style="height:100%;position:relative;width:100%"><div class="wistia_swatch" style="height:100%;left:0;opacity:0;overflow:hidden;position:absolute;top:0;transition:opacity 200ms;width:100%;"><img src="https://fast.wistia.com/embed/medias/jpqafa9mg4/swatch" style="filter:blur(5px);height:100%;object-fit:contain;width:100%;" alt="" aria-hidden="true" onload="this.parentNode.style.opacity=1;" /></div></div></div></div>
        </div>
      </div>
      <div class="slide">
        <div class="wistia-video">
          <div class="wistia_responsive_padding" style="padding:56.25% 0 0 0;position:relative;"><div class="wistia_responsive_wrapper" style="height:100%;left:0;position:absolute;top:0;width:100%;"><div class="wistia_embed wistia_async_sxvahxzyzt seo=false videoFoam=true" style="height:100%;position:relative;width:100%"><div class="wistia_swatch" style="height:100%;left:0;opacity:0;overflow:hidden;position:absolute;top:0;transition:opacity 200ms;width:100%;"><img src="https://fast.wistia.com/embed/medias/sxvahxzyzt/swatch" style="filter:blur(5px);height:100%;object-fit:contain;width:100%;" alt="" aria-hidden="true" onload="this.parentNode.style.opacity=1;" /></div></div></div></div>
        </div>
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
    img {
      height: 60vh;
    }
  }

  .wistia-video {
    height: 60vh;
    width: 55vw;
    display: inline-block;
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
