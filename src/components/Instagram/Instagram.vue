<template>
  <div :class="$style.box">
    <InstagramLogo>
      <img src="@/assets/imgs/3.png" />
    </InstagramLogo>
    <p>برای دیدن کلیه خدمات در اینستاگرام همراه ما باشید</p>
  </div>
</template>

<script>
  import InstagramLogo from './InstagramLogo.vue';
  export default {
    name: 'Instagram',
    components: {
      InstagramLogo
    }
  };
</script>

<style lang="scss" module>
  .box {
    margin: 0 36px 19px 30px;

    background: linear-gradient(
      90deg,
      rgba(228, 50, 128, 1) 0%,
      rgba(235, 72, 128, 1) 35%,
      rgba(247, 108, 128, 1) 68%,
      rgba(254, 131, 128, 1) 100%
    );
    padding: 18px 23px 18px 14px;
    box-shadow: 4px 2px 5px 0px #a8a6a6;
    display: flex;
    text-align: right;
    border-radius: 50px;
    p {
      color: #fff;
      font-size: 15px;

      padding: 8px 9px;
      font-weight: bold;
      word-spacing: -1.2px;
      letter-spacing: -0.2px;
    }
  }
</style>
