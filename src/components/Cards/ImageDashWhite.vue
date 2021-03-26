<template>
  <div :class="$style.image_dash">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'ImageDashWhite'
  };
</script>

<style lang="scss" module>
  .image_dash {
    position: relative;
    margin: -1px 150.3px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 12%;
    }

    img {
      width: 100%;
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
    }
  }
</style>
