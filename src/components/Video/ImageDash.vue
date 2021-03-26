<template>
  <div :class="$style.image">
    <img src="@/assets/imgs/4.png" />
  </div>
</template>

<script>
  export default {
    name: 'ImageDash'
  };
</script>

<style lang="scss" module>
  .image {
    position: relative;
    margin: 0 31.4%;
    &:before {
      content: '';
      display: block;
      padding-bottom: 9%;
    }
    img {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      width: 100%;
    }
  }
</style>
