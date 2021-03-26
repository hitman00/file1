<template>
  <div :class="$style.box">
    <h1>چرا کلاب سلامتی و زیبایی دکتر زمانی را انتخاب کنیم؟</h1>
    <ImageDash />
    <p>
      اگر به دنبال کلینیک تخصصی پوست و زیبایی جهت انجام کلیه خدمات جوانسازی از
      جمله تزریق ژل و چربی، بوتاکس و ..هستید، کلاب سلامت و زیبایی دکتر فرشته
      زمانی با بهره گیری از بهترین مواد و جدیدترین متدها، آماده ارائه خدمات
      تخصصی به شماست. ما در کلینیک تخصصی دکتر زمانی، با تاکید بر تبحر و تجربه،
      صبورانه و متعهدانه در این مسیر در کنار شما هستیم.
    </p>
    <div :class="$style.botton" @click="scroll_t">
      توضیحات بیشتر
    </div>
    <PlayVideo />
  </div>
</template>

<script>
  import PlayVideo from './PlayVideo.vue';
  import ImageDash from './ImageDash.vue';
  export default {
    name: 'VideoMain',
    data: () => ({
      roll: null
    }),
    methods: {
      scroll_t() {
        window.scrollTo({
          behavior: 'smooth',
          top: this.roll
        });
      }
    },
    mounted() {
      this.roll = document.getElementById('scroll_t').offsetTop;
    },
    components: {
      PlayVideo,
      ImageDash
    }
  };
</script>

<style lang="scss" module>
  .box {
    background: #f9ebea;
    h1 {
      font-size: 16px;
      color: #000;
      font-weight: bold;
      text-align: center;
      word-spacing: -1px;
      padding-top: 29px;
      padding-bottom: 10px;
      line-height: 25px;
    }
    p {
      margin: 9px 31px 20px;
      font-size: 14px;
      line-height: 1.7;
      text-align: justify;
      text-align-last: center;
      color: #341d51;
      word-spacing: -3px;
    }
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
    line-height: 24px;
    &:hover {
      opacity: 0.8;
    }
  }
</style>
