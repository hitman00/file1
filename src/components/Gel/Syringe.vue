<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <slot></slot>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Syringe'
  };
</script>

<style lang="scss" module>
  .image {
    position: relative;
    width: 100%;
    &::before {
      content: '';
      display: block;
      padding-bottom: 61%;
    }
    .imagedef {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      box-shadow: -1px -4px 5px 0px rgba(172, 172, 172, 0.3);
      border-top-right-radius: 25px;
      border-top-left-radius: 25px;
      img {
        width: 100%;
        height: 100%;
      }
    }
  }
</style>
