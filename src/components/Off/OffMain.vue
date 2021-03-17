<template>
  <div :class="$style.box">
    <div :class="$style.fixbox">
      <OffImage />
      <p>
        تخفیف ها و آفرهای ویژه ی هفتگی ما را از دست ندهید. هر هفته با یک پکیج
        تخفیفی ویژه
      </p>
      <Special />
      <h1>استفاده از معتبرترین و بهترین برند های دنیا</h1>
      <div :class="$style.brands">
        <BrandsImages v-for="(item, id) in brands" :key="id">
          <img :src="item"
        /></BrandsImages>
      </div>
    </div>
  </div>
</template>

<script>
  import OffImage from './OffImage.vue';
  import Special from './SpecialImage.vue';
  import BrandsImages from './BrandsImages.vue';
  export default {
    name: 'off',
    data: () => ({
      brands: [
        require('@/assets/imgs/masport.png'),
        require('@/assets/imgs/masport.png'),
        require('@/assets/imgs/masport.png'),
        require('@/assets/imgs/masport.png'),
        require('@/assets/imgs/masport.png'),
        require('@/assets/imgs/masport.png')
      ]
    }),
    components: {
      OffImage,
      Special,
      BrandsImages
    }
  };
</script>

<style lang="scss" module>
  .box {
    width: 100%;
    float: left;
    .fixbox {
      background: #f9ebea;
      margin: 0 8px;
      p {
        text-align: justify;
        text-align-last: center;
        word-spacing: -1px;
        letter-spacing: -1px;
        margin-bottom: 10px;
        font-size: 14px;
        margin-top: -100px;
        color: #fff;
        position: relative;
      }
      h1 {
        text-align: center;
        font-weight: bold;
        margin: 47px 0 0 0;
        margin-top: 47px;
        font-size: 16px;
      }
      .brands {
        width: 100%;
        display: flex;
        flex-flow: row wrap;
        background: #f9ebea;
        padding-bottom: 22px;
      }
    }
  }
</style>
