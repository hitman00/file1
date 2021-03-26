<template>
  <div :class="$style.QustionAnsware">
    <div :class="[$style.qustion, openxx]" @click="test">
      <div :class="$style.plus">
        <img src="@/assets/imgs/plus.png" />
      </div>
      {{ question }}
    </div>
    <transition :name="$style.fade">
      <div :class="$style.answare" v-if="show">
        {{ answer }}
      </div>
    </transition>
  </div>
</template>
<script>
  export default {
    name: 'QustionBox',
    props: {
      question: {
        type: String,
        default: ''
      },
      answer: {
        type: String,
        default: ''
      }
    },
    data() {
      return {
        show: false
      };
    },
    methods: {
      test() {
        //  let isIos = 'maAmaSkghsjhasads`345u8934';
        this.show = !this.show;
      }
    },
    computed: {
      openxx() {
        const x = [this.$style.qustion];
        if (this.show == true) {
          x.push(this.$style.show);
        }
        return x;
      },
      openyy() {
        const y = [this.$style.answare];
        if (this.show == true) {
          y.push(this.$style.hide);
        }
        return y;
      }
    }
  };
</script>

<style lang="scss" module>
  .QustionAnsware {
    width: 100%;
    display: flex;
    margin-bottom: 8px;
    float: left;
    flex-direction: column;
    padding: 0px 26px;

    .qustion {
      cursor: pointer;
      padding: 9px;
      border-radius: 50px;
      background: #fff;
      font-size: 13.5px;
      color: #4c4c4c;
      font-weight: bold;
      box-shadow: 0px 0px 4px rgba(187, 180, 180, 0.3);
      line-height: 1.5;
      transition: all 0.5s;
      width: 100%;
      margin-bottom: 2px;

      &.show {
        border-radius: 20px 20px 0 0;
        border-bottom: 1px solid #bc96ff;
      }
    }
    .plus {
      width: 15px;
      float: right;
      margin: 3px 1px 4px 11px;
      img {
        width: 100%;
        display: block;
      }
    }
    .answare {
      width: 100%;
      padding: 20px;
      border-radius: 0px 0px 20px 20px;
      background: #e1c9f3;
      font-size: 13px;
      text-align: justify;
      line-height: 1.5;
      overflow: hidden;
      &.hide {
        display: block;
      }
    }
    .fade {
      &:global(-enter-active),
      &:global(-leave-active) {
        transition: all 0.9s ease;
      }

      &:global(-enter-to),
      &:global(-leave) {
        opacity: 1;
        max-height: 400px;
      }

      &:global(-enter),
      &:global(-leave-to) {
        opacity: 0;
        max-height: 0;
      }
    }
  }
</style>
