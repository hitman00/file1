<template>
  <div :class="$style.footer">
    <div :class="$style.textbox">
      کلیه حقوق این وب سایت متعلق به doctorzam می باشد
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Footer'
  };
</script>

<style lang="scss" module>
  .footer {
    width: 100%;

    .textbox {
      padding: 19px;
      background: #412261;
      text-align: center;
      color: #fff;
      font-size: 16px;
      margin: 0 8px;
    }
  }
</style>
