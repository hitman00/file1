<template>
  <div :class="$style.box">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'Box1'
  };
</script>

<style lang="scss" module>
  .box {
    background: #472971;
    border-radius: 41px;
    margin: 10px 46px;
    display: flex;
    justify-content: center;
    padding: 9px;
  }
</style>
