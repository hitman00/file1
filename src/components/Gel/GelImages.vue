<template>
  <div :class="$style.gel">
    <div :class="$style.box">
      <Slider animation="fade" :class="$style.special_height">
        <Slider-item
          v-for="(i, index) in list"
          :key="index"
          :style="i"
          @click="hello"
        >
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
    },
    methods: {
      hello() {
        console.log('here');
      }
    }
  };
</script>
<style lang="scss" module>
  .gel {
    float: left;
    width: 100%;

    .box {
      position: relative;
      margin: 0 37px 96px;
      z-index: 1;
      img {
        width: 100%;
        height: 100%;
      }
      .special_height {
        height: 212px !important;
      }
    }
  }
</style>

<!--
<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <img src="@/assets/imgs/face.jpg" />
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Images'
  };
</script>

<style lang="scss" module>
  .image {
    position: relative;

    margin: 0px 37.5px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 57.2%;
    }
    .imagedef {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      img {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>
-->
