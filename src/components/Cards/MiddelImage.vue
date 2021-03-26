<template>
  <div :class="$style.protocolImage">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'MiddelImage'
  };
</script>

<style lang="scss" module>
  .protocolImage {
    position: relative;
    width: 80px;
    margin: 5px auto 7px auto;
    &::before {
      content: '';
      display: block;
      padding-bottom: 100%;
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
