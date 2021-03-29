<template>
  <div :class="$style.gel">
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
    name: 'GelImages',
    components: {
      Slider,
      SliderItem
    },
    data() {
      return {
        list: [
          require('@/assets/imgs/face.jpg'),
          require('@/assets/imgs/face2.jpg'),
          require('@/assets/imgs/face3.jpg'),
          require('@/assets/imgs/face4.jpg')
        ],
        sliderValue: 2
      };
    }
  };
</script>
<style lang="scss" module>
  .gel {
    float: left;
    width: 100%;
  }
  .box {
    position: relative;
    margin: 0 37px 79px;
    z-index: 1;
    img {
      width: 100%;
      height: 100%;
    }
    :global {
      .slider {
        overflow: visible;
        height: auto !important;
        overflow: unset !important;
        padding-bottom: 57.1%;
        .slider-btn {
          background: none;
        }
        .slider-btn-right {
          right: -42px;
        }
        .slider-btn-left {
          left: -42px;
        }
        .slider-btn-right,
        .slider-btn-left {
          &:hover .slider-icon {
            border-color: #00d8f5;
          }
        }
        .slider-icon {
          border-color: #000;
          margin-bottom: 31px;
          width: 18px;
          height: 18px;
        }
      }
    }
  }
</style>
