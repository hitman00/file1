<template>
  <a href="http://www.instagram.com" :class="$style.box">
    <div :class="$style.insta_logo">
      <img src="@/assets/imgs/3.png" />
    </div>
    <p>برای دیدن کلیه خدمات در اینستاگرام همراه ما باشید</p>
  </a>
</template>

<script>
  export default {
    name: 'Instagram'
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
    padding: 18px 22px 18px 14px;
    box-shadow: 4px 2px 5px 0px #a8a6a6;
    display: flex;
    text-align: right;
    border-radius: 50px;
    cursor: pointer;
    transition: all 0.3s;
    &:hover {
      opacity: 0.8;
    }
    p {
      color: #fff;
      font-size: 15px;

      padding: 8px 9px;
      font-weight: bold;
      word-spacing: -1.2px;
      letter-spacing: -0.2px;
    }
  }
  .insta_logo {
    width: 41px;
    img {
      width: 100%;
      display: block;
    }
  }
</style>
