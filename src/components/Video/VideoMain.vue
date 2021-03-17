<template>
  <div :class="$style.box">
    <h1>چرا کلاب سلامتی و زیبایی دکتر زمانی را انتخاب کنیم؟</h1>

    <ImageDash>
      <img src="@/assets/imgs/4.png" />
    </ImageDash>
    <p>
      اگر به دنبال کلینیک تخصصی پوست و زیبایی جهت انجام کلیه خدمات جوانسازی از
      جمله تزریق ژل و چربی، بوتاکس و ..هستید، کلاب سلامت و زیبایی دکتر فرشته
      زمانی با بهره گیری از بهترین مواد و جدیدترین متدها، آماده ارائه خدمات
      تخصصی به شماست. ما در کلینیک تخصصی دکتر زمانی، با تاکید بر تبحر و تجربه،
      صبورانه و متعهدانه در این مسیر در کنار شما هستیم.
    </p>
    <transition :name="$style.fade">
      <div :class="$style.botton" @click="test">
        توضیحات بیشتر
      </div>
      ></transition
    >
    <Video />
  </div>
</template>

<script>
  import Video from './PlayVideo.vue';
  import ImageDash from './ImageDash.vue';
  export default {
    name: 'VideoMain',
    data: () => ({
      change: true,
      r: Number,
      show: true
    }),
    methods: {
      test() {
        this.change = !this.change;
        window.scroll(0, this.r);
        console.log('ad');
      }
    },
    mounted() {
      this.r = document.getElementById('scroll_t').offsetTop;
    },
    components: {
      Video,
      ImageDash
    }
  };
</script>

<style lang="scss" module>
  .box {
    width: 100%;
    float: left;
    background: #f9ebea;
    h1 {
      font-size: 16px;
      color: #000;
      font-weight: bold;
      text-align: center;
      word-spacing: -1px;
      padding-top: 29px;
      padding-bottom: 10px;
    }
    p {
      margin: 8px auto 20px auto;
      font-size: 14px;
      line-height: 1.7;
      text-align: justify;
      text-align-last: center;
      color: #341d51;
      word-spacing: -3px;
      padding: 1px 31px 0px 31px;
    }

    .botton {
      background: #bc96ff;
      border-radius: 5px;
      margin: 0 169px;
      font-size: 15px;
      color: #fff;
      padding: 5px;
      text-align: center;
      margin-bottom: 39px;
      cursor: pointer;
      transform: height 2s;
    }
    .fade {
      &:global(-enter-active),
      &:global(-leave-active) {
        transition: all 0.9s ease;
      }

      &:global(-enter-to),
      &:global(-leave) {
        opacity: 1;
        max-height: 400px;
      }

      &:global(-enter),
      &:global(-leave-to) {
        opacity: 0;
        max-height: 0;
      }
    }
  }
</style>
