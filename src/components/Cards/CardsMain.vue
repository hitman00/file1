<template>
  <div :class="$style.imagebox" id="scroll_t">
    <Protocol />
    <Natural />
    <div :class="$style.makeup">
      <img src="@/assets/imgs/makeup.png" />
    </div>
    <Material />
    <Doctor />
  </div>
</template>

<script>
  import Protocol from './ProtocolBox.vue';
  import Natural from './Natural';
  import Material from './Material.vue';
  import Doctor from './Doctor.vue';
  export default {
    name: 'CardsMain',
    components: {
      Protocol,
      Natural,
      Material,
      Doctor
    }
  };
</script>

<style lang="scss" module>
  .imagebox {
    padding-top: 35px;
    background: url('./../../assets/imgs/5.jpg');
    background-repeat: no-repeat;
    background-size: cover;
  }
  .makeup {
    position: relative;
    margin: 3px 18px 0px 18px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 71.9%;
    }
    img {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      width: 100%;
    }
  }
</style>
