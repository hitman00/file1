<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'BrandsImages'
  };
</script>

<style lang="scss" module>
  .image {
    position: relative;
    width: 40.6%;
    margin: 24px 35px -6px -18px;

    &::before {
      content: '';
      display: block;
      padding-bottom: 60.5%;
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
