<template>
  <div :class="$style.image">
    <div :class="$style.imagedef">
      <img src="@/assets/imgs/1.jpg" />
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Imagex'
  };
</script>

<style lang="scss" module>
  .image {
    position: relative;
    width: 100%;
    &::before {
      content: '';
      display: block;
      padding-bottom: 155.4%;
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
