<template>
  <div :class="$style.protocol">
    <MiddleImage>
      <img src="@/assets/imgs/natural.png" />
    </MiddleImage>

    <Titel>زیبایی طبیعی</Titel>
    <ImageDashWhite>
      <img src="@/assets/imgs/4-whit.png" />
    </ImageDashWhite>
    <Paragraph>
      استفاده از جدیدترین متدهای جوانسازی و بهترین مواد اولیه جهت افزایش زیبایی
      طبیعی، هنر ماست.
    </Paragraph>
  </div>
</template>

<script>
  import ImageDashWhite from './ImageDashWhite';
  import MiddleImage from './MiddelImage.vue';
  import Titel from './Title.vue';
  import Paragraph from './Paragraph.vue';

  export default {
    name: 'Natural',
    components: {
      ImageDashWhite,
      MiddleImage,
      Titel,
      Paragraph
    }
  };
</script>

<style lang="scss" module>
  .protocol {
    padding-top: 1px;
    margin: 0 15px;

    padding-bottom: 1px;
    background: #ffbaa1;
    border-radius: 20px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
  }
</style>
