<template>
  <div :class="$style.box">
    <div :class="$style.image_cycle">
      <img src="@/assets/imgs/cycle.png" />
    </div>
    <p>{{ services }}</p>
  </div>
</template>

<script>
  export default {
    name: 'ListOfService',
    props: {
      services: {
        type: String,
        default: ''
      }
    }
  };
</script>

<style lang="scss" module>
  .box {
    margin-bottom: 7.5px;
    .image_cycle {
      width: 19px;
      height: 18px;
      float: right;
      img {
        width: 100%;
        height: 100%;
      }
    }
    p {
      overflow: hidden;
      color: #fff;
      font-size: 12.5px;
      line-height: 1.8;
      text-align: right;
      word-spacing: -1.2px;
      padding-right: 8px;
    }
  }
</style>
