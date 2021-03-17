<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'ImageDashWhite'
  };
</script>

<style lang="scss" module>
  .image {
    position: relative;
    margin: -1px 150.3px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 12%;
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
      }
    }
  }
</style>
