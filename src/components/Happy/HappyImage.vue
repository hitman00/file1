<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <img src="@/assets/imgs/laph.jpg" />
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
    margin: 0 8px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 71.1%;
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
