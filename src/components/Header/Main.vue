<template>
  <div :class="$style.box">
    <img :class="$style.image" src="@/assets/imgs/1.jpg" />
    <div :class="$style.text_box">
      <h1>زیبایی طبیعی</h1>
      <p>ارایه دهنده بهترین خدمات جوانسازی پوست، بوتاکس،ژل لب</p>
      <a :class="[$style.boxbackground, $style.light]" href="tel:09021804129">
        تماس و مشاوره رایگان
        <img src="@/assets/imgs/2.png"
      /></a>
      <a :class="$style.boxbackground" href="https://www.instagram.com/">
        اینستاگرام ما
        <img src="@/assets/imgs/3.png"
      /></a>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'HeaderMain'
  };
</script>

<style lang="scss" module>
  .box {
    position: relative;
    margin-bottom: 30px;
    &::before {
      content: '';
      display: block;
      padding-bottom: 190%;
    }
    .image {
      overflow: hidden;
      position: absolute;
      left: 0;
      right: 0;
      top: 0;
      bottom: 0;
      width: 100%;
    }
  }
  .text_box {
    position: absolute;
    text-align: center;
    bottom: 10px;
    left: 0;
    right: 0;

    h1 {
      font-size: 33px;
      color: $colorh1;
      margin-bottom: 9px;
      font-weight: bold;
      line-height: 51px;
    }
    p {
      font-size: 18px;
      margin-bottom: 20px;
      color: #35313a;
      line-height: 28px;
    }
    a {
      color: #fff;
      font-size: 20px;
      margin-top: 3px;
    }
  }
  .boxbackground {
    background: #5c457b;
    border-radius: 41px;
    margin: 10px 46px;
    padding: 9px;
    display: block;
    &.light {
      background: #472971;
    }
    &:hover {
      opacity: 0.8;
    }
    img {
      width: 40px;
      height: 40px;
      vertical-align: middle;
      margin-right: 9px;
    }
  }
  .textbox {
    color: #fff;
    font-size: 20px;
    margin-top: 3px;
    display: inline-block;
  }
</style>
