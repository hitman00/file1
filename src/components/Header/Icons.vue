<template>
  <div :class="$style.imagebox">
    <div :class="$style.imagedef">
      <img :class="[$style.disp1, newtest]" src="@/assets/imgs/2.png" />
      <img :class="[$style.disp2, newtest]" src="@/assets/imgs/3.png" />
    </div>
  </div>
</template>

<script>
  export default {
    name: 'Icons',
    props: {
      them: {
        type: String,
        default: 'addsa'
      }
    },
    computed: {
      newtest() {
        let n = [this.$style.imagedef];
        console.log(n);

        let t = [this.$style.disp2];
        if (this.them === 'insta') {
          n.push(this.$style.disp3);
          console.log(n);
        } else if (this.them === 'tel') {
          t.push(this.$style.disp3);
          console.log(t);
        }

        return n, t;
      }
    }
  };
</script>

<style lang="scss" module>
  .imagebox {
    position: relative;
    width: 40px;
    float: left;
    margin: 9px 0px 10px 70px;
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
        display: none;
      }
      .disp1 {
        display: block;
      }
      &.disp2 {
        display: block;
      }
      &.disp3 {
        display: none;
      }
    }
  }
</style>
