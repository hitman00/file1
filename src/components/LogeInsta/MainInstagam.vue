<template>
  <div :class="$style.box">
    <div :class="$style.layout">
      <div :class="$style.logo">
        <span> <img src="@/assets/imgs/logo-insta.webp"/></span>
      </div>
      <div :class="$style.textbox">
        <h1>در اینستاگرام همراه ما باشید</h1>
        <p>برای آشنایی بیشتر با خدمات و نظرات مشتریان</p>
        <div :class="$style.botton">بزن بریم</div>
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'LogeInsta',
    components: {}
  };
</script>

<style lang="scss" module>
  .box {
    width: 100%;
    display: flex;
    .layout {
      width: 100%;
      margin: 0 8px;
      background: #f1f2f2;
      padding-bottom: 19px;
      .logo {
        float: right;
        width: 110px;
        height: 108px;
        margin: 37px 33px 0px 33px;
        background: #fff;
        border-radius: 50%;
        box-shadow: 1px 3px 3px #d9d8d8;
        span {
          width: 72px;
          height: 73px;
          display: block;
          margin: 17px auto;

          img {
            width: 100%;
            height: 100%;
          }
        }
      }
      .textbox {
        float: right;
        h1 {
          font-size: 21px;
          color: #e9014f;
          margin-top: 42px;
          margin-bottom: 4px;
        }
        p {
          font-size: 12px;
          color: #666666;
          text-align: center;
          font-weight: 900;
        }
        .botton {
          border-radius: 50px;
          color: #fff;
          text-align: center;
          font-size: 18px;
          background: linear-gradient(
            90deg,
            rgba(228, 50, 128, 1) 0%,
            rgba(242, 93, 128, 1) 50%,
            rgba(255, 132, 128, 1) 100%
          );
          margin: 23px 40px 10px 42px;
          font-weight: 700;
          padding: 1.5px 5.5px 9.5px 5.5px;
          box-shadow: 1px 1px 3px #7b7b7b;
          letter-spacing: 1px;
        }
      }
    }
  }
</style>
