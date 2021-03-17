<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <slot></slot>
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
    width: 82px;
    margin: 0 auto;
    &::before {
      content: '';
      display: block;
      padding-bottom: 100%;
    }
    .imagedef {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      border-radius: 50px;
      margin-top: 5px;

      img {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>
