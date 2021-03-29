<template>
  <div :class="$style.box">
    <div :class="$style.iteams">
      <Slider animation="fade">
        <Slider-item v-for="(i, index) in list" :key="index" :style="i">
          <div :class="$style.box2">
            <div :class="$style.avatarbox">
              <div :class="$style.avatar">
                <img :src="i.linki" />
              </div>
            </div>
          </div>
          <div :class="$style.name">{{ i.fname }}</div>
          <div :class="$style.comment">{{ i.comment }}</div>
        </Slider-item>
      </Slider>
    </div>
  </div>
</template>

<script>
  import {Slider, SliderItem} from 'vue-easy-slider';
  export default {
    name: 'SanazMain',
    components: {
      SliderItem,
      Slider
    },
    data() {
      return {
        list: [
          {
            linki: require('@/assets/imgs/avatar-sanaz.jpg'),
            fname: 'ساناز',
            comment:
              ' خانم دکتر جان خواستم از رفتار پسندیده پرسنل مطب تشکر کنم، خونگرم و مهربون هستند درست مثل خودتون '
          },
          {
            linki: require('@/assets/imgs/sanaz2.png'),
            fname: 'پارمیس',
            comment:
              ' من شنبه اومدم هایفو انجام دادم امروز هر کی منو می بینه میگه چقدر عالی شدی، مرسی واقعا ایشالا چند ماه دیگه بیام ایران دوباره میام پیشتون. '
          },
          {
            linki: require('@/assets/imgs/sanaz3.jpg'),
            fname: 'ساناز',
            comment:
              ' خانم دکتر جان خواستم از رفتار پسندیده پرسنل مطب تشکر کنم، خونگرم و مهربون هستند درست مثل خودتون '
          },
          {
            linki: require('@/assets/imgs/sanaz4.jpg'),
            fname: 'ساناز',
            comment:
              ' خانم دکتر جان خواستم از رفتار پسندیده پرسنل مطب تشکر کنم، خونگرم و مهربون هستند درست مثل خودتون '
          },
          {
            linki: require('@/assets/imgs/sanaz5.jpg'),
            fname: 'ساناز',
            comment:
              ' خانم دکتر جان خواستم از رفتار پسندیده پرسنل مطب تشکر کنم، خونگرم و مهربون هستند درست مثل خودتون '
          },
          {
            linki: require('@/assets/imgs/sanaz6.png'),
            fname: 'ساناز',
            comment:
              ' خانم دکتر جان خواستم از رفتار پسندیده پرسنل مطب تشکر کنم، خونگرم و مهربون هستند درست مثل خودتون '
          }
        ],
        sliderValue: 2
      };
    }
  };
</script>

<style lang="scss" module>
  .box {
    float: left;
    width: 100%;
    .iteams {
      height: 330px;
      margin: 0px 8px;
      background: url('./../../assets/imgs/background-sanaz.jpg');
      background-size: cover;
      background-repeat: no-repeat;
      :global {
        .slider {
          .slider-icon {
            border-color: #fff;
            width: 18px;
            height: 18px;
            margin-top: 18px;
          }
        }
      }
    }
    .name {
      font-size: 16px;
      float: left;
      color: #fff;
      font-weight: bold;
      text-align: center;
      width: 100%;
    }
    .comment {
      font-size: 14px;
      color: #fff;
      margin-top: 20px;
      text-align: justify;
      word-spacing: -2px;
      float: left;
      padding: 0 67px 0 46px;
    }
  }
  .box2 {
    width: 100%;
    float: left;
    .avatarbox {
      width: 105px;
      height: 95px;
      background: url('./../../assets/imgs/background-avatar.png');
      background-size: contain;
      background-repeat: no-repeat;
      margin: 35px auto 0 auto;
      padding-top: 3px;
    }
  }
  .avatar {
    width: 82px;
    height: 82px;
    position: relative;
    margin: 0 auto;

    img {
      width: 100%;
      height: 100%;
      display: block;
      border-radius: 50px;
    }
  }
</style>
