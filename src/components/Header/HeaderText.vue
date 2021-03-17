<template>
  <div :class="$style.box">
    <h1>زیبایی طبیعی</h1>
    <p>ارایه دهنده بهترین خدمات جوانسازی پوست، بوتاکس،ژل لب</p>
    <div :class="$style.bottonss">
      <Box1
        ><a href="tel:09021804129">
          <div :class="$style.textbox">تماس و مشاوره رایگان</div>

          <div :class="$style.imagebox">
            <div :class="$style.imagedef">
              <img src="@/assets/imgs/2.png" />
            </div></div
        ></a>
      </Box1>

      <Box1 :class="$style.boxbackground"
        ><a href="https://www.instagram.com/">
          <div :class="$style.textbox">اینستاگرام ما</div>

          <div :class="$style.imagebox">
            <div :class="$style.imagedef">
              <img src="@/assets/imgs/3.png" />
            </div></div
        ></a>
      </Box1>
    </div>
  </div>
</template>

<script>
  import Box1 from './HeaderBox.vue';

  export default {
    name: 'Text1',
    data: () => ({}),
    components: {
      Box1
    }
  };
</script>

<style lang="scss" module>
  .box {
    h1 {
      font-size: 33px;
      color: $colorh1;
      margin-bottom: 9px;

      font-weight: bold;
    }
    p {
      font-size: 18px;

      margin-bottom: 20px;
      color: #35313a;
    }
    .bottonss {
      text-align: center;
      a {
        display: flex;
      }
      .boxbackground {
        background: #5c457b;
      }
      .textbox {
        color: #fff;
        font-size: 20px;
        margin-top: 3px;
      }
      .imagebox {
        position: relative;
        width: 40px; // margin: 9px 0px 10px 70px;
        margin-right: 14px;
        &::before {
          content: '';
          display: block;
          padding-bottom: 100%;
        }
        .imagedef {
          overflow: hidden;
          position: absolute;
          left: 0;
          right: 0;
          top: 0;
          bottom: 0;
          img {
            width: 100%;
            height: 100%;
          }
        }
      }
    }
  }
</style>
