<template>
  <div :class="$style.title">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'Title'
  };
</script>

<style lang="scss" module>
  .title {
    color: #fff;
    font-size: 18px;
    font-weight: bold;
    text-align: center;
  }
</style>
