<template>
  <div :class="$style.box">
    <Imagex />
    <div :class="$style.text_box">
      <Textx />
    </div>
  </div>
</template>

<script>
  import Imagex from './HeaderImage.vue';
  import Textx from './HeaderText.vue';

  export default {
    name: 'Part1',
    components: {
      Imagex,
      Textx
    }
  };
</script>

<style lang="scss" module>
  .box {
    width: 100%;

    .text_box {
      position: relative;
      text-align: center;

      margin: -94px 0 51px 0;
      width: 100%;
    }
  }
</style>
