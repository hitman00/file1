<template>
  <div :class="$style.box">
    <div :class="$style.fixbox">
      <div :class="$style.off_image">
        <img :class="$style.imagedef" src="@/assets/imgs/off.jpg" />
      </div>
      <p>
        تخفیف ها و آفرهای ویژه ی هفتگی ما را از دست ندهید. هر هفته با یک پکیج
        تخفیفی ویژه
      </p>
      <Special />
      <h1>استفاده از معتبرترین و بهترین برند های دنیا</h1>
      <div :class="$style.brands">
        <div
          :class="$style.brands_image"
          v-for="(item, id) in brands"
          :key="id"
        >
          <img :class="$style.imagedef" :src="item" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
  import Special from './SpecialImage.vue';
  export default {
    name: 'OffMain',
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
      Special
    }
  };
</script>

<style lang="scss" module>
  .box {
    width: 100%;
    float: left;
  }
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
      margin: 47px 0 24px 0;
      font-size: 16px;
    }
  }
  .brands {
    width: 100%;
    display: flex;
    flex-flow: row wrap;
    background: #f9ebea;
  }

  .off_image {
    position: relative;
    margin: 0 auto;
    &:before {
      content: '';
      display: block;
      padding-bottom: 82%;
    }
  }
  .brands_image {
    position: relative;
    width: 40.6%;
    margin: 0 auto 17px;
    &:before {
      content: '';
      display: block;
      padding-bottom: 60.5%;
    }
  }
  .imagedef {
    overflow: hidden;
    position: absolute;
    left: 0;
    right: 0;
    top: 0;
    bottom: 0;
    width: 100%;
  }
</style>
