<template>
  <div :class="$style.protocol">
    <MiddleImage>
      <img src="@/assets/imgs/material.png" />
    </MiddleImage>

    <Titel> استفاده از مواد و متریال اصل و دارای تاییدیه </Titel>
    <ImageDashWhite>
      <img src="@/assets/imgs/4-whit.png" />
    </ImageDashWhite>
    <Paragraph>
      استفاده از مواد اولیه اورجینال، بدون عوارض جانبی. کلیه مواد مورد استفاده،
      در حضور شما باز می شود و برای اطمینان بیش تر جعبه در اختیار شما قرار خواهد
      گرفت.
    </Paragraph>
  </div>
</template>

<script>
  import ImageDashWhite from './ImageDashWhite';
  import MiddleImage from './MiddelImage.vue';
  import Titel from './Title.vue';
  import Paragraph from './Paragraph.vue';

  export default {
    name: 'Material',
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

    margin: -2px 18px 17px 18px;
    background: #bb9de4;
    border-radius: 20px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
  }
</style>
