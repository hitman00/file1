<template>
  <div :class="$style.special">
    <div :class="$style.box">
      <Slider animation="fade" :class="$style.special_height">
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
      margin: 4px 12.8px 47px 12.8px;
      z-index: 1;
      img {
        width: 100%;
        height: 100%;
      }
      .special_height {
        height: 401px !important;
        border-radius: 5px;
      }
    }
  }
</style>
