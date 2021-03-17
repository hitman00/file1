<template>
  <div :class="$style.protocol">
    <CoronaImage>
      <img src="@/assets/imgs/corona.png" />
    </CoronaImage>
    <MiddleImage>
      <img src="@/assets/imgs/protocol.png" />
    </MiddleImage>

    <Titel>رعایت پروتکل ورود به مطب</Titel>
    <ImageDashWhite>
      <img src="@/assets/imgs/4-whit.png" />
    </ImageDashWhite>
    <Paragraph>
      سلامتی شما برای ما شرط اول است، به همین منظور برای ورود به مطب تمام پروتکل
      های لازم اجرا میشود.
    </Paragraph>
  </div>
</template>

<script>
  import ImageDashWhite from './ImageDashWhite';
  import CoronaImage from './CronaImage';
  import MiddleImage from './MiddelImage.vue';
  import Titel from './Title.vue';
  import Paragraph from './Paragraph.vue';

  export default {
    name: 'Protocol',
    components: {
      ImageDashWhite,
      CoronaImage,
      MiddleImage,
      Titel,
      Paragraph
    }
  };
</script>

<style lang="scss" module>
  .protocol {
    margin: 0 15px 30px 15px;

    background: #bb9ce4;
    border: 5px solid #d8c171;
    border-radius: 20px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.3);
  }
</style>
