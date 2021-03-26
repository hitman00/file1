<template>
  <div :class="[$style.box, test]">
    <div :class="$style.telfix">
      <div :class="$style.text">
        <div :class="$style.telnumber">
          <div :class="$style.imagetel">
            <img src="@/assets/imgs/tel.png" />
          </div>
          0902 - 1804129
        </div>
        <div :class="$style.paragraph">تماس و مشاوره رایگان</div>
      </div>
      <div :class="$style.logoinsta">
        <img src="@/assets/imgs/instabottom.png" alt="" />
      </div>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'TelMain',
    data() {
      return {
        top: false
      };
    },
    computed: {
      test() {
        let a = [this.$style.box];
        if (this.top) {
          a.push(this.$style.boxfix);
        }
        return a;
      }
    },
    mounted() {
      window.onscroll = () => {
        if (document.documentElement.scrollTop > 50) {
          this.top = true;
        } else {
          this.top = false;
        }
      };
    }
  };
</script>

<style lang="scss" module>
  .box {
    display: none;
    width: 100%;
    float: left;
    height: 70px;
    &.boxfix {
      display: block;
    }
    .telfix {
      position: fixed;
      width: 100%;
      background: #ad3afe;
      height: 70px;
      bottom: 0;
      left: 0;
      right: 0;
      z-index: 1000;
      .text {
        text-align: center;
        .telnumber {
          height: 34px;
          font-size: 16px;
          font-weight: 600;
          color: #fff;
          padding-top: 10px;
          width: 128px;
          margin: 0 auto;
          direction: ltr;
          animation: test2 4s alternate infinite linear;
          @keyframes test2 {
            0% {
              transform: scale(0.8);
            }
            3.5% {
              transform: scale(1.2);
            }
            7% {
              transform: scale(0.8);
            }
            10.5% {
              transform: scale(1.2);
            }
            14% {
              transform: scale(1);
            }
            86% {
              transform: scale(1);
            }
            89.5% {
              transform: scale(1.2);
            }
            93% {
              transform: scale(0.6);
            }
            96.5% {
              transform: scale(1.2);
            }
            100% {
              transform: scale(0.6);
            }
          }
          .imagetel {
            width: 20px;
            height: 20px;
            float: left;
            margin: -3px 10px 4px 0;
            img {
              width: 100%;
              height: 100%;
            }
          }
        }
      }
      .paragraph {
        padding-bottom: 10px;
        display: block;
        text-align: center;
        color: #fff;
      }
      .logoinsta {
        position: absolute;
        width: 50px;
        height: 50px;
        top: -22px;
        right: 20px;
        box-shadow: 0px 5px 5px 2px rgba(64, 64, 64, 0.65);
        border-radius: 15px;
        animation: test 4s alternate infinite linear;
        @keyframes test {
          0% {
            transform: rotate(-20deg);
          }
          3.5% {
            transform: rotate(20deg);
          }
          7% {
            transform: rotate(-20deg);
          }
          10.5% {
            transform: rotate(20deg);
          }
          14% {
            transform: rotate(0deg);
          }
          86% {
            transform: rotate(0deg);
          }
          89.5% {
            transform: rotate(20deg);
          }
          93% {
            transform: rotate(-20deg);
          }
          96.5% {
            transform: rotate(20deg);
          }
          100% {
            transform: rotate(-20deg);
          }
        }
        img {
          width: 100%;
          height: 100%;
        }
      }
    }
  }
</style>
