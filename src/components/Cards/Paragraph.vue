<template>
  <div :class="$style.paragraph">
    <slot></slot>
  </div>
</template>

<script>
  export default {
    name: 'paragraph'
  };
</script>

<style lang="scss" module>
  .paragraph {
    margin: 6px 10px 8px 10px;
    font-size: 14px;
    color: #fff;
    text-align: justify;
    text-align-last: center;
  }
</style>
