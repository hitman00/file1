<template>
  <div :class="$style.special">
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
    name: 'SpecialImage',
    components: {
      Slider,
      SliderItem
    },
    data() {
      return {
        list: [
          require('@/assets/imgs/special.jpg'),
          require('@/assets/imgs/special2.jpg'),
          require('@/assets/imgs/special3.jpg'),
          require('@/assets/imgs/special4.jpg')
        ],
        sliderValue: 2
      };
    }
  };
</script>

<style lang="scss" module>
  .special {
    float: left;
    width: 100%;

    .box {
      position: relative;
      margin: 5px 2.86% 47px;
      z-index: 1;
      :global {
        .slider {
          height: auto !important;
          border-radius: 5px;
          padding-bottom: 94.6%;
          .slider-btn-right,
          .slider-btn-left {
            background: none;
          }
        }
      }
      img {
        width: 100%;
        height: 100%;
      }
      :global {
        .slider {
          .slider-icon {
            border-color: #000;
          }
        }
      }
    }
  }
</style>
