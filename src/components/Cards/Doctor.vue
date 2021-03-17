<template>
  <div :class="$style.protocol">
    <MiddleImage>
      <img src="@/assets/imgs/doctor.png" />
    </MiddleImage>

    <Titel>تجربه و مهارت پزشک</Titel>
    <ImageDashWhite>
      <img src="@/assets/imgs/4-whit.png" />
    </ImageDashWhite>
    <Paragraph>
      بیش از 10 سال سابقه در زمینه زیبایی و جوانسازی با استفاده ازبهترین و
      جدیدترین متدهای روز دنیا.
    </Paragraph>
  </div>
</template>

<script>
  import ImageDashWhite from './ImageDashWhite';
  import MiddleImage from './MiddelImage.vue';
  import Titel from './Title.vue';
  import Paragraph from './Paragraph.vue';

  export default {
    name: 'Doctor',
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
    position: relative;
    padding-top: 0.5px;
    padding-bottom: 1px;
    margin: 6px 18px 20px 18px;
    background: #ffb89f;
    border-radius: 20px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
  }
</style>
