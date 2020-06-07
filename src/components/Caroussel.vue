<template>
  <div class="caroussel">
    <agile>
      <div class="slide">
        <div class="video">
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
        <div class="video">
          <div class="wistia_responsive_padding" style="padding:56.25% 0 0 0;position:relative;"><div class="wistia_responsive_wrapper" style="height:100%;left:0;position:absolute;top:0;width:100%;"><div class="wistia_embed wistia_async_jpqafa9mg4 seo=false videoFoam=true" style="height:100%;position:relative;width:100%"><div class="wistia_swatch" style="height:100%;left:0;opacity:0;overflow:hidden;position:absolute;top:0;transition:opacity 200ms;width:100%;"><img src="https://fast.wistia.com/embed/medias/jpqafa9mg4/swatch" style="filter:blur(5px);height:100%;object-fit:contain;width:100%;" alt="" aria-hidden="true" onload="this.parentNode.style.opacity=1;" /></div></div></div></div>
        </div>
      </div>
      <div class="slide">
        <div class="video">
          <div class="wistia_responsive_padding" style="padding:56.25% 0 0 0;position:relative;"><div class="wistia_responsive_wrapper" style="height:100%;left:0;position:absolute;top:0;width:100%;"><div class="wistia_embed wistia_async_sxvahxzyzt seo=false videoFoam=true" style="height:100%;position:relative;width:100%"><div class="wistia_swatch" style="height:100%;left:0;opacity:0;overflow:hidden;position:absolute;top:0;transition:opacity 200ms;width:100%;"><img src="https://fast.wistia.com/embed/medias/sxvahxzyzt/swatch" style="filter:blur(5px);height:100%;object-fit:contain;width:100%;" alt="" aria-hidden="true" onload="this.parentNode.style.opacity=1;" /></div></div></div></div>
        </div>
      </div>
      <div class="slide">
        <div class="video iplayer-video">
        <iframe src="//iplayerhd.com/player/video/b1ff7b31-c97f-41eb-9be2-b3a45f7b85c4" allowtransparency="true" frameborder="0" scrolling="no" allowfullscreen></iframe>
        </div>
      </div>
      <div class="slide">
        <div class="video iplayer-video">
          <iframe src="//iplayerhd.com/player/video/645191b4-3949-4fb5-86f8-25bf64e5add3" allowtransparency="true" frameborder="0" scrolling="no" allowfullscreen></iframe>
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
    img, iframe {
      height: 60vh;
    }
  }

  .video {
    height: 60vh;
    width: 55vw;
    display: inline-grid;
    align-content: center;
  }

  .video.iplayer-video {
    position: relative;

    iframe {
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      border: 0;
    }
  }

  @media (max-width: 600px) {
    .video {
      width: 75vw;
      height: 50vh;
    }
  }

  @media (min-width: 800px) {
    .agile__nav-button {
      padding: 0 30px;
      margin-left: 30px;
      margin-left: 30px
    }
  }

  .agile__nav-button {
    z-index: 5;
    margin-top: -60vh;
    padding: 0 10px;
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
