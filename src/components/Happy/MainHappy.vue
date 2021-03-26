<template>
  <div :class="$style.happy_box">
    <div :class="$style.box">
      <Slider animation="fade" :class="$style.height_slider">
        <Slider-item v-for="(i, index) in list" :key="index" :style="i">
          <!--  <p style="line-height: 280px; font-size: 5rem; text-align: center;">
            Page{{ index + 1 }}
          </p> -->
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
      img {
        width: 100%;
        height: 100%;
      }
      .height_slider {
        height: 320px !important;
      }
    }
  }
</style>
