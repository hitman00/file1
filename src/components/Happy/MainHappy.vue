<template>
  <div :class="$style.happy_box">
    <div :class="$style.box">
      <Slider animation="fade">
        <Slider-item v-for="(i, index) in list" :key="index" :style="i">
          <img :src="i" alt="" />
        </Slider-item>
      </Slider>
    </div>
  </div>
</template>

<script>
  import {Slider, SliderItem} from 'vue-easy-slider';

  export default {
    name: 'MainHappy',
    components: {
      Slider,
      SliderItem
    },
    data() {
      return {
        list: [
          require('@/assets/imgs/laph.jpg'),
          require('@/assets/imgs/happy2.jpg'),
          require('@/assets/imgs/certificate.png')
        ],
        sliderValue: 2
      };
    }
  };
</script>

<style lang="scss" module>
  .happy_box {
    float: left;
    width: 100%;

    .box {
      position: relative;
      margin: 0 8px;
      z-index: 1;
      :global {
        .slider {
          height: auto !important;
          padding-bottom: 71.2%;
        }
      }
      img {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>
