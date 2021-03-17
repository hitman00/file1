<template>
  <div :class="$style.main">
    <div :class="$style.box">
      <Part1 />
      <Part2 />
      <Part3 />
      <Part4 />
      <Instagram />
      <Sanaz />
      <Part5 />
      <Off />
      <Service />
      <LogeInsta />
      <HappyImg />
      <Address />
      <Footer />
      <Tel />
    </div>
  </div>
</template>

<script>
  import Part1 from './components/Header/HeaderMain.vue';
  import Part2 from './components/Video/VideoMain.vue';
  import Part3 from './components/Cards/CardsMain.vue';
  import Part4 from './components/Gel/GelMain.vue';
  import Instagram from './components/Instagram/Instagram.vue';
  import Sanaz from './components/Sanaz/SanazMain.vue';
  import Part5 from './components/Abouts/AboutMainl.vue';
  import Off from './components/Off/OffMain.vue';
  import Service from './components/Service/ServiceMain.vue';
  import LogeInsta from './components/LogeInsta/MainInstagam.vue';
  import HappyImg from './components/Happy/MainHappy.vue';
  import Address from './components/Address/AddressMain.vue';
  import Footer from './components/FooterBox/FooterMain.vue';
  import Tel from './components/Telephone/TelMain.vue';
  export default {
    name: 'App',
    data: () => ({}),

    components: {
      Part1,
      Part2,
      Part3,
      Part4,
      Instagram,
      Sanaz,
      Part5,
      Off,
      Service,
      LogeInsta,
      HappyImg,
      Address,
      Footer,
      Tel
    }
  };
</script>

<style lang="scss" module>
  @font-face {
    font-family: Iransans;
    src: url('./assets/font/1.woff2');
  }
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    direction: rtl;
  }
  * ul {
    list-style-type: none;
  }
  a {
    text-decoration: none;
  }
  body {
    font-family: Iransans;
  }

  .main {
    width: 100%;
    margin: 0 auto;
    float: right;
    .box {
      max-width: 465.7px;
      margin: 0 auto;
    }
  }
</style>
